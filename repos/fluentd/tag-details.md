<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.8-1.0`](#fluentdv1168-10)
-	[`fluentd:v1.16.8-debian-1.0`](#fluentdv1168-debian-10)
-	[`fluentd:v1.18-1`](#fluentdv118-1)
-	[`fluentd:v1.18-debian-1`](#fluentdv118-debian-1)
-	[`fluentd:v1.18.0-1.0`](#fluentdv1180-10)
-	[`fluentd:v1.18.0-debian-1.0`](#fluentdv1180-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:26da511c05952bf0eb1bafe44b8d6e5c22e5956cf249ca2b1f31b58cb4640c99
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
$ docker pull fluentd@sha256:fbfc9bba839a42d5b5d2762530eb480309bb6b634d49b05623cf1c55339a4bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13509279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67856d15ed229333f703f25d0dca497343d4480dfad1b7e05fbba88a8426f02`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4debbdb0f911c5a6e01cc1643f908bb8db04777534fa3cdb81db39d945d09ba6`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 10.1 MB (10086242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3a0d5bab45faadc6a6f18eb50324643db72fef9bddbeb7700320669f0cc54`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d14147eee879f45943b0411811cae295fd7b8ea752cf7e2a49b20108057c0`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b62b34491d5780e65e11bb3f3e876cecf56f750ed114f9155e9eb9b28ae308`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:260ecf0b8d8066ca228c08d3222755612d31d03e91a9e58a62a1a142bbdc1c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52afb200e9f8c8101adc0c4cd7fe1909715b4403007f7a429c947593c2cdb9`

```dockerfile
```

-	Layers:
	-	`sha256:2d26f2ffa55bde84cafbab81c48e27de088c68588c996feffaed7d2c16b7bacd`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 972.8 KB (972759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed396271942deba1985acba0d0d9c6ad7b07fcf7c58c23218e1e2fcc61c4478c`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 14.9 KB (14856 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:83a87c14c041e626d8bc2543e5273bc2c7121763758dcd4b9c37187284f49cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12299356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e56d502fa527c511179ec447dfcae2e2b2dbee30bdc4fde6d476c23bf51d88`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b576c8bfe3cd90f8abdb27167b1ccf1b615751d0ecf975b06e7e0090c3a15`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 9.1 MB (9119653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f932bd6990d9af1d764fd5e8ed472a4cc4580a29591fe102eef621caf0efb19`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5154b26a8a1a65d3539f56a0621ce1be390b341d99256bfad6f8b1823c8c970`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97efe8a03db875c86ce84f91c4d106a0dc77e3c8bcb011d516bbb93f2f0b81`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:bcae9e3ce74dbeed79436268690dbeef12a673ba9fc48d55def7956cbd704c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143b2a56c351f646a3482dab11d4ca59a5556797525f2ae3da333f8b4f7239b9`

```dockerfile
```

-	Layers:
	-	`sha256:583cfcf8b09bca67618476429799443e90b0779d4065418fed968b317dc0c916`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cb5771afc7d84e8e717c60144fc70ec7692bc5a721e6884508c43d93c0c64f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13578054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0a6dc663ac792ffeea78faf736023f0d6cc61de3f49a2c7f2669461a27222`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eac0f794f35dd21a50ffe3a8aa3c90ed1abdc83894d9adc2a798e2d61656bd`  
		Last Modified: Sat, 15 Feb 2025 06:35:45 GMT  
		Size: 10.2 MB (10214464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fb865b862765b27bc92a2740809a61e8e5615173e583efd7f61e7ee2cf802`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f307bbe8260b53e3de03bc07b3c8548515b326371c8148bd65a295f31a28aa8`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161836b294706554acbe6e40e52c3219c98f4f11ded69d83ee849f718716d9d3`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7483c66f371562c48496c8d3006533bf4b49ee383ef6541cfed437e4d55200ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb10a90fc8153a210f2dfb7705628229501bc70e3f1205dc0fdfe1a0c3518cb4`

```dockerfile
```

-	Layers:
	-	`sha256:ea4aa20a6b3288b0fecfc93cfcfcd20f1e724c09dc8774308ae759a6ab9fa734`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 972.9 KB (972901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8213b169a36e5a508c94530786274818c882cdd9a44f44a28c54df94251e3a81`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:2d5dd6de34473cf5e26b9ac4c9f265a38798ac1c6cfd551c9307925e8ec8cea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12610800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b9bc42e5473692d13094bb26c35d265b760100fa1052d30df2f8e49b1b2454`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a5e8449d213a5ffc76f9f6ecc451d44b4a97f2f5bd0d000977e72aea0a951`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 9.4 MB (9353191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c246acea2bc9b5fe9f1ba7441ca5758e17a3b78c4f10f905449229c426711907`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58701eb3fa68f3262fdc1713004ae7b861adcbd1c15f4296f8a4743d2711694a`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd8599e8bd203fb81e78c21c9cc2e83f3c5a0fee1d2af35b3effcab7d01252`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7402f3dcde1b466c339ef64deddcf357b5432a8f94ddde5af380cc32df0d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c03fa47216f9da0bc0ee3c51e9086e1555d2f32905041f870a485887218a624`

```dockerfile
```

-	Layers:
	-	`sha256:b91288251a1fdd2d1a129920893d55d52523e5a7aae24397221a42bdda5744ba`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 969.7 KB (969682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0de1857b95fb21e202289b3510b23b03626e523a576677108dde6ae5e3bf536`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9b26f373d9756fdd9a2f3abed53bc34efec0f348d6b9c67e1cc009c1c73bb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13240672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f35dd176b1809aad53f77759641816527b3a02c1d46439ee120a8a52b25f68`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeed9dc76376a6743086aedaf5d78e3cba2b6d06ed9e5eddecbcd5a5e1619a5a`  
		Last Modified: Sat, 15 Feb 2025 01:14:28 GMT  
		Size: 9.9 MB (9872370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10226f89004ae0a38d6d917f4da07f05851c55f0d35439f3c9efac570988db`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6831625e07b4156af52683e748c75ec4c6472b592bc3e275fee2a45701b09`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630533c9fdcdb5139ffe4ad4ecb58a39e09550dde57d51f672141536ce5da298`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:a989e18c0f4a50ee66fee23ff10f349c6eeb741a48a9ac7d2ed94401b7fd48f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8d036e605ecda86676b5bfcdee37af6f6f46bbe6e2abeb4c38ba308cbf951`

```dockerfile
```

-	Layers:
	-	`sha256:75662b4e746d43d292ec045b8aeac2083f4731e0853c1eea3d646435757adc45`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 968.5 KB (968465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92abc9f0408870fa60f0cd877fbff73b107ac61fcaca01ddecc1cf857b19ca25`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 14.9 KB (14891 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:c64264d171d5cee4f91d4b213eccf7a7ba8bdd3a453a03928fa23dfdf05d46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12899067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fb47d60c2f61056ce153379fd7af83e1eb72ce95d033f3bb378f8ae598ae15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26795c9d7cbedbb061762126dee87400bcde0b301c13a89541c19945e7c2411b`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 9.6 MB (9642077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfaa5c8bf2b0e302a41897a4b65a3f3f66c0aa9e27b14ad97384e78517bbd45`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d3bed418f9ce23888e7cee8e81bce35e4e88a984c4728d1a6b158715eea453`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb109503f502bd2dfd9413be3791e42084012bb51f7cdd0ecd59b87ad1ea32`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:32f2698336ef5fb1f7e0a4feca6a3b685547d349de37fb3aae8cf1fe9d8c1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90f400a3560d4a199d0e4247c2dd963af4850dd23a5e7d5867199d850900b1d`

```dockerfile
```

-	Layers:
	-	`sha256:114fc7556a550965bdaeefa06f749964a0dd03420062f0efff0429098b51a448`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 967.8 KB (967849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1186777b12e9af7a92af466d79de1bf0eb0f02eb6367b706cf196622afcb3fb2`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:a629282bab906110e6076a3ab6213994cb8968c6a66f6911a1279e93315b581b
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

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:9a6031a7847da5f8f8c078e3365d05cddae45e4154f82ae1cefb898bd29549f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17377325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d896b4173191b297a8ce89653cbae7b93a112c95c28cc2f365858c9ac0335`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a32d90807b8c266738ea14cd3e118e4768654defb91b50136dc9a6b0bc31b`  
		Last Modified: Mon, 05 May 2025 17:08:22 GMT  
		Size: 14.0 MB (13954293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adfdc1828c2d31a5de1814bb38d8a28fa002ed47b96f239189b4c8cc45a6df0`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ea8d191bf9d49c93dfd104561e662db0e92d73ba4bd4240cb2eb8cdaa21bf9`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54c1cf1fa695c810fbfe199431cff4ecc3b8b82e1211edb1fc75010beeb260`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47cc0e4d55b853e3e6c13394cffe12f03b73ac14aafe24647915f08825309a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.8 KB (985762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf49178659567a3c5cfea77dcd301fc47d4e7d19ce0df284a2a13d0baea222d`

```dockerfile
```

-	Layers:
	-	`sha256:d388e0e72fab25eeab7fd07986700f0f59b2b52a60619f63b107afe8523e1731`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 972.1 KB (972085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158eae0f30771041092b66fafc68a3d4e925d505aa127e56381ed9b7c25f4eb5`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:c67e5954c6a67580d1d6dead81c4dd227b55a24de3dd1c697e1a4c04a4912896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16128241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54dc979745728f3feeb8c631a850a618d7189d7a77607e3a31b17e9c8cf737`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb461cd0447c30e6f47ac22106339df6656175ca947a682e4139676ef49d9bac`  
		Last Modified: Mon, 05 May 2025 17:02:43 GMT  
		Size: 12.9 MB (12948542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114896794c63d360bf3d13fb25f0a4834997aed226eebe5906c718e3e04c48a2`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dd51604d63e2e6aebb7a3f6aa195bfa84410e0da7b4a1eb306c2943673ecf3`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885f423c7a2aeaa4f9d012b1467208a9ba63ae72846572f3c286dbdf25bb40c1`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6f4995175e4ebd137d9f13369a54eebbce594856855db1a4cbd79155408329f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf119bfb2e251adfb3fa32df21ef8700b3db633abb830dd2990eef73e5b9218`

```dockerfile
```

-	Layers:
	-	`sha256:217a028cc2191c25586f1a48d81b2f652f5fcbdfeef4ea3c24ff8fcc7210c322`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1b09454e111f51beda23fd7380ffb92b059847ff6cf65f89e5aa5e23df54d68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17358353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4f26801fc8321d5035e9debfc87b7911a17eaa2f9625af7195f9c5f67ec384`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc473f850f35b5a7826ec9de45cde95129757cc6764277ea02764832a8153e6b`  
		Last Modified: Tue, 06 May 2025 00:52:11 GMT  
		Size: 14.0 MB (13994760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005300d6574d7422ea3722ed2d710767f3da975a49b8712a1847aed4e8c90ce`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854bb9ee89fb78ee5064c124b8c02d5c1d52930c87059d9bb9c98fc8f68d1c07`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb55f480cec42d4cc22e4959d97ced3af248e4b95a92dfbec6b92227cd8db40`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0cba1d0f7a7f14014b09263b4f20cdc9011c4a00ebf96654be0b8908f7d17654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1cfec90fcb027426189089c9bfc46047828bbd519e706dcc703691101d1e09`

```dockerfile
```

-	Layers:
	-	`sha256:baff5d9e1919250d93625c2e6c29b0dc1d493f1c6f139772379a0de47c61f88a`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 972.2 KB (972215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096844a215107599403a351c348becdd78aeae01c2533540ac0f2fcf73dc3f48`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:0c6b26e6fb7b5816f35ef5dd4f1f8f53e605511e45231ee1c5600b1dbc7d7372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16336143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370923aca611751c50fa7dcf7ca4e96f8ad05371b5a6ed2d4494668a1f52ae56`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8efe777959a38c2c89efd478e401cc5d0e78354762837db411c4681d2b8a2`  
		Last Modified: Mon, 05 May 2025 17:03:02 GMT  
		Size: 13.1 MB (13078528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e825681b479afd1afdffe8990c474cf2dca6631c7dbd60ccb66cade52fbadd`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04152820ab23d53b3e6c3839c7b2232a90cee4a1b9dc7f0009e33f54bc7c0e10`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b495eb1f73bfc0a176476a2188e1609d102704b1ffa67bf306dd670dc82249`  
		Last Modified: Mon, 05 May 2025 17:03:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fed5265d09b6d8ee2c5d45dfeed575b10201efcaa4052237424066f6ac195b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffee674304e50b7d3cfe378cd4ae09fcd62b4989f932d46773900bde5802160f`

```dockerfile
```

-	Layers:
	-	`sha256:e7f428965dd82aa2c331bda5b580b0d677e25f6a7990f7acaac0b22001f96452`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 969.0 KB (969013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c19989b05fb86871a059536e3815a246edcb86218a1b96418727f2833a8d61`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:11ccd8d5aa27870a9afc1559490f8b717087c0a4f959bbc78e830f86f3e9afca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16923334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec6386058a78f7f2e782a7b4718ba7e25e9cc68f79ea1edcfb349f501ffdfbe`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdded5621b14ece04f6a04ce3ce4aae12af69f54fa87e962aef880bd4eebcb02`  
		Last Modified: Mon, 05 May 2025 21:29:18 GMT  
		Size: 13.6 MB (13555032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53e02a774a04bfa786b4fc95a868731e1ed94d5a16b012e5f3913cf657c8ca`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd0e13df1e819edf02417230f42ec67a1671e5c89d7241da83ee639d4d453d`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134e17ab9aed318f6a90a354f87ce02ad5a3b38651d223bd3214344b1ab7e516`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:eb4071cb0d8ec63e2805a930129f35cc661f9e30c158f5ee0ace45298f208a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3bb4c1157586b38f940532db0ecbfa6c491ead1ecec3f572a72a2b5bcfd8f`

```dockerfile
```

-	Layers:
	-	`sha256:d758cf74f9c292a0185a51b66093d8eafed1d033972cd064929b24430671ae03`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 967.8 KB (967785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987418cd31d857c4874c71ef4af2c9dd79c98cfadc3102de8e77fe9eb498cc6c`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:d06e3804725441731dd76b4c5fbd1e43f2d0e26539f9c614f2d874441e9ab78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16760732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fdc38b92b4befcb4ac797bc64f68fcbb99585a2ed8e59e7819ad8afa8e2b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41ba77b5370f95e99f37e27abbedb283003a08f80229ab726e9d312daefc8c`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 13.5 MB (13503742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e6c9e81efa239126cb4694734e19f0c48b75c4be5deced36f51fc330c6c100`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c6d3b633c22097dac9428cfafd0614fc03f13b508322e609d91c40019ddece`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c26116190d0b9f3756f93b5394c0e9f7805387d6519ef98ca7d133ea640a97`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1f65597df96dc927c401cd54b5544a0d3c8755f27e50b2aec837d3e41a39766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.9 KB (980852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161f73fa05a702c1293690e6b9db20c046aa35d675b04eccf2a23914c59ce778`

```dockerfile
```

-	Layers:
	-	`sha256:13a1bbfc9a1d9f9a08c2224ac7371546ebfb21870511762f1c6b55833bdfcf37`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 967.2 KB (967175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6106b9a88939060be11b494d551452034c39acb125a3403bd1852695a3511a91`  
		Last Modified: Mon, 05 May 2025 19:23:07 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:c9f075b393f824512d8726e11a89d09e9b3b342e409a1f72df1136592ad458a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:6a6beb77ad999bde5ebd755c4c49b2dfcf03894584a8c807eb8dae4c4284f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b185c4bcbfea65b8bc10405e260f068d0ab48c0e7d63cd03ddcdc64ca835b60`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7633e3133f3cd11826b27263ce775541c067b4b2048f4e86655f471a82ce4a70`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 3.5 MB (3500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead891eaa911af415e0a68e057f82fe0d73cc00b062161e452e1403c4193247`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3bc76498e792d96c21ff737e6cc5daffb432d0ce4d19f19bf976815461e9a9`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 36.0 MB (35956627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c67ec9231c31d77ff43f924aa25a0f3489e25455a2c7c2aa521175191ea2d`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88debe1843a087aebaeec0a26d5ec0d9152a23621dd698c3002997dda7c4be02`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 14.3 MB (14257535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec5ae26cfbeb353e1cd05dd1f236ebc32a7a8ec1333447c24c6bc8eec241b8`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d71a872861f48a89724ffe0655a5fb359f499607b7c93d7b95e4b63a90ec109`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d6b23b1fe97692b713d1a46bca30661faa12cc874bad2d359c9f5f44846ccb`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ed38ebab8870578c832eff364ae2604f97c50df76666f96400838ebad293880f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca362666c1a17241b227bf995faef8d898c33fb084009d3355211c267c8442e`

```dockerfile
```

-	Layers:
	-	`sha256:54e07c8f7902fc3381687c4fb4b977d1c11ac23761ca3bab2185cc61e0ea9156`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 2.6 MB (2565376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3744f3803e20373a74f79ae1527dedddc84c16e27569ec26d1a426a7930e61a`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:abdef644cb29f86a39517e18639ff0559711fe40cb295c3045b2190be1d2fc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75390482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b25a053f99643b756fe1e20628714d60d57c9c431a670041047ec6803cfbf3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003df61415509173427026694951f93a0c0f9bd1c3bd389aa81574fd3cfbdd5d`  
		Last Modified: Thu, 22 May 2025 03:39:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5562ff4eff2d484cca8afe39dbc5bc323d0e8b50f7fc80a611e5cdfaade7d7`  
		Last Modified: Thu, 22 May 2025 03:49:14 GMT  
		Size: 32.3 MB (32319689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc6d875c82818109716bcd51c9565bb1d0cf7f6dfc11ae03c699637b0bf5e6`  
		Last Modified: Thu, 22 May 2025 03:49:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7849c33fed2ac610cbcad1d54c690377d3111e5dd896cb40958d713454a0f`  
		Last Modified: Thu, 22 May 2025 06:21:04 GMT  
		Size: 14.2 MB (14236958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9aea0b0d5fe3a37412ad103fafd28f2cb3017d90e0a2e9e08311e49aa09383`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59198e475e66818b1f9453f400d47da0cc4650e65bc23f4083faaa93448eface`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b351cf8e0edde87518c10ec960b508c5ffa49b0ae19784167c1ace55b3c87f0`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b525209b8b4b1b2bbc6294ee87ca786ba62c006356f17c5e468b767d923d91c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abf33a3f06def5d14c6a30590aeb899a15f248f8f0c53d778c26d331d957d3a`

```dockerfile
```

-	Layers:
	-	`sha256:c90913206c291b3b1d213730cd7b5b4939837f378272965ce3823fab75b9a071`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 2.6 MB (2569171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0669a02a7755d4585c0a85fb1bc6c129066a96d927e92cf111f18397358379d5`  
		Last Modified: Thu, 22 May 2025 06:21:02 GMT  
		Size: 21.2 KB (21176 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:2b4ea01391138cd73bf8bf93d8a6d167b415b9a1497c8e700af65cb4739fc7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3e25b60389ad1fadd75564ff9a3d215d77305d99fd168156de3289a5d71e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca064f7c0632bec8acecd8b2fe7cfec7ddc1f6739cc172bad82631759a0712`  
		Last Modified: Mon, 28 Apr 2025 21:47:05 GMT  
		Size: 2.9 MB (2907778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fffc0adfa58cdc3d151691d776cbcb61baada317e35196a3f17ebbf2a3bcb`  
		Last Modified: Tue, 29 Apr 2025 12:20:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be8585055c5f15a8e239091c44bbdb27a60ea0950c21ff87e57d2e1acfcfe2`  
		Last Modified: Tue, 29 Apr 2025 12:38:50 GMT  
		Size: 32.2 MB (32153197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ed88a730e4e62edc6a6ecde7fe3d9b3add4fec579cfd18a6a7dce4c1468f2`  
		Last Modified: Tue, 29 Apr 2025 12:38:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10da961b885298f136f5753564582b4f8ed2c5b5a8f722a4ab93abeb4d3e03f`  
		Last Modified: Mon, 05 May 2025 17:41:09 GMT  
		Size: 14.2 MB (14157933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94616c245e0c0bef7027df2ac132cc2f341a77ef8de840e3a3a7a33cf960449e`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2667b1c06e4e879148ab6abb9cdad639994032dd148245e2406cde5d0573dae8`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84c088a0845bc764f0787c35736834ee8dfa6d7c261e5179eeaef02f713149`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8f7ff7c632294e8e889247cc292d555223507df711352229b245809f8c9d4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bcbc28221db758b0be762ed4c8adfdfc90cdb2c28a565fe4460d84548eb01`

```dockerfile
```

-	Layers:
	-	`sha256:38e1ac6b36e271fe4c531586790ef6fd400265663588a87d6ff3d56974cd29ca`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 2.5 MB (2549394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330d4994cf9823b85cef42a8b5caac6f362d9037db55f9a5219891712fecdc36`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:08f8436ff564aaf28878d5551ee17f805c32846f2936701bf17aa3ef0049ec12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81543828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46aaae4a533897c0ac188c5cb3f40fff8509420bf7b0007a3398682e1727c1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bd6bc7ca0b1d67b661b24fbf46a7691f56dab2d717dfc202a60f1c920c7b9`  
		Last Modified: Thu, 22 May 2025 07:15:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0d016cbefd1f183a6741c762a038411814f8c44cdeff5c89aab23d745767c`  
		Last Modified: Thu, 22 May 2025 07:32:27 GMT  
		Size: 35.9 MB (35893938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a583eb9b8ffeb88a9bddc73657225fcc4131a3cceae7ec12b494aa1e4f8c7ac`  
		Last Modified: Thu, 22 May 2025 07:32:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcb89f875aa45ab00431997fb7536d4efd5f856ad1c469f3afa61ed4e230a0`  
		Last Modified: Thu, 22 May 2025 12:04:41 GMT  
		Size: 14.3 MB (14257831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf929688dcbde826cc7144d447191ae3261e310a2837fca69360b87d4f4250c`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74289355eaa62414e966b0ae1b08e2c6eb847b5647561ae20837c02321dc501d`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d433f0249005b342037a27c1b3ac3fca3d2b12f27140bd7fd535426e1b654`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ddd1b75f961612eeafde1c8f0e6f0694e8b2f41e4e6579254b5276d7c990bdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d334d2aabba82615949a2241421365a14d669bab8d396fdb3d6e7ee6dbffb641`

```dockerfile
```

-	Layers:
	-	`sha256:bfe5057a927e40212feba0cd89f3ead14c1ac08517e89a2ab355c8d3a6857a5c`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 2.6 MB (2565616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6002c36254235655f2b1d4fbc696712b33d68ef4f797d0083c77596fcacfb379`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 21.2 KB (21198 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:2e8c002c57ca2e5b99734e99a6d035d828049b1659e7b39415a6caf5364cd181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78918179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3b99db55896f7e74ee1caf3f026b13ea28dfb777e73b28b4f4dcf59b4eb26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbad29e8ec8e3d730986bc3a5c20018eb5cdae0101d7cb02600bf74c9dcc714`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 3.5 MB (3505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15ce14ce993ffff9f48b39579455b175fc24dba4a9dc09744eaffc5e7941f50`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcab8a3b917254fd76d87f9c839c9dfea6fe8be32466c7cdf30f9b0682ce256`  
		Last Modified: Wed, 21 May 2025 23:26:42 GMT  
		Size: 32.2 MB (32158845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d97937ade131e6a39f462c67ec0fb9abadb4c47e0140ea248369f8e1c793e8`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d7bd94b3b6ec7997b3673b71cafdc4da0962220dcae6a6ef7847082c5fe977`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 14.0 MB (14043455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0bc6ccf27e2dbb22a0807fe0acff45f95b788518ae32ed4b09af32a787192`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8923eb30b786021b0b5944aae3b17629d70e6402930d1edefb38a692dbbf3d`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeff9cf9649fde97cce766e02303ce6fe54b9fd0791b9a53989f72aa03c5220`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f2d19fa96c925e55c21b1fcf3ed17d9bb15d4e3867b3fc5484f7a46fb4a1b7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66d3cefc287a8fc2ac2a9189cbcff8692677e23aef3b5e11d4056166113482`

```dockerfile
```

-	Layers:
	-	`sha256:567bcef49d090c48a91ba26dc695bef9f3ca51c6ae710084de4eed25bd626d86`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 2.6 MB (2562555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f89de5fde4548c4cdd823ad034c51f85609cae07f42645b98b565274588cad`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:feadd1c0496e71534265a0c93ee48eaaa63f6d4c7feb5133c48d65a622e36d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84252411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904e38d9347584e2a8bedd5a8d50910f2ed34ef8136194d399544358cb590a03`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dd76f60873e36a2ef2d22238cf80226734882a65c6026751c657d5e01c4ff`  
		Last Modified: Mon, 28 Apr 2025 21:47:41 GMT  
		Size: 3.7 MB (3702919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a5d43e9710a6e7cc4fa2a97548175c06fb684ef5a6bf6bf104beb7d07f590`  
		Last Modified: Tue, 29 Apr 2025 03:23:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691ab89116c60731f2d6fd6257a8c2c94601b5d4158ce7a2d0f6e9965b36d91`  
		Last Modified: Tue, 29 Apr 2025 03:35:58 GMT  
		Size: 33.8 MB (33827394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be576cfe66606b1543169d9a80faed604780093b6dd97706df1c9848c856ddbf`  
		Last Modified: Tue, 29 Apr 2025 03:35:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298daac89f779d25bfc7bb933205057d633512a1ef7ed294258890efa9a150f0`  
		Last Modified: Mon, 05 May 2025 21:34:11 GMT  
		Size: 14.7 MB (14651257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62557ac80b6879954a5f7d21b23347725c1876123f30a469ce20406065578c5`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4f0711f69edf3665b20cd07829f54f8f7a335647a1b809258ee34e1ecbcaa`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f406313f370d8e4770561b18f2a9aa98f5fcc13bbdfc51caab71879409cc0129`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7bcaa33be5a62066aa082f6093b8b122b2a9ddf7c2d6796faf7650a87d7e90b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdd6c7803e7001f9fc9e687176615554466141391c77f362dd20cf173aa247`

```dockerfile
```

-	Layers:
	-	`sha256:660c7b77b89dc1c68766cc8e5f516e5101717d5ca937132e3a4748d2d5de92cd`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 2.6 MB (2551487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183814280fa003136769b5d771cef601bd82981e3384a0228793faaab0fbe96d`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8c3e8f7e5033c9eb3e38ee8d4635179b615b2dbae5658f8d6e9e2e5b3c1e8646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77531896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264c41a63c4476344ef89225f4f703d0850d2bd309bb1932997202b71820969`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea620f7f490e88536a1b4c6ec0bc57e080f770ab010a69f37900a29d34f73bf`  
		Last Modified: Thu, 22 May 2025 03:25:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4e07ad6df1e8ef820771bf3ceb20d87afe840a4e0447a7cbc9470c8db11db`  
		Last Modified: Thu, 22 May 2025 03:33:57 GMT  
		Size: 33.1 MB (33092007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa788e379cb46c980dbacc1575b979443bdeae78f05d06172db2c76550dd47a6`  
		Last Modified: Thu, 22 May 2025 03:33:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0049b745e6c9498a8d88aaa17d32bf7268e9467991ebec5dc5fd72455f0b619c`  
		Last Modified: Thu, 22 May 2025 06:13:18 GMT  
		Size: 14.4 MB (14389786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a780155e12d3f0b33a331f4a1e57d0ae6f65eda695ffa4666fec76363dacc`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c120c771f4e25c3afc3aa7c826430571012f5178e38f95ac800c0bea04f59`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88fa262df5e59930e4e62fb26327d08f496d19325f23e1fb825d73966b095d`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c3f377896625383df7d57740e025c84ebd85f077bfd5e565fab14705991e926f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce10054f11f500cf9e436883eb89707c4280dde8f72fc3705068762c63d5021`

```dockerfile
```

-	Layers:
	-	`sha256:14bcaaee77fc7af3de9d075253e295a8a5fe5ffa11d3ae8ed3421bcbf7fd381a`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 2.6 MB (2565093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27457fbf099bb9edf02ad8939589b691cda4e58db0f113a9b9885c401f371617`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.8-1.0`

```console
$ docker pull fluentd@sha256:a629282bab906110e6076a3ab6213994cb8968c6a66f6911a1279e93315b581b
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

### `fluentd:v1.16.8-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:9a6031a7847da5f8f8c078e3365d05cddae45e4154f82ae1cefb898bd29549f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17377325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d896b4173191b297a8ce89653cbae7b93a112c95c28cc2f365858c9ac0335`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a32d90807b8c266738ea14cd3e118e4768654defb91b50136dc9a6b0bc31b`  
		Last Modified: Mon, 05 May 2025 17:08:22 GMT  
		Size: 14.0 MB (13954293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adfdc1828c2d31a5de1814bb38d8a28fa002ed47b96f239189b4c8cc45a6df0`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ea8d191bf9d49c93dfd104561e662db0e92d73ba4bd4240cb2eb8cdaa21bf9`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54c1cf1fa695c810fbfe199431cff4ecc3b8b82e1211edb1fc75010beeb260`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:47cc0e4d55b853e3e6c13394cffe12f03b73ac14aafe24647915f08825309a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.8 KB (985762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf49178659567a3c5cfea77dcd301fc47d4e7d19ce0df284a2a13d0baea222d`

```dockerfile
```

-	Layers:
	-	`sha256:d388e0e72fab25eeab7fd07986700f0f59b2b52a60619f63b107afe8523e1731`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 972.1 KB (972085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158eae0f30771041092b66fafc68a3d4e925d505aa127e56381ed9b7c25f4eb5`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:c67e5954c6a67580d1d6dead81c4dd227b55a24de3dd1c697e1a4c04a4912896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16128241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54dc979745728f3feeb8c631a850a618d7189d7a77607e3a31b17e9c8cf737`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb461cd0447c30e6f47ac22106339df6656175ca947a682e4139676ef49d9bac`  
		Last Modified: Mon, 05 May 2025 17:02:43 GMT  
		Size: 12.9 MB (12948542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114896794c63d360bf3d13fb25f0a4834997aed226eebe5906c718e3e04c48a2`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dd51604d63e2e6aebb7a3f6aa195bfa84410e0da7b4a1eb306c2943673ecf3`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885f423c7a2aeaa4f9d012b1467208a9ba63ae72846572f3c286dbdf25bb40c1`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6f4995175e4ebd137d9f13369a54eebbce594856855db1a4cbd79155408329f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf119bfb2e251adfb3fa32df21ef8700b3db633abb830dd2990eef73e5b9218`

```dockerfile
```

-	Layers:
	-	`sha256:217a028cc2191c25586f1a48d81b2f652f5fcbdfeef4ea3c24ff8fcc7210c322`  
		Last Modified: Mon, 05 May 2025 17:02:42 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1b09454e111f51beda23fd7380ffb92b059847ff6cf65f89e5aa5e23df54d68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17358353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4f26801fc8321d5035e9debfc87b7911a17eaa2f9625af7195f9c5f67ec384`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc473f850f35b5a7826ec9de45cde95129757cc6764277ea02764832a8153e6b`  
		Last Modified: Tue, 06 May 2025 00:52:11 GMT  
		Size: 14.0 MB (13994760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005300d6574d7422ea3722ed2d710767f3da975a49b8712a1847aed4e8c90ce`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854bb9ee89fb78ee5064c124b8c02d5c1d52930c87059d9bb9c98fc8f68d1c07`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb55f480cec42d4cc22e4959d97ced3af248e4b95a92dfbec6b92227cd8db40`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0cba1d0f7a7f14014b09263b4f20cdc9011c4a00ebf96654be0b8908f7d17654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1cfec90fcb027426189089c9bfc46047828bbd519e706dcc703691101d1e09`

```dockerfile
```

-	Layers:
	-	`sha256:baff5d9e1919250d93625c2e6c29b0dc1d493f1c6f139772379a0de47c61f88a`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 972.2 KB (972215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096844a215107599403a351c348becdd78aeae01c2533540ac0f2fcf73dc3f48`  
		Last Modified: Tue, 06 May 2025 00:52:10 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:0c6b26e6fb7b5816f35ef5dd4f1f8f53e605511e45231ee1c5600b1dbc7d7372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16336143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370923aca611751c50fa7dcf7ca4e96f8ad05371b5a6ed2d4494668a1f52ae56`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8efe777959a38c2c89efd478e401cc5d0e78354762837db411c4681d2b8a2`  
		Last Modified: Mon, 05 May 2025 17:03:02 GMT  
		Size: 13.1 MB (13078528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e825681b479afd1afdffe8990c474cf2dca6631c7dbd60ccb66cade52fbadd`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04152820ab23d53b3e6c3839c7b2232a90cee4a1b9dc7f0009e33f54bc7c0e10`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b495eb1f73bfc0a176476a2188e1609d102704b1ffa67bf306dd670dc82249`  
		Last Modified: Mon, 05 May 2025 17:03:02 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fed5265d09b6d8ee2c5d45dfeed575b10201efcaa4052237424066f6ac195b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffee674304e50b7d3cfe378cd4ae09fcd62b4989f932d46773900bde5802160f`

```dockerfile
```

-	Layers:
	-	`sha256:e7f428965dd82aa2c331bda5b580b0d677e25f6a7990f7acaac0b22001f96452`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 969.0 KB (969013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c19989b05fb86871a059536e3815a246edcb86218a1b96418727f2833a8d61`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:11ccd8d5aa27870a9afc1559490f8b717087c0a4f959bbc78e830f86f3e9afca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16923334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec6386058a78f7f2e782a7b4718ba7e25e9cc68f79ea1edcfb349f501ffdfbe`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdded5621b14ece04f6a04ce3ce4aae12af69f54fa87e962aef880bd4eebcb02`  
		Last Modified: Mon, 05 May 2025 21:29:18 GMT  
		Size: 13.6 MB (13555032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53e02a774a04bfa786b4fc95a868731e1ed94d5a16b012e5f3913cf657c8ca`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd0e13df1e819edf02417230f42ec67a1671e5c89d7241da83ee639d4d453d`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134e17ab9aed318f6a90a354f87ce02ad5a3b38651d223bd3214344b1ab7e516`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:eb4071cb0d8ec63e2805a930129f35cc661f9e30c158f5ee0ace45298f208a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3bb4c1157586b38f940532db0ecbfa6c491ead1ecec3f572a72a2b5bcfd8f`

```dockerfile
```

-	Layers:
	-	`sha256:d758cf74f9c292a0185a51b66093d8eafed1d033972cd064929b24430671ae03`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 967.8 KB (967785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987418cd31d857c4874c71ef4af2c9dd79c98cfadc3102de8e77fe9eb498cc6c`  
		Last Modified: Mon, 05 May 2025 21:29:17 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:d06e3804725441731dd76b4c5fbd1e43f2d0e26539f9c614f2d874441e9ab78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16760732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fdc38b92b4befcb4ac797bc64f68fcbb99585a2ed8e59e7819ad8afa8e2b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41ba77b5370f95e99f37e27abbedb283003a08f80229ab726e9d312daefc8c`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 13.5 MB (13503742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e6c9e81efa239126cb4694734e19f0c48b75c4be5deced36f51fc330c6c100`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c6d3b633c22097dac9428cfafd0614fc03f13b508322e609d91c40019ddece`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c26116190d0b9f3756f93b5394c0e9f7805387d6519ef98ca7d133ea640a97`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b1f65597df96dc927c401cd54b5544a0d3c8755f27e50b2aec837d3e41a39766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.9 KB (980852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161f73fa05a702c1293690e6b9db20c046aa35d675b04eccf2a23914c59ce778`

```dockerfile
```

-	Layers:
	-	`sha256:13a1bbfc9a1d9f9a08c2224ac7371546ebfb21870511762f1c6b55833bdfcf37`  
		Last Modified: Mon, 05 May 2025 19:23:08 GMT  
		Size: 967.2 KB (967175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6106b9a88939060be11b494d551452034c39acb125a3403bd1852695a3511a91`  
		Last Modified: Mon, 05 May 2025 19:23:07 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.8-debian-1.0`

```console
$ docker pull fluentd@sha256:c9f075b393f824512d8726e11a89d09e9b3b342e409a1f72df1136592ad458a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `fluentd:v1.16.8-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:6a6beb77ad999bde5ebd755c4c49b2dfcf03894584a8c807eb8dae4c4284f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b185c4bcbfea65b8bc10405e260f068d0ab48c0e7d63cd03ddcdc64ca835b60`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7633e3133f3cd11826b27263ce775541c067b4b2048f4e86655f471a82ce4a70`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 3.5 MB (3500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead891eaa911af415e0a68e057f82fe0d73cc00b062161e452e1403c4193247`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3bc76498e792d96c21ff737e6cc5daffb432d0ce4d19f19bf976815461e9a9`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 36.0 MB (35956627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c67ec9231c31d77ff43f924aa25a0f3489e25455a2c7c2aa521175191ea2d`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88debe1843a087aebaeec0a26d5ec0d9152a23621dd698c3002997dda7c4be02`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 14.3 MB (14257535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec5ae26cfbeb353e1cd05dd1f236ebc32a7a8ec1333447c24c6bc8eec241b8`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d71a872861f48a89724ffe0655a5fb359f499607b7c93d7b95e4b63a90ec109`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d6b23b1fe97692b713d1a46bca30661faa12cc874bad2d359c9f5f44846ccb`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ed38ebab8870578c832eff364ae2604f97c50df76666f96400838ebad293880f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca362666c1a17241b227bf995faef8d898c33fb084009d3355211c267c8442e`

```dockerfile
```

-	Layers:
	-	`sha256:54e07c8f7902fc3381687c4fb4b977d1c11ac23761ca3bab2185cc61e0ea9156`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 2.6 MB (2565376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3744f3803e20373a74f79ae1527dedddc84c16e27569ec26d1a426a7930e61a`  
		Last Modified: Thu, 22 May 2025 00:14:34 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:abdef644cb29f86a39517e18639ff0559711fe40cb295c3045b2190be1d2fc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75390482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b25a053f99643b756fe1e20628714d60d57c9c431a670041047ec6803cfbf3a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003df61415509173427026694951f93a0c0f9bd1c3bd389aa81574fd3cfbdd5d`  
		Last Modified: Thu, 22 May 2025 03:39:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5562ff4eff2d484cca8afe39dbc5bc323d0e8b50f7fc80a611e5cdfaade7d7`  
		Last Modified: Thu, 22 May 2025 03:49:14 GMT  
		Size: 32.3 MB (32319689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc6d875c82818109716bcd51c9565bb1d0cf7f6dfc11ae03c699637b0bf5e6`  
		Last Modified: Thu, 22 May 2025 03:49:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7849c33fed2ac610cbcad1d54c690377d3111e5dd896cb40958d713454a0f`  
		Last Modified: Thu, 22 May 2025 06:21:04 GMT  
		Size: 14.2 MB (14236958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9aea0b0d5fe3a37412ad103fafd28f2cb3017d90e0a2e9e08311e49aa09383`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59198e475e66818b1f9453f400d47da0cc4650e65bc23f4083faaa93448eface`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b351cf8e0edde87518c10ec960b508c5ffa49b0ae19784167c1ace55b3c87f0`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b525209b8b4b1b2bbc6294ee87ca786ba62c006356f17c5e468b767d923d91c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abf33a3f06def5d14c6a30590aeb899a15f248f8f0c53d778c26d331d957d3a`

```dockerfile
```

-	Layers:
	-	`sha256:c90913206c291b3b1d213730cd7b5b4939837f378272965ce3823fab75b9a071`  
		Last Modified: Thu, 22 May 2025 06:21:03 GMT  
		Size: 2.6 MB (2569171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0669a02a7755d4585c0a85fb1bc6c129066a96d927e92cf111f18397358379d5`  
		Last Modified: Thu, 22 May 2025 06:21:02 GMT  
		Size: 21.2 KB (21176 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:2b4ea01391138cd73bf8bf93d8a6d167b415b9a1497c8e700af65cb4739fc7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3e25b60389ad1fadd75564ff9a3d215d77305d99fd168156de3289a5d71e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca064f7c0632bec8acecd8b2fe7cfec7ddc1f6739cc172bad82631759a0712`  
		Last Modified: Mon, 28 Apr 2025 21:47:05 GMT  
		Size: 2.9 MB (2907778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fffc0adfa58cdc3d151691d776cbcb61baada317e35196a3f17ebbf2a3bcb`  
		Last Modified: Tue, 29 Apr 2025 12:20:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be8585055c5f15a8e239091c44bbdb27a60ea0950c21ff87e57d2e1acfcfe2`  
		Last Modified: Tue, 29 Apr 2025 12:38:50 GMT  
		Size: 32.2 MB (32153197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ed88a730e4e62edc6a6ecde7fe3d9b3add4fec579cfd18a6a7dce4c1468f2`  
		Last Modified: Tue, 29 Apr 2025 12:38:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10da961b885298f136f5753564582b4f8ed2c5b5a8f722a4ab93abeb4d3e03f`  
		Last Modified: Mon, 05 May 2025 17:41:09 GMT  
		Size: 14.2 MB (14157933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94616c245e0c0bef7027df2ac132cc2f341a77ef8de840e3a3a7a33cf960449e`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2667b1c06e4e879148ab6abb9cdad639994032dd148245e2406cde5d0573dae8`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84c088a0845bc764f0787c35736834ee8dfa6d7c261e5179eeaef02f713149`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8f7ff7c632294e8e889247cc292d555223507df711352229b245809f8c9d4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bcbc28221db758b0be762ed4c8adfdfc90cdb2c28a565fe4460d84548eb01`

```dockerfile
```

-	Layers:
	-	`sha256:38e1ac6b36e271fe4c531586790ef6fd400265663588a87d6ff3d56974cd29ca`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 2.5 MB (2549394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330d4994cf9823b85cef42a8b5caac6f362d9037db55f9a5219891712fecdc36`  
		Last Modified: Mon, 05 May 2025 17:41:08 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:08f8436ff564aaf28878d5551ee17f805c32846f2936701bf17aa3ef0049ec12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81543828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46aaae4a533897c0ac188c5cb3f40fff8509420bf7b0007a3398682e1727c1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bd6bc7ca0b1d67b661b24fbf46a7691f56dab2d717dfc202a60f1c920c7b9`  
		Last Modified: Thu, 22 May 2025 07:15:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0d016cbefd1f183a6741c762a038411814f8c44cdeff5c89aab23d745767c`  
		Last Modified: Thu, 22 May 2025 07:32:27 GMT  
		Size: 35.9 MB (35893938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a583eb9b8ffeb88a9bddc73657225fcc4131a3cceae7ec12b494aa1e4f8c7ac`  
		Last Modified: Thu, 22 May 2025 07:32:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcb89f875aa45ab00431997fb7536d4efd5f856ad1c469f3afa61ed4e230a0`  
		Last Modified: Thu, 22 May 2025 12:04:41 GMT  
		Size: 14.3 MB (14257831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf929688dcbde826cc7144d447191ae3261e310a2837fca69360b87d4f4250c`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74289355eaa62414e966b0ae1b08e2c6eb847b5647561ae20837c02321dc501d`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d433f0249005b342037a27c1b3ac3fca3d2b12f27140bd7fd535426e1b654`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ddd1b75f961612eeafde1c8f0e6f0694e8b2f41e4e6579254b5276d7c990bdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d334d2aabba82615949a2241421365a14d669bab8d396fdb3d6e7ee6dbffb641`

```dockerfile
```

-	Layers:
	-	`sha256:bfe5057a927e40212feba0cd89f3ead14c1ac08517e89a2ab355c8d3a6857a5c`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 2.6 MB (2565616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6002c36254235655f2b1d4fbc696712b33d68ef4f797d0083c77596fcacfb379`  
		Last Modified: Thu, 22 May 2025 12:04:40 GMT  
		Size: 21.2 KB (21198 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:2e8c002c57ca2e5b99734e99a6d035d828049b1659e7b39415a6caf5364cd181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78918179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3b99db55896f7e74ee1caf3f026b13ea28dfb777e73b28b4f4dcf59b4eb26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbad29e8ec8e3d730986bc3a5c20018eb5cdae0101d7cb02600bf74c9dcc714`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 3.5 MB (3505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15ce14ce993ffff9f48b39579455b175fc24dba4a9dc09744eaffc5e7941f50`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcab8a3b917254fd76d87f9c839c9dfea6fe8be32466c7cdf30f9b0682ce256`  
		Last Modified: Wed, 21 May 2025 23:26:42 GMT  
		Size: 32.2 MB (32158845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d97937ade131e6a39f462c67ec0fb9abadb4c47e0140ea248369f8e1c793e8`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d7bd94b3b6ec7997b3673b71cafdc4da0962220dcae6a6ef7847082c5fe977`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 14.0 MB (14043455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0bc6ccf27e2dbb22a0807fe0acff45f95b788518ae32ed4b09af32a787192`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8923eb30b786021b0b5944aae3b17629d70e6402930d1edefb38a692dbbf3d`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeff9cf9649fde97cce766e02303ce6fe54b9fd0791b9a53989f72aa03c5220`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f2d19fa96c925e55c21b1fcf3ed17d9bb15d4e3867b3fc5484f7a46fb4a1b7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66d3cefc287a8fc2ac2a9189cbcff8692677e23aef3b5e11d4056166113482`

```dockerfile
```

-	Layers:
	-	`sha256:567bcef49d090c48a91ba26dc695bef9f3ca51c6ae710084de4eed25bd626d86`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 2.6 MB (2562555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f89de5fde4548c4cdd823ad034c51f85609cae07f42645b98b565274588cad`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:feadd1c0496e71534265a0c93ee48eaaa63f6d4c7feb5133c48d65a622e36d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84252411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904e38d9347584e2a8bedd5a8d50910f2ed34ef8136194d399544358cb590a03`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dd76f60873e36a2ef2d22238cf80226734882a65c6026751c657d5e01c4ff`  
		Last Modified: Mon, 28 Apr 2025 21:47:41 GMT  
		Size: 3.7 MB (3702919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a5d43e9710a6e7cc4fa2a97548175c06fb684ef5a6bf6bf104beb7d07f590`  
		Last Modified: Tue, 29 Apr 2025 03:23:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691ab89116c60731f2d6fd6257a8c2c94601b5d4158ce7a2d0f6e9965b36d91`  
		Last Modified: Tue, 29 Apr 2025 03:35:58 GMT  
		Size: 33.8 MB (33827394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be576cfe66606b1543169d9a80faed604780093b6dd97706df1c9848c856ddbf`  
		Last Modified: Tue, 29 Apr 2025 03:35:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298daac89f779d25bfc7bb933205057d633512a1ef7ed294258890efa9a150f0`  
		Last Modified: Mon, 05 May 2025 21:34:11 GMT  
		Size: 14.7 MB (14651257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62557ac80b6879954a5f7d21b23347725c1876123f30a469ce20406065578c5`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4f0711f69edf3665b20cd07829f54f8f7a335647a1b809258ee34e1ecbcaa`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f406313f370d8e4770561b18f2a9aa98f5fcc13bbdfc51caab71879409cc0129`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7bcaa33be5a62066aa082f6093b8b122b2a9ddf7c2d6796faf7650a87d7e90b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdd6c7803e7001f9fc9e687176615554466141391c77f362dd20cf173aa247`

```dockerfile
```

-	Layers:
	-	`sha256:660c7b77b89dc1c68766cc8e5f516e5101717d5ca937132e3a4748d2d5de92cd`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 2.6 MB (2551487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183814280fa003136769b5d771cef601bd82981e3384a0228793faaab0fbe96d`  
		Last Modified: Mon, 05 May 2025 21:34:10 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.8-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8c3e8f7e5033c9eb3e38ee8d4635179b615b2dbae5658f8d6e9e2e5b3c1e8646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77531896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264c41a63c4476344ef89225f4f703d0850d2bd309bb1932997202b71820969`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Mar 2025 11:33:53 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Fri, 02 May 2025 09:54:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 02 May 2025 09:54:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.8
# Fri, 02 May 2025 09:54:06 GMT
ENV TINI_VERSION=0.18.0
# Fri, 02 May 2025 09:54:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.8  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 02 May 2025 09:54:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 02 May 2025 09:54:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 02 May 2025 09:54:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 02 May 2025 09:54:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 02 May 2025 09:54:06 GMT
USER fluent
# Fri, 02 May 2025 09:54:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 02 May 2025 09:54:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea620f7f490e88536a1b4c6ec0bc57e080f770ab010a69f37900a29d34f73bf`  
		Last Modified: Thu, 22 May 2025 03:25:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4e07ad6df1e8ef820771bf3ceb20d87afe840a4e0447a7cbc9470c8db11db`  
		Last Modified: Thu, 22 May 2025 03:33:57 GMT  
		Size: 33.1 MB (33092007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa788e379cb46c980dbacc1575b979443bdeae78f05d06172db2c76550dd47a6`  
		Last Modified: Thu, 22 May 2025 03:33:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0049b745e6c9498a8d88aaa17d32bf7268e9467991ebec5dc5fd72455f0b619c`  
		Last Modified: Thu, 22 May 2025 06:13:18 GMT  
		Size: 14.4 MB (14389786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a780155e12d3f0b33a331f4a1e57d0ae6f65eda695ffa4666fec76363dacc`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c120c771f4e25c3afc3aa7c826430571012f5178e38f95ac800c0bea04f59`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88fa262df5e59930e4e62fb26327d08f496d19325f23e1fb825d73966b095d`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.8-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c3f377896625383df7d57740e025c84ebd85f077bfd5e565fab14705991e926f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce10054f11f500cf9e436883eb89707c4280dde8f72fc3705068762c63d5021`

```dockerfile
```

-	Layers:
	-	`sha256:14bcaaee77fc7af3de9d075253e295a8a5fe5ffa11d3ae8ed3421bcbf7fd381a`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 2.6 MB (2565093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27457fbf099bb9edf02ad8939589b691cda4e58db0f113a9b9885c401f371617`  
		Last Modified: Thu, 22 May 2025 06:13:17 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-1`

```console
$ docker pull fluentd@sha256:26da511c05952bf0eb1bafe44b8d6e5c22e5956cf249ca2b1f31b58cb4640c99
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

### `fluentd:v1.18-1` - linux; amd64

```console
$ docker pull fluentd@sha256:fbfc9bba839a42d5b5d2762530eb480309bb6b634d49b05623cf1c55339a4bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13509279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67856d15ed229333f703f25d0dca497343d4480dfad1b7e05fbba88a8426f02`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4debbdb0f911c5a6e01cc1643f908bb8db04777534fa3cdb81db39d945d09ba6`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 10.1 MB (10086242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3a0d5bab45faadc6a6f18eb50324643db72fef9bddbeb7700320669f0cc54`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d14147eee879f45943b0411811cae295fd7b8ea752cf7e2a49b20108057c0`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b62b34491d5780e65e11bb3f3e876cecf56f750ed114f9155e9eb9b28ae308`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:260ecf0b8d8066ca228c08d3222755612d31d03e91a9e58a62a1a142bbdc1c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52afb200e9f8c8101adc0c4cd7fe1909715b4403007f7a429c947593c2cdb9`

```dockerfile
```

-	Layers:
	-	`sha256:2d26f2ffa55bde84cafbab81c48e27de088c68588c996feffaed7d2c16b7bacd`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 972.8 KB (972759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed396271942deba1985acba0d0d9c6ad7b07fcf7c58c23218e1e2fcc61c4478c`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 14.9 KB (14856 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:83a87c14c041e626d8bc2543e5273bc2c7121763758dcd4b9c37187284f49cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12299356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e56d502fa527c511179ec447dfcae2e2b2dbee30bdc4fde6d476c23bf51d88`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b576c8bfe3cd90f8abdb27167b1ccf1b615751d0ecf975b06e7e0090c3a15`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 9.1 MB (9119653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f932bd6990d9af1d764fd5e8ed472a4cc4580a29591fe102eef621caf0efb19`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5154b26a8a1a65d3539f56a0621ce1be390b341d99256bfad6f8b1823c8c970`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97efe8a03db875c86ce84f91c4d106a0dc77e3c8bcb011d516bbb93f2f0b81`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bcae9e3ce74dbeed79436268690dbeef12a673ba9fc48d55def7956cbd704c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143b2a56c351f646a3482dab11d4ca59a5556797525f2ae3da333f8b4f7239b9`

```dockerfile
```

-	Layers:
	-	`sha256:583cfcf8b09bca67618476429799443e90b0779d4065418fed968b317dc0c916`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cb5771afc7d84e8e717c60144fc70ec7692bc5a721e6884508c43d93c0c64f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13578054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0a6dc663ac792ffeea78faf736023f0d6cc61de3f49a2c7f2669461a27222`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eac0f794f35dd21a50ffe3a8aa3c90ed1abdc83894d9adc2a798e2d61656bd`  
		Last Modified: Sat, 15 Feb 2025 06:35:45 GMT  
		Size: 10.2 MB (10214464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fb865b862765b27bc92a2740809a61e8e5615173e583efd7f61e7ee2cf802`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f307bbe8260b53e3de03bc07b3c8548515b326371c8148bd65a295f31a28aa8`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161836b294706554acbe6e40e52c3219c98f4f11ded69d83ee849f718716d9d3`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7483c66f371562c48496c8d3006533bf4b49ee383ef6541cfed437e4d55200ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb10a90fc8153a210f2dfb7705628229501bc70e3f1205dc0fdfe1a0c3518cb4`

```dockerfile
```

-	Layers:
	-	`sha256:ea4aa20a6b3288b0fecfc93cfcfcd20f1e724c09dc8774308ae759a6ab9fa734`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 972.9 KB (972901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8213b169a36e5a508c94530786274818c882cdd9a44f44a28c54df94251e3a81`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; 386

```console
$ docker pull fluentd@sha256:2d5dd6de34473cf5e26b9ac4c9f265a38798ac1c6cfd551c9307925e8ec8cea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12610800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b9bc42e5473692d13094bb26c35d265b760100fa1052d30df2f8e49b1b2454`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a5e8449d213a5ffc76f9f6ecc451d44b4a97f2f5bd0d000977e72aea0a951`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 9.4 MB (9353191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c246acea2bc9b5fe9f1ba7441ca5758e17a3b78c4f10f905449229c426711907`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58701eb3fa68f3262fdc1713004ae7b861adcbd1c15f4296f8a4743d2711694a`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd8599e8bd203fb81e78c21c9cc2e83f3c5a0fee1d2af35b3effcab7d01252`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7402f3dcde1b466c339ef64deddcf357b5432a8f94ddde5af380cc32df0d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c03fa47216f9da0bc0ee3c51e9086e1555d2f32905041f870a485887218a624`

```dockerfile
```

-	Layers:
	-	`sha256:b91288251a1fdd2d1a129920893d55d52523e5a7aae24397221a42bdda5744ba`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 969.7 KB (969682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0de1857b95fb21e202289b3510b23b03626e523a576677108dde6ae5e3bf536`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9b26f373d9756fdd9a2f3abed53bc34efec0f348d6b9c67e1cc009c1c73bb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13240672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f35dd176b1809aad53f77759641816527b3a02c1d46439ee120a8a52b25f68`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeed9dc76376a6743086aedaf5d78e3cba2b6d06ed9e5eddecbcd5a5e1619a5a`  
		Last Modified: Sat, 15 Feb 2025 01:14:28 GMT  
		Size: 9.9 MB (9872370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10226f89004ae0a38d6d917f4da07f05851c55f0d35439f3c9efac570988db`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6831625e07b4156af52683e748c75ec4c6472b592bc3e275fee2a45701b09`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630533c9fdcdb5139ffe4ad4ecb58a39e09550dde57d51f672141536ce5da298`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a989e18c0f4a50ee66fee23ff10f349c6eeb741a48a9ac7d2ed94401b7fd48f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8d036e605ecda86676b5bfcdee37af6f6f46bbe6e2abeb4c38ba308cbf951`

```dockerfile
```

-	Layers:
	-	`sha256:75662b4e746d43d292ec045b8aeac2083f4731e0853c1eea3d646435757adc45`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 968.5 KB (968465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92abc9f0408870fa60f0cd877fbff73b107ac61fcaca01ddecc1cf857b19ca25`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 14.9 KB (14891 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; s390x

```console
$ docker pull fluentd@sha256:c64264d171d5cee4f91d4b213eccf7a7ba8bdd3a453a03928fa23dfdf05d46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12899067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fb47d60c2f61056ce153379fd7af83e1eb72ce95d033f3bb378f8ae598ae15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26795c9d7cbedbb061762126dee87400bcde0b301c13a89541c19945e7c2411b`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 9.6 MB (9642077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfaa5c8bf2b0e302a41897a4b65a3f3f66c0aa9e27b14ad97384e78517bbd45`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d3bed418f9ce23888e7cee8e81bce35e4e88a984c4728d1a6b158715eea453`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb109503f502bd2dfd9413be3791e42084012bb51f7cdd0ecd59b87ad1ea32`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:32f2698336ef5fb1f7e0a4feca6a3b685547d349de37fb3aae8cf1fe9d8c1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90f400a3560d4a199d0e4247c2dd963af4850dd23a5e7d5867199d850900b1d`

```dockerfile
```

-	Layers:
	-	`sha256:114fc7556a550965bdaeefa06f749964a0dd03420062f0efff0429098b51a448`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 967.8 KB (967849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1186777b12e9af7a92af466d79de1bf0eb0f02eb6367b706cf196622afcb3fb2`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-debian-1`

```console
$ docker pull fluentd@sha256:d0e3feff84005d619bac90a0758779bf95dccfc8854abdda05467d895a3202dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `fluentd:v1.18-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:23436baafb2c9d27eb4e7307988828f224bc9685dea3ed93c76e555869906a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72832468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5025bca51a1719500078f6fcd20e1cba6cfd97bc25af8f801c522481989a2a70`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7633e3133f3cd11826b27263ce775541c067b4b2048f4e86655f471a82ce4a70`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 3.5 MB (3500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead891eaa911af415e0a68e057f82fe0d73cc00b062161e452e1403c4193247`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3bc76498e792d96c21ff737e6cc5daffb432d0ce4d19f19bf976815461e9a9`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 36.0 MB (35956627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c67ec9231c31d77ff43f924aa25a0f3489e25455a2c7c2aa521175191ea2d`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3c7e9819d7804c6fcd6fa5df1daf8351b1e35804e10c7016fd63eda05bb4d`  
		Last Modified: Thu, 22 May 2025 00:14:41 GMT  
		Size: 5.1 MB (5147448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e020dd939c72abd293d288262979a25a33a55d164f043535c170a175d2659`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be566ec6f6f265dd3cb6123ff391d34faf00900374770755d6123e27459d6738`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb88fbdfe27989cd4e9fcc7b7d9ca25f9080f0b6c5438be29c6d9ebb544e05d3`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c862dfa8656a27781a167c49aadf25f7c5a7e185b5a6891658ccfeea5ec91c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6590f83e0f5807ef5659606dcb774b60b93db872573db66fd0772c0700ecceb`

```dockerfile
```

-	Layers:
	-	`sha256:388783ab52336d520a813b6fccd80af38827ab3f520658e0ceeac39e1e916f6f`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 2.6 MB (2569212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bc927d4df332c5edb2bc342822e64a0e6a69b4b1133b372b781796c12e7034`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cc4378e2795e9b511eba55bf911949b29d1404122d8326339e90b3a73c7c97b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea89b9b1302eda176e4fe192485d482916a1ad901636a9854ee3b5ff1510169`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003df61415509173427026694951f93a0c0f9bd1c3bd389aa81574fd3cfbdd5d`  
		Last Modified: Thu, 22 May 2025 03:39:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5562ff4eff2d484cca8afe39dbc5bc323d0e8b50f7fc80a611e5cdfaade7d7`  
		Last Modified: Thu, 22 May 2025 03:49:14 GMT  
		Size: 32.3 MB (32319689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc6d875c82818109716bcd51c9565bb1d0cf7f6dfc11ae03c699637b0bf5e6`  
		Last Modified: Thu, 22 May 2025 03:49:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98141f64067943e6cf38b657e57ef9fd6c219a8144f106d49a419bb03f2610c7`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 5.1 MB (5064044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbd0794f2e9c91d37028c0fed04827664849bd9238bb84877a3ebfc5c376ce`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21237248ffbda32bee414b4770165462875c093f4dfc3aab66f3a43cf1152a58`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d0ab259d978083c0c0a36ef9ce9fa11b3f0977f4fa12b9ad6b166def18481`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d96de84d3c36b73edcf03d56a6120964cf1f793130808d0b996bea9d34054aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850e8558f950668ca2d898dbe598aa21519669c17e6b00d77f4ac01e00cb9ec`

```dockerfile
```

-	Layers:
	-	`sha256:9a011b9eb596ef0e3bc09899afa5546451ec3114a972d79a678abf35e3035da6`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 2.6 MB (2573007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d61188bf429fcc4393841f4f614d11ab7706cde134b1356e1b1e0beafb67442d`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:989d105beecb382cf58e0f66f519767d4938c52cb4439d0a02a3a13c93bcd7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63947896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23da3f5746bac05b0f1d5b63ef55856d135885e4b2ab17fb2873d9c1ccde0f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca064f7c0632bec8acecd8b2fe7cfec7ddc1f6739cc172bad82631759a0712`  
		Last Modified: Mon, 28 Apr 2025 21:47:05 GMT  
		Size: 2.9 MB (2907778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fffc0adfa58cdc3d151691d776cbcb61baada317e35196a3f17ebbf2a3bcb`  
		Last Modified: Tue, 29 Apr 2025 12:20:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be8585055c5f15a8e239091c44bbdb27a60ea0950c21ff87e57d2e1acfcfe2`  
		Last Modified: Tue, 29 Apr 2025 12:38:50 GMT  
		Size: 32.2 MB (32153197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ed88a730e4e62edc6a6ecde7fe3d9b3add4fec579cfd18a6a7dce4c1468f2`  
		Last Modified: Tue, 29 Apr 2025 12:38:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a24b93bec042a8ff6474347b09ef9da88aa89d3912e6f386ad54720bc700b`  
		Last Modified: Tue, 29 Apr 2025 17:47:55 GMT  
		Size: 4.9 MB (4946454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548e2c225c91afdb04ea543da0ce0dd220abd7ec2bf7b00cf59c5f5b0644c9d`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a74dec10f690376a470d900f486ea05d5e4b80f86b993daa6a787f26d5ad5d`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0603c81d0988e5cb5ee3ddeadf237279b0e01563b63f91b047429e2add266790`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cd8191d0e48cac0b25055c448a570662afc7b72c10e475b0569150b424d0bf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3569f468c6f9ba38bcfac7a4053c0285b64d7514829de0a5dfc57fdeb6a9dd`

```dockerfile
```

-	Layers:
	-	`sha256:b66255ec1fbacd76060b4881c85e1d59ee3ac1f98168b172dd9cd1cce1b7a70e`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 2.6 MB (2553230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9720fe8e46902a6d514f8f05ff5d801773d937be1a1baf8fcbf7637b87295d3`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:6a8f433ddf8adf3a378a6f3f3d0f9cc7e56ce96134009ce6a6cadd8c16246082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72428868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9614b46e01bba46b1339e39a9737b8e01138c97dac5f7665635a801639a6911f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bd6bc7ca0b1d67b661b24fbf46a7691f56dab2d717dfc202a60f1c920c7b9`  
		Last Modified: Thu, 22 May 2025 07:15:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0d016cbefd1f183a6741c762a038411814f8c44cdeff5c89aab23d745767c`  
		Last Modified: Thu, 22 May 2025 07:32:27 GMT  
		Size: 35.9 MB (35893938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a583eb9b8ffeb88a9bddc73657225fcc4131a3cceae7ec12b494aa1e4f8c7ac`  
		Last Modified: Thu, 22 May 2025 07:32:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b481b90ab469fc4fc455caabcf7a8890040f83d7e0e6384701d85921ea4cec`  
		Last Modified: Thu, 22 May 2025 12:07:38 GMT  
		Size: 5.1 MB (5142866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb9817ab0c796e4659a16496d5f92247ff4fa90ebb43cf44f4377bb19b8b7f2`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b927cef6faf683814dc8619e3eb92a7c06ca07b18e7526b9c86a59569f9add`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911cc88409db00347dbcc57d922571cccf1252df868b55e37806fcca293a893`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e4769d728de6b99edf608237890e5f338713fe1613eeeb82744149d195b3a1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9724a530c63d337aa666d4eed7d7ff3ce1b193545b62b46a64b353093ebd7eb`

```dockerfile
```

-	Layers:
	-	`sha256:59cb05919bc1cad7d8cbab2e5f1e4ad85a4dcc90b152660c4dfa8f58f69b6ddf`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 2.6 MB (2569452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccb84257decb51526363f49916adae598d7f7a930298726438851225e24b48f`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:96522306ceabbf83988beb74de0f04490f13766be66c0a8788dd636ed2c1c50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70005726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc961979a96f34e5ef3c4d4d591402afd975c3e78d03a94cd5a9daa7db1c291`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbad29e8ec8e3d730986bc3a5c20018eb5cdae0101d7cb02600bf74c9dcc714`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 3.5 MB (3505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15ce14ce993ffff9f48b39579455b175fc24dba4a9dc09744eaffc5e7941f50`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcab8a3b917254fd76d87f9c839c9dfea6fe8be32466c7cdf30f9b0682ce256`  
		Last Modified: Wed, 21 May 2025 23:26:42 GMT  
		Size: 32.2 MB (32158845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d97937ade131e6a39f462c67ec0fb9abadb4c47e0140ea248369f8e1c793e8`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f65cf61b6469c05acb14ce1cf8ddc9089ff2b1fe83f7658053164ce0dc6434`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 5.1 MB (5131003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e078909a22e32856b074a16431e7077154e7bfdf203fbd047e58f711ae62671`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2619051c5bc653d40e96d230006cc0995032c7a8cf7db0b1c9fdcb1b15a008`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a5f15f5d4cbe6df5854d92a4721cde4edff7b9e982ce5e14eab209ebc7efa3`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:963b645373e17a7dd5df0898751bb575e80d4e2ce26ea85859fc7a5e2c45f0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80435bb9cd78eb6cc20abfe8ba11fb58048085cbbc154edf89b73ecbd8732767`

```dockerfile
```

-	Layers:
	-	`sha256:da8660b26801ade57a754efa47ef52a57207aa7ff2e58d15540160ad170efd0a`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 2.6 MB (2566391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7918247ad76a0acf403f0a53b10d6d0472e6b86f35ebc70976c8c283498c5b1d`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0fcde532ba25d3dde498f59301524917821062910f855a5b7b791892110f3694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75070333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82d024ebd0d2459354ff11b5916f6741789e91d56ec04804dff1c230b5725a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dd76f60873e36a2ef2d22238cf80226734882a65c6026751c657d5e01c4ff`  
		Last Modified: Mon, 28 Apr 2025 21:47:41 GMT  
		Size: 3.7 MB (3702919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a5d43e9710a6e7cc4fa2a97548175c06fb684ef5a6bf6bf104beb7d07f590`  
		Last Modified: Tue, 29 Apr 2025 03:23:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691ab89116c60731f2d6fd6257a8c2c94601b5d4158ce7a2d0f6e9965b36d91`  
		Last Modified: Tue, 29 Apr 2025 03:35:58 GMT  
		Size: 33.8 MB (33827394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be576cfe66606b1543169d9a80faed604780093b6dd97706df1c9848c856ddbf`  
		Last Modified: Tue, 29 Apr 2025 03:35:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81a860b54840304151bd241744c72b6f18873fd80599e4f1dc43407c7d9570d`  
		Last Modified: Tue, 29 Apr 2025 08:12:32 GMT  
		Size: 5.5 MB (5469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889443c94761ef6542694206721cd60466ae4325f2ec52bab0641812ec85060c`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8022a886dbb790c6f755aa7941e4164a6200bd1eb1d1a82b9b71dc44e613e5`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124fbfc530324bc33fcf9282e5b97dfc96ea9e07137a2d347bda72ced5395d3`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:49782b7c6023352105a8df78345d298655f4e3da367daabcaf8ef904882a3176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925659ced1d1c7bbcb87670ca990b821dacf4df5d86e883367d534048a5442bb`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e23d5af8202e37b6685fdc1d02a69065aa3e2066e14c491c2eeb2905f5b50`  
		Last Modified: Tue, 29 Apr 2025 08:12:32 GMT  
		Size: 2.6 MB (2555323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39149fa1517ed2e29b5bf688f0a737c1759723612a338c78e654c5568f9b4370`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8848159eafd94e2585d97a62e61d545f27ac6829b2c7600b47b33dfe20f776a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68320748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25730be9fd4eda5a8c9927b31f044d36d831f0dcbbee0907a13c5b68adcb195a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea620f7f490e88536a1b4c6ec0bc57e080f770ab010a69f37900a29d34f73bf`  
		Last Modified: Thu, 22 May 2025 03:25:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4e07ad6df1e8ef820771bf3ceb20d87afe840a4e0447a7cbc9470c8db11db`  
		Last Modified: Thu, 22 May 2025 03:33:57 GMT  
		Size: 33.1 MB (33092007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa788e379cb46c980dbacc1575b979443bdeae78f05d06172db2c76550dd47a6`  
		Last Modified: Thu, 22 May 2025 03:33:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54d00cad86f035d3097aa8ec728acecae3e1c8e2cf20157b07937663360848`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 5.2 MB (5178639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d12508e0859181af16aae446f3eb0a5f4b736960443f1260b6738b678bcf0f`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13818cd3319901e4ead2990df572f803aa97d376b31ef427342afbc734a50fc`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db741e2555ad98d05af73bdc958fd01902c66b08ebf20367e9dd3b3436e5547`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd81e1b9a187a2b293ea98be5b2a25bb65c93e7fbdd75940149048c3846ad28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f8a8378a51828a47ff59d9009621450245946c4230aaf9f98075f2b537c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:d34eba0e1c04a0f36730094513259e438bd0fc53ad47c8c33b69b1384c883ca6`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 2.6 MB (2568929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff131baf5c5e2f9bc4e7f085d8c648ef4c9847d32c9e36c25bc8a4ce01f3c5a`  
		Last Modified: Thu, 22 May 2025 06:16:11 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-1.0`

```console
$ docker pull fluentd@sha256:26da511c05952bf0eb1bafe44b8d6e5c22e5956cf249ca2b1f31b58cb4640c99
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

### `fluentd:v1.18.0-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:fbfc9bba839a42d5b5d2762530eb480309bb6b634d49b05623cf1c55339a4bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13509279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67856d15ed229333f703f25d0dca497343d4480dfad1b7e05fbba88a8426f02`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4debbdb0f911c5a6e01cc1643f908bb8db04777534fa3cdb81db39d945d09ba6`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 10.1 MB (10086242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3a0d5bab45faadc6a6f18eb50324643db72fef9bddbeb7700320669f0cc54`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d14147eee879f45943b0411811cae295fd7b8ea752cf7e2a49b20108057c0`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b62b34491d5780e65e11bb3f3e876cecf56f750ed114f9155e9eb9b28ae308`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:260ecf0b8d8066ca228c08d3222755612d31d03e91a9e58a62a1a142bbdc1c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52afb200e9f8c8101adc0c4cd7fe1909715b4403007f7a429c947593c2cdb9`

```dockerfile
```

-	Layers:
	-	`sha256:2d26f2ffa55bde84cafbab81c48e27de088c68588c996feffaed7d2c16b7bacd`  
		Last Modified: Fri, 14 Feb 2025 19:28:01 GMT  
		Size: 972.8 KB (972759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed396271942deba1985acba0d0d9c6ad7b07fcf7c58c23218e1e2fcc61c4478c`  
		Last Modified: Fri, 14 Feb 2025 19:28:00 GMT  
		Size: 14.9 KB (14856 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:83a87c14c041e626d8bc2543e5273bc2c7121763758dcd4b9c37187284f49cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12299356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e56d502fa527c511179ec447dfcae2e2b2dbee30bdc4fde6d476c23bf51d88`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b576c8bfe3cd90f8abdb27167b1ccf1b615751d0ecf975b06e7e0090c3a15`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 9.1 MB (9119653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f932bd6990d9af1d764fd5e8ed472a4cc4580a29591fe102eef621caf0efb19`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5154b26a8a1a65d3539f56a0621ce1be390b341d99256bfad6f8b1823c8c970`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97efe8a03db875c86ce84f91c4d106a0dc77e3c8bcb011d516bbb93f2f0b81`  
		Last Modified: Sat, 15 Feb 2025 09:08:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bcae9e3ce74dbeed79436268690dbeef12a673ba9fc48d55def7956cbd704c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143b2a56c351f646a3482dab11d4ca59a5556797525f2ae3da333f8b4f7239b9`

```dockerfile
```

-	Layers:
	-	`sha256:583cfcf8b09bca67618476429799443e90b0779d4065418fed968b317dc0c916`  
		Last Modified: Sat, 15 Feb 2025 09:08:11 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cb5771afc7d84e8e717c60144fc70ec7692bc5a721e6884508c43d93c0c64f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13578054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0a6dc663ac792ffeea78faf736023f0d6cc61de3f49a2c7f2669461a27222`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eac0f794f35dd21a50ffe3a8aa3c90ed1abdc83894d9adc2a798e2d61656bd`  
		Last Modified: Sat, 15 Feb 2025 06:35:45 GMT  
		Size: 10.2 MB (10214464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fb865b862765b27bc92a2740809a61e8e5615173e583efd7f61e7ee2cf802`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f307bbe8260b53e3de03bc07b3c8548515b326371c8148bd65a295f31a28aa8`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161836b294706554acbe6e40e52c3219c98f4f11ded69d83ee849f718716d9d3`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7483c66f371562c48496c8d3006533bf4b49ee383ef6541cfed437e4d55200ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb10a90fc8153a210f2dfb7705628229501bc70e3f1205dc0fdfe1a0c3518cb4`

```dockerfile
```

-	Layers:
	-	`sha256:ea4aa20a6b3288b0fecfc93cfcfcd20f1e724c09dc8774308ae759a6ab9fa734`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 972.9 KB (972901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8213b169a36e5a508c94530786274818c882cdd9a44f44a28c54df94251e3a81`  
		Last Modified: Sat, 15 Feb 2025 06:35:44 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:2d5dd6de34473cf5e26b9ac4c9f265a38798ac1c6cfd551c9307925e8ec8cea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12610800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b9bc42e5473692d13094bb26c35d265b760100fa1052d30df2f8e49b1b2454`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a5e8449d213a5ffc76f9f6ecc451d44b4a97f2f5bd0d000977e72aea0a951`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 9.4 MB (9353191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c246acea2bc9b5fe9f1ba7441ca5758e17a3b78c4f10f905449229c426711907`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58701eb3fa68f3262fdc1713004ae7b861adcbd1c15f4296f8a4743d2711694a`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd8599e8bd203fb81e78c21c9cc2e83f3c5a0fee1d2af35b3effcab7d01252`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7402f3dcde1b466c339ef64deddcf357b5432a8f94ddde5af380cc32df0d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c03fa47216f9da0bc0ee3c51e9086e1555d2f32905041f870a485887218a624`

```dockerfile
```

-	Layers:
	-	`sha256:b91288251a1fdd2d1a129920893d55d52523e5a7aae24397221a42bdda5744ba`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 969.7 KB (969682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0de1857b95fb21e202289b3510b23b03626e523a576677108dde6ae5e3bf536`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9b26f373d9756fdd9a2f3abed53bc34efec0f348d6b9c67e1cc009c1c73bb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13240672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f35dd176b1809aad53f77759641816527b3a02c1d46439ee120a8a52b25f68`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeed9dc76376a6743086aedaf5d78e3cba2b6d06ed9e5eddecbcd5a5e1619a5a`  
		Last Modified: Sat, 15 Feb 2025 01:14:28 GMT  
		Size: 9.9 MB (9872370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10226f89004ae0a38d6d917f4da07f05851c55f0d35439f3c9efac570988db`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a6831625e07b4156af52683e748c75ec4c6472b592bc3e275fee2a45701b09`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630533c9fdcdb5139ffe4ad4ecb58a39e09550dde57d51f672141536ce5da298`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a989e18c0f4a50ee66fee23ff10f349c6eeb741a48a9ac7d2ed94401b7fd48f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc8d036e605ecda86676b5bfcdee37af6f6f46bbe6e2abeb4c38ba308cbf951`

```dockerfile
```

-	Layers:
	-	`sha256:75662b4e746d43d292ec045b8aeac2083f4731e0853c1eea3d646435757adc45`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 968.5 KB (968465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92abc9f0408870fa60f0cd877fbff73b107ac61fcaca01ddecc1cf857b19ca25`  
		Last Modified: Sat, 15 Feb 2025 01:14:27 GMT  
		Size: 14.9 KB (14891 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:c64264d171d5cee4f91d4b213eccf7a7ba8bdd3a453a03928fa23dfdf05d46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12899067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fb47d60c2f61056ce153379fd7af83e1eb72ce95d033f3bb378f8ae598ae15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
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
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26795c9d7cbedbb061762126dee87400bcde0b301c13a89541c19945e7c2411b`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 9.6 MB (9642077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfaa5c8bf2b0e302a41897a4b65a3f3f66c0aa9e27b14ad97384e78517bbd45`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d3bed418f9ce23888e7cee8e81bce35e4e88a984c4728d1a6b158715eea453`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb109503f502bd2dfd9413be3791e42084012bb51f7cdd0ecd59b87ad1ea32`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:32f2698336ef5fb1f7e0a4feca6a3b685547d349de37fb3aae8cf1fe9d8c1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90f400a3560d4a199d0e4247c2dd963af4850dd23a5e7d5867199d850900b1d`

```dockerfile
```

-	Layers:
	-	`sha256:114fc7556a550965bdaeefa06f749964a0dd03420062f0efff0429098b51a448`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 967.8 KB (967849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1186777b12e9af7a92af466d79de1bf0eb0f02eb6367b706cf196622afcb3fb2`  
		Last Modified: Sat, 15 Feb 2025 07:10:36 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-debian-1.0`

```console
$ docker pull fluentd@sha256:d0e3feff84005d619bac90a0758779bf95dccfc8854abdda05467d895a3202dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `fluentd:v1.18.0-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:23436baafb2c9d27eb4e7307988828f224bc9685dea3ed93c76e555869906a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72832468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5025bca51a1719500078f6fcd20e1cba6cfd97bc25af8f801c522481989a2a70`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7633e3133f3cd11826b27263ce775541c067b4b2048f4e86655f471a82ce4a70`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 3.5 MB (3500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead891eaa911af415e0a68e057f82fe0d73cc00b062161e452e1403c4193247`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3bc76498e792d96c21ff737e6cc5daffb432d0ce4d19f19bf976815461e9a9`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 36.0 MB (35956627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c67ec9231c31d77ff43f924aa25a0f3489e25455a2c7c2aa521175191ea2d`  
		Last Modified: Wed, 21 May 2025 23:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3c7e9819d7804c6fcd6fa5df1daf8351b1e35804e10c7016fd63eda05bb4d`  
		Last Modified: Thu, 22 May 2025 00:14:41 GMT  
		Size: 5.1 MB (5147448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e020dd939c72abd293d288262979a25a33a55d164f043535c170a175d2659`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be566ec6f6f265dd3cb6123ff391d34faf00900374770755d6123e27459d6738`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb88fbdfe27989cd4e9fcc7b7d9ca25f9080f0b6c5438be29c6d9ebb544e05d3`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c862dfa8656a27781a167c49aadf25f7c5a7e185b5a6891658ccfeea5ec91c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6590f83e0f5807ef5659606dcb774b60b93db872573db66fd0772c0700ecceb`

```dockerfile
```

-	Layers:
	-	`sha256:388783ab52336d520a813b6fccd80af38827ab3f520658e0ceeac39e1e916f6f`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 2.6 MB (2569212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bc927d4df332c5edb2bc342822e64a0e6a69b4b1133b372b781796c12e7034`  
		Last Modified: Thu, 22 May 2025 00:14:40 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cc4378e2795e9b511eba55bf911949b29d1404122d8326339e90b3a73c7c97b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea89b9b1302eda176e4fe192485d482916a1ad901636a9854ee3b5ff1510169`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003df61415509173427026694951f93a0c0f9bd1c3bd389aa81574fd3cfbdd5d`  
		Last Modified: Thu, 22 May 2025 03:39:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5562ff4eff2d484cca8afe39dbc5bc323d0e8b50f7fc80a611e5cdfaade7d7`  
		Last Modified: Thu, 22 May 2025 03:49:14 GMT  
		Size: 32.3 MB (32319689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc6d875c82818109716bcd51c9565bb1d0cf7f6dfc11ae03c699637b0bf5e6`  
		Last Modified: Thu, 22 May 2025 03:49:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98141f64067943e6cf38b657e57ef9fd6c219a8144f106d49a419bb03f2610c7`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 5.1 MB (5064044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbd0794f2e9c91d37028c0fed04827664849bd9238bb84877a3ebfc5c376ce`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21237248ffbda32bee414b4770165462875c093f4dfc3aab66f3a43cf1152a58`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d0ab259d978083c0c0a36ef9ce9fa11b3f0977f4fa12b9ad6b166def18481`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d96de84d3c36b73edcf03d56a6120964cf1f793130808d0b996bea9d34054aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850e8558f950668ca2d898dbe598aa21519669c17e6b00d77f4ac01e00cb9ec`

```dockerfile
```

-	Layers:
	-	`sha256:9a011b9eb596ef0e3bc09899afa5546451ec3114a972d79a678abf35e3035da6`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 2.6 MB (2573007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d61188bf429fcc4393841f4f614d11ab7706cde134b1356e1b1e0beafb67442d`  
		Last Modified: Thu, 22 May 2025 06:24:35 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:989d105beecb382cf58e0f66f519767d4938c52cb4439d0a02a3a13c93bcd7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63947896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23da3f5746bac05b0f1d5b63ef55856d135885e4b2ab17fb2873d9c1ccde0f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca064f7c0632bec8acecd8b2fe7cfec7ddc1f6739cc172bad82631759a0712`  
		Last Modified: Mon, 28 Apr 2025 21:47:05 GMT  
		Size: 2.9 MB (2907778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fffc0adfa58cdc3d151691d776cbcb61baada317e35196a3f17ebbf2a3bcb`  
		Last Modified: Tue, 29 Apr 2025 12:20:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be8585055c5f15a8e239091c44bbdb27a60ea0950c21ff87e57d2e1acfcfe2`  
		Last Modified: Tue, 29 Apr 2025 12:38:50 GMT  
		Size: 32.2 MB (32153197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ed88a730e4e62edc6a6ecde7fe3d9b3add4fec579cfd18a6a7dce4c1468f2`  
		Last Modified: Tue, 29 Apr 2025 12:38:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a24b93bec042a8ff6474347b09ef9da88aa89d3912e6f386ad54720bc700b`  
		Last Modified: Tue, 29 Apr 2025 17:47:55 GMT  
		Size: 4.9 MB (4946454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548e2c225c91afdb04ea543da0ce0dd220abd7ec2bf7b00cf59c5f5b0644c9d`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a74dec10f690376a470d900f486ea05d5e4b80f86b993daa6a787f26d5ad5d`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0603c81d0988e5cb5ee3ddeadf237279b0e01563b63f91b047429e2add266790`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cd8191d0e48cac0b25055c448a570662afc7b72c10e475b0569150b424d0bf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3569f468c6f9ba38bcfac7a4053c0285b64d7514829de0a5dfc57fdeb6a9dd`

```dockerfile
```

-	Layers:
	-	`sha256:b66255ec1fbacd76060b4881c85e1d59ee3ac1f98168b172dd9cd1cce1b7a70e`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 2.6 MB (2553230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9720fe8e46902a6d514f8f05ff5d801773d937be1a1baf8fcbf7637b87295d3`  
		Last Modified: Tue, 29 Apr 2025 17:47:54 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:6a8f433ddf8adf3a378a6f3f3d0f9cc7e56ce96134009ce6a6cadd8c16246082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72428868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9614b46e01bba46b1339e39a9737b8e01138c97dac5f7665635a801639a6911f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bd6bc7ca0b1d67b661b24fbf46a7691f56dab2d717dfc202a60f1c920c7b9`  
		Last Modified: Thu, 22 May 2025 07:15:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0d016cbefd1f183a6741c762a038411814f8c44cdeff5c89aab23d745767c`  
		Last Modified: Thu, 22 May 2025 07:32:27 GMT  
		Size: 35.9 MB (35893938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a583eb9b8ffeb88a9bddc73657225fcc4131a3cceae7ec12b494aa1e4f8c7ac`  
		Last Modified: Thu, 22 May 2025 07:32:25 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b481b90ab469fc4fc455caabcf7a8890040f83d7e0e6384701d85921ea4cec`  
		Last Modified: Thu, 22 May 2025 12:07:38 GMT  
		Size: 5.1 MB (5142866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb9817ab0c796e4659a16496d5f92247ff4fa90ebb43cf44f4377bb19b8b7f2`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b927cef6faf683814dc8619e3eb92a7c06ca07b18e7526b9c86a59569f9add`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911cc88409db00347dbcc57d922571cccf1252df868b55e37806fcca293a893`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e4769d728de6b99edf608237890e5f338713fe1613eeeb82744149d195b3a1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9724a530c63d337aa666d4eed7d7ff3ce1b193545b62b46a64b353093ebd7eb`

```dockerfile
```

-	Layers:
	-	`sha256:59cb05919bc1cad7d8cbab2e5f1e4ad85a4dcc90b152660c4dfa8f58f69b6ddf`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 2.6 MB (2569452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccb84257decb51526363f49916adae598d7f7a930298726438851225e24b48f`  
		Last Modified: Thu, 22 May 2025 12:07:37 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:96522306ceabbf83988beb74de0f04490f13766be66c0a8788dd636ed2c1c50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70005726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc961979a96f34e5ef3c4d4d591402afd975c3e78d03a94cd5a9daa7db1c291`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbad29e8ec8e3d730986bc3a5c20018eb5cdae0101d7cb02600bf74c9dcc714`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 3.5 MB (3505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15ce14ce993ffff9f48b39579455b175fc24dba4a9dc09744eaffc5e7941f50`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcab8a3b917254fd76d87f9c839c9dfea6fe8be32466c7cdf30f9b0682ce256`  
		Last Modified: Wed, 21 May 2025 23:26:42 GMT  
		Size: 32.2 MB (32158845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d97937ade131e6a39f462c67ec0fb9abadb4c47e0140ea248369f8e1c793e8`  
		Last Modified: Wed, 21 May 2025 23:26:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f65cf61b6469c05acb14ce1cf8ddc9089ff2b1fe83f7658053164ce0dc6434`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 5.1 MB (5131003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e078909a22e32856b074a16431e7077154e7bfdf203fbd047e58f711ae62671`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2619051c5bc653d40e96d230006cc0995032c7a8cf7db0b1c9fdcb1b15a008`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a5f15f5d4cbe6df5854d92a4721cde4edff7b9e982ce5e14eab209ebc7efa3`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:963b645373e17a7dd5df0898751bb575e80d4e2ce26ea85859fc7a5e2c45f0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80435bb9cd78eb6cc20abfe8ba11fb58048085cbbc154edf89b73ecbd8732767`

```dockerfile
```

-	Layers:
	-	`sha256:da8660b26801ade57a754efa47ef52a57207aa7ff2e58d15540160ad170efd0a`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 2.6 MB (2566391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7918247ad76a0acf403f0a53b10d6d0472e6b86f35ebc70976c8c283498c5b1d`  
		Last Modified: Wed, 21 May 2025 23:46:16 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:0fcde532ba25d3dde498f59301524917821062910f855a5b7b791892110f3694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75070333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82d024ebd0d2459354ff11b5916f6741789e91d56ec04804dff1c230b5725a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dd76f60873e36a2ef2d22238cf80226734882a65c6026751c657d5e01c4ff`  
		Last Modified: Mon, 28 Apr 2025 21:47:41 GMT  
		Size: 3.7 MB (3702919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a5d43e9710a6e7cc4fa2a97548175c06fb684ef5a6bf6bf104beb7d07f590`  
		Last Modified: Tue, 29 Apr 2025 03:23:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691ab89116c60731f2d6fd6257a8c2c94601b5d4158ce7a2d0f6e9965b36d91`  
		Last Modified: Tue, 29 Apr 2025 03:35:58 GMT  
		Size: 33.8 MB (33827394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be576cfe66606b1543169d9a80faed604780093b6dd97706df1c9848c856ddbf`  
		Last Modified: Tue, 29 Apr 2025 03:35:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81a860b54840304151bd241744c72b6f18873fd80599e4f1dc43407c7d9570d`  
		Last Modified: Tue, 29 Apr 2025 08:12:32 GMT  
		Size: 5.5 MB (5469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889443c94761ef6542694206721cd60466ae4325f2ec52bab0641812ec85060c`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8022a886dbb790c6f755aa7941e4164a6200bd1eb1d1a82b9b71dc44e613e5`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124fbfc530324bc33fcf9282e5b97dfc96ea9e07137a2d347bda72ced5395d3`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:49782b7c6023352105a8df78345d298655f4e3da367daabcaf8ef904882a3176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925659ced1d1c7bbcb87670ca990b821dacf4df5d86e883367d534048a5442bb`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e23d5af8202e37b6685fdc1d02a69065aa3e2066e14c491c2eeb2905f5b50`  
		Last Modified: Tue, 29 Apr 2025 08:12:32 GMT  
		Size: 2.6 MB (2555323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39149fa1517ed2e29b5bf688f0a737c1759723612a338c78e654c5568f9b4370`  
		Last Modified: Tue, 29 Apr 2025 08:12:31 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8848159eafd94e2585d97a62e61d545f27ac6829b2c7600b47b33dfe20f776a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68320748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25730be9fd4eda5a8c9927b31f044d36d831f0dcbbee0907a13c5b68adcb195a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 02 Dec 2024 04:34:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["irb"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea620f7f490e88536a1b4c6ec0bc57e080f770ab010a69f37900a29d34f73bf`  
		Last Modified: Thu, 22 May 2025 03:25:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4e07ad6df1e8ef820771bf3ceb20d87afe840a4e0447a7cbc9470c8db11db`  
		Last Modified: Thu, 22 May 2025 03:33:57 GMT  
		Size: 33.1 MB (33092007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa788e379cb46c980dbacc1575b979443bdeae78f05d06172db2c76550dd47a6`  
		Last Modified: Thu, 22 May 2025 03:33:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54d00cad86f035d3097aa8ec728acecae3e1c8e2cf20157b07937663360848`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 5.2 MB (5178639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d12508e0859181af16aae446f3eb0a5f4b736960443f1260b6738b678bcf0f`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13818cd3319901e4ead2990df572f803aa97d376b31ef427342afbc734a50fc`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db741e2555ad98d05af73bdc958fd01902c66b08ebf20367e9dd3b3436e5547`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd81e1b9a187a2b293ea98be5b2a25bb65c93e7fbdd75940149048c3846ad28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f8a8378a51828a47ff59d9009621450245946c4230aaf9f98075f2b537c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:d34eba0e1c04a0f36730094513259e438bd0fc53ad47c8c33b69b1384c883ca6`  
		Last Modified: Thu, 22 May 2025 06:16:12 GMT  
		Size: 2.6 MB (2568929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff131baf5c5e2f9bc4e7f085d8c648ef4c9847d32c9e36c25bc8a4ce01f3c5a`  
		Last Modified: Thu, 22 May 2025 06:16:11 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json
