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
$ docker pull fluentd@sha256:d8753842ee519c00e7abd60b40ff3fac03cc6333a0f33ff9bdadaacd12285810
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
$ docker pull fluentd@sha256:7995b31ea5a4916c1556a5e4d3c4a7597e63b50456e65e3214780ebcd5ea27cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81908123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55814ac550d5ed90410fa160d03b72c60a3780525ab796275a1f176924e7eb8f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77444f72ec27da57e1514fe30b3bd9df19b89e45af3964d6caa39afc741efc18`  
		Last Modified: Tue, 25 Feb 2025 02:34:58 GMT  
		Size: 3.5 MB (3499332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b3152e3e2096181d3fc2de2c8fdd61bf366df9842791246d1dcf30341a45e`  
		Last Modified: Tue, 25 Feb 2025 02:34:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e19521013c5e837d619341aa7b91b6f3f0252dfcb903a97077c9df22bd7ae1`  
		Last Modified: Tue, 25 Feb 2025 02:34:58 GMT  
		Size: 35.9 MB (35949499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5f1a629292b824d28be6db12556e1d4084fa0ddf50faed57483ac8bf7f203`  
		Last Modified: Tue, 25 Feb 2025 02:34:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e72cd4f59b66cb132186f4c2030418da7d95c40502c63d22470666eb8025b7`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 14.2 MB (14237597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7287256f23e3c6f07530af8f7c3d9e3b1d967911f382a5e91ddaa51692a10266`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f016fe4d8b94149b944cfcb8c6b9bc3832f0f1d51ed78bada86958316f93b`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e65e080f36e77becfbb099c3cf6dea72bfc807d47f605a9c893660cbc9f55b4`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4d141b737c69d29a106134219cfd69da8afd7b72b56930fb4fe9a1f37c514908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc54c72a06b91cf10009e90a8466ececd7b78b505869f9e0227cdfebf99e63`

```dockerfile
```

-	Layers:
	-	`sha256:d25041dcb5ecf93ebb0277344b1d4e9051a6309c0038c215032cdeb8ad5bb8aa`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 2.5 MB (2545794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d8d827794feb5681e33e164526a71ee612156a78eaad5fe3b3a7ea9e11f14b`  
		Last Modified: Tue, 25 Feb 2025 03:23:23 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:bd41207ee1b9d0fda9a20d26661cd5d16626f6e6068633cf3658aa8636e5b3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75339343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e487b6201997fc7a2b3c193845b59b8c4dacc76924d47d8fbc7b3e54c07b7748`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb796b4078c24eacc4e96fa6314434576ef2cb38939712321f810114f707a3`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 3.1 MB (3073429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc6bbc44c189ac8a47708a7e65a210775688d0fd3df160a14b423364ed9ebc9`  
		Last Modified: Tue, 25 Feb 2025 07:53:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a7610f814d2917ce66eac3a6e0c706a7221d38ecb3b52e77da4551f21ed75`  
		Last Modified: Tue, 25 Feb 2025 07:59:59 GMT  
		Size: 32.3 MB (32310017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeddc5d5277515fe4fde129b1017e9a5be6e85ef444ce449049c15c43281aeb`  
		Last Modified: Tue, 25 Feb 2025 07:59:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83de581b39384b84d1c68908ae84e18bffbbcc38812f4f4a3fa666709293b356`  
		Last Modified: Tue, 25 Feb 2025 09:57:12 GMT  
		Size: 14.2 MB (14212873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f193ea7cf7138c8a65157bd1fceb54c1ec6fc8902404962ffb6a05a9dadc17`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d009c8b64b7a4c2f2186f57921bdefa08f702a61a4d670e23fcbca9875a631`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb88a37b904a22ec81937d7703f2e42eff50ed6c82960508ca37d89958e996ee`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6ccf894769aa8822e746383fe25dfe0863a7407a2cbc8b081f4f79adc8c9ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecca1a823d61db67f8a40d924af1309a8012d4a8aca93f1687c26bc949079c7`

```dockerfile
```

-	Layers:
	-	`sha256:1e8dad05b912eca2a512c7a0170bf5ad0c09fb5063a69307306bb0528a8433d8`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 2.5 MB (2549281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:063736f66a7c1f4491ad9b12dd985bbfa29157039e1107c13399a6dbca172cb5`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:bad8829d614f4714e002e0192d9975bd250d0c2a116ac7051eb9bd9824071622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73117335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a79b71b94140393907908a2b9f4deced7b89aa3dee626543b185d1e8fc85b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa00c010a50d2538d1c9dce260e0670c1f23132407fb79f24a3ea3a43af6ba`  
		Last Modified: Tue, 25 Feb 2025 12:56:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478f73f8ce2c65c709ee2e6a8916af059a187c52f1e2dd098045f746336173b`  
		Last Modified: Tue, 25 Feb 2025 13:14:26 GMT  
		Size: 32.1 MB (32145430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9c41f8aa4115e4ab80b8ab849109e1bd78637bec8e4f6d7eeb67b2b450c6e`  
		Last Modified: Tue, 25 Feb 2025 13:14:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc5f1e4b19a778d1066b7042fa6179501a0496cbfc805a6a11190b1f6b00b7c`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 14.1 MB (14141981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60639c500f6b69e75b0d67515d68d2b640be63fdaf50b6a9664f8c58e85c6b65`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fbc92c6dc9b13439a1b8c5d2d12d87db680909ff062092060c73242a90dbd4`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253b3967405ecc8b986f3c6bfd923f44b7b88bae99c0c2751c1a6542a32ddeb`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1603e958f9afa78a7646c88e007d1de925c9e9540c1b7034ad00ae59ce17a5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10953e479e6aa030d4d4f07d533d6602fd1f62bd6ac97b0d6d73acaf076ad4e3`

```dockerfile
```

-	Layers:
	-	`sha256:3e3eaf5ca7463ab0180002fa311a775c6ddbe843cd7d295d48c5281ec87ca0d9`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 2.5 MB (2548020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6f15cfa998520b7f5a0565b88f7b8351a7034f59d29c8820c7623b243262e`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:40a27eb44155a8ed27f1e2087ac7a63a2c3891d9cc05f5b606f7ee3d6bd2b189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81483316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f900196543813e2dd0dfc81c5ca7665d195b831e6eb42590b9b065961c33d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d23f62980d9b0556214c013074faf49617432dc72038575e16558436e840c`  
		Last Modified: Tue, 25 Feb 2025 10:09:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d534dc9ec0a37b348c66b43ac1785942dbd5088ccf3f87961752338b5a2b6b`  
		Last Modified: Tue, 25 Feb 2025 10:20:21 GMT  
		Size: 35.9 MB (35869687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f948c724172e15609ec22db3ee957ec8e568073d1476571a3fb601c7f60a805`  
		Last Modified: Tue, 25 Feb 2025 10:20:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81fb1df5e946c0981161ab8875e3ce9f5a621e7c19011926970c0a63706ad13`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 14.2 MB (14239923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099db12bda0ba2d54d37a566b4269b69b5ef16b6cd21a0454141be61f85e65f5`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05fd91425bae1f791f306ee3ba37c1f82d881619866df80e58fc23384a3137`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727a67839d6008ebaa50c52bede558ae61595c5693742665bb0cfc7ae16e5f9`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:56bafce208311f15a042dbba53e679dd37fa34be9d0eec297543dae1c3cd39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16af2ee47ee7a7688f125e2b1fd27b0174fe92bdeaad4b29e475f80fd74df95`

```dockerfile
```

-	Layers:
	-	`sha256:8138624f83ab1dc1bd0f3f3e8acb83f76ffeab47fa164790d93ddc3883d53935`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 2.5 MB (2546034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e5090246b1629a2b7bf9367883a96678ffd8e818f6b884fd9f584361e84ec2`  
		Last Modified: Tue, 25 Feb 2025 14:55:25 GMT  
		Size: 21.2 KB (21198 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:a87f85daca35d5427728e37441886939961c6fe30a9ca50028d066c4c7903430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78873952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88e2204e672eb0ec4bbd503d9c1ef39aed6838d58a08506ea8d90db6dbac738`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3292a3220ab080841dc4b33e824dd20af65f71491c3ffde5c26a0c234e4043a`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 3.5 MB (3503439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca20b53c4a7810c52d4ad4ec45881533889dfba975e6fc040cc82b02f74e28f`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd7acbc020d76cf20ffe21d9b8d9fb01defd4285a758df9e27ed24a517f17a2`  
		Last Modified: Tue, 25 Feb 2025 03:24:11 GMT  
		Size: 32.1 MB (32145894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74114f3a304ee1aade20e246e99767eccb6e2420ff638a5d75d73d99cba6ae5`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38495c2ccee799c782eeb5709315751f946a3610f54c9d68becbfa6cbebb8d`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 14.0 MB (14027634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb5b3901813fdba5629eebe56348096c29c9acdd10aa4d70dc39ecd8e9f18a`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb0c024ca9c0767099820b0121764ba5bdabcfa8a595259518e8a63ca81606`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ba43ffc8721972da7e619e86b057ca9ea2d1f68da19908354418149615ff6`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:83e409c903ccfe4746ee84e94cdd0cfb9a5ca8f337d0e7ae6dda412d984392fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6beb2b5756a5fb1a295e43fb6c4b9d8607c0f1cbd35de55db56d6a9697ae7`

```dockerfile
```

-	Layers:
	-	`sha256:86c09bde3ad2586c53dc0ffc25b747ff8eef242fb8fc57c01e279e5d05517a72`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 2.5 MB (2542930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d6e5f5bb167b9543ec34e9bb1a3d91fd2319b96c7c50bfa82bd4a6d2219573`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:950042de2ec9c7234efa3c4ad5c0484f8d57602c1d8819660ee020b7ae7fdbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84206587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7725401d38d858c84aa19d7f73942d2bcf12f85d3b364c21a5de27dd5228ad5e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a43af6979a93ac649908165249f4bb955edcab70ac04e8f3ac9d6c7ffeebec`  
		Last Modified: Tue, 25 Feb 2025 07:22:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592351a0c4ef43e36a2ff54afd0a867ebd5eeb7bd3dba102040e0c6c87bb6ef`  
		Last Modified: Tue, 25 Feb 2025 07:30:55 GMT  
		Size: 33.8 MB (33818197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70279d426fc5e6924753fb6f710cf7db1e2ca9a757eb62263c5e9a23f4cc98b`  
		Last Modified: Tue, 25 Feb 2025 07:30:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7efe9997822b790d0b5c4f9783248d922b203deb6ebd5701deed2a49c41eaa7`  
		Last Modified: Tue, 25 Feb 2025 12:05:07 GMT  
		Size: 14.6 MB (14630697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4571f25bb8a490960234ab9f34b37335a3fdc05ab93169173b10490ead6968f1`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6a1c2ce32c9555bbecb880dd29902c6a5468e33d6a0ff4300ee1c89c64d996`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761e8c5a65993e38217ba6d8cdcad32753d962356aea95608f390e8c5f79db56`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4008c17150aa888259778cc75dfd1347c83bbdaf59cedd21cf5f716e37849ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d792658448da3078469c726aba2f48deb53614208902187427a8815d4e5fd03e`

```dockerfile
```

-	Layers:
	-	`sha256:446c242375b98c94e35713077c4f688fc28ba2b6cacca34e3113269c46b10190`  
		Last Modified: Tue, 25 Feb 2025 12:05:07 GMT  
		Size: 2.6 MB (2550113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26224d5c0780928504d08891a796472831ba220adbd631d1b25dad571b072d84`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:20246fe209d6fa9fc83367765969ee94d461954727f2a2e7ddb263467c18e070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77486925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115943e7243e98aba8a25e81136da317c6eef549961cde26f8352a34f10159aa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f059893784660d506287970229898dece31ad607ee75f8af7896ae23e7b42`  
		Last Modified: Tue, 25 Feb 2025 06:38:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b1e40e23a16b0bf7ec3f668f54c4a27b878db312799318b319d6a926e10411`  
		Last Modified: Tue, 25 Feb 2025 06:44:43 GMT  
		Size: 33.1 MB (33084236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3191e6b1f30a857074a7012bb632e9425d85c506e46b6febae7a336af8bd3893`  
		Last Modified: Tue, 25 Feb 2025 06:44:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621800c1c67d37c56f882b17105f9519696366d8642aa874cb038dfaa716a47`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 14.4 MB (14372059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea007bb35f1f18209d89b0fbff37c255fb8e84c51f3610dfb2c03c552ce72dd`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34da2e278963987f5507570bf9676b1a2ed7786d7b0a532071454a42a0e31d6d`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea77e86cda02cd1aed6a5ca7c58bff7932b50f61f1cd262e9a32d7955ae16d`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:16908b27ab7042cce238efeae0e6a1ed95c6fc936640765311dd944e43ec6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ef43b9dbc212933c67d5e33331c25992ae609d55cd89af6334353742b6afc`

```dockerfile
```

-	Layers:
	-	`sha256:5457cdd1bfe13e1ddc27ee213adaf5f0ea95d8626936683d4ea9bff38a82d7fe`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 2.5 MB (2545511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f923ba5ff54edb61dfe9f55b9a0ef2cf70f939623a45c32d896a1f8d92d447a3`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 21.1 KB (21103 bytes)  
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
$ docker pull fluentd@sha256:cb6f6768aa27bcfd976b33e48833eeb9a6bb25ee5d4e6d609f49af2e11fc390e
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
$ docker pull fluentd@sha256:91b0833c0d36c274bd63d8780ca01f9edbbf46738841dbcc9766cef280eb1dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81904730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc8e9fda80d4caded68bf629b82ba0824267fa99f32e8eee42cff825fa6cd94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8a126e16f182f2190d852c32868a653bb744267c88f79f72bcd9a6ad131e5`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 3.5 MB (3499331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2e961874d440895f78d64ad8cfa72f90cbaec413e84e76ad1c5f24b7f907a2`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f7c0de6fd8ae30d05e3c10de0a2a60879ab8c160e72375ed4ebf6c8e99ed0`  
		Last Modified: Mon, 17 Mar 2025 23:19:03 GMT  
		Size: 36.0 MB (35950065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320203a9f6e524a3462d074fe0a9cfbadd1faedfae58be7306f070236ff42ac`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19db9cf86b7ad569403a1746d2c0946f28a12a94fd0f05854f0acbc6e080fd47`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 14.2 MB (14248075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b2f5e4ca068dffb60e84a356b4b46d9be2faf8bf219274dc7469c069c744bf`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8e6403dfec6b944b4ec4cc2cca5406f299cf5600f1e3c2cfe5fc516a8ea69c`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e482d80085dc76079ff586c1da8e28dc551b4c68e7f3044a8f01c23473a5c45`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:921533c84045133e0b91930e0d6884bec9e2b04c09b2188a6627bc8c88fc0c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef5ccb3c25b00f28e832c0e18846a9846c9c2ad032ae5be4a6e9dc1e35492a2`

```dockerfile
```

-	Layers:
	-	`sha256:0320e583812ffa61e075a0509b5395169c80fa81e161e3f3a45fdf2114865695`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 2.5 MB (2545838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7355b09607256b18d614f00de8c3d5f2e48bcb29a4546e20818eadef6fb79ea4`  
		Last Modified: Tue, 18 Mar 2025 00:27:30 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:bd41207ee1b9d0fda9a20d26661cd5d16626f6e6068633cf3658aa8636e5b3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75339343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e487b6201997fc7a2b3c193845b59b8c4dacc76924d47d8fbc7b3e54c07b7748`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb796b4078c24eacc4e96fa6314434576ef2cb38939712321f810114f707a3`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 3.1 MB (3073429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc6bbc44c189ac8a47708a7e65a210775688d0fd3df160a14b423364ed9ebc9`  
		Last Modified: Tue, 25 Feb 2025 07:53:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a7610f814d2917ce66eac3a6e0c706a7221d38ecb3b52e77da4551f21ed75`  
		Last Modified: Tue, 25 Feb 2025 07:59:59 GMT  
		Size: 32.3 MB (32310017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeddc5d5277515fe4fde129b1017e9a5be6e85ef444ce449049c15c43281aeb`  
		Last Modified: Tue, 25 Feb 2025 07:59:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83de581b39384b84d1c68908ae84e18bffbbcc38812f4f4a3fa666709293b356`  
		Last Modified: Tue, 25 Feb 2025 09:57:12 GMT  
		Size: 14.2 MB (14212873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f193ea7cf7138c8a65157bd1fceb54c1ec6fc8902404962ffb6a05a9dadc17`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d009c8b64b7a4c2f2186f57921bdefa08f702a61a4d670e23fcbca9875a631`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb88a37b904a22ec81937d7703f2e42eff50ed6c82960508ca37d89958e996ee`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6ccf894769aa8822e746383fe25dfe0863a7407a2cbc8b081f4f79adc8c9ad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecca1a823d61db67f8a40d924af1309a8012d4a8aca93f1687c26bc949079c7`

```dockerfile
```

-	Layers:
	-	`sha256:1e8dad05b912eca2a512c7a0170bf5ad0c09fb5063a69307306bb0528a8433d8`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 2.5 MB (2549281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:063736f66a7c1f4491ad9b12dd985bbfa29157039e1107c13399a6dbca172cb5`  
		Last Modified: Tue, 25 Feb 2025 09:57:11 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:bad8829d614f4714e002e0192d9975bd250d0c2a116ac7051eb9bd9824071622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73117335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a79b71b94140393907908a2b9f4deced7b89aa3dee626543b185d1e8fc85b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa00c010a50d2538d1c9dce260e0670c1f23132407fb79f24a3ea3a43af6ba`  
		Last Modified: Tue, 25 Feb 2025 12:56:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478f73f8ce2c65c709ee2e6a8916af059a187c52f1e2dd098045f746336173b`  
		Last Modified: Tue, 25 Feb 2025 13:14:26 GMT  
		Size: 32.1 MB (32145430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9c41f8aa4115e4ab80b8ab849109e1bd78637bec8e4f6d7eeb67b2b450c6e`  
		Last Modified: Tue, 25 Feb 2025 13:14:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc5f1e4b19a778d1066b7042fa6179501a0496cbfc805a6a11190b1f6b00b7c`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 14.1 MB (14141981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60639c500f6b69e75b0d67515d68d2b640be63fdaf50b6a9664f8c58e85c6b65`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fbc92c6dc9b13439a1b8c5d2d12d87db680909ff062092060c73242a90dbd4`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253b3967405ecc8b986f3c6bfd923f44b7b88bae99c0c2751c1a6542a32ddeb`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1603e958f9afa78a7646c88e007d1de925c9e9540c1b7034ad00ae59ce17a5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10953e479e6aa030d4d4f07d533d6602fd1f62bd6ac97b0d6d73acaf076ad4e3`

```dockerfile
```

-	Layers:
	-	`sha256:3e3eaf5ca7463ab0180002fa311a775c6ddbe843cd7d295d48c5281ec87ca0d9`  
		Last Modified: Tue, 25 Feb 2025 17:36:03 GMT  
		Size: 2.5 MB (2548020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6f15cfa998520b7f5a0565b88f7b8351a7034f59d29c8820c7623b243262e`  
		Last Modified: Tue, 25 Feb 2025 17:36:02 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:40a27eb44155a8ed27f1e2087ac7a63a2c3891d9cc05f5b606f7ee3d6bd2b189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81483316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f900196543813e2dd0dfc81c5ca7665d195b831e6eb42590b9b065961c33d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d23f62980d9b0556214c013074faf49617432dc72038575e16558436e840c`  
		Last Modified: Tue, 25 Feb 2025 10:09:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d534dc9ec0a37b348c66b43ac1785942dbd5088ccf3f87961752338b5a2b6b`  
		Last Modified: Tue, 25 Feb 2025 10:20:21 GMT  
		Size: 35.9 MB (35869687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f948c724172e15609ec22db3ee957ec8e568073d1476571a3fb601c7f60a805`  
		Last Modified: Tue, 25 Feb 2025 10:20:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81fb1df5e946c0981161ab8875e3ce9f5a621e7c19011926970c0a63706ad13`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 14.2 MB (14239923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099db12bda0ba2d54d37a566b4269b69b5ef16b6cd21a0454141be61f85e65f5`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05fd91425bae1f791f306ee3ba37c1f82d881619866df80e58fc23384a3137`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727a67839d6008ebaa50c52bede558ae61595c5693742665bb0cfc7ae16e5f9`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:56bafce208311f15a042dbba53e679dd37fa34be9d0eec297543dae1c3cd39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2567232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16af2ee47ee7a7688f125e2b1fd27b0174fe92bdeaad4b29e475f80fd74df95`

```dockerfile
```

-	Layers:
	-	`sha256:8138624f83ab1dc1bd0f3f3e8acb83f76ffeab47fa164790d93ddc3883d53935`  
		Last Modified: Tue, 25 Feb 2025 14:55:26 GMT  
		Size: 2.5 MB (2546034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e5090246b1629a2b7bf9367883a96678ffd8e818f6b884fd9f584361e84ec2`  
		Last Modified: Tue, 25 Feb 2025 14:55:25 GMT  
		Size: 21.2 KB (21198 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:a87f85daca35d5427728e37441886939961c6fe30a9ca50028d066c4c7903430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78873952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88e2204e672eb0ec4bbd503d9c1ef39aed6838d58a08506ea8d90db6dbac738`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3292a3220ab080841dc4b33e824dd20af65f71491c3ffde5c26a0c234e4043a`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 3.5 MB (3503439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca20b53c4a7810c52d4ad4ec45881533889dfba975e6fc040cc82b02f74e28f`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd7acbc020d76cf20ffe21d9b8d9fb01defd4285a758df9e27ed24a517f17a2`  
		Last Modified: Tue, 25 Feb 2025 03:24:11 GMT  
		Size: 32.1 MB (32145894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74114f3a304ee1aade20e246e99767eccb6e2420ff638a5d75d73d99cba6ae5`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38495c2ccee799c782eeb5709315751f946a3610f54c9d68becbfa6cbebb8d`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 14.0 MB (14027634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb5b3901813fdba5629eebe56348096c29c9acdd10aa4d70dc39ecd8e9f18a`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb0c024ca9c0767099820b0121764ba5bdabcfa8a595259518e8a63ca81606`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ba43ffc8721972da7e619e86b057ca9ea2d1f68da19908354418149615ff6`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:83e409c903ccfe4746ee84e94cdd0cfb9a5ca8f337d0e7ae6dda412d984392fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6beb2b5756a5fb1a295e43fb6c4b9d8607c0f1cbd35de55db56d6a9697ae7`

```dockerfile
```

-	Layers:
	-	`sha256:86c09bde3ad2586c53dc0ffc25b747ff8eef242fb8fc57c01e279e5d05517a72`  
		Last Modified: Tue, 25 Feb 2025 05:14:30 GMT  
		Size: 2.5 MB (2542930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d6e5f5bb167b9543ec34e9bb1a3d91fd2319b96c7c50bfa82bd4a6d2219573`  
		Last Modified: Tue, 25 Feb 2025 05:14:29 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:950042de2ec9c7234efa3c4ad5c0484f8d57602c1d8819660ee020b7ae7fdbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84206587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7725401d38d858c84aa19d7f73942d2bcf12f85d3b364c21a5de27dd5228ad5e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a43af6979a93ac649908165249f4bb955edcab70ac04e8f3ac9d6c7ffeebec`  
		Last Modified: Tue, 25 Feb 2025 07:22:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592351a0c4ef43e36a2ff54afd0a867ebd5eeb7bd3dba102040e0c6c87bb6ef`  
		Last Modified: Tue, 25 Feb 2025 07:30:55 GMT  
		Size: 33.8 MB (33818197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70279d426fc5e6924753fb6f710cf7db1e2ca9a757eb62263c5e9a23f4cc98b`  
		Last Modified: Tue, 25 Feb 2025 07:30:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7efe9997822b790d0b5c4f9783248d922b203deb6ebd5701deed2a49c41eaa7`  
		Last Modified: Tue, 25 Feb 2025 12:05:07 GMT  
		Size: 14.6 MB (14630697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4571f25bb8a490960234ab9f34b37335a3fdc05ab93169173b10490ead6968f1`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6a1c2ce32c9555bbecb880dd29902c6a5468e33d6a0ff4300ee1c89c64d996`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761e8c5a65993e38217ba6d8cdcad32753d962356aea95608f390e8c5f79db56`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4008c17150aa888259778cc75dfd1347c83bbdaf59cedd21cf5f716e37849ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d792658448da3078469c726aba2f48deb53614208902187427a8815d4e5fd03e`

```dockerfile
```

-	Layers:
	-	`sha256:446c242375b98c94e35713077c4f688fc28ba2b6cacca34e3113269c46b10190`  
		Last Modified: Tue, 25 Feb 2025 12:05:07 GMT  
		Size: 2.6 MB (2550113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26224d5c0780928504d08891a796472831ba220adbd631d1b25dad571b072d84`  
		Last Modified: Tue, 25 Feb 2025 12:05:06 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:20246fe209d6fa9fc83367765969ee94d461954727f2a2e7ddb263467c18e070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77486925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115943e7243e98aba8a25e81136da317c6eef549961cde26f8352a34f10159aa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 31 Jan 2025 07:58:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 07:58:59 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 07:58:59 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f059893784660d506287970229898dece31ad607ee75f8af7896ae23e7b42`  
		Last Modified: Tue, 25 Feb 2025 06:38:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b1e40e23a16b0bf7ec3f668f54c4a27b878db312799318b319d6a926e10411`  
		Last Modified: Tue, 25 Feb 2025 06:44:43 GMT  
		Size: 33.1 MB (33084236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3191e6b1f30a857074a7012bb632e9425d85c506e46b6febae7a336af8bd3893`  
		Last Modified: Tue, 25 Feb 2025 06:44:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621800c1c67d37c56f882b17105f9519696366d8642aa874cb038dfaa716a47`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 14.4 MB (14372059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea007bb35f1f18209d89b0fbff37c255fb8e84c51f3610dfb2c03c552ce72dd`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34da2e278963987f5507570bf9676b1a2ed7786d7b0a532071454a42a0e31d6d`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea77e86cda02cd1aed6a5ca7c58bff7932b50f61f1cd262e9a32d7955ae16d`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:16908b27ab7042cce238efeae0e6a1ed95c6fc936640765311dd944e43ec6ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ef43b9dbc212933c67d5e33331c25992ae609d55cd89af6334353742b6afc`

```dockerfile
```

-	Layers:
	-	`sha256:5457cdd1bfe13e1ddc27ee213adaf5f0ea95d8626936683d4ea9bff38a82d7fe`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 2.5 MB (2545511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f923ba5ff54edb61dfe9f55b9a0ef2cf70f939623a45c32d896a1f8d92d447a3`  
		Last Modified: Tue, 25 Feb 2025 09:33:53 GMT  
		Size: 21.1 KB (21103 bytes)  
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
$ docker pull fluentd@sha256:865ab159dcccf5aaf8f288e8616c73c1b025465817a2ea6cd4e0fa962d6de870
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
$ docker pull fluentd@sha256:a2f1b719ebc57cd1c84241ce7beccfb66037bf4c54387aaae13d6003a26cc1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72811577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2c39398438d941a88d1c4e7806a3ec2cac146ca1b72af9fefd0c80fbc9ce6a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77444f72ec27da57e1514fe30b3bd9df19b89e45af3964d6caa39afc741efc18`  
		Last Modified: Tue, 25 Feb 2025 02:34:58 GMT  
		Size: 3.5 MB (3499332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8b3152e3e2096181d3fc2de2c8fdd61bf366df9842791246d1dcf30341a45e`  
		Last Modified: Tue, 25 Feb 2025 02:34:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e19521013c5e837d619341aa7b91b6f3f0252dfcb903a97077c9df22bd7ae1`  
		Last Modified: Tue, 25 Feb 2025 02:34:58 GMT  
		Size: 35.9 MB (35949499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5f1a629292b824d28be6db12556e1d4084fa0ddf50faed57483ac8bf7f203`  
		Last Modified: Tue, 25 Feb 2025 02:34:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115d330cc2bdb6f0ba967cf966d474131988a258d9b5a25fe2d58f044ef1ea52`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 5.1 MB (5141047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9fda58e2072b96a230378a42fa8339491946991d43e74badfa9eb77a7b4c6`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7af2fe3116b182da8cbeeaa2d58483da70f9d1f887066c0a621dfee325c9060`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adc165bfe7846b605a9f779d9a4e0e1299af390fa37d65dfebf29e86daf1fa7`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:804aad0d408ca6f0dbe4ced3c579213d5a353704ca48fd90dc33fdc2d181c7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194438845c8117dba25136ffdf0a9d2681bc074e2fececf8181dc7d7f65dbf3f`

```dockerfile
```

-	Layers:
	-	`sha256:33f654fe9a7d4ad81e11ef8a0f017f586cf201de6293c185e8f1359cce71d40d`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 2.5 MB (2549630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8437297a6414727a0de66ca4a399aadee7cb3002f1b5095cc1ac08dba4ffc910`  
		Last Modified: Tue, 25 Feb 2025 03:23:29 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d4ec66bc79e541109d034d459140cb27e22c666247c6891ca1cdc03fad389301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66185545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9ed26cb61041d0d536fd030372ff4624a4d55c975ffd88647530bf97d7695e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb796b4078c24eacc4e96fa6314434576ef2cb38939712321f810114f707a3`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 3.1 MB (3073429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc6bbc44c189ac8a47708a7e65a210775688d0fd3df160a14b423364ed9ebc9`  
		Last Modified: Tue, 25 Feb 2025 07:53:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a7610f814d2917ce66eac3a6e0c706a7221d38ecb3b52e77da4551f21ed75`  
		Last Modified: Tue, 25 Feb 2025 07:59:59 GMT  
		Size: 32.3 MB (32310017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeddc5d5277515fe4fde129b1017e9a5be6e85ef444ce449049c15c43281aeb`  
		Last Modified: Tue, 25 Feb 2025 07:59:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32de484f2a4c14c9893815280d258aa34ec081c770aecc476ccc0483594e6987`  
		Last Modified: Tue, 25 Feb 2025 10:00:34 GMT  
		Size: 5.1 MB (5059067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98951eb254acd568a8937faf2685b91bb7c6fba38c68175a2e252ea1fa8d9f3`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7f4ae2bdb6934dbd25cc9aa29d8949c4437da51b96081ff7b703cdb41686f`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935c21fb971658154fb36c2c6bce8a205640e7073f1297e9860220b7316a9c09`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6700f6e1b5ed8fe336ac93c2a142571f338785a723ce5a04e3e88c6327ae0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea2c4a1cdfea74e04acc1a5c7ee31fbfd7303ab42e259901b47d58a008173ab`

```dockerfile
```

-	Layers:
	-	`sha256:68c15bfd7f37391f6f407d593ed0197d2a6968b048690a77f48c755f9604edf3`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 2.6 MB (2553117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0eb66ae2bcf82ec116904d686fd228ab037c7395e38d163a653289b6f81f5d4`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f0e6d68c34957c0c23d55caa5d195647b0aa521dba62df76763b4145b6ab9b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2917c895064e26f974a53f42a72a7b8251086bbd6876b415cde24af5d3d0fa0d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa00c010a50d2538d1c9dce260e0670c1f23132407fb79f24a3ea3a43af6ba`  
		Last Modified: Tue, 25 Feb 2025 12:56:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478f73f8ce2c65c709ee2e6a8916af059a187c52f1e2dd098045f746336173b`  
		Last Modified: Tue, 25 Feb 2025 13:14:26 GMT  
		Size: 32.1 MB (32145430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9c41f8aa4115e4ab80b8ab849109e1bd78637bec8e4f6d7eeb67b2b450c6e`  
		Last Modified: Tue, 25 Feb 2025 13:14:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f71e2fda4ee12b335c93d752e3e2b0119b09cecd47aeb30534efe1c576b781`  
		Last Modified: Tue, 25 Feb 2025 17:39:24 GMT  
		Size: 4.9 MB (4937313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6576d0a6ca449e8ff0d6965d33f9d88f998ac32e27465d357b7aaec97904d7`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212c93e58fedca4dbd0d9844e0b2868f1c5a9599a32dcae988f57f3095fc19d0`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60ee97852ba0827ad6ade820ee99a1972c042cb5352bec689c96dd7fd9839b7`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8d284c9c8ccf22596e04db377928f40816ba76301c022ce9ddd7ef8c4ca8e695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef2121df94b0eb0b0d6f0c0ab3b445da5d8de45b66722f47862c93e884b0916`

```dockerfile
```

-	Layers:
	-	`sha256:5925c16212422d9ca9b1fc67bf2ac3dedd270f98d676e4156e4786af7c806273`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 2.6 MB (2551856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2524f3aa05ddef65305e3bb2efe96db6c634af9fc85539441e526956cd0d03f`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:20e19ccedd35d81176af562be76b6db853e043e602e605ecf8d6a9f96920cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d493210fd5af7763f4a94bc50e5945bc616d1ab6b08dc7ed78c8057a2ed856`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d23f62980d9b0556214c013074faf49617432dc72038575e16558436e840c`  
		Last Modified: Tue, 25 Feb 2025 10:09:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d534dc9ec0a37b348c66b43ac1785942dbd5088ccf3f87961752338b5a2b6b`  
		Last Modified: Tue, 25 Feb 2025 10:20:21 GMT  
		Size: 35.9 MB (35869687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f948c724172e15609ec22db3ee957ec8e568073d1476571a3fb601c7f60a805`  
		Last Modified: Tue, 25 Feb 2025 10:20:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3bcddc9e30ee8e1f49a7680f5bb361237b6e6fa57a68722aa99977b8f87505`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 5.1 MB (5137551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d69cb98227255e16b2a491ed04790538a6026f54e5ec1bdd306017247d56ea`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3067401437d6dcad614664c1836ed4a2ba866cc5114d43e74d93fdec26088e2`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823e6632d1d2e987e84a74d80693f1cda2af588ab3d3b1e60c549adaa9966e33`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:02aa0b103d3f939675d7f1939236d977c65761d88e42aab2bcb5f892ad239535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6178378aba8d03b35c9cd429ecf915063832ad2e11d0ba3138c1f4b8784de4f`

```dockerfile
```

-	Layers:
	-	`sha256:7d640da375264518a07e8a5b1a0043c6284bb8e3b51a6aa64a7235aba9cd0a06`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 2.5 MB (2549870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24180e8a073776f85ff9dd2551ea81269afae2ce1519fcf24a6de9b4e1a3b6bd`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 20.3 KB (20341 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:191f2b0f37621120565a8296f2f78dd1964ec1af5a7bd0fa12c1ee856f8bef0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69972921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb1fd9ee7f6f7f30f3b290d4781934445a4366128007c77abb1fbabc19b96a4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3292a3220ab080841dc4b33e824dd20af65f71491c3ffde5c26a0c234e4043a`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 3.5 MB (3503439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca20b53c4a7810c52d4ad4ec45881533889dfba975e6fc040cc82b02f74e28f`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd7acbc020d76cf20ffe21d9b8d9fb01defd4285a758df9e27ed24a517f17a2`  
		Last Modified: Tue, 25 Feb 2025 03:24:11 GMT  
		Size: 32.1 MB (32145894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74114f3a304ee1aade20e246e99767eccb6e2420ff638a5d75d73d99cba6ae5`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678221b4ca801317e7f4e45eddda9c462cca5d6d7e1b002ba80c94df568c522a`  
		Last Modified: Tue, 25 Feb 2025 04:19:44 GMT  
		Size: 5.1 MB (5126608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aee01d9903559d3f0be8e098f2b0f7d4ddfe6930610e7442ebbec32160c08c`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0017ba95652022ab445d4448eb47b0e8f86ef140632e9a9ec79d1d3137f65f`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599a64d8d0fbe4ede42142dabe5af8c410ef605e225a67e6f1bc087c8f3ee154`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b3f0060b16e33571092380b0fe405afe16a561ffaf652123abc4c2ccbf5ce97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93aae3545b0cfab1c6aa3c9b4bda4fdad3de66b13360187a28691a278317660`

```dockerfile
```

-	Layers:
	-	`sha256:e481ead25b3e0263024e1a4b5486b32fdd044f9be3af1b156f07a4e3f83f51db`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 2.5 MB (2546766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54eee7b4e864fd78457e11bc972788f7aac6c269b4ada58e717d844d9556485c`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:518c27a1dd1bdb838dfcd82ce6cf5a413143d269524d8f19c3d755937db15660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75040422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6e544a9f856899c718b3d79dd3cc5d040ba6d8ee198b56108cd13494a1aeec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a43af6979a93ac649908165249f4bb955edcab70ac04e8f3ac9d6c7ffeebec`  
		Last Modified: Tue, 25 Feb 2025 07:22:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592351a0c4ef43e36a2ff54afd0a867ebd5eeb7bd3dba102040e0c6c87bb6ef`  
		Last Modified: Tue, 25 Feb 2025 07:30:55 GMT  
		Size: 33.8 MB (33818197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70279d426fc5e6924753fb6f710cf7db1e2ca9a757eb62263c5e9a23f4cc98b`  
		Last Modified: Tue, 25 Feb 2025 07:30:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7314785c47db7b249173cbcec32b86b0c4915e50915e60c89681000fd79b31b`  
		Last Modified: Tue, 25 Feb 2025 12:09:47 GMT  
		Size: 5.5 MB (5464535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f58de7922cf82dee65662077ee34dec47711ce0c995b8cee87ebe3aecffd45`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b7b9f3da980a8805c27dd67f3cc4abc4b4651cf4877641c7d3674ac70ae71`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dfc51dee20d8d7f26425f201019faf97e5e6ac35bfdd9fd63b1805171e8482`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a232762692a94c8fb179dac68229a51c56c6e2418060dfabd855cd75d7a5a4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70870d91f6ae32c45926507e7237fcb3dd8b4c6a50b0e3f2216aef827cc222af`

```dockerfile
```

-	Layers:
	-	`sha256:7943097387eb8b7d465b47acac1626fc63d359cb36b6171d79edfedc0135acfb`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 2.6 MB (2553949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddf606fc40abdf60c17faf26ef3bb2908b6f5433740f3736432c54ef8560e7b`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:f5a39c6cb1ae143e6e0d2706c512e39d0aefc261cce7466b0c3d8962465e6a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68287217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56354d53e9688d62a46d72dbbddc9210eb11e1ef1f944a28c6272023cfa51c80`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f059893784660d506287970229898dece31ad607ee75f8af7896ae23e7b42`  
		Last Modified: Tue, 25 Feb 2025 06:38:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b1e40e23a16b0bf7ec3f668f54c4a27b878db312799318b319d6a926e10411`  
		Last Modified: Tue, 25 Feb 2025 06:44:43 GMT  
		Size: 33.1 MB (33084236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3191e6b1f30a857074a7012bb632e9425d85c506e46b6febae7a336af8bd3893`  
		Last Modified: Tue, 25 Feb 2025 06:44:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c374c6d69514f329a8d4dce6bfb12ce219f31ef2a88723f30527d1938ac38`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 5.2 MB (5172350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eeab1a8cb5b7073c9159dafd97815d9b95684c591bfac01a850a6e6e7841b2`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b4bb889eb9f19971c8b6bf6e1934eb95abb247ea74b106a18b674d4b3d1e62`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4421e02776a25c6703bc6042cfd144e994033fe4b863bda2dd2ce96cadf336`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:506d3f9fbafd85974dc0b3d70b6fdb82fc0d8800fc52391db725f6aba0e5a561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4229eac5056a16854a300f02311a9864ab29a42d871dfaf24a525856dd0a1`

```dockerfile
```

-	Layers:
	-	`sha256:6b8ada79dff8768371d8e2d7ead2d2aaf80fd5685d88c201e653f00408b8c1d5`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 2.5 MB (2549347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b650bcd6f044f91607007e878fea3c93df47eabaabcd57c3053aa215c1c6d`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
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
$ docker pull fluentd@sha256:9b3a6a59dc9a9e6c2a1cb331942264b2092c0a32d56282b9b57f8a582a9e12cd
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
$ docker pull fluentd@sha256:8e947eff0ba8fbe57d7007c7c18c7c5dc8b7d06862e7c201056b0e948de64097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72805163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5fed660c963075f655d14fb8dc83773083bf8ffc8bb09fe42571eb12bc6b49`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8a126e16f182f2190d852c32868a653bb744267c88f79f72bcd9a6ad131e5`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 3.5 MB (3499331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2e961874d440895f78d64ad8cfa72f90cbaec413e84e76ad1c5f24b7f907a2`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f7c0de6fd8ae30d05e3c10de0a2a60879ab8c160e72375ed4ebf6c8e99ed0`  
		Last Modified: Mon, 17 Mar 2025 23:19:03 GMT  
		Size: 36.0 MB (35950065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320203a9f6e524a3462d074fe0a9cfbadd1faedfae58be7306f070236ff42ac`  
		Last Modified: Mon, 17 Mar 2025 23:19:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf48cfb6a77f59d94e54b84672ee9091bfa14a3e35994bc4bad5da4e7c21aa`  
		Last Modified: Tue, 18 Mar 2025 00:27:41 GMT  
		Size: 5.1 MB (5148509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf8e1634cb92b2f1d4e60fb6dbac80160600a94534ff5ed674cf4e9e2af265f`  
		Last Modified: Tue, 18 Mar 2025 00:27:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec3a34e32dbd27d40ebad90a68c4d3000da2d0a1d4f54bb7378340e18f76611`  
		Last Modified: Tue, 18 Mar 2025 00:27:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9833ac88c470f4275505aeef09e07d4d35a8ba05c8142a8080d6f27d150185ba`  
		Last Modified: Tue, 18 Mar 2025 00:27:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:40571f186739c0ffdac61302fc45e29485d46eab77cb13a8b1c5a92d992056ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b9704546e979dcdd6518552a8f222d0f5f0b13eb299faea79cc57d7c01c53`

```dockerfile
```

-	Layers:
	-	`sha256:2682d9386902b0ff381981aaf937b804c1fa1ea95d6afd2e54bbf891b833508b`  
		Last Modified: Tue, 18 Mar 2025 00:27:40 GMT  
		Size: 2.5 MB (2549674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0801f879111ae6a0a07f33a956b77191240072b7184eb83499eb98828bf9bb41`  
		Last Modified: Tue, 18 Mar 2025 00:27:40 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d4ec66bc79e541109d034d459140cb27e22c666247c6891ca1cdc03fad389301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66185545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9ed26cb61041d0d536fd030372ff4624a4d55c975ffd88647530bf97d7695e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb796b4078c24eacc4e96fa6314434576ef2cb38939712321f810114f707a3`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 3.1 MB (3073429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc6bbc44c189ac8a47708a7e65a210775688d0fd3df160a14b423364ed9ebc9`  
		Last Modified: Tue, 25 Feb 2025 07:53:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a7610f814d2917ce66eac3a6e0c706a7221d38ecb3b52e77da4551f21ed75`  
		Last Modified: Tue, 25 Feb 2025 07:59:59 GMT  
		Size: 32.3 MB (32310017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeddc5d5277515fe4fde129b1017e9a5be6e85ef444ce449049c15c43281aeb`  
		Last Modified: Tue, 25 Feb 2025 07:59:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32de484f2a4c14c9893815280d258aa34ec081c770aecc476ccc0483594e6987`  
		Last Modified: Tue, 25 Feb 2025 10:00:34 GMT  
		Size: 5.1 MB (5059067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98951eb254acd568a8937faf2685b91bb7c6fba38c68175a2e252ea1fa8d9f3`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7f4ae2bdb6934dbd25cc9aa29d8949c4437da51b96081ff7b703cdb41686f`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935c21fb971658154fb36c2c6bce8a205640e7073f1297e9860220b7316a9c09`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6700f6e1b5ed8fe336ac93c2a142571f338785a723ce5a04e3e88c6327ae0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea2c4a1cdfea74e04acc1a5c7ee31fbfd7303ab42e259901b47d58a008173ab`

```dockerfile
```

-	Layers:
	-	`sha256:68c15bfd7f37391f6f407d593ed0197d2a6968b048690a77f48c755f9604edf3`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 2.6 MB (2553117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0eb66ae2bcf82ec116904d686fd228ab037c7395e38d163a653289b6f81f5d4`  
		Last Modified: Tue, 25 Feb 2025 10:00:33 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f0e6d68c34957c0c23d55caa5d195647b0aa521dba62df76763b4145b6ab9b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2917c895064e26f974a53f42a72a7b8251086bbd6876b415cde24af5d3d0fa0d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa00c010a50d2538d1c9dce260e0670c1f23132407fb79f24a3ea3a43af6ba`  
		Last Modified: Tue, 25 Feb 2025 12:56:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478f73f8ce2c65c709ee2e6a8916af059a187c52f1e2dd098045f746336173b`  
		Last Modified: Tue, 25 Feb 2025 13:14:26 GMT  
		Size: 32.1 MB (32145430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9c41f8aa4115e4ab80b8ab849109e1bd78637bec8e4f6d7eeb67b2b450c6e`  
		Last Modified: Tue, 25 Feb 2025 13:14:25 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f71e2fda4ee12b335c93d752e3e2b0119b09cecd47aeb30534efe1c576b781`  
		Last Modified: Tue, 25 Feb 2025 17:39:24 GMT  
		Size: 4.9 MB (4937313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6576d0a6ca449e8ff0d6965d33f9d88f998ac32e27465d357b7aaec97904d7`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212c93e58fedca4dbd0d9844e0b2868f1c5a9599a32dcae988f57f3095fc19d0`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60ee97852ba0827ad6ade820ee99a1972c042cb5352bec689c96dd7fd9839b7`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8d284c9c8ccf22596e04db377928f40816ba76301c022ce9ddd7ef8c4ca8e695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef2121df94b0eb0b0d6f0c0ab3b445da5d8de45b66722f47862c93e884b0916`

```dockerfile
```

-	Layers:
	-	`sha256:5925c16212422d9ca9b1fc67bf2ac3dedd270f98d676e4156e4786af7c806273`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 2.6 MB (2551856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2524f3aa05ddef65305e3bb2efe96db6c634af9fc85539441e526956cd0d03f`  
		Last Modified: Tue, 25 Feb 2025 17:39:23 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:20e19ccedd35d81176af562be76b6db853e043e602e605ecf8d6a9f96920cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d493210fd5af7763f4a94bc50e5945bc616d1ab6b08dc7ed78c8057a2ed856`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d23f62980d9b0556214c013074faf49617432dc72038575e16558436e840c`  
		Last Modified: Tue, 25 Feb 2025 10:09:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d534dc9ec0a37b348c66b43ac1785942dbd5088ccf3f87961752338b5a2b6b`  
		Last Modified: Tue, 25 Feb 2025 10:20:21 GMT  
		Size: 35.9 MB (35869687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f948c724172e15609ec22db3ee957ec8e568073d1476571a3fb601c7f60a805`  
		Last Modified: Tue, 25 Feb 2025 10:20:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3bcddc9e30ee8e1f49a7680f5bb361237b6e6fa57a68722aa99977b8f87505`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 5.1 MB (5137551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d69cb98227255e16b2a491ed04790538a6026f54e5ec1bdd306017247d56ea`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3067401437d6dcad614664c1836ed4a2ba866cc5114d43e74d93fdec26088e2`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823e6632d1d2e987e84a74d80693f1cda2af588ab3d3b1e60c549adaa9966e33`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:02aa0b103d3f939675d7f1939236d977c65761d88e42aab2bcb5f892ad239535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6178378aba8d03b35c9cd429ecf915063832ad2e11d0ba3138c1f4b8784de4f`

```dockerfile
```

-	Layers:
	-	`sha256:7d640da375264518a07e8a5b1a0043c6284bb8e3b51a6aa64a7235aba9cd0a06`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 2.5 MB (2549870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24180e8a073776f85ff9dd2551ea81269afae2ce1519fcf24a6de9b4e1a3b6bd`  
		Last Modified: Tue, 25 Feb 2025 14:58:23 GMT  
		Size: 20.3 KB (20341 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:191f2b0f37621120565a8296f2f78dd1964ec1af5a7bd0fa12c1ee856f8bef0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69972921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb1fd9ee7f6f7f30f3b290d4781934445a4366128007c77abb1fbabc19b96a4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3292a3220ab080841dc4b33e824dd20af65f71491c3ffde5c26a0c234e4043a`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 3.5 MB (3503439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca20b53c4a7810c52d4ad4ec45881533889dfba975e6fc040cc82b02f74e28f`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd7acbc020d76cf20ffe21d9b8d9fb01defd4285a758df9e27ed24a517f17a2`  
		Last Modified: Tue, 25 Feb 2025 03:24:11 GMT  
		Size: 32.1 MB (32145894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74114f3a304ee1aade20e246e99767eccb6e2420ff638a5d75d73d99cba6ae5`  
		Last Modified: Tue, 25 Feb 2025 03:24:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678221b4ca801317e7f4e45eddda9c462cca5d6d7e1b002ba80c94df568c522a`  
		Last Modified: Tue, 25 Feb 2025 04:19:44 GMT  
		Size: 5.1 MB (5126608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aee01d9903559d3f0be8e098f2b0f7d4ddfe6930610e7442ebbec32160c08c`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0017ba95652022ab445d4448eb47b0e8f86ef140632e9a9ec79d1d3137f65f`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599a64d8d0fbe4ede42142dabe5af8c410ef605e225a67e6f1bc087c8f3ee154`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b3f0060b16e33571092380b0fe405afe16a561ffaf652123abc4c2ccbf5ce97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93aae3545b0cfab1c6aa3c9b4bda4fdad3de66b13360187a28691a278317660`

```dockerfile
```

-	Layers:
	-	`sha256:e481ead25b3e0263024e1a4b5486b32fdd044f9be3af1b156f07a4e3f83f51db`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 2.5 MB (2546766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54eee7b4e864fd78457e11bc972788f7aac6c269b4ada58e717d844d9556485c`  
		Last Modified: Tue, 25 Feb 2025 04:19:43 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:518c27a1dd1bdb838dfcd82ce6cf5a413143d269524d8f19c3d755937db15660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75040422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6e544a9f856899c718b3d79dd3cc5d040ba6d8ee198b56108cd13494a1aeec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a43af6979a93ac649908165249f4bb955edcab70ac04e8f3ac9d6c7ffeebec`  
		Last Modified: Tue, 25 Feb 2025 07:22:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592351a0c4ef43e36a2ff54afd0a867ebd5eeb7bd3dba102040e0c6c87bb6ef`  
		Last Modified: Tue, 25 Feb 2025 07:30:55 GMT  
		Size: 33.8 MB (33818197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70279d426fc5e6924753fb6f710cf7db1e2ca9a757eb62263c5e9a23f4cc98b`  
		Last Modified: Tue, 25 Feb 2025 07:30:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7314785c47db7b249173cbcec32b86b0c4915e50915e60c89681000fd79b31b`  
		Last Modified: Tue, 25 Feb 2025 12:09:47 GMT  
		Size: 5.5 MB (5464535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f58de7922cf82dee65662077ee34dec47711ce0c995b8cee87ebe3aecffd45`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b7b9f3da980a8805c27dd67f3cc4abc4b4651cf4877641c7d3674ac70ae71`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dfc51dee20d8d7f26425f201019faf97e5e6ac35bfdd9fd63b1805171e8482`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a232762692a94c8fb179dac68229a51c56c6e2418060dfabd855cd75d7a5a4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70870d91f6ae32c45926507e7237fcb3dd8b4c6a50b0e3f2216aef827cc222af`

```dockerfile
```

-	Layers:
	-	`sha256:7943097387eb8b7d465b47acac1626fc63d359cb36b6171d79edfedc0135acfb`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 2.6 MB (2553949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddf606fc40abdf60c17faf26ef3bb2908b6f5433740f3736432c54ef8560e7b`  
		Last Modified: Tue, 25 Feb 2025 12:09:46 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:f5a39c6cb1ae143e6e0d2706c512e39d0aefc261cce7466b0c3d8962465e6a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68287217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56354d53e9688d62a46d72dbbddc9210eb11e1ef1f944a28c6272023cfa51c80`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.7
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f059893784660d506287970229898dece31ad607ee75f8af7896ae23e7b42`  
		Last Modified: Tue, 25 Feb 2025 06:38:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b1e40e23a16b0bf7ec3f668f54c4a27b878db312799318b319d6a926e10411`  
		Last Modified: Tue, 25 Feb 2025 06:44:43 GMT  
		Size: 33.1 MB (33084236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3191e6b1f30a857074a7012bb632e9425d85c506e46b6febae7a336af8bd3893`  
		Last Modified: Tue, 25 Feb 2025 06:44:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c374c6d69514f329a8d4dce6bfb12ce219f31ef2a88723f30527d1938ac38`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 5.2 MB (5172350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eeab1a8cb5b7073c9159dafd97815d9b95684c591bfac01a850a6e6e7841b2`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b4bb889eb9f19971c8b6bf6e1934eb95abb247ea74b106a18b674d4b3d1e62`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4421e02776a25c6703bc6042cfd144e994033fe4b863bda2dd2ce96cadf336`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:506d3f9fbafd85974dc0b3d70b6fdb82fc0d8800fc52391db725f6aba0e5a561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4229eac5056a16854a300f02311a9864ab29a42d871dfaf24a525856dd0a1`

```dockerfile
```

-	Layers:
	-	`sha256:6b8ada79dff8768371d8e2d7ead2d2aaf80fd5685d88c201e653f00408b8c1d5`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 2.5 MB (2549347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b650bcd6f044f91607007e878fea3c93df47eabaabcd57c3053aa215c1c6d`  
		Last Modified: Tue, 25 Feb 2025 09:37:13 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json
