<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.7-1.0`](#fluentdv1167-10)
-	[`fluentd:v1.16.7-debian-1.0`](#fluentdv1167-debian-10)
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
$ docker pull fluentd@sha256:8f6621c6c32d49a334d97857790173087073b8a42e3c6f3a629d6328cfae8b79
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
$ docker pull fluentd@sha256:39d9febe071e2e73a7384455c00e55a7b9eae5821e0e03a2c2df4f1f4455779f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17362173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd935a287d31fd25265b6f82ceb18ecf0d0dc4d520b1562f6d144d49dcd7cff`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafc288f05039d230f9790c92d80970b28fb8bd4ab6f6337057449127a5ee21`  
		Last Modified: Fri, 14 Feb 2025 19:27:42 GMT  
		Size: 13.9 MB (13939139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f8f39f9b117cb82c827b7c3c4fbd1eef25e3dde3bb25d078ac89fe6390ff4f`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27f9e76346d4597dbaef3883968c32c49d941cae18c59d12848caea03790a4`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a053dff077af81471092e271a85bf91b48d5956d02a4dce4f58d59c9e848f5`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:41b653ed4fbb7c2b9e35400eba83af3280f06e589a9dfe6ef092a37a74bd5da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.7 KB (985726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42388cbb837d65fc548a9258f735a103fec87d1babe07d94a1148354c1f0a729`

```dockerfile
```

-	Layers:
	-	`sha256:1b35d9ea7c0607f8e1fbef762e93c3c66fccbf4d60a988d5f499ce2404d37107`  
		Last Modified: Fri, 14 Feb 2025 19:27:42 GMT  
		Size: 972.0 KB (972049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc055f5bc20ec78cf29f888371aa51fc3886b961f3c847cafb0ac3b8e62c5230`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:61b4ecb6e3ba1929f230bb2230866edff6566de0e974bbcb88aca68b4a5b79c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16110941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578e16655eda45d18ce19e8353ebb9177441728d417b957543e641d813a72ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702eae2b412a93d08594bea2e718e340c915ade5e68856463da25fd0b1b55f5c`  
		Last Modified: Sat, 15 Feb 2025 09:07:00 GMT  
		Size: 12.9 MB (12931245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986e789097d156bbdbdc5afeaf233d3cc7a4a0418fb0c91fe7530e4979d430c`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a417707a08f29b267e0f672ed6a0eccdc781f3c3506c4b534e4f44bd732b2`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1450fb80f71ddc0c70cabbdb97595e9f2147d3be2fabf7283b3e24715d3c5b4e`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8556b29894fad6278ab50ae91af6c09274c10f7d44b6d10e070212cfc0b3257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847d49c784cd2d1f49a95f1681449659e3e1c200652f1ee82706cec8a7f73844`

```dockerfile
```

-	Layers:
	-	`sha256:d8c9453975dcc01d7cb21503450150f68a63b4fc6c4072e2649321863a9639a4`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:248e93c792b109e0e5e53fdb69b022ae69b68f3161339ea6f43528a763b1e26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d5fc18a223a367dba40433f350f1bd1aa82cd69bfbe635baa2517f38eb7479`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac5e4d83642815488a67d30e8e536cccf527b55f2adf3065108401802197c82`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 14.0 MB (13982416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec3bc5dd7337e815de05ee24c5b47f38ac9babca5e8074457040b78404bdae`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09beee3521ccfebfd187c14ae9c301ce03c4c78ce8d9e4af050a81cddd142c`  
		Last Modified: Sat, 15 Feb 2025 06:34:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1648bc821679daf1e9ff790c8114bb2979b554ea6192fad84541a53118f51b`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ea1e5fda13fd7de92d2313908295ed32720eff35aeb3020ec53069a82722ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05155fe9263071b1738d473b051a227b5e961c8d05e57ecfbc925320dc05ac35`

```dockerfile
```

-	Layers:
	-	`sha256:0da9f4423f8c5c1046d3c4db4ae152aeaa7031072de16aa42a4d145bc357672d`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 972.2 KB (972179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d42b7895502287e56fa8c463611876e7c7e3b39614367cfb0b14c57a19565a`  
		Last Modified: Sat, 15 Feb 2025 06:34:39 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:ce17b7c675e43caad07c1cef1eb6183718d2c52356d9d97e215fcd19e531d895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16320044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7488d9dd3c92873234e8d00004dc53aa324d836788799b302de50c1358d2041`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc388d1f493dca56a53a2626098cdd71bccad9a5d66d8078b7710194dcf5397f`  
		Last Modified: Fri, 14 Feb 2025 19:25:34 GMT  
		Size: 13.1 MB (13062432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4843edaa49ce6de455ce5051ce9c5821e91b2315a330183a5ac55c6b315bb186`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fb6a969d1bf18f35c536e13d2b35001617a15c7ed2316d7fb258645cbd318d`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce11216e5f1558af2dadcc188b9d7b10a145cf4ca6fc5f7c9f0ca8b17bd52d23`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:25743347427f3c98c00eb6182bff96007edaae3adeefb38ae549d22ebad00d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc9bc2631454779098d4a81c28fcfa4d2681114d59a22a4c2aa4e585bbe7bcc`

```dockerfile
```

-	Layers:
	-	`sha256:bc81c1c536ad3ce0cfde9c887e21d0e6d2ffbc22e241afc3f0630d2d200e19d7`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 969.0 KB (968977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f325d9c57c5d351b0983518724f6cacf85c00a1099cf0757a2c2b040ad0c0d73`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ac37bb027d243b8be26f3ebb0f5e17b2ed753873e9b93931cef9df86e886408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16908232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f96b9859ede6ed9f0ff23cc71cb596e92774a9dd6eec1f61d3200ad12a131c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550851ed00854bf84e1226e97d61a68876cb884e1b41d1ef2c6d2e17aa10f6ef`  
		Last Modified: Sat, 15 Feb 2025 01:12:36 GMT  
		Size: 13.5 MB (13539929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c27fd63a04677340d0e74b4e85a2e3cdb72c0088cd5b7f6d9bc072796376181`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c039641837a859854d01a99543a495e42f15d3f3edca047130d2507874924`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a77ae68fd5681af3d487f8301330d9ba96ef6e4577a34d77d37f7daa7f17e`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9e0ce1b41214efdda76a8d1ef6e0005fdd0f6b94e4b3d661bb8349939281efe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d19e38fe07dcdb9423f9c39a8d9306fd32611cd535856d5732810c21ad70972`

```dockerfile
```

-	Layers:
	-	`sha256:c45db0ab3cf5ec450a0a456f08cdb9b535f0ad8ae5364afda96f4c32e1b30748`  
		Last Modified: Sat, 15 Feb 2025 01:12:36 GMT  
		Size: 967.7 KB (967749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102217c469e80429fd3854b31f040bf29fe8388f5e2168e82009dbb5942bc04`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:ea2c78e352ee5b906676ab29d58b876c8d633c34ef4286be05b40a6f4c046cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16748565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df449370eabde5ee0049c5f3c0da826231d4197b4bc29db3b0781b4575ffd24`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437b6f6ee442a8f58e02c31315423148733518186f7876c11b78e58ed5d1047`  
		Last Modified: Sat, 15 Feb 2025 07:09:05 GMT  
		Size: 13.5 MB (13491578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b44ddb87520263eea3200f0c9da6f3bc982f947670cb2f2fca1377f889021db`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c218d9279ab2ba2cefbbfba0afcea650de821e01a3a5aa54cadeb9d61342cc`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb2c87b6d849ba71c1a072a4dd0878c50295473dfa34f7ed3642230f00f391e`  
		Last Modified: Sat, 15 Feb 2025 07:09:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5452abb3dbc43390a58e8aaced1f4d3cf2bcd6cf55104921b5d1640ab7d96a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991895310aa9b01b48c92f28ccbf85bc52809b3e5279f9ca4e987d0c9060bd43`

```dockerfile
```

-	Layers:
	-	`sha256:87aa1015f9efcee2975c5e25cdde837dd0a8db71303e600db95a36ab639cdd27`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 967.1 KB (967139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19336607e6691a9871290ab50b8203cfa7e590ef19e9e15087698f93ecf28c96`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:76028c536fc55f4087c6f5438c3d4a388efb48639bbfdb6b4e2ccc0884139da9
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
$ docker pull fluentd@sha256:2e2009a283fcf6c3f60eaa6d0c361730e46ed467a8a1d78c06d17a27d33f0288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81938098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecf6f1c37c06e27bd8e8d9e1e7e90d045a359ecf60dc31e5ed33682ce94c085`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c226faf7bed8a12e29eb84f2e18d6944f226b76e7ab699863e165403d0ba4`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 3.5 MB (3499333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36abc0fca086e6999407f981c69938ee8dd1837f0565dca22b2b918cfe12e91d`  
		Last Modified: Mon, 28 Apr 2025 22:07:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e674df25f2be9bfae7f45a1d65025495004459ad5f1f280f9fe71ea5f2c76a`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 36.0 MB (35956660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ae8c310adf866d680dd353fab5c3ce736d43082f5d142ca8c1602f89199a0`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9060b462ecab8263b9ca264d1c145afef80d9297187580d3d8bd0cb7a9702dc1`  
		Last Modified: Mon, 28 Apr 2025 22:25:58 GMT  
		Size: 14.3 MB (14252067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d449e7b3f75276463f53876cad2cfb208af91a900c0d1a72852b5462f7400217`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca49d03456a9d7bd7e320629f2061804044376a3d09b30567503b9a3dee96a`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fdc1ea0abbcb802917196e3c373918265d2cca3412106c524528c43f8b78ef`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d0346832b22873f1a7d2e18f90e3feb2c5542d750fe4a631077134f3c9bd0d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef2b9cabe731ba0902afcdda9e53a3fc5cda2624815262c23dda97a3d2e67c`

```dockerfile
```

-	Layers:
	-	`sha256:d54806aef8c31936592514089996517c27664e4d54488cfb5fe032beec85f611`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 2.5 MB (2547168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f761745f83c913399804470572c4f727ffaeee07e4a7e2ff06b29ec9ec5096e`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:4463aa93b595b1871fdb5c0a1632c0a76d210544dc1d4b9524c162771a46e388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75383594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a81421689b3d2374a137272892a0f50928c2dd11b0c2e0aa1e1cf254f82ddf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ace276ccf28d2fc068800ff40da67bacf13b8d590cd438ae9b974a85399b7`  
		Last Modified: Tue, 08 Apr 2025 08:01:12 GMT  
		Size: 32.3 MB (32318421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a44c44c2bc2a89734853f98cc590486713b86056d616d936e75ae922029e2e`  
		Last Modified: Tue, 08 Apr 2025 08:01:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc659e8fed1b9ba3199b611c23b1839e9a66c0fb05e2317f605ba9f4218656d`  
		Last Modified: Tue, 08 Apr 2025 10:24:32 GMT  
		Size: 14.2 MB (14231495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efea622418a713c1deb03d9ef6864443df74acc81414c47e929d0b57457e8418`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29db160306b1b450971f42335377d14e9af1d6e37ec2823e1dcdd3684924f05`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cb116c0d47f802a2716dcd89b30a9bfd24e469c2f7553cdb65e6cfbf0a09ca`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2e7889c91890635d48f21b277a534822123bdf00cf2d6c436798e2c15c3d7e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be39a97a4d304812c6d7c7c2f9814944946bde79115930e1af6c7f128db9406`

```dockerfile
```

-	Layers:
	-	`sha256:f85be45fcb4b3a0076b781457646ad74ad5b0fda18dc2309c9cf2830bb576636`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 2.6 MB (2550655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1f5c91ba88bc709c4c18cb3389ed45502ff0065815e03850fee4bd47a4ea18`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:6225f2f3c123b7f9308e0c794861638043e0d79c059e304546ad38920afbd9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73155905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43f59dbd5dc9554e965dd167cf845f3fc443ee8aa7a199c4459755f8188f6dd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4117fa5740138e3dc627d5e676c7952b8b38f59e516999aaf123bd52413e129`  
		Last Modified: Tue, 08 Apr 2025 16:43:18 GMT  
		Size: 32.2 MB (32153152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6edf3a23aa90880dd4a05fbca27132e93e2ee600deb0da6097a09b4fc1e039`  
		Last Modified: Tue, 08 Apr 2025 16:43:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d4620679ccbe0350e125834b5d8164035965d60a95d10fe9cfd437648b9987`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 14.2 MB (14154710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99621bad8f185fbc3c43b3a6a753adfcf5669a67bd257e2d09f1032fe78d540`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8e9e32832c74bbeb5b5eb5e788172f54af00e747b8352e5a35d6938b4ed10`  
		Last Modified: Tue, 08 Apr 2025 21:16:27 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d859f00b45edc80bda333427efeeade3e126e578ef0f1fb871e17d797cb514`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d40acc61aa68470bb65fabe231cd46bc07fb44f966e7060d84845ac3162aa32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8522d3c801b4f8d9c36cdd0ff46bff65ef8808e52f5980ff27dcef4ee810b24`

```dockerfile
```

-	Layers:
	-	`sha256:d007ce09f323c8a69d57c40f4f0f6cb7368e76912c26d9575c3d40123f3bce2c`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 2.5 MB (2549394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca78db6af1f19e2100f0c7ef2d5bcf7ef12990ec42a9ecec7c67f11fdb1c712`  
		Last Modified: Tue, 08 Apr 2025 21:16:27 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:827269b6f1f227fb0c8760bdee15e475fec4e50d2d1d549e9dd6247123aeaf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81522313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e882ad68ffd44126559df7fbf195be211e947f5d9637773dfd106af888b2ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44e83d5e2f979ccb91fe45546e2434667ec6a256cef574d5bd0d3d34393e72`  
		Last Modified: Tue, 08 Apr 2025 10:44:18 GMT  
		Size: 35.9 MB (35876184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed31c8969ebe3e759650c451926c94d1f34d68db1ce32159605128a26facc3`  
		Last Modified: Tue, 08 Apr 2025 10:44:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715b0538be86e9aa00e19f65e3005d88440688cbfac3c92f1211f742ff76809`  
		Last Modified: Tue, 08 Apr 2025 15:31:50 GMT  
		Size: 14.3 MB (14254529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb697e0a439fcb39f03394b92575a31ee6859a628f707876654002a1fe445958`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80d4a150d314e5f75e3dee470417e7753c5da648fc25eeaa84191a41066f7fd`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278238a5d692eb5ee9a178faef8e615aa814a5900cad56189e645660b9a6d87d`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6d55b56d71737bf9fb288914140343b02fffeda39341f26ef922ad43511823cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ce444e414d0444b1f6f137c52ac103bf4de12c2f0372755f214d5912a64877`

```dockerfile
```

-	Layers:
	-	`sha256:9b1eaecc31bc8b6875771ad6e3751741038cba05ede9e6dea3add94dc91bb21c`  
		Last Modified: Tue, 08 Apr 2025 15:31:50 GMT  
		Size: 2.5 MB (2547408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b06bb4f0efd495e7a990c26d30947c3cd7ebd42f79f38faaff4591fd7cd5ada`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:a7c1ff04388bf0066e3d096d2e228310bdd93c19438d138e50a958f46db4b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78920456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bd5f56871b038dafb0ab3c40783c74fa99d35d0e52f816f315312c1d70473e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9412fa976ce72ab10f7b2c17f54a325cba9a50db87a33cea3460d4bc3863cdd`  
		Last Modified: Mon, 28 Apr 2025 22:01:01 GMT  
		Size: 3.5 MB (3503437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bbcc7945c4987927c2d71ca40f36fd31129a9caf625c8ebb899a07ab8f18b8`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995c80b04acf004d88342453f4bb952afa6bb13309b817a14550cfc003740ae8`  
		Last Modified: Mon, 28 Apr 2025 22:01:02 GMT  
		Size: 32.2 MB (32159534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9024a427c2e8512bc862d20a0e3389f0e36db601cc86606e37028d5517c922e`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2227a6a806b41423b9c42ffe08afd7b363dd25518d7dd6306f65e4c1d56883`  
		Last Modified: Mon, 28 Apr 2025 22:24:13 GMT  
		Size: 14.0 MB (14044225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26552c80deaa05b1723a991be51de1233856a7f25165f4fbc97710a1c98c826c`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defc2b980fe1db9ecd7a5845f858dd4275d33585cee820feaf50877d956de4cf`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b4dbc9acf5539cbd602d30b470402dbe5e6b7b414843cc12e5597bde897c`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e0da57acbcef54427725bb2a09f4a79b205ffba876d85994d1c65554ef2fce01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4856db763ae8f6380d815fd9aa05c2f2bb0c7f4e1b612c26f86a8e7fd30bae6e`

```dockerfile
```

-	Layers:
	-	`sha256:3432d03c14b3931a0dde66403ea372fd01368efb923149c1283f9effe2e023b0`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 2.5 MB (2544304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:672c31277d93de6c04e1578ff73f9348e93610bdac6f31e744cdf906304c08a5`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5f97e6bd64374ad18701f1ccb02675f58682b139db5a33e692abee6acc122ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84249308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e68450ca6daf82c46e8b47a1f5e95b8a5ea808886bb24a7d4ce71a2bf5808f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae72dbe92456a45d4bf52d40dc3054a905511705bf8835f853e2f5e266d527`  
		Last Modified: Tue, 08 Apr 2025 07:27:56 GMT  
		Size: 33.8 MB (33826920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7addc1391d7bf16a1f4fb683dea9cac116cacf776d5c005e23fd3408c88d9e`  
		Last Modified: Tue, 08 Apr 2025 07:27:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0835b3fdff11507d5ad1a68812e824a2725c1a3df7f7f8f3b38a1c59d3b58`  
		Last Modified: Tue, 08 Apr 2025 15:50:59 GMT  
		Size: 14.6 MB (14648847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc029a6f19136053921c03bb4a8bcef018a647bb47015b7a014d42240254e31`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac2075ef2d5b1c57810c25bbe21f7f02a3a972c2af8d75d4c7c2a370662411`  
		Last Modified: Tue, 08 Apr 2025 15:51:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5836244308e4fecf58026563e4bca8ea9f1f9e56a6b6a171396acb53d65763`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2cb92cacd6ee0add8e2268380421338f0910170dcc4a30cf5be197dac07ccef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc29750c46d6e6b494f66b923dd5ac85b27cae32344c860f6b869352e833db8`

```dockerfile
```

-	Layers:
	-	`sha256:31be3ed3167e6df28703a3fc57d0ab074a0ff2c1bac8634c5f79f00ba2592cc2`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 2.6 MB (2551487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b6cd011d61d75e468742f7d6816b72ab6246a5380373e1a216bec511ac1058`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8af90cd5ad2fd2322d69be14e75dab1ac8079b5fe67f01dadbc2313c2770c382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77525772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf9ab66405ea02a905df7b363de6999d0a5454dbbb909bea81de25fecd5303`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbfcf42c8f8c0538a68f41e339e27ad611182847b1d51a2079b2b7a55ecfaa0`  
		Last Modified: Tue, 08 Apr 2025 06:18:13 GMT  
		Size: 33.1 MB (33091086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4e8a3c3c5e9cf10583a16d9b24256dc43681f90d1fd230eaa443cd24bc0910`  
		Last Modified: Tue, 08 Apr 2025 06:18:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57c722e2a6678356029ac46859cada57405277e3a5e7a30b5f8888216dcf97`  
		Last Modified: Tue, 08 Apr 2025 10:17:02 GMT  
		Size: 14.4 MB (14384316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c000e773559e1fe6083ae46de302441515cab188d2d052305448c699e6f0304a`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee76bd8d25c5bd070c7c9de2943ed481081677010c0df90f195145e26cc29f`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743b4c4f7706d05cce6c9f6d9af81e2eed7b51ae1a305e9728d673040012089c`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:516accf2173444927a34821e0dc5047a49d124f61db6b8137a3997540b9604ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0397dad58d0c3ba1c478a8a4cb80f43f961dc1535496f1bfbd8d889ded600c29`

```dockerfile
```

-	Layers:
	-	`sha256:51c355074035a79213a6d1e4f8e15726dbd869e9b4015a63dd32f874c23562b8`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 2.5 MB (2546885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41be9e4236749a101a9b1f9ca108446f2895c7496c36e55783689d4dfadaaca1`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.7-1.0`

```console
$ docker pull fluentd@sha256:8f6621c6c32d49a334d97857790173087073b8a42e3c6f3a629d6328cfae8b79
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

### `fluentd:v1.16.7-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:39d9febe071e2e73a7384455c00e55a7b9eae5821e0e03a2c2df4f1f4455779f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17362173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd935a287d31fd25265b6f82ceb18ecf0d0dc4d520b1562f6d144d49dcd7cff`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafc288f05039d230f9790c92d80970b28fb8bd4ab6f6337057449127a5ee21`  
		Last Modified: Fri, 14 Feb 2025 19:27:42 GMT  
		Size: 13.9 MB (13939139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f8f39f9b117cb82c827b7c3c4fbd1eef25e3dde3bb25d078ac89fe6390ff4f`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27f9e76346d4597dbaef3883968c32c49d941cae18c59d12848caea03790a4`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a053dff077af81471092e271a85bf91b48d5956d02a4dce4f58d59c9e848f5`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:41b653ed4fbb7c2b9e35400eba83af3280f06e589a9dfe6ef092a37a74bd5da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.7 KB (985726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42388cbb837d65fc548a9258f735a103fec87d1babe07d94a1148354c1f0a729`

```dockerfile
```

-	Layers:
	-	`sha256:1b35d9ea7c0607f8e1fbef762e93c3c66fccbf4d60a988d5f499ce2404d37107`  
		Last Modified: Fri, 14 Feb 2025 19:27:42 GMT  
		Size: 972.0 KB (972049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc055f5bc20ec78cf29f888371aa51fc3886b961f3c847cafb0ac3b8e62c5230`  
		Last Modified: Fri, 14 Feb 2025 19:27:41 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:61b4ecb6e3ba1929f230bb2230866edff6566de0e974bbcb88aca68b4a5b79c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16110941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578e16655eda45d18ce19e8353ebb9177441728d417b957543e641d813a72ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 18:28:25 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702eae2b412a93d08594bea2e718e340c915ade5e68856463da25fd0b1b55f5c`  
		Last Modified: Sat, 15 Feb 2025 09:07:00 GMT  
		Size: 12.9 MB (12931245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986e789097d156bbdbdc5afeaf233d3cc7a4a0418fb0c91fe7530e4979d430c`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a417707a08f29b267e0f672ed6a0eccdc781f3c3506c4b534e4f44bd732b2`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1450fb80f71ddc0c70cabbdb97595e9f2147d3be2fabf7283b3e24715d3c5b4e`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8556b29894fad6278ab50ae91af6c09274c10f7d44b6d10e070212cfc0b3257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847d49c784cd2d1f49a95f1681449659e3e1c200652f1ee82706cec8a7f73844`

```dockerfile
```

-	Layers:
	-	`sha256:d8c9453975dcc01d7cb21503450150f68a63b4fc6c4072e2649321863a9639a4`  
		Last Modified: Sat, 15 Feb 2025 09:06:58 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:248e93c792b109e0e5e53fdb69b022ae69b68f3161339ea6f43528a763b1e26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d5fc18a223a367dba40433f350f1bd1aa82cd69bfbe635baa2517f38eb7479`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac5e4d83642815488a67d30e8e536cccf527b55f2adf3065108401802197c82`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 14.0 MB (13982416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec3bc5dd7337e815de05ee24c5b47f38ac9babca5e8074457040b78404bdae`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09beee3521ccfebfd187c14ae9c301ce03c4c78ce8d9e4af050a81cddd142c`  
		Last Modified: Sat, 15 Feb 2025 06:34:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1648bc821679daf1e9ff790c8114bb2979b554ea6192fad84541a53118f51b`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ea1e5fda13fd7de92d2313908295ed32720eff35aeb3020ec53069a82722ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05155fe9263071b1738d473b051a227b5e961c8d05e57ecfbc925320dc05ac35`

```dockerfile
```

-	Layers:
	-	`sha256:0da9f4423f8c5c1046d3c4db4ae152aeaa7031072de16aa42a4d145bc357672d`  
		Last Modified: Sat, 15 Feb 2025 06:34:40 GMT  
		Size: 972.2 KB (972179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d42b7895502287e56fa8c463611876e7c7e3b39614367cfb0b14c57a19565a`  
		Last Modified: Sat, 15 Feb 2025 06:34:39 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:ce17b7c675e43caad07c1cef1eb6183718d2c52356d9d97e215fcd19e531d895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16320044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7488d9dd3c92873234e8d00004dc53aa324d836788799b302de50c1358d2041`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-x86.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a0b3986f0bfd04a0ec563f46510a21b6474ca6882bdf4b9f75c257c07db73d9c`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3255446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc388d1f493dca56a53a2626098cdd71bccad9a5d66d8078b7710194dcf5397f`  
		Last Modified: Fri, 14 Feb 2025 19:25:34 GMT  
		Size: 13.1 MB (13062432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4843edaa49ce6de455ce5051ce9c5821e91b2315a330183a5ac55c6b315bb186`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fb6a969d1bf18f35c536e13d2b35001617a15c7ed2316d7fb258645cbd318d`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce11216e5f1558af2dadcc188b9d7b10a145cf4ca6fc5f7c9f0ca8b17bd52d23`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:25743347427f3c98c00eb6182bff96007edaae3adeefb38ae549d22ebad00d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc9bc2631454779098d4a81c28fcfa4d2681114d59a22a4c2aa4e585bbe7bcc`

```dockerfile
```

-	Layers:
	-	`sha256:bc81c1c536ad3ce0cfde9c887e21d0e6d2ffbc22e241afc3f0630d2d200e19d7`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 969.0 KB (968977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f325d9c57c5d351b0983518724f6cacf85c00a1099cf0757a2c2b040ad0c0d73`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ac37bb027d243b8be26f3ebb0f5e17b2ed753873e9b93931cef9df86e886408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16908232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f96b9859ede6ed9f0ff23cc71cb596e92774a9dd6eec1f61d3200ad12a131c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-ppc64le.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9f4b9efb5cb4f152be62bf5eb5a9da9c7fbc32d1512d2da59fb9a3ef4d86c5f8`  
		Last Modified: Fri, 14 Feb 2025 12:02:22 GMT  
		Size: 3.4 MB (3366133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550851ed00854bf84e1226e97d61a68876cb884e1b41d1ef2c6d2e17aa10f6ef`  
		Last Modified: Sat, 15 Feb 2025 01:12:36 GMT  
		Size: 13.5 MB (13539929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c27fd63a04677340d0e74b4e85a2e3cdb72c0088cd5b7f6d9bc072796376181`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c039641837a859854d01a99543a495e42f15d3f3edca047130d2507874924`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a77ae68fd5681af3d487f8301330d9ba96ef6e4577a34d77d37f7daa7f17e`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9e0ce1b41214efdda76a8d1ef6e0005fdd0f6b94e4b3d661bb8349939281efe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d19e38fe07dcdb9423f9c39a8d9306fd32611cd535856d5732810c21ad70972`

```dockerfile
```

-	Layers:
	-	`sha256:c45db0ab3cf5ec450a0a456f08cdb9b535f0ad8ae5364afda96f4c32e1b30748`  
		Last Modified: Sat, 15 Feb 2025 01:12:36 GMT  
		Size: 967.7 KB (967749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102217c469e80429fd3854b31f040bf29fe8388f5e2168e82009dbb5942bc04`  
		Last Modified: Sat, 15 Feb 2025 01:12:35 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:ea2c78e352ee5b906676ab29d58b876c8d633c34ef4286be05b40a6f4c046cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16748565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df449370eabde5ee0049c5f3c0da826231d4197b4bc29db3b0781b4575ffd24`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
ADD alpine-minirootfs-3.19.7-s390x.tar.gz / # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62a7dfd821a632af62a9715f001a029d205a5e5f54a9b51b1cbe108b75f19d8b`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.3 MB (3254821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437b6f6ee442a8f58e02c31315423148733518186f7876c11b78e58ed5d1047`  
		Last Modified: Sat, 15 Feb 2025 07:09:05 GMT  
		Size: 13.5 MB (13491578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b44ddb87520263eea3200f0c9da6f3bc982f947670cb2f2fca1377f889021db`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c218d9279ab2ba2cefbbfba0afcea650de821e01a3a5aa54cadeb9d61342cc`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb2c87b6d849ba71c1a072a4dd0878c50295473dfa34f7ed3642230f00f391e`  
		Last Modified: Sat, 15 Feb 2025 07:09:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5452abb3dbc43390a58e8aaced1f4d3cf2bcd6cf55104921b5d1640ab7d96a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991895310aa9b01b48c92f28ccbf85bc52809b3e5279f9ca4e987d0c9060bd43`

```dockerfile
```

-	Layers:
	-	`sha256:87aa1015f9efcee2975c5e25cdde837dd0a8db71303e600db95a36ab639cdd27`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 967.1 KB (967139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19336607e6691a9871290ab50b8203cfa7e590ef19e9e15087698f93ecf28c96`  
		Last Modified: Sat, 15 Feb 2025 07:09:04 GMT  
		Size: 13.7 KB (13675 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.7-debian-1.0`

```console
$ docker pull fluentd@sha256:76028c536fc55f4087c6f5438c3d4a388efb48639bbfdb6b4e2ccc0884139da9
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

### `fluentd:v1.16.7-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:2e2009a283fcf6c3f60eaa6d0c361730e46ed467a8a1d78c06d17a27d33f0288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81938098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecf6f1c37c06e27bd8e8d9e1e7e90d045a359ecf60dc31e5ed33682ce94c085`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c226faf7bed8a12e29eb84f2e18d6944f226b76e7ab699863e165403d0ba4`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 3.5 MB (3499333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36abc0fca086e6999407f981c69938ee8dd1837f0565dca22b2b918cfe12e91d`  
		Last Modified: Mon, 28 Apr 2025 22:07:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e674df25f2be9bfae7f45a1d65025495004459ad5f1f280f9fe71ea5f2c76a`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 36.0 MB (35956660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ae8c310adf866d680dd353fab5c3ce736d43082f5d142ca8c1602f89199a0`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9060b462ecab8263b9ca264d1c145afef80d9297187580d3d8bd0cb7a9702dc1`  
		Last Modified: Mon, 28 Apr 2025 22:25:58 GMT  
		Size: 14.3 MB (14252067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d449e7b3f75276463f53876cad2cfb208af91a900c0d1a72852b5462f7400217`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca49d03456a9d7bd7e320629f2061804044376a3d09b30567503b9a3dee96a`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fdc1ea0abbcb802917196e3c373918265d2cca3412106c524528c43f8b78ef`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d0346832b22873f1a7d2e18f90e3feb2c5542d750fe4a631077134f3c9bd0d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef2b9cabe731ba0902afcdda9e53a3fc5cda2624815262c23dda97a3d2e67c`

```dockerfile
```

-	Layers:
	-	`sha256:d54806aef8c31936592514089996517c27664e4d54488cfb5fe032beec85f611`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 2.5 MB (2547168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f761745f83c913399804470572c4f727ffaeee07e4a7e2ff06b29ec9ec5096e`  
		Last Modified: Mon, 28 Apr 2025 22:25:57 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:4463aa93b595b1871fdb5c0a1632c0a76d210544dc1d4b9524c162771a46e388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75383594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a81421689b3d2374a137272892a0f50928c2dd11b0c2e0aa1e1cf254f82ddf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ace276ccf28d2fc068800ff40da67bacf13b8d590cd438ae9b974a85399b7`  
		Last Modified: Tue, 08 Apr 2025 08:01:12 GMT  
		Size: 32.3 MB (32318421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a44c44c2bc2a89734853f98cc590486713b86056d616d936e75ae922029e2e`  
		Last Modified: Tue, 08 Apr 2025 08:01:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc659e8fed1b9ba3199b611c23b1839e9a66c0fb05e2317f605ba9f4218656d`  
		Last Modified: Tue, 08 Apr 2025 10:24:32 GMT  
		Size: 14.2 MB (14231495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efea622418a713c1deb03d9ef6864443df74acc81414c47e929d0b57457e8418`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29db160306b1b450971f42335377d14e9af1d6e37ec2823e1dcdd3684924f05`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cb116c0d47f802a2716dcd89b30a9bfd24e469c2f7553cdb65e6cfbf0a09ca`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2e7889c91890635d48f21b277a534822123bdf00cf2d6c436798e2c15c3d7e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be39a97a4d304812c6d7c7c2f9814944946bde79115930e1af6c7f128db9406`

```dockerfile
```

-	Layers:
	-	`sha256:f85be45fcb4b3a0076b781457646ad74ad5b0fda18dc2309c9cf2830bb576636`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 2.6 MB (2550655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1f5c91ba88bc709c4c18cb3389ed45502ff0065815e03850fee4bd47a4ea18`  
		Last Modified: Tue, 08 Apr 2025 10:24:31 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:6225f2f3c123b7f9308e0c794861638043e0d79c059e304546ad38920afbd9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73155905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43f59dbd5dc9554e965dd167cf845f3fc443ee8aa7a199c4459755f8188f6dd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4117fa5740138e3dc627d5e676c7952b8b38f59e516999aaf123bd52413e129`  
		Last Modified: Tue, 08 Apr 2025 16:43:18 GMT  
		Size: 32.2 MB (32153152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6edf3a23aa90880dd4a05fbca27132e93e2ee600deb0da6097a09b4fc1e039`  
		Last Modified: Tue, 08 Apr 2025 16:43:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d4620679ccbe0350e125834b5d8164035965d60a95d10fe9cfd437648b9987`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 14.2 MB (14154710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99621bad8f185fbc3c43b3a6a753adfcf5669a67bd257e2d09f1032fe78d540`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8e9e32832c74bbeb5b5eb5e788172f54af00e747b8352e5a35d6938b4ed10`  
		Last Modified: Tue, 08 Apr 2025 21:16:27 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d859f00b45edc80bda333427efeeade3e126e578ef0f1fb871e17d797cb514`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d40acc61aa68470bb65fabe231cd46bc07fb44f966e7060d84845ac3162aa32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8522d3c801b4f8d9c36cdd0ff46bff65ef8808e52f5980ff27dcef4ee810b24`

```dockerfile
```

-	Layers:
	-	`sha256:d007ce09f323c8a69d57c40f4f0f6cb7368e76912c26d9575c3d40123f3bce2c`  
		Last Modified: Tue, 08 Apr 2025 21:16:28 GMT  
		Size: 2.5 MB (2549394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca78db6af1f19e2100f0c7ef2d5bcf7ef12990ec42a9ecec7c67f11fdb1c712`  
		Last Modified: Tue, 08 Apr 2025 21:16:27 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:827269b6f1f227fb0c8760bdee15e475fec4e50d2d1d549e9dd6247123aeaf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81522313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e882ad68ffd44126559df7fbf195be211e947f5d9637773dfd106af888b2ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44e83d5e2f979ccb91fe45546e2434667ec6a256cef574d5bd0d3d34393e72`  
		Last Modified: Tue, 08 Apr 2025 10:44:18 GMT  
		Size: 35.9 MB (35876184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed31c8969ebe3e759650c451926c94d1f34d68db1ce32159605128a26facc3`  
		Last Modified: Tue, 08 Apr 2025 10:44:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715b0538be86e9aa00e19f65e3005d88440688cbfac3c92f1211f742ff76809`  
		Last Modified: Tue, 08 Apr 2025 15:31:50 GMT  
		Size: 14.3 MB (14254529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb697e0a439fcb39f03394b92575a31ee6859a628f707876654002a1fe445958`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80d4a150d314e5f75e3dee470417e7753c5da648fc25eeaa84191a41066f7fd`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278238a5d692eb5ee9a178faef8e615aa814a5900cad56189e645660b9a6d87d`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6d55b56d71737bf9fb288914140343b02fffeda39341f26ef922ad43511823cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ce444e414d0444b1f6f137c52ac103bf4de12c2f0372755f214d5912a64877`

```dockerfile
```

-	Layers:
	-	`sha256:9b1eaecc31bc8b6875771ad6e3751741038cba05ede9e6dea3add94dc91bb21c`  
		Last Modified: Tue, 08 Apr 2025 15:31:50 GMT  
		Size: 2.5 MB (2547408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b06bb4f0efd495e7a990c26d30947c3cd7ebd42f79f38faaff4591fd7cd5ada`  
		Last Modified: Tue, 08 Apr 2025 15:31:49 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:a7c1ff04388bf0066e3d096d2e228310bdd93c19438d138e50a958f46db4b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78920456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bd5f56871b038dafb0ab3c40783c74fa99d35d0e52f816f315312c1d70473e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9412fa976ce72ab10f7b2c17f54a325cba9a50db87a33cea3460d4bc3863cdd`  
		Last Modified: Mon, 28 Apr 2025 22:01:01 GMT  
		Size: 3.5 MB (3503437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bbcc7945c4987927c2d71ca40f36fd31129a9caf625c8ebb899a07ab8f18b8`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995c80b04acf004d88342453f4bb952afa6bb13309b817a14550cfc003740ae8`  
		Last Modified: Mon, 28 Apr 2025 22:01:02 GMT  
		Size: 32.2 MB (32159534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9024a427c2e8512bc862d20a0e3389f0e36db601cc86606e37028d5517c922e`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2227a6a806b41423b9c42ffe08afd7b363dd25518d7dd6306f65e4c1d56883`  
		Last Modified: Mon, 28 Apr 2025 22:24:13 GMT  
		Size: 14.0 MB (14044225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26552c80deaa05b1723a991be51de1233856a7f25165f4fbc97710a1c98c826c`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defc2b980fe1db9ecd7a5845f858dd4275d33585cee820feaf50877d956de4cf`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b4dbc9acf5539cbd602d30b470402dbe5e6b7b414843cc12e5597bde897c`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e0da57acbcef54427725bb2a09f4a79b205ffba876d85994d1c65554ef2fce01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4856db763ae8f6380d815fd9aa05c2f2bb0c7f4e1b612c26f86a8e7fd30bae6e`

```dockerfile
```

-	Layers:
	-	`sha256:3432d03c14b3931a0dde66403ea372fd01368efb923149c1283f9effe2e023b0`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 2.5 MB (2544304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:672c31277d93de6c04e1578ff73f9348e93610bdac6f31e744cdf906304c08a5`  
		Last Modified: Mon, 28 Apr 2025 22:24:12 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5f97e6bd64374ad18701f1ccb02675f58682b139db5a33e692abee6acc122ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84249308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e68450ca6daf82c46e8b47a1f5e95b8a5ea808886bb24a7d4ce71a2bf5808f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae72dbe92456a45d4bf52d40dc3054a905511705bf8835f853e2f5e266d527`  
		Last Modified: Tue, 08 Apr 2025 07:27:56 GMT  
		Size: 33.8 MB (33826920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7addc1391d7bf16a1f4fb683dea9cac116cacf776d5c005e23fd3408c88d9e`  
		Last Modified: Tue, 08 Apr 2025 07:27:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0835b3fdff11507d5ad1a68812e824a2725c1a3df7f7f8f3b38a1c59d3b58`  
		Last Modified: Tue, 08 Apr 2025 15:50:59 GMT  
		Size: 14.6 MB (14648847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc029a6f19136053921c03bb4a8bcef018a647bb47015b7a014d42240254e31`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac2075ef2d5b1c57810c25bbe21f7f02a3a972c2af8d75d4c7c2a370662411`  
		Last Modified: Tue, 08 Apr 2025 15:51:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5836244308e4fecf58026563e4bca8ea9f1f9e56a6b6a171396acb53d65763`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2cb92cacd6ee0add8e2268380421338f0910170dcc4a30cf5be197dac07ccef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc29750c46d6e6b494f66b923dd5ac85b27cae32344c860f6b869352e833db8`

```dockerfile
```

-	Layers:
	-	`sha256:31be3ed3167e6df28703a3fc57d0ab074a0ff2c1bac8634c5f79f00ba2592cc2`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 2.6 MB (2551487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b6cd011d61d75e468742f7d6816b72ab6246a5380373e1a216bec511ac1058`  
		Last Modified: Tue, 08 Apr 2025 15:50:58 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8af90cd5ad2fd2322d69be14e75dab1ac8079b5fe67f01dadbc2313c2770c382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77525772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf9ab66405ea02a905df7b363de6999d0a5454dbbb909bea81de25fecd5303`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 07:58:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 31 Jan 2025 07:58:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV TINI_VERSION=0.18.0
# Fri, 31 Jan 2025 07:58:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.7  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 31 Jan 2025 07:58:59 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 31 Jan 2025 07:58:59 GMT
USER fluent
# Fri, 31 Jan 2025 07:58:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 31 Jan 2025 07:58:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbfcf42c8f8c0538a68f41e339e27ad611182847b1d51a2079b2b7a55ecfaa0`  
		Last Modified: Tue, 08 Apr 2025 06:18:13 GMT  
		Size: 33.1 MB (33091086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4e8a3c3c5e9cf10583a16d9b24256dc43681f90d1fd230eaa443cd24bc0910`  
		Last Modified: Tue, 08 Apr 2025 06:18:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57c722e2a6678356029ac46859cada57405277e3a5e7a30b5f8888216dcf97`  
		Last Modified: Tue, 08 Apr 2025 10:17:02 GMT  
		Size: 14.4 MB (14384316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c000e773559e1fe6083ae46de302441515cab188d2d052305448c699e6f0304a`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee76bd8d25c5bd070c7c9de2943ed481081677010c0df90f195145e26cc29f`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743b4c4f7706d05cce6c9f6d9af81e2eed7b51ae1a305e9728d673040012089c`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:516accf2173444927a34821e0dc5047a49d124f61db6b8137a3997540b9604ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0397dad58d0c3ba1c478a8a4cb80f43f961dc1535496f1bfbd8d889ded600c29`

```dockerfile
```

-	Layers:
	-	`sha256:51c355074035a79213a6d1e4f8e15726dbd869e9b4015a63dd32f874c23562b8`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
		Size: 2.5 MB (2546885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41be9e4236749a101a9b1f9ca108446f2895c7496c36e55783689d4dfadaaca1`  
		Last Modified: Tue, 08 Apr 2025 10:17:01 GMT  
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
$ docker pull fluentd@sha256:dfc88fced9234384c32f26b839c02466b28adcce85469939864811860d811c72
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
$ docker pull fluentd@sha256:fa90baf528e6d56740f51bc79696e978cf86412c23d0aea4403e02517097232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72832948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609c502b23a3191a195545328dfc3dbf135b95c9f061d4a674fdf6675a313657`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c226faf7bed8a12e29eb84f2e18d6944f226b76e7ab699863e165403d0ba4`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 3.5 MB (3499333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36abc0fca086e6999407f981c69938ee8dd1837f0565dca22b2b918cfe12e91d`  
		Last Modified: Mon, 28 Apr 2025 22:07:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e674df25f2be9bfae7f45a1d65025495004459ad5f1f280f9fe71ea5f2c76a`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 36.0 MB (35956660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ae8c310adf866d680dd353fab5c3ce736d43082f5d142ca8c1602f89199a0`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581af7caed41da96d13726c26c462e2bc0fabcc0bc35ac46e15d737562b7291e`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 5.1 MB (5146917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f8d2466977af4b9c4c45ff9dd55d02017cb6b621c8db173fa9d216c6cfa3e1`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32258058af23692d3b7f7dbc5a989efc2d1b21272521a86153f0649b9969b9`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f589733ba1b90219aa0bf449a5231c320417ad2d06d42e1d2c2772b0bfba4ab`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8a29d4677c2310397b12f72ee817075f5a3cfde9d637c8ec61285cc4e943a0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67316f4e5bf6c571b8982f3695a44242eb12456d4336c8f7c43d860d55ec50f8`

```dockerfile
```

-	Layers:
	-	`sha256:4b029a1598883523f00f17ac2472bfedc21c4ef464e2a54e0b49997b9923d0ab`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 2.6 MB (2551004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f9aed701a4bc111e7bfc37e990cbd9e1288b9274a5820091865adcc88e4ede`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:69df2de33d5304c10291d266d13489f9844646e98055b662f0466123dbf3af52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66215700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07ed22733355faebc4d4bc37dc3b7b6ae9f3c21f5f7cab5833ae5c2559a466`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ace276ccf28d2fc068800ff40da67bacf13b8d590cd438ae9b974a85399b7`  
		Last Modified: Tue, 08 Apr 2025 08:01:12 GMT  
		Size: 32.3 MB (32318421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a44c44c2bc2a89734853f98cc590486713b86056d616d936e75ae922029e2e`  
		Last Modified: Tue, 08 Apr 2025 08:01:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8f97336d7e59c5adf9af8a95c9477d24ec8257fbc6274e29cc07a199e3e51b`  
		Last Modified: Tue, 08 Apr 2025 10:27:55 GMT  
		Size: 5.1 MB (5063606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc5633a4d4cae1ece486b96a14221daf842f656f7e72e9630a80d51b18978cd`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2c1cb2918a2b5fbd3891604a4f57642e989f94b35ba313a43c0a0a0e77531`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f237b4515133b03d62c56e2ccdd843ed2b9199027139b371695ca4f29e807`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:706e2ca512efbd398d5133250a0e51b6468acc65b082212425f417690ff3e414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfe1a3b0708c9338e18bfdc7a5d06b9c93525c3d70f1ad0de28bcb0220c17ee`

```dockerfile
```

-	Layers:
	-	`sha256:622f4a3a551ef6c6ab8876f63a89b82f8bd9d3fd7a887c86009190f189823565`  
		Last Modified: Tue, 08 Apr 2025 10:27:55 GMT  
		Size: 2.6 MB (2554491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a476b22b3d54358eaf3e6e9480171aab49942f40bbe1a78e9fcb9b83c50264f0`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ed14294e1f464a07b4033d5f3c36a2cbfca381806a5b01548c614dd28411b372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63947370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0dfd1769b23c437fb3e787721ae113b0c9f8e20a711e80b597c3b0fd46571`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4117fa5740138e3dc627d5e676c7952b8b38f59e516999aaf123bd52413e129`  
		Last Modified: Tue, 08 Apr 2025 16:43:18 GMT  
		Size: 32.2 MB (32153152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6edf3a23aa90880dd4a05fbca27132e93e2ee600deb0da6097a09b4fc1e039`  
		Last Modified: Tue, 08 Apr 2025 16:43:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6def64c40517228066388345a28caba204361ccfd529fb38ab3e9849485b9016`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 4.9 MB (4946180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4763eddd391d93d205c09bad5325b934a482bab633f4c36e82edca6f642c7`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148be0726117f99869134531937d954d6e16e4d12faadb24e7b08776ec69b6fc`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d193908b25c6d8c00d205589ae1597455ecf66f5a31d9e206f744c6635f068`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:815750f57126e20d11e5ebbe12686305bfbd66172177bd4775da969de76c72b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c36bf1da5d0cd32fc006f950011851d4d7cf2e5666f3709b63c021c1ff0c518`

```dockerfile
```

-	Layers:
	-	`sha256:d4fcc6b93101088aadc974ed7b702b7d206339a6ff7d74646c0e3be9347d1a5f`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 2.6 MB (2553230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f616949f0b9071c82ccdf962e8449ee25dff64b86d0cd7440540a0755d8769`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:48507c1240769b3d3d8b171f4d9bec8b18ea2d43dcc18b1f6c913653e40476f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af94c54b989101bef7e07b836c6154f1d1fafa73a583c77d1237f395dca1723`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44e83d5e2f979ccb91fe45546e2434667ec6a256cef574d5bd0d3d34393e72`  
		Last Modified: Tue, 08 Apr 2025 10:44:18 GMT  
		Size: 35.9 MB (35876184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed31c8969ebe3e759650c451926c94d1f34d68db1ce32159605128a26facc3`  
		Last Modified: Tue, 08 Apr 2025 10:44:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd827b16ff9512ff69b60a90d93907c6a1186af054a965889f5e9b6b44bbca`  
		Last Modified: Tue, 08 Apr 2025 15:34:50 GMT  
		Size: 5.1 MB (5142552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c54890505b8b179097accfd0573b08bca8ef30d296e1e9d17931f69d5c8fdb1`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb9ca4ac028b4f609b25121bbe5cf7bddf9fec325518734a1a528942b244fa0`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3027d900232316473a5e0929231605d47ff673353e2e46692086abbb33e882`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2a6da2fc629e8f79da156f33e8ffe631fba39c0d559ee68d304a9cdf99f51285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c13c13bba62a96cf713ed8a4c38ae8b02744bb90b1ff07c2dd872d13e1000f5`

```dockerfile
```

-	Layers:
	-	`sha256:0199231c73566c1a54eb64a07e190b088739301262c8f63c1123b3b90d64c6ca`  
		Last Modified: Tue, 08 Apr 2025 15:34:50 GMT  
		Size: 2.6 MB (2551244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f69badd40ff4bc9b1b67b76b9d528854c65c24c8fcce4846e73a722dac5b999`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:e9438e7cf1b67149471eab1f12ba698bc9944da735fef4ee616ea773d9f6f0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70006819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2543f34bf5349205dc42fa7b793e335862db3ee0c7f7c325bc18a41c29ccc08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9412fa976ce72ab10f7b2c17f54a325cba9a50db87a33cea3460d4bc3863cdd`  
		Last Modified: Mon, 28 Apr 2025 22:01:01 GMT  
		Size: 3.5 MB (3503437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bbcc7945c4987927c2d71ca40f36fd31129a9caf625c8ebb899a07ab8f18b8`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995c80b04acf004d88342453f4bb952afa6bb13309b817a14550cfc003740ae8`  
		Last Modified: Mon, 28 Apr 2025 22:01:02 GMT  
		Size: 32.2 MB (32159534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9024a427c2e8512bc862d20a0e3389f0e36db601cc86606e37028d5517c922e`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeacd56e71b47b24954a7dfd14c069dde0aadef2e719e32db636bdfb9b1d815`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 5.1 MB (5130590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736d3b3d23fe5494026aaa45d7be17bd4e9f1d95ad60cdafc3d18b4ae0211d59`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e05e6d267fef9cc5f6aae4a6b66e5030c860a42d89fab854376d2c051bf3d6a`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b5cad63451cb01d96fcaa424fb72080075cabc398d24d87f091b00d69a494`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:efea967a26e32bc3547fb1b1d71ea0d996f3abea5044f5365d1daef3cef71226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552666e6359550bbc7067d93e08b4fb720d0b960437bde5a70653929b0d041e`

```dockerfile
```

-	Layers:
	-	`sha256:384be78545961fe1fbef01c33e13cd92f0d44f901efb7002a69692292b413483`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 2.5 MB (2548140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477c949ab79630ff23588fc2319f2ac3d59d0a97109b902a3c0d2a5a4130d7aa`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:fea7dff078c11b00ce643a9cb477ce76b2ed2a20a9b2a4f7f3359318bd94fe00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75069595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52df5f7ad56c8586010f91ec8d096db477b13979c59dde638302ff2de4fa7f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae72dbe92456a45d4bf52d40dc3054a905511705bf8835f853e2f5e266d527`  
		Last Modified: Tue, 08 Apr 2025 07:27:56 GMT  
		Size: 33.8 MB (33826920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7addc1391d7bf16a1f4fb683dea9cac116cacf776d5c005e23fd3408c88d9e`  
		Last Modified: Tue, 08 Apr 2025 07:27:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7913a8c90efabaa317e8ff85b680a5be4c78c8830de22c5d6029041843e14c4a`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 5.5 MB (5469127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fbe5848d43f1abf230d27a865b61bf1d4fc365fd37193b4494e1c9cdf8423c`  
		Last Modified: Tue, 08 Apr 2025 15:55:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1985e50320662f17f9e96cb28ea091411330d025fa90bf20f81f526877983a78`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caffa023fccdb66d5cf9456a469b13490613baa792a80739e0f30719213efb53`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f59bb78428da10c33d60955926cfdbdc058265a792b1bcfede2d4057b6b3904f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ba64cc59db63fb6e04013ef0f7e70ed179404cde5a57689d5ce30a61ef0ea1`

```dockerfile
```

-	Layers:
	-	`sha256:ee60a1a83da0f9a15f5b9b25bac96afe949def0355a9f0e56ad1258180e077e6`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 2.6 MB (2555323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c84bd836aba21f83efc6b31fe7d0824b54aa3bf2db5a813f318359f43fe11a7`  
		Last Modified: Tue, 08 Apr 2025 15:55:59 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:dbd2c0246fda6c14f779aa604b66075783f14c0acdac3da8e58ea7fe3896aef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68319466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46d061716f11f077e689bd5105bb05e7beac8f65a1a68473fd182225c131d73`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbfcf42c8f8c0538a68f41e339e27ad611182847b1d51a2079b2b7a55ecfaa0`  
		Last Modified: Tue, 08 Apr 2025 06:18:13 GMT  
		Size: 33.1 MB (33091086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4e8a3c3c5e9cf10583a16d9b24256dc43681f90d1fd230eaa443cd24bc0910`  
		Last Modified: Tue, 08 Apr 2025 06:18:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58eb9ae1ce8b01d83a732f15d3a36392495796f74535a814dbb91fb8b82a66e7`  
		Last Modified: Tue, 08 Apr 2025 10:21:11 GMT  
		Size: 5.2 MB (5178005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709056eaf4d91fc06176f32670c48d198c2e30790f7d63b958977cd9b42cbfd`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1fe8210c93c6ad1ab46c751f9baf3e4d7ddf25acd8049e386caabbac82392b`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e0c38d59fa099c748721fd2f00fa5d2d983a149f23aab1ea14a963ba8e132`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7ec785eeb0b03ab976f6225b4b77083ecaf8311f3eab0a80315084cff5404c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd951d7a28e17b490fff26024d66e22b13d38169b35b67f08ac8f22652c7c61`

```dockerfile
```

-	Layers:
	-	`sha256:00bdf4039450120befc0186248ee5b7bd980f730ac455f48e0f655608feeeb8a`  
		Last Modified: Tue, 08 Apr 2025 10:21:11 GMT  
		Size: 2.6 MB (2550721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d50f0445d3a35bd3a9e1179603c4d403297b24579e8afa18debc06266874d3`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
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
$ docker pull fluentd@sha256:dfc88fced9234384c32f26b839c02466b28adcce85469939864811860d811c72
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
$ docker pull fluentd@sha256:fa90baf528e6d56740f51bc79696e978cf86412c23d0aea4403e02517097232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72832948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609c502b23a3191a195545328dfc3dbf135b95c9f061d4a674fdf6675a313657`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c226faf7bed8a12e29eb84f2e18d6944f226b76e7ab699863e165403d0ba4`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 3.5 MB (3499333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36abc0fca086e6999407f981c69938ee8dd1837f0565dca22b2b918cfe12e91d`  
		Last Modified: Mon, 28 Apr 2025 22:07:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e674df25f2be9bfae7f45a1d65025495004459ad5f1f280f9fe71ea5f2c76a`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 36.0 MB (35956660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ae8c310adf866d680dd353fab5c3ce736d43082f5d142ca8c1602f89199a0`  
		Last Modified: Mon, 28 Apr 2025 22:07:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581af7caed41da96d13726c26c462e2bc0fabcc0bc35ac46e15d737562b7291e`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 5.1 MB (5146917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f8d2466977af4b9c4c45ff9dd55d02017cb6b621c8db173fa9d216c6cfa3e1`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32258058af23692d3b7f7dbc5a989efc2d1b21272521a86153f0649b9969b9`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f589733ba1b90219aa0bf449a5231c320417ad2d06d42e1d2c2772b0bfba4ab`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8a29d4677c2310397b12f72ee817075f5a3cfde9d637c8ec61285cc4e943a0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67316f4e5bf6c571b8982f3695a44242eb12456d4336c8f7c43d860d55ec50f8`

```dockerfile
```

-	Layers:
	-	`sha256:4b029a1598883523f00f17ac2472bfedc21c4ef464e2a54e0b49997b9923d0ab`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 2.6 MB (2551004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f9aed701a4bc111e7bfc37e990cbd9e1288b9274a5820091865adcc88e4ede`  
		Last Modified: Mon, 28 Apr 2025 22:24:19 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:69df2de33d5304c10291d266d13489f9844646e98055b662f0466123dbf3af52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66215700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07ed22733355faebc4d4bc37dc3b7b6ae9f3c21f5f7cab5833ae5c2559a466`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ace276ccf28d2fc068800ff40da67bacf13b8d590cd438ae9b974a85399b7`  
		Last Modified: Tue, 08 Apr 2025 08:01:12 GMT  
		Size: 32.3 MB (32318421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a44c44c2bc2a89734853f98cc590486713b86056d616d936e75ae922029e2e`  
		Last Modified: Tue, 08 Apr 2025 08:01:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8f97336d7e59c5adf9af8a95c9477d24ec8257fbc6274e29cc07a199e3e51b`  
		Last Modified: Tue, 08 Apr 2025 10:27:55 GMT  
		Size: 5.1 MB (5063606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc5633a4d4cae1ece486b96a14221daf842f656f7e72e9630a80d51b18978cd`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab2c1cb2918a2b5fbd3891604a4f57642e989f94b35ba313a43c0a0a0e77531`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f237b4515133b03d62c56e2ccdd843ed2b9199027139b371695ca4f29e807`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:706e2ca512efbd398d5133250a0e51b6468acc65b082212425f417690ff3e414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfe1a3b0708c9338e18bfdc7a5d06b9c93525c3d70f1ad0de28bcb0220c17ee`

```dockerfile
```

-	Layers:
	-	`sha256:622f4a3a551ef6c6ab8876f63a89b82f8bd9d3fd7a887c86009190f189823565`  
		Last Modified: Tue, 08 Apr 2025 10:27:55 GMT  
		Size: 2.6 MB (2554491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a476b22b3d54358eaf3e6e9480171aab49942f40bbe1a78e9fcb9b83c50264f0`  
		Last Modified: Tue, 08 Apr 2025 10:27:54 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ed14294e1f464a07b4033d5f3c36a2cbfca381806a5b01548c614dd28411b372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63947370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0dfd1769b23c437fb3e787721ae113b0c9f8e20a711e80b597c3b0fd46571`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4117fa5740138e3dc627d5e676c7952b8b38f59e516999aaf123bd52413e129`  
		Last Modified: Tue, 08 Apr 2025 16:43:18 GMT  
		Size: 32.2 MB (32153152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6edf3a23aa90880dd4a05fbca27132e93e2ee600deb0da6097a09b4fc1e039`  
		Last Modified: Tue, 08 Apr 2025 16:43:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6def64c40517228066388345a28caba204361ccfd529fb38ab3e9849485b9016`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 4.9 MB (4946180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4763eddd391d93d205c09bad5325b934a482bab633f4c36e82edca6f642c7`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148be0726117f99869134531937d954d6e16e4d12faadb24e7b08776ec69b6fc`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d193908b25c6d8c00d205589ae1597455ecf66f5a31d9e206f744c6635f068`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:815750f57126e20d11e5ebbe12686305bfbd66172177bd4775da969de76c72b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c36bf1da5d0cd32fc006f950011851d4d7cf2e5666f3709b63c021c1ff0c518`

```dockerfile
```

-	Layers:
	-	`sha256:d4fcc6b93101088aadc974ed7b702b7d206339a6ff7d74646c0e3be9347d1a5f`  
		Last Modified: Tue, 08 Apr 2025 21:19:49 GMT  
		Size: 2.6 MB (2553230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f616949f0b9071c82ccdf962e8449ee25dff64b86d0cd7440540a0755d8769`  
		Last Modified: Tue, 08 Apr 2025 21:19:48 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:48507c1240769b3d3d8b171f4d9bec8b18ea2d43dcc18b1f6c913653e40476f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af94c54b989101bef7e07b836c6154f1d1fafa73a583c77d1237f395dca1723`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44e83d5e2f979ccb91fe45546e2434667ec6a256cef574d5bd0d3d34393e72`  
		Last Modified: Tue, 08 Apr 2025 10:44:18 GMT  
		Size: 35.9 MB (35876184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed31c8969ebe3e759650c451926c94d1f34d68db1ce32159605128a26facc3`  
		Last Modified: Tue, 08 Apr 2025 10:44:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd827b16ff9512ff69b60a90d93907c6a1186af054a965889f5e9b6b44bbca`  
		Last Modified: Tue, 08 Apr 2025 15:34:50 GMT  
		Size: 5.1 MB (5142552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c54890505b8b179097accfd0573b08bca8ef30d296e1e9d17931f69d5c8fdb1`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb9ca4ac028b4f609b25121bbe5cf7bddf9fec325518734a1a528942b244fa0`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3027d900232316473a5e0929231605d47ff673353e2e46692086abbb33e882`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2a6da2fc629e8f79da156f33e8ffe631fba39c0d559ee68d304a9cdf99f51285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c13c13bba62a96cf713ed8a4c38ae8b02744bb90b1ff07c2dd872d13e1000f5`

```dockerfile
```

-	Layers:
	-	`sha256:0199231c73566c1a54eb64a07e190b088739301262c8f63c1123b3b90d64c6ca`  
		Last Modified: Tue, 08 Apr 2025 15:34:50 GMT  
		Size: 2.6 MB (2551244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f69badd40ff4bc9b1b67b76b9d528854c65c24c8fcce4846e73a722dac5b999`  
		Last Modified: Tue, 08 Apr 2025 15:34:49 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:e9438e7cf1b67149471eab1f12ba698bc9944da735fef4ee616ea773d9f6f0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70006819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2543f34bf5349205dc42fa7b793e335862db3ee0c7f7c325bc18a41c29ccc08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9412fa976ce72ab10f7b2c17f54a325cba9a50db87a33cea3460d4bc3863cdd`  
		Last Modified: Mon, 28 Apr 2025 22:01:01 GMT  
		Size: 3.5 MB (3503437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bbcc7945c4987927c2d71ca40f36fd31129a9caf625c8ebb899a07ab8f18b8`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995c80b04acf004d88342453f4bb952afa6bb13309b817a14550cfc003740ae8`  
		Last Modified: Mon, 28 Apr 2025 22:01:02 GMT  
		Size: 32.2 MB (32159534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9024a427c2e8512bc862d20a0e3389f0e36db601cc86606e37028d5517c922e`  
		Last Modified: Mon, 28 Apr 2025 22:01:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeacd56e71b47b24954a7dfd14c069dde0aadef2e719e32db636bdfb9b1d815`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 5.1 MB (5130590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736d3b3d23fe5494026aaa45d7be17bd4e9f1d95ad60cdafc3d18b4ae0211d59`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e05e6d267fef9cc5f6aae4a6b66e5030c860a42d89fab854376d2c051bf3d6a`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b5cad63451cb01d96fcaa424fb72080075cabc398d24d87f091b00d69a494`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:efea967a26e32bc3547fb1b1d71ea0d996f3abea5044f5365d1daef3cef71226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552666e6359550bbc7067d93e08b4fb720d0b960437bde5a70653929b0d041e`

```dockerfile
```

-	Layers:
	-	`sha256:384be78545961fe1fbef01c33e13cd92f0d44f901efb7002a69692292b413483`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 2.5 MB (2548140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477c949ab79630ff23588fc2319f2ac3d59d0a97109b902a3c0d2a5a4130d7aa`  
		Last Modified: Mon, 28 Apr 2025 22:25:24 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:fea7dff078c11b00ce643a9cb477ce76b2ed2a20a9b2a4f7f3359318bd94fe00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75069595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52df5f7ad56c8586010f91ec8d096db477b13979c59dde638302ff2de4fa7f6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae72dbe92456a45d4bf52d40dc3054a905511705bf8835f853e2f5e266d527`  
		Last Modified: Tue, 08 Apr 2025 07:27:56 GMT  
		Size: 33.8 MB (33826920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7addc1391d7bf16a1f4fb683dea9cac116cacf776d5c005e23fd3408c88d9e`  
		Last Modified: Tue, 08 Apr 2025 07:27:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7913a8c90efabaa317e8ff85b680a5be4c78c8830de22c5d6029041843e14c4a`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 5.5 MB (5469127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fbe5848d43f1abf230d27a865b61bf1d4fc365fd37193b4494e1c9cdf8423c`  
		Last Modified: Tue, 08 Apr 2025 15:55:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1985e50320662f17f9e96cb28ea091411330d025fa90bf20f81f526877983a78`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caffa023fccdb66d5cf9456a469b13490613baa792a80739e0f30719213efb53`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f59bb78428da10c33d60955926cfdbdc058265a792b1bcfede2d4057b6b3904f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ba64cc59db63fb6e04013ef0f7e70ed179404cde5a57689d5ce30a61ef0ea1`

```dockerfile
```

-	Layers:
	-	`sha256:ee60a1a83da0f9a15f5b9b25bac96afe949def0355a9f0e56ad1258180e077e6`  
		Last Modified: Tue, 08 Apr 2025 15:56:00 GMT  
		Size: 2.6 MB (2555323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c84bd836aba21f83efc6b31fe7d0824b54aa3bf2db5a813f318359f43fe11a7`  
		Last Modified: Tue, 08 Apr 2025 15:55:59 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:dbd2c0246fda6c14f779aa604b66075783f14c0acdac3da8e58ea7fe3896aef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68319466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46d061716f11f077e689bd5105bb05e7beac8f65a1a68473fd182225c131d73`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbfcf42c8f8c0538a68f41e339e27ad611182847b1d51a2079b2b7a55ecfaa0`  
		Last Modified: Tue, 08 Apr 2025 06:18:13 GMT  
		Size: 33.1 MB (33091086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4e8a3c3c5e9cf10583a16d9b24256dc43681f90d1fd230eaa443cd24bc0910`  
		Last Modified: Tue, 08 Apr 2025 06:18:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58eb9ae1ce8b01d83a732f15d3a36392495796f74535a814dbb91fb8b82a66e7`  
		Last Modified: Tue, 08 Apr 2025 10:21:11 GMT  
		Size: 5.2 MB (5178005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709056eaf4d91fc06176f32670c48d198c2e30790f7d63b958977cd9b42cbfd`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1fe8210c93c6ad1ab46c751f9baf3e4d7ddf25acd8049e386caabbac82392b`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e0c38d59fa099c748721fd2f00fa5d2d983a149f23aab1ea14a963ba8e132`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7ec785eeb0b03ab976f6225b4b77083ecaf8311f3eab0a80315084cff5404c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd951d7a28e17b490fff26024d66e22b13d38169b35b67f08ac8f22652c7c61`

```dockerfile
```

-	Layers:
	-	`sha256:00bdf4039450120befc0186248ee5b7bd980f730ac455f48e0f655608feeeb8a`  
		Last Modified: Tue, 08 Apr 2025 10:21:11 GMT  
		Size: 2.6 MB (2550721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d50f0445d3a35bd3a9e1179603c4d403297b24579e8afa18debc06266874d3`  
		Last Modified: Tue, 08 Apr 2025 10:21:10 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json
