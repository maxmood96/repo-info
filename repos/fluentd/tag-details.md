<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.6-1.0`](#fluentdv1166-10)
-	[`fluentd:v1.16.6-debian-1.0`](#fluentdv1166-debian-10)
-	[`fluentd:v1.18-1`](#fluentdv118-1)
-	[`fluentd:v1.18-debian-1`](#fluentdv118-debian-1)
-	[`fluentd:v1.18.0-1.0`](#fluentdv1180-10)
-	[`fluentd:v1.18.0-debian-1.0`](#fluentdv1180-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:24a309c34863c4e97a8e890123fe936ef7779879f90d0e2b3165d61e98483d91
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
$ docker pull fluentd@sha256:4c0a5948bdec411ed6543d46d6896b75b23fdb26c779deb16facff0d5a165260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13486709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b6c77172c0473fd643200caa5c720f03277f583b27dcdb8a81b93dd4fdbb0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd378b01f03e6be712dcfcdb323317cca29acf1ba1e5cfcf4e51a34cd50d49`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 10.1 MB (10071273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aeb3ce22de6a9f47c7553fdb4ec0e782152ede465a8ec31d04870e1ebec4fc`  
		Last Modified: Tue, 07 Jan 2025 03:34:23 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c056cce2ddac76a24273a6be985fe440a9ddcbf652c9a04d7a42aa488fe4e9`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072211c40b59ec7b7c38df6453a207d8645dfe9a21362dce86fd4bbf7c84c2c`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7cde16897feb8f9913040d6e0f873a8173e0a11a9e0ca6378419dccb8701c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.8 KB (981752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d3f92390a910c14018c2ad6fde454bb5a0f5dc83a8c8ebedf7ebae7ff574`

```dockerfile
```

-	Layers:
	-	`sha256:940969d9a7406d40753c78203a1ff07ce91da381dcfd4a38efe7f13559bdaaf5`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 966.9 KB (966895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f51382362c1a792939fbcd7505f44969d3c0684f4a6e55fb358f260b83bbab9e`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65c9e421ed2513049edf7712c00ec27014a49520c8e8dd0bfa98db48017f2256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12270882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894f9486c3539563d1f402091e22a2c21fedb0fde6567937193a981d4dadddec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
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
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58b9263897cc0e79ef4c6e654d14352ced6a609a760bec255f8f0a2b39e26`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 9.1 MB (9099087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5665918c386010085ebb738d6eb1e7378309c19c6137ed7f582cb5c94a9a1cc`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73443ffa09ef618036cffc98c38421d9ec3fad5a2a4e5d8c386d9cf54ae41e77`  
		Last Modified: Tue, 07 Jan 2025 18:12:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b046d755911d1c8d32e7545f94db43ea045030f91f6e80d997a90bf084352014`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b04b911c8c0e7aaadc86b94e844de8561ce28a1eab56eaff56807535d653901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3bfda6bc781b19a9ee3b2860418e953862c63d3743cdc508e1f34580df957`

```dockerfile
```

-	Layers:
	-	`sha256:4f7b656259434256f0c66a9af2f481098c68c784662073018d1879293387864f`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4276938d2b57b1444d9a9baf1845ed1c71e3f6290f52334f3d5d653c9fee1141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13546606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217f8030ec9be0ea182db5b089659ffba5d3a24636ef97e8af84a38089144059`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1eb4b6684518896815f538154ac77386d0f4e8a5e5a1db410bf766e81c6f1`  
		Last Modified: Tue, 07 Jan 2025 15:35:26 GMT  
		Size: 10.2 MB (10192491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9481ad8fa03c61d0f3f12a5aad626700181a57ab4f9253301a349c8829149e2`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf2598d98331c3efd2672d4adbdc5a071eb9c5deba1ef533d68325a715ed3a`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2616908a602bb3563d13154d1bf52965c3ae47732a2d164531906d3682d962c`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:01b4921e77406f889d0437125b71bdf5f805cf04641a193eb3c0d5c8699e28dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.0 KB (982001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac5ac88201f97ce5374ce04294cdf1b6c7168970276cc2c99b7e235fff87b1`

```dockerfile
```

-	Layers:
	-	`sha256:3cf4c4489f806262ce791a8d0d075723ec462c1cbe852a02a9de5f768adbdd57`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 967.0 KB (967037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d187a63c79ddb91a2e0179f2797fcea1fa99c3ab862784dcaf7657bb889bd1`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:3b5c41740e127b2f7d11ece929062854204aa3d6fa9f18fd56be996e290be7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12579072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8bc33303f4a49f716042880ea26989704a7fb3f6eec1fa3854dacface2811`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86.tar.gz / # buildkit
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
	-	`sha256:ddad413607a62a4ff60ecbc53c13444783ab17a333628bcce0b2783b8aaea52a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.2 MB (3247827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ebd472c2c4b8c770ef6eebb5cbe24ce510939e072c5f9e54fa3fb8818280cc`  
		Size: 9.3 MB (9329077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7165958473bb23f17c1bcadd899abf68a02c4d2d3c29dbda0587f303f418f361`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429212592506ac6d80c94fc40441c2c47791db0d9c9a294d140516b2544ab19`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2268a222e0dbb04a424d5f4d2e6616909cf3e29903504a3cc4770426e7f6bea0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:3529f1fa68c6e021001144d35ec781a3da00c91615ce1f2ff57c99aa415e066e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.6 KB (978642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7484e9ca5a6499c1f1cc83722a881ff38e4b4348bdba4db63635fd47601cbf`

```dockerfile
```

-	Layers:
	-	`sha256:5f0eb9912709e5e6237727b146db6c49cf2d482c306631e667484ed630ea335a`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 963.8 KB (963818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad97972a90445331ceba4e37ee3b6c3d2f4f1252859d36e39a8f984fe8a083d0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8d15fba21b09b17efb24a833ece5a662b154de8dc05073d952579644c84e2b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13217994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abdf903efa8b689278ac12c0253e6c38ed90ab1286a27ed2ddbb80973d9a9bb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:14bbc05bcc91b6abaa1bc3bf5f448fd6260254d09a572cb88c4a8b8b3eaba807`  
		Last Modified: Tue, 07 Jan 2025 02:32:41 GMT  
		Size: 3.4 MB (3362221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a33dfed01d5417a57d4f45cfbe928b58c88eec772bf26ac6e5b6a340464ba3`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 9.9 MB (9853607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a58106e64ea15d2ae20c1eea3281aee6cb3e91b09a3eb406579523c1d407a5`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75268cb14ad8a568e21378f40ce4ea09fb692dcd6aa489c70c60e7a7c8cc856d`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6094d9f76c3cf37404c3e1c5b117c681cc454a3abfaa93e95920d77c6bc23b50`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e31280462d48e1a92de6b71658bd72440fd001c50d05aa67c1400dbf5854461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.5 KB (977494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38bce77f83a6e6328655287ba5ddda0bdb5335c9ce63734f4eaba845480ffbe`

```dockerfile
```

-	Layers:
	-	`sha256:1e6cc067b49ca30756bb9fe2794b8880136938ab5392c453fcf0182581d3ddf1`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 962.6 KB (962601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365d1ee83e9b66c8657c5396285020215532f2d7e13621e289ec5fa32667acc9`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:7d04fe8d748f98b7f89a69cc5c50c98903dca36d41f88f04ef80be67c60e5ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12878929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8298105f2e4482e393f24f932643016f0c4be4eea2c72a1a5b64071496d534`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-s390x.tar.gz / # buildkit
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
	-	`sha256:c4672aa17160cbc8f6b41aa2f65cabe08127bf890ea6e72064b57e28d86daa7d`  
		Last Modified: Tue, 07 Jan 2025 02:33:22 GMT  
		Size: 3.2 MB (3247312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caad40faeab658b1492659aa8a77d262981dd0068cca18be7f90f410f5fa337`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 9.6 MB (9629450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f4b2df8638dae157f53da71da26e377bb1d2f4d99cd355f7f906bca2f48c1`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634b3e9b2aa7f6500b26fc5705d7153abba5966f1d052a9125d85bcb917e91f5`  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b97bf6e2b56384e1f1fc573163b1908172cb476a538e6bfc9ffe784a679bfde`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:031207cae7590e9bf888427eeb0a07bf194dd73708bc727f6e9cde8b904db72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.8 KB (976838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1500dd0b96d22a47b222742642f7aa6cc6da0748366e60c42e854804b84582`

```dockerfile
```

-	Layers:
	-	`sha256:e325a002bcd4d4c25a459aa84b41cad23d135795b9053ea23bdca9fbdda56a8a`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 962.0 KB (961985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a7a7190a30fee7904cbe99d8c9059425326504ce2d1e6c3a2a620adf1daba2`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:8521a27ad53f4caa43323c13a104f1290f8a75c0ff24f461380a77c159c6ba02
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
$ docker pull fluentd@sha256:474f5eaf94d61a153ddad5d9e15dce2f28123247b9da0bc4cf7eff7506e3e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17480176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b9ccabaa774a625f0f63ac1236426973f1d1fbe2e3c0220be46b67cd2bf04`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa555f4bf60a280901108577bc638df9a56b44ef5f1868273eef6637d9c594e`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 14.1 MB (14064740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d115ebef31cf8f4881a094533fa947cfbc41502b0b6e884bab960d5b6e822`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ca33510f826b57178a1be839e03c011775cb26cd963cc50232b5d2262dd67b`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2496c3df6841b80203f2564734143e09829b11bdcb0c19b00df711c09142b926`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbf1e04858fbd520a150d0d0668531db25f353180139fecf41023c3ee147383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.5 KB (978536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc580e81d1ad339b90f066e7cfcfc4473015068e4aab3d7e06c24da3fa120c7`

```dockerfile
```

-	Layers:
	-	`sha256:bebc34c9c0aaabfc919df10e82e9c44335c20273d292e4909a66322bfd9c30f1`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 964.9 KB (964859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de0d5898450c77a101e3d6d6138ace810869c4bed3a3fd61ae25ee51176c6fa`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:f838c525b22e19c3f03003bdde757845a6386767695d6a86b09d80774ec65166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16226330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4bb288a3e2821f1d54617d859da42e13dd5019e0da83ef0d2ce986344ef575`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437fa92e8133a224fcc6adddfc4f6ea974c6c0ce3da4948f213c160a9a3d4df1`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 13.1 MB (13054538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849442fc539a0b9a411699e80f09b10a1d8f7e1e9b30643f3ec8ca7ac3c7771b`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23299f37d95ecf57ec0e756ea488b19c4fa86e6812c1dbd6a6d9123c616170e2`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf8d5a014c12ed1ac48ec07233cc62657435625dd2d6ec29352c67d5d14f23`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f6f794dd731a7a48a9a57b30b001e66f9d7df490e53ade2b367fe08d619a74cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1190c39f571d25a4f0e0dc307fbe5f3043783f48744569278efc15dc50614a9d`

```dockerfile
```

-	Layers:
	-	`sha256:01434e6fc9223460b0f4d077957a229402db564b1dadfd123b4f68f63516d32b`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:74b0067475ae041c6198d3793ad2ddd9508ccd07b4aa390c35195852bff14e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17464127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea9741ee81730bbb170e7652203f4fccf85251a0526bf7d0cea65875e9653d8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927635d247db211f041af36d26c36ad4dc2f118f43e9e321aca0bf88730bf05a`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 14.1 MB (14110014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0253092aeeb54691968322ee8099f993ece4e4ca9f8d8a08dd6d7f661e67550`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918fd2c39faee9d6b9abedbc3a51b6ae6e0c66a455927e6792e52d3212365285`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75528794271ad4d8a4574c18a7aeedfb2818b9fe62f409bf9431c0d1fe9c2791`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:afd98a1e166beee08920a759d1acde89cbf4fc129ef9501f9a272660ad748b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.8 KB (978761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f33705d1087b67863a64823440b18541c5c026a95b81fa766f453be6fb0404b`

```dockerfile
```

-	Layers:
	-	`sha256:10d9a5aa0ffc64f7abab1bf37449041c50cd9138595e91695d504283d136ea45`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 965.0 KB (964989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dd3d5fb88736d41340c31f993e82dcdb855fc87bf62302adb2dbf096de99f8`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:8cfcd5259f9b62978c547bd4f278d822af548850eb08009c5b3c55563720693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16438461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1639893c83252af4ea55604cae8328c11e89b0b99c5e1fcf82d8bcdfa81cc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-x86.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddad413607a62a4ff60ecbc53c13444783ab17a333628bcce0b2783b8aaea52a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.2 MB (3247827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ec3ea3cb08b7449f3a69e6e93ad2581567c93dffdbe494e5b50688e1b9f60`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 13.2 MB (13188469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835672619cac0dbf2c65befed0da927d454afc2b0498a420bd40e7d2e57f980`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd9ba0aaa744010f4376d798acc18150af0bc9a384172c1586528b395694e05`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed83130aaaf0194b08d61e7362bdcb8712bb13c63a8f5cbf13e35fab1856ad4`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:157120c1cd99cdfd2cb0022165a648c1385ead38ceff4ffb2c3c061a20399c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.4 KB (975439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19baed831a69d1e87168160421f6210e729ceb1994de3dcad46fc51e3c886b85`

```dockerfile
```

-	Layers:
	-	`sha256:5b28a2deda27a62c9fd2d42333359a3f8560a460fb2a5afa67131b0b986e14cf`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 961.8 KB (961787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44a9aa3d9dfd0b1a7bb8bab9488d6eaa3c564e9351b6b93d0ed0c4de3bc33ee`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d45a46fe4b70ba42d1dc0812a25a628ebf2b6690d267f30278194f51eef789fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17031668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a4ad81899f98ee6628fbdef2a0d71901309d50006a97c05aada366d48ba16`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-ppc64le.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14bbc05bcc91b6abaa1bc3bf5f448fd6260254d09a572cb88c4a8b8b3eaba807`  
		Last Modified: Tue, 07 Jan 2025 02:32:41 GMT  
		Size: 3.4 MB (3362221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4008434a20b55a051df0081bb30bae2ae3d1bb29cac5b989f667add4a426d`  
		Last Modified: Tue, 07 Jan 2025 09:42:40 GMT  
		Size: 13.7 MB (13667280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4333b95f1d75b0dc5d6cbbab2b7d021c7c3101ec9165f2b9b917d431864279e`  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64863a8bfde9a85f070e4ebc9d3e7a23f976f69c6883ec33974612047368d0ba`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce00931bf140610ae70cbb0b1f2a2e6ba17cab7b9bf28753ed53c1e25e538d8`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a6398c1e3ea6f414ac57a60e3934a956da58bf1cd72e4d4e03e96e2bf7cd9eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.3 KB (974270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fa1c69480ca76fbac55f4da6f3abf66e35b163820c0b4d4353c0a0f34e897a`

```dockerfile
```

-	Layers:
	-	`sha256:e55f0d3390c79616ed0c5cf18e6f4f495dd27e9671490f51317b7ca88264db7b`  
		Last Modified: Tue, 07 Jan 2025 09:42:40 GMT  
		Size: 960.6 KB (960559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c37b773e1bd1ad1e20c275c3a1eeb9958b93c099a549cbe57e27a466ae2e02`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:a5fd16a19b8b9e2cf7f1ed1dfd857b06541a8742c6085f9c15d88b488191570d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16896696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06d38234315765f1b4065fd555793fed7fab6a26ff570bf69bdeb9a202daa25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-s390x.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c4672aa17160cbc8f6b41aa2f65cabe08127bf890ea6e72064b57e28d86daa7d`  
		Last Modified: Tue, 07 Jan 2025 02:33:22 GMT  
		Size: 3.2 MB (3247312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98087691dd98f054c576fc20cf4b43494c36e41cea2b0a647ae53d928143310d`  
		Last Modified: Tue, 07 Jan 2025 15:24:35 GMT  
		Size: 13.6 MB (13647222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e2527a4f28074eb8928ac419944f07d329eb325d42a33bc709876b3cf2132e`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db330b53bd1d32b769176dff9f74d6f8e29700b591c2419e879c4458689f05f4`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a65953c848535ab81bfe8d6adbda74c00e74eb2e7ffb431f1123d78454d346`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ac70da475594c7cba0954782f1a64ee48c66bddba89f662a199b17642747ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.6 KB (973626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4f83451b77c80c26dc056e570c342380e7f94e57d240b5a478ac2400799380`

```dockerfile
```

-	Layers:
	-	`sha256:2f9c54c3d02f6f2944af29bd0ba3929bbf65e7113f02d52cb01b3fb726c7b448`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 959.9 KB (959949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5fc25f79e9bcdb96532b5fd5ba987883a4812fb6a955a3f6e54bb10796c82af`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:d8c5900486bfea8d8eb17375b8b83b1c37a9379fe0b16f9f36ab22be18f8e012
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
$ docker pull fluentd@sha256:48e381e24f6c3cad2ab581a99562812db5092d85638b2bf4cdf954c9606ec0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92354349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fb5d87c034b27aad3e744c7820ef4e83e4ec7edb2125ed2752e90429926aa4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6192766bba5c3464689794dd8795a413e7faa5070ebda6b1758995794f7ce2`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 13.7 MB (13670848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65b87ea982cfdb7796b311117e8d63e47322d8d0f90a9e974623f2fc11dc8e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b11361083bd06be74efb93cfaee92caca7f9a4e60fbe9c951dea9f9bf4f5e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 36.3 MB (36269137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db821620208c36c4857340805266208dc856ce52aa716ef809ecf0edfd8842e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83168a5f59e1f24acc15a2897d2520fc4b3acb4b14fbe99fc6777dc418f92cf`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 14.2 MB (14180392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4508b995191c3adcaa82150cf93c499816c53ddd9eb5d00ff88ccea07e6c9`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b50424c52f0ad7ebfebd6f06df398237a3c518fe217d2f7863d04d5d5c4af`  
		Last Modified: Wed, 08 Jan 2025 04:32:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d75370819b873ad4a1ad416d68a81d5306b705fc7748acb3613585c462bb71`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fbd7a81479c6ec5ab315390a61ac58cfe48b5f3e872656ce04f28a47cb0d7dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c65774f7360540e75b635c21234891285f7cac11c354bf1c1daef76e391db12`

```dockerfile
```

-	Layers:
	-	`sha256:27be3de03fdda380506d6c6ae95ab5066cfce8ac064bdeefab2444033a74784c`  
		Size: 2.6 MB (2570733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73b460942e182030cbe47353b6efe1ecc200584b04b4f380b2891c31f5bbbe1`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d64ac6c1d2b0000283dfb3a8d0c0bcff4f1f09aa03bba336c00072333a3d0dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326dc0b99e592001bd3875c19c9a0c2bbffd0741ddcd6dda6b035d1c8142af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c710cd50384381178d4a99b3fba9d2dfa69803556729285a1b50fd8deb12`  
		Last Modified: Wed, 25 Dec 2024 04:16:42 GMT  
		Size: 11.4 MB (11429897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dc8997201556ba03f5167cc7439004539824c7ac936f6fc0474c405d4bc997`  
		Last Modified: Wed, 25 Dec 2024 04:16:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b214593604478100cd665874141b1ad172f1d67397e2a60685aaef9bc432daa`  
		Last Modified: Wed, 25 Dec 2024 04:22:25 GMT  
		Size: 32.2 MB (32241968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a18dfcc4e105b009878324d3b5e5c829c8fa74d4600726658f68ddd462790`  
		Last Modified: Wed, 25 Dec 2024 04:22:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8c25c5deb885c55a430c438c64f7414215de0a87938b79a0f32609cac5079b`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 14.2 MB (14164960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5628e1275e2900f9e492a95a75526b6f483b7d5f88eeea1d2109ced35ff2f6ee`  
		Last Modified: Wed, 25 Dec 2024 06:28:33 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383b4eb6e65cf32698c7dfe546bb386c1088d7fdea1259e99a8084521791fc12`  
		Last Modified: Wed, 08 Jan 2025 04:32:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6335223be1732443ca5f74f1904d93e77007d11d4a70a883a69342df31e1c8`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b95c9fc42a867e8396be376cc8abd61ec3fdf6d882e1648654d02cb3b5350a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5593c1c860e006e5717b5b3aa41152b866965716c027026e42e0499000ef4f`

```dockerfile
```

-	Layers:
	-	`sha256:a93bbd5e0464b83b1018676638a3b1abfb349d857e010b71c16caac075ac03a1`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 2.6 MB (2574225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee4dc684bff7699ae1388db81f5f0efb3475bee07843850912834def543fef9`  
		Last Modified: Wed, 25 Dec 2024 06:28:33 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f3b6c538f34729b18a1b52e043ab4a54a424d892c72b04e53e67f3482426d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80869262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e34125f2f52a3c7413ca099aa76ca67f06a4287b7cbb14e6918f6692162b7c5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d05cb7c792ad963ab034afd2d15f759666da36de314b89fe00a60ccf1416c`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 10.8 MB (10766076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c75dc3e8dde657a75eb239ba3c01bb8fd67cd4c4edc2a7d4fa5b51badea60`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae61764a59ae0274f10a54b02df6b575a4b310e95e0fc9ddb756c26d2402ea0c`  
		Last Modified: Wed, 25 Dec 2024 12:27:52 GMT  
		Size: 32.1 MB (32082882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3a50097f6887ed6f64a61d1b54bb85dd938a22dfea772aa9fd51cfdda6bd5`  
		Last Modified: Wed, 25 Dec 2024 12:27:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86e02ea51c655cb090a59c73e9c9ad1b7f2694adae35da434e8d93d2ccde980`  
		Last Modified: Wed, 25 Dec 2024 16:31:57 GMT  
		Size: 14.1 MB (14084391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97b28d724cd9c23173da31ba2cc9d16d361095fe7b47d3029f0bd9d613fa38`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b709e6916253fa350cbf6c87b6296c7988c4cfb62d6bf2bd34ed0ada6a6fcea`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb83acb444fa2671db7d6ff345083ba38116e3c46844499f2831e3fbd1b6ea4`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2618b4175ea3625ca8ca5f8ef9f16d81a1c8b965b430b9d52bc626e73ff0d2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0e231ef2b569b4fa512d3fdc8a7884d6a882989a690197082c2d16ba3b5e55`

```dockerfile
```

-	Layers:
	-	`sha256:68cf86dd6e67d6bd47785782b74ce9a264c7b9cffd49dc2e69ac8ad0534f2198`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 2.6 MB (2572974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34115f9b42ecc4ef2e5cbf42d486e5bee1b66f44f8dbc7e2825b91d850bd2ea3`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2e29d3ac561e60d8d92c6a501285e136c03671e286189f31f4136f9c41183709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91009673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73abaa93c10594e760e5fb92883be2656592f8fe30688c6aab82403133d49a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670f5d8e14300025cf13b44458e85c51bee541e9d990f1e8e30b6a3524c3059`  
		Size: 12.5 MB (12516720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423b11e942a877e3918d0adc5fb8b1fff467ed3585db43efdc3c1638f6db54f`  
		Last Modified: Wed, 25 Dec 2024 06:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff8aa22c0dae194cfd3bbebe2ea2a126863d846aeb0e3f5afb02506c17b9246`  
		Last Modified: Wed, 25 Dec 2024 06:28:09 GMT  
		Size: 36.3 MB (36251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f872efb343a3030f7cf3df15e4730ae7995e23546ec5c40e7d5d4b1edc400`  
		Last Modified: Wed, 25 Dec 2024 06:28:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c9d55e06bd5bfb6464c8cbc770c4d235386f81d8a36c25002daaf6237e69b1`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 14.2 MB (14180108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ac5ee126c4ccf2e235778c2c2f85b9cc4d5b295ed0e160fe6ddcac0b160ef`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c33c9e87183964c610201b32044b4239db24ee31150248f201e992b793c83`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a623f11804ffc62f88a47a92e001b707982d9eef10f5d44dff124c44dbb8ec`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:24cafd3853f101eacd09fd23f9449b5ca60c7f7c52c3170cd43980381c8a3ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9442093b677b9087f93481b43d8e9a7d5bb65029eeab53d225446ffe2afd404c`

```dockerfile
```

-	Layers:
	-	`sha256:2583fdbdc08bdb8d8f514d9f7d01377d181bf3ff2748250d9b6cfe0e661925e8`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 2.6 MB (2570978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e484ef1edca1b80cc8008e3c3982a97a10ab907f16b8f9692772195dc253ba`  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:c51d54d4bb153fe14b5543dcb86363bad19aa5402ae323ac5c1512a2b26ddc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88485988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d67f0c4c745e91e288953a92030442498976f8ff923ecf03759ef45fc2ba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10752e01b1d65ccc3fe4892885524c7253244c0d05700692c4963c312a828e0`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 13.2 MB (13224941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb2b027029d23a36df20aa6d33d9a01b2d9b6566babd2b308cd26838c6f9d83`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc1b90e59458c949ca171a23e501f88b96941019a9d47b40c362e44ad182f2`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 32.1 MB (32080992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5c988d253d80c0614a4fc3323c1601e309e6ac635bc20d599c6e110354a98`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ff300cea88a0c842d300c75ae33a4400fee041546e0a6c402e7a667c75ef4a`  
		Last Modified: Tue, 24 Dec 2024 23:24:06 GMT  
		Size: 14.0 MB (13972277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb606a594beaeb3e62f377b7d2b1844a98e57a8ee6d972c5b6e576d40ec8bbf`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5742577212058aad230cc5abbaf87219ea7d9a0b29a788a93219706971dcc`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08acd3ba85a3b926fb7d37518822d4f48b1f9b3c40d74587025e3f2b013388`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cee2bd76d1263b80223fe43974ee50d26fc2129a39a29a44c89a494d5148881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a31a42e9e0e2e5c193b93713cdfdcb01108218a0bfd513e13f691b2657e6339`

```dockerfile
```

-	Layers:
	-	`sha256:aebfee1c090b7bc68f49e022d1059185dba3fede60a41e6e8d8fc136af5de665`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 2.6 MB (2567857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b651912b100e3b54de07d23e433a1f02a03d3e5a2cd65d9edd0dc67ab5fb1fa`  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ef9bcf12783fb6baf0901092596ff594179022b05a05991c8539388989b5973f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94770659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19d6d2f554c63c000525670ed847a6a1bf94724fb610bad38b1ac6b204c58ee`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3ea8a05c45526233e9213e7f2425280f25b80169948122fa7cfe93cc27458`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 14.4 MB (14402509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb31ee5cbf5a52d5431decdea9b6a5f38d4f650ca23edb6a395971c6231dcf2a`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362979882e32b13f5e21c8d29cd4ce7cc9863c68c688e3496f7b36abf3f127f`  
		Last Modified: Wed, 25 Dec 2024 09:00:36 GMT  
		Size: 33.7 MB (33730252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb364227e0f85d5ca3fb62c8f4d0aee3fea245933199a2f18aaf271468d8dd`  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc355fc61d843e31aad30fde330f991ad0202d4e39495ff8ce248aaa82a83bd`  
		Last Modified: Wed, 25 Dec 2024 12:13:30 GMT  
		Size: 14.6 MB (14572266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93492bb8b78fd7a6435e1e57b101eee74110fd0a101ab3df55c92b020e0cf00`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707465ab28075fa6451ce32f86e6e21acb50fad23fd8632b547c2bdca42c118e`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276be4b02741e39d4fbbab00953bb00c83feab3e2b7c2cf6cfcac04d1f4a052d`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a44bf21eb3a4a844bfb048c89de1b68b87dabac66ca02babf472c0d999ff52ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12265d912157fdd417694ef44ed8114a00899d5b9635319c42ad95374ce8da75`

```dockerfile
```

-	Layers:
	-	`sha256:43be7fb8afdb5a2e00607f880ed07b872f009eb6d801e8506eb5d63e8091e212`  
		Last Modified: Wed, 25 Dec 2024 12:13:30 GMT  
		Size: 2.6 MB (2575081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7f579c58ce63ad16099febba09691dd28dfc8598cc3aa36f6d8f175d877afd`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:29fba350601bcc8fe9b57c281e68f3e0ac95d7b668918d50de6d84bd1c005236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86056020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9148a7da572972239616b41fea2de55c3a31a4ac0bb504cd216777c8e0982a36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50be06e5ebedc40968798c3d6b6a09d3c7011f3ca20978a6c6e2a8f05a089d9`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 11.8 MB (11848389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7e7bc1a175ba0bd702f8259a0ace929069093dfd095b7fb5d977eda015a26`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a466601d6790e51cdc4e1d4575bcda2544830e27bcde57beb05638455a65e6`  
		Last Modified: Wed, 25 Dec 2024 02:59:38 GMT  
		Size: 33.0 MB (33014423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390762e91aff3a4bb685f14354e6e1626a8a9f79c28023e83801823963a5444`  
		Last Modified: Wed, 25 Dec 2024 02:59:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914400ec87bce3ff98ee4bda0282052bb8e1207aea51f7a569e205288bf8635d`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 14.3 MB (14311918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65373a34e0784b58bc51b329ad083c7dc773c85dde24ead8632e2e1a26947c07`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c183842c0d3df3ed035ae3851da5e04f0386da3f7786e23b0342936e3f16d2`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d130ea94d48528e77e6956b20f6468b9d7d4218274865d85f457530256463366`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:245628b0c95d0e82186e9f03563617780cbf3b16d50a86f8f065dee84d64cdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea5374beb4798e82a93b7cf7c0edfdd4ea8583754ef94a51f115a152920ec3`

```dockerfile
```

-	Layers:
	-	`sha256:9dc3b94819ef607d19d7f204776c6568c1f3d3ceb210603eba05be89f96dc61a`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 2.6 MB (2570445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d854f18317ffaab4893423d6bd03506ce7c6de768d6a65a17933f6617996fc41`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-1.0`

```console
$ docker pull fluentd@sha256:8521a27ad53f4caa43323c13a104f1290f8a75c0ff24f461380a77c159c6ba02
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

### `fluentd:v1.16.6-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:474f5eaf94d61a153ddad5d9e15dce2f28123247b9da0bc4cf7eff7506e3e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17480176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b9ccabaa774a625f0f63ac1236426973f1d1fbe2e3c0220be46b67cd2bf04`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa555f4bf60a280901108577bc638df9a56b44ef5f1868273eef6637d9c594e`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 14.1 MB (14064740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d115ebef31cf8f4881a094533fa947cfbc41502b0b6e884bab960d5b6e822`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ca33510f826b57178a1be839e03c011775cb26cd963cc50232b5d2262dd67b`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2496c3df6841b80203f2564734143e09829b11bdcb0c19b00df711c09142b926`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbf1e04858fbd520a150d0d0668531db25f353180139fecf41023c3ee147383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.5 KB (978536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc580e81d1ad339b90f066e7cfcfc4473015068e4aab3d7e06c24da3fa120c7`

```dockerfile
```

-	Layers:
	-	`sha256:bebc34c9c0aaabfc919df10e82e9c44335c20273d292e4909a66322bfd9c30f1`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 964.9 KB (964859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de0d5898450c77a101e3d6d6138ace810869c4bed3a3fd61ae25ee51176c6fa`  
		Last Modified: Tue, 07 Jan 2025 03:34:18 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:f838c525b22e19c3f03003bdde757845a6386767695d6a86b09d80774ec65166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16226330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4bb288a3e2821f1d54617d859da42e13dd5019e0da83ef0d2ce986344ef575`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437fa92e8133a224fcc6adddfc4f6ea974c6c0ce3da4948f213c160a9a3d4df1`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 13.1 MB (13054538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849442fc539a0b9a411699e80f09b10a1d8f7e1e9b30643f3ec8ca7ac3c7771b`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23299f37d95ecf57ec0e756ea488b19c4fa86e6812c1dbd6a6d9123c616170e2`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf8d5a014c12ed1ac48ec07233cc62657435625dd2d6ec29352c67d5d14f23`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f6f794dd731a7a48a9a57b30b001e66f9d7df490e53ade2b367fe08d619a74cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1190c39f571d25a4f0e0dc307fbe5f3043783f48744569278efc15dc50614a9d`

```dockerfile
```

-	Layers:
	-	`sha256:01434e6fc9223460b0f4d077957a229402db564b1dadfd123b4f68f63516d32b`  
		Last Modified: Tue, 07 Jan 2025 18:11:31 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:74b0067475ae041c6198d3793ad2ddd9508ccd07b4aa390c35195852bff14e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17464127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea9741ee81730bbb170e7652203f4fccf85251a0526bf7d0cea65875e9653d8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927635d247db211f041af36d26c36ad4dc2f118f43e9e321aca0bf88730bf05a`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 14.1 MB (14110014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0253092aeeb54691968322ee8099f993ece4e4ca9f8d8a08dd6d7f661e67550`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918fd2c39faee9d6b9abedbc3a51b6ae6e0c66a455927e6792e52d3212365285`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75528794271ad4d8a4574c18a7aeedfb2818b9fe62f409bf9431c0d1fe9c2791`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:afd98a1e166beee08920a759d1acde89cbf4fc129ef9501f9a272660ad748b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.8 KB (978761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f33705d1087b67863a64823440b18541c5c026a95b81fa766f453be6fb0404b`

```dockerfile
```

-	Layers:
	-	`sha256:10d9a5aa0ffc64f7abab1bf37449041c50cd9138595e91695d504283d136ea45`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 965.0 KB (964989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dd3d5fb88736d41340c31f993e82dcdb855fc87bf62302adb2dbf096de99f8`  
		Last Modified: Tue, 07 Jan 2025 15:34:16 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:8cfcd5259f9b62978c547bd4f278d822af548850eb08009c5b3c55563720693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16438461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb1639893c83252af4ea55604cae8328c11e89b0b99c5e1fcf82d8bcdfa81cc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-x86.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddad413607a62a4ff60ecbc53c13444783ab17a333628bcce0b2783b8aaea52a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.2 MB (3247827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ec3ea3cb08b7449f3a69e6e93ad2581567c93dffdbe494e5b50688e1b9f60`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 13.2 MB (13188469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835672619cac0dbf2c65befed0da927d454afc2b0498a420bd40e7d2e57f980`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd9ba0aaa744010f4376d798acc18150af0bc9a384172c1586528b395694e05`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed83130aaaf0194b08d61e7362bdcb8712bb13c63a8f5cbf13e35fab1856ad4`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:157120c1cd99cdfd2cb0022165a648c1385ead38ceff4ffb2c3c061a20399c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.4 KB (975439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19baed831a69d1e87168160421f6210e729ceb1994de3dcad46fc51e3c886b85`

```dockerfile
```

-	Layers:
	-	`sha256:5b28a2deda27a62c9fd2d42333359a3f8560a460fb2a5afa67131b0b986e14cf`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 961.8 KB (961787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44a9aa3d9dfd0b1a7bb8bab9488d6eaa3c564e9351b6b93d0ed0c4de3bc33ee`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d45a46fe4b70ba42d1dc0812a25a628ebf2b6690d267f30278194f51eef789fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17031668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a4ad81899f98ee6628fbdef2a0d71901309d50006a97c05aada366d48ba16`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-ppc64le.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14bbc05bcc91b6abaa1bc3bf5f448fd6260254d09a572cb88c4a8b8b3eaba807`  
		Last Modified: Tue, 07 Jan 2025 02:32:41 GMT  
		Size: 3.4 MB (3362221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4008434a20b55a051df0081bb30bae2ae3d1bb29cac5b989f667add4a426d`  
		Last Modified: Tue, 07 Jan 2025 09:42:40 GMT  
		Size: 13.7 MB (13667280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4333b95f1d75b0dc5d6cbbab2b7d021c7c3101ec9165f2b9b917d431864279e`  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64863a8bfde9a85f070e4ebc9d3e7a23f976f69c6883ec33974612047368d0ba`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce00931bf140610ae70cbb0b1f2a2e6ba17cab7b9bf28753ed53c1e25e538d8`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a6398c1e3ea6f414ac57a60e3934a956da58bf1cd72e4d4e03e96e2bf7cd9eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.3 KB (974270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fa1c69480ca76fbac55f4da6f3abf66e35b163820c0b4d4353c0a0f34e897a`

```dockerfile
```

-	Layers:
	-	`sha256:e55f0d3390c79616ed0c5cf18e6f4f495dd27e9671490f51317b7ca88264db7b`  
		Last Modified: Tue, 07 Jan 2025 09:42:40 GMT  
		Size: 960.6 KB (960559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c37b773e1bd1ad1e20c275c3a1eeb9958b93c099a549cbe57e27a466ae2e02`  
		Last Modified: Tue, 07 Jan 2025 09:42:39 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:a5fd16a19b8b9e2cf7f1ed1dfd857b06541a8742c6085f9c15d88b488191570d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16896696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06d38234315765f1b4065fd555793fed7fab6a26ff570bf69bdeb9a202daa25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.5-s390x.tar.gz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c4672aa17160cbc8f6b41aa2f65cabe08127bf890ea6e72064b57e28d86daa7d`  
		Last Modified: Tue, 07 Jan 2025 02:33:22 GMT  
		Size: 3.2 MB (3247312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98087691dd98f054c576fc20cf4b43494c36e41cea2b0a647ae53d928143310d`  
		Last Modified: Tue, 07 Jan 2025 15:24:35 GMT  
		Size: 13.6 MB (13647222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e2527a4f28074eb8928ac419944f07d329eb325d42a33bc709876b3cf2132e`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db330b53bd1d32b769176dff9f74d6f8e29700b591c2419e879c4458689f05f4`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a65953c848535ab81bfe8d6adbda74c00e74eb2e7ffb431f1123d78454d346`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ac70da475594c7cba0954782f1a64ee48c66bddba89f662a199b17642747ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.6 KB (973626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4f83451b77c80c26dc056e570c342380e7f94e57d240b5a478ac2400799380`

```dockerfile
```

-	Layers:
	-	`sha256:2f9c54c3d02f6f2944af29bd0ba3929bbf65e7113f02d52cb01b3fb726c7b448`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 959.9 KB (959949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5fc25f79e9bcdb96532b5fd5ba987883a4812fb6a955a3f6e54bb10796c82af`  
		Last Modified: Tue, 07 Jan 2025 15:24:34 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-debian-1.0`

```console
$ docker pull fluentd@sha256:d8c5900486bfea8d8eb17375b8b83b1c37a9379fe0b16f9f36ab22be18f8e012
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

### `fluentd:v1.16.6-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:48e381e24f6c3cad2ab581a99562812db5092d85638b2bf4cdf954c9606ec0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92354349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fb5d87c034b27aad3e744c7820ef4e83e4ec7edb2125ed2752e90429926aa4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6192766bba5c3464689794dd8795a413e7faa5070ebda6b1758995794f7ce2`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 13.7 MB (13670848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65b87ea982cfdb7796b311117e8d63e47322d8d0f90a9e974623f2fc11dc8e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b11361083bd06be74efb93cfaee92caca7f9a4e60fbe9c951dea9f9bf4f5e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 36.3 MB (36269137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db821620208c36c4857340805266208dc856ce52aa716ef809ecf0edfd8842e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83168a5f59e1f24acc15a2897d2520fc4b3acb4b14fbe99fc6777dc418f92cf`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 14.2 MB (14180392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4508b995191c3adcaa82150cf93c499816c53ddd9eb5d00ff88ccea07e6c9`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b50424c52f0ad7ebfebd6f06df398237a3c518fe217d2f7863d04d5d5c4af`  
		Last Modified: Wed, 08 Jan 2025 04:32:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d75370819b873ad4a1ad416d68a81d5306b705fc7748acb3613585c462bb71`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fbd7a81479c6ec5ab315390a61ac58cfe48b5f3e872656ce04f28a47cb0d7dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c65774f7360540e75b635c21234891285f7cac11c354bf1c1daef76e391db12`

```dockerfile
```

-	Layers:
	-	`sha256:27be3de03fdda380506d6c6ae95ab5066cfce8ac064bdeefab2444033a74784c`  
		Size: 2.6 MB (2570733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73b460942e182030cbe47353b6efe1ecc200584b04b4f380b2891c31f5bbbe1`  
		Last Modified: Tue, 24 Dec 2024 23:25:38 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d64ac6c1d2b0000283dfb3a8d0c0bcff4f1f09aa03bba336c00072333a3d0dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83594122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326dc0b99e592001bd3875c19c9a0c2bbffd0741ddcd6dda6b035d1c8142af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c710cd50384381178d4a99b3fba9d2dfa69803556729285a1b50fd8deb12`  
		Last Modified: Wed, 25 Dec 2024 04:16:42 GMT  
		Size: 11.4 MB (11429897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dc8997201556ba03f5167cc7439004539824c7ac936f6fc0474c405d4bc997`  
		Last Modified: Wed, 25 Dec 2024 04:16:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b214593604478100cd665874141b1ad172f1d67397e2a60685aaef9bc432daa`  
		Last Modified: Wed, 25 Dec 2024 04:22:25 GMT  
		Size: 32.2 MB (32241968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a18dfcc4e105b009878324d3b5e5c829c8fa74d4600726658f68ddd462790`  
		Last Modified: Wed, 25 Dec 2024 04:22:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8c25c5deb885c55a430c438c64f7414215de0a87938b79a0f32609cac5079b`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 14.2 MB (14164960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5628e1275e2900f9e492a95a75526b6f483b7d5f88eeea1d2109ced35ff2f6ee`  
		Last Modified: Wed, 25 Dec 2024 06:28:33 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383b4eb6e65cf32698c7dfe546bb386c1088d7fdea1259e99a8084521791fc12`  
		Last Modified: Wed, 08 Jan 2025 04:32:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6335223be1732443ca5f74f1904d93e77007d11d4a70a883a69342df31e1c8`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b95c9fc42a867e8396be376cc8abd61ec3fdf6d882e1648654d02cb3b5350a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5593c1c860e006e5717b5b3aa41152b866965716c027026e42e0499000ef4f`

```dockerfile
```

-	Layers:
	-	`sha256:a93bbd5e0464b83b1018676638a3b1abfb349d857e010b71c16caac075ac03a1`  
		Last Modified: Wed, 25 Dec 2024 06:28:34 GMT  
		Size: 2.6 MB (2574225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee4dc684bff7699ae1388db81f5f0efb3475bee07843850912834def543fef9`  
		Last Modified: Wed, 25 Dec 2024 06:28:33 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f3b6c538f34729b18a1b52e043ab4a54a424d892c72b04e53e67f3482426d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80869262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e34125f2f52a3c7413ca099aa76ca67f06a4287b7cbb14e6918f6692162b7c5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d05cb7c792ad963ab034afd2d15f759666da36de314b89fe00a60ccf1416c`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 10.8 MB (10766076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c75dc3e8dde657a75eb239ba3c01bb8fd67cd4c4edc2a7d4fa5b51badea60`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae61764a59ae0274f10a54b02df6b575a4b310e95e0fc9ddb756c26d2402ea0c`  
		Last Modified: Wed, 25 Dec 2024 12:27:52 GMT  
		Size: 32.1 MB (32082882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3a50097f6887ed6f64a61d1b54bb85dd938a22dfea772aa9fd51cfdda6bd5`  
		Last Modified: Wed, 25 Dec 2024 12:27:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86e02ea51c655cb090a59c73e9c9ad1b7f2694adae35da434e8d93d2ccde980`  
		Last Modified: Wed, 25 Dec 2024 16:31:57 GMT  
		Size: 14.1 MB (14084391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97b28d724cd9c23173da31ba2cc9d16d361095fe7b47d3029f0bd9d613fa38`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b709e6916253fa350cbf6c87b6296c7988c4cfb62d6bf2bd34ed0ada6a6fcea`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb83acb444fa2671db7d6ff345083ba38116e3c46844499f2831e3fbd1b6ea4`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2618b4175ea3625ca8ca5f8ef9f16d81a1c8b965b430b9d52bc626e73ff0d2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0e231ef2b569b4fa512d3fdc8a7884d6a882989a690197082c2d16ba3b5e55`

```dockerfile
```

-	Layers:
	-	`sha256:68cf86dd6e67d6bd47785782b74ce9a264c7b9cffd49dc2e69ac8ad0534f2198`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 2.6 MB (2572974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34115f9b42ecc4ef2e5cbf42d486e5bee1b66f44f8dbc7e2825b91d850bd2ea3`  
		Last Modified: Wed, 25 Dec 2024 16:31:56 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2e29d3ac561e60d8d92c6a501285e136c03671e286189f31f4136f9c41183709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91009673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73abaa93c10594e760e5fb92883be2656592f8fe30688c6aab82403133d49a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670f5d8e14300025cf13b44458e85c51bee541e9d990f1e8e30b6a3524c3059`  
		Size: 12.5 MB (12516720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423b11e942a877e3918d0adc5fb8b1fff467ed3585db43efdc3c1638f6db54f`  
		Last Modified: Wed, 25 Dec 2024 06:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff8aa22c0dae194cfd3bbebe2ea2a126863d846aeb0e3f5afb02506c17b9246`  
		Last Modified: Wed, 25 Dec 2024 06:28:09 GMT  
		Size: 36.3 MB (36251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f872efb343a3030f7cf3df15e4730ae7995e23546ec5c40e7d5d4b1edc400`  
		Last Modified: Wed, 25 Dec 2024 06:28:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c9d55e06bd5bfb6464c8cbc770c4d235386f81d8a36c25002daaf6237e69b1`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 14.2 MB (14180108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ac5ee126c4ccf2e235778c2c2f85b9cc4d5b295ed0e160fe6ddcac0b160ef`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c33c9e87183964c610201b32044b4239db24ee31150248f201e992b793c83`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a623f11804ffc62f88a47a92e001b707982d9eef10f5d44dff124c44dbb8ec`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:24cafd3853f101eacd09fd23f9449b5ca60c7f7c52c3170cd43980381c8a3ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9442093b677b9087f93481b43d8e9a7d5bb65029eeab53d225446ffe2afd404c`

```dockerfile
```

-	Layers:
	-	`sha256:2583fdbdc08bdb8d8f514d9f7d01377d181bf3ff2748250d9b6cfe0e661925e8`  
		Last Modified: Wed, 25 Dec 2024 10:53:56 GMT  
		Size: 2.6 MB (2570978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e484ef1edca1b80cc8008e3c3982a97a10ab907f16b8f9692772195dc253ba`  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c51d54d4bb153fe14b5543dcb86363bad19aa5402ae323ac5c1512a2b26ddc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88485988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d67f0c4c745e91e288953a92030442498976f8ff923ecf03759ef45fc2ba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10752e01b1d65ccc3fe4892885524c7253244c0d05700692c4963c312a828e0`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 13.2 MB (13224941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb2b027029d23a36df20aa6d33d9a01b2d9b6566babd2b308cd26838c6f9d83`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc1b90e59458c949ca171a23e501f88b96941019a9d47b40c362e44ad182f2`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 32.1 MB (32080992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5c988d253d80c0614a4fc3323c1601e309e6ac635bc20d599c6e110354a98`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ff300cea88a0c842d300c75ae33a4400fee041546e0a6c402e7a667c75ef4a`  
		Last Modified: Tue, 24 Dec 2024 23:24:06 GMT  
		Size: 14.0 MB (13972277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb606a594beaeb3e62f377b7d2b1844a98e57a8ee6d972c5b6e576d40ec8bbf`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5742577212058aad230cc5abbaf87219ea7d9a0b29a788a93219706971dcc`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08acd3ba85a3b926fb7d37518822d4f48b1f9b3c40d74587025e3f2b013388`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cee2bd76d1263b80223fe43974ee50d26fc2129a39a29a44c89a494d5148881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a31a42e9e0e2e5c193b93713cdfdcb01108218a0bfd513e13f691b2657e6339`

```dockerfile
```

-	Layers:
	-	`sha256:aebfee1c090b7bc68f49e022d1059185dba3fede60a41e6e8d8fc136af5de665`  
		Last Modified: Tue, 24 Dec 2024 23:24:05 GMT  
		Size: 2.6 MB (2567857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b651912b100e3b54de07d23e433a1f02a03d3e5a2cd65d9edd0dc67ab5fb1fa`  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ef9bcf12783fb6baf0901092596ff594179022b05a05991c8539388989b5973f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94770659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19d6d2f554c63c000525670ed847a6a1bf94724fb610bad38b1ac6b204c58ee`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3ea8a05c45526233e9213e7f2425280f25b80169948122fa7cfe93cc27458`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 14.4 MB (14402509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb31ee5cbf5a52d5431decdea9b6a5f38d4f650ca23edb6a395971c6231dcf2a`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362979882e32b13f5e21c8d29cd4ce7cc9863c68c688e3496f7b36abf3f127f`  
		Last Modified: Wed, 25 Dec 2024 09:00:36 GMT  
		Size: 33.7 MB (33730252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb364227e0f85d5ca3fb62c8f4d0aee3fea245933199a2f18aaf271468d8dd`  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc355fc61d843e31aad30fde330f991ad0202d4e39495ff8ce248aaa82a83bd`  
		Last Modified: Wed, 25 Dec 2024 12:13:30 GMT  
		Size: 14.6 MB (14572266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93492bb8b78fd7a6435e1e57b101eee74110fd0a101ab3df55c92b020e0cf00`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707465ab28075fa6451ce32f86e6e21acb50fad23fd8632b547c2bdca42c118e`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276be4b02741e39d4fbbab00953bb00c83feab3e2b7c2cf6cfcac04d1f4a052d`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a44bf21eb3a4a844bfb048c89de1b68b87dabac66ca02babf472c0d999ff52ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12265d912157fdd417694ef44ed8114a00899d5b9635319c42ad95374ce8da75`

```dockerfile
```

-	Layers:
	-	`sha256:43be7fb8afdb5a2e00607f880ed07b872f009eb6d801e8506eb5d63e8091e212`  
		Last Modified: Wed, 25 Dec 2024 12:13:30 GMT  
		Size: 2.6 MB (2575081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7f579c58ce63ad16099febba09691dd28dfc8598cc3aa36f6d8f175d877afd`  
		Last Modified: Wed, 25 Dec 2024 12:13:29 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:29fba350601bcc8fe9b57c281e68f3e0ac95d7b668918d50de6d84bd1c005236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86056020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9148a7da572972239616b41fea2de55c3a31a4ac0bb504cd216777c8e0982a36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LANG=C.UTF-8
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_VERSION=3.2.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Thu, 22 Aug 2024 02:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Aug 2024 02:52:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["irb"]
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 22 Aug 2024 02:52:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.6
# Thu, 22 Aug 2024 02:52:20 GMT
ENV TINI_VERSION=0.18.0
# Thu, 22 Aug 2024 02:52:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.6  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 22 Aug 2024 02:52:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 22 Aug 2024 02:52:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 22 Aug 2024 02:52:20 GMT
USER fluent
# Thu, 22 Aug 2024 02:52:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50be06e5ebedc40968798c3d6b6a09d3c7011f3ca20978a6c6e2a8f05a089d9`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 11.8 MB (11848389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7e7bc1a175ba0bd702f8259a0ace929069093dfd095b7fb5d977eda015a26`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a466601d6790e51cdc4e1d4575bcda2544830e27bcde57beb05638455a65e6`  
		Last Modified: Wed, 25 Dec 2024 02:59:38 GMT  
		Size: 33.0 MB (33014423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390762e91aff3a4bb685f14354e6e1626a8a9f79c28023e83801823963a5444`  
		Last Modified: Wed, 25 Dec 2024 02:59:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914400ec87bce3ff98ee4bda0282052bb8e1207aea51f7a569e205288bf8635d`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 14.3 MB (14311918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65373a34e0784b58bc51b329ad083c7dc773c85dde24ead8632e2e1a26947c07`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c183842c0d3df3ed035ae3851da5e04f0386da3f7786e23b0342936e3f16d2`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d130ea94d48528e77e6956b20f6468b9d7d4218274865d85f457530256463366`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:245628b0c95d0e82186e9f03563617780cbf3b16d50a86f8f065dee84d64cdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea5374beb4798e82a93b7cf7c0edfdd4ea8583754ef94a51f115a152920ec3`

```dockerfile
```

-	Layers:
	-	`sha256:9dc3b94819ef607d19d7f204776c6568c1f3d3ceb210603eba05be89f96dc61a`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 2.6 MB (2570445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d854f18317ffaab4893423d6bd03506ce7c6de768d6a65a17933f6617996fc41`  
		Last Modified: Wed, 25 Dec 2024 05:22:42 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-1`

```console
$ docker pull fluentd@sha256:24a309c34863c4e97a8e890123fe936ef7779879f90d0e2b3165d61e98483d91
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
$ docker pull fluentd@sha256:4c0a5948bdec411ed6543d46d6896b75b23fdb26c779deb16facff0d5a165260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13486709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b6c77172c0473fd643200caa5c720f03277f583b27dcdb8a81b93dd4fdbb0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd378b01f03e6be712dcfcdb323317cca29acf1ba1e5cfcf4e51a34cd50d49`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 10.1 MB (10071273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aeb3ce22de6a9f47c7553fdb4ec0e782152ede465a8ec31d04870e1ebec4fc`  
		Last Modified: Tue, 07 Jan 2025 03:34:23 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c056cce2ddac76a24273a6be985fe440a9ddcbf652c9a04d7a42aa488fe4e9`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072211c40b59ec7b7c38df6453a207d8645dfe9a21362dce86fd4bbf7c84c2c`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7cde16897feb8f9913040d6e0f873a8173e0a11a9e0ca6378419dccb8701c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.8 KB (981752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d3f92390a910c14018c2ad6fde454bb5a0f5dc83a8c8ebedf7ebae7ff574`

```dockerfile
```

-	Layers:
	-	`sha256:940969d9a7406d40753c78203a1ff07ce91da381dcfd4a38efe7f13559bdaaf5`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 966.9 KB (966895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f51382362c1a792939fbcd7505f44969d3c0684f4a6e55fb358f260b83bbab9e`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65c9e421ed2513049edf7712c00ec27014a49520c8e8dd0bfa98db48017f2256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12270882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894f9486c3539563d1f402091e22a2c21fedb0fde6567937193a981d4dadddec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
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
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58b9263897cc0e79ef4c6e654d14352ced6a609a760bec255f8f0a2b39e26`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 9.1 MB (9099087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5665918c386010085ebb738d6eb1e7378309c19c6137ed7f582cb5c94a9a1cc`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73443ffa09ef618036cffc98c38421d9ec3fad5a2a4e5d8c386d9cf54ae41e77`  
		Last Modified: Tue, 07 Jan 2025 18:12:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b046d755911d1c8d32e7545f94db43ea045030f91f6e80d997a90bf084352014`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b04b911c8c0e7aaadc86b94e844de8561ce28a1eab56eaff56807535d653901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3bfda6bc781b19a9ee3b2860418e953862c63d3743cdc508e1f34580df957`

```dockerfile
```

-	Layers:
	-	`sha256:4f7b656259434256f0c66a9af2f481098c68c784662073018d1879293387864f`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4276938d2b57b1444d9a9baf1845ed1c71e3f6290f52334f3d5d653c9fee1141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13546606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217f8030ec9be0ea182db5b089659ffba5d3a24636ef97e8af84a38089144059`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1eb4b6684518896815f538154ac77386d0f4e8a5e5a1db410bf766e81c6f1`  
		Last Modified: Tue, 07 Jan 2025 15:35:26 GMT  
		Size: 10.2 MB (10192491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9481ad8fa03c61d0f3f12a5aad626700181a57ab4f9253301a349c8829149e2`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf2598d98331c3efd2672d4adbdc5a071eb9c5deba1ef533d68325a715ed3a`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2616908a602bb3563d13154d1bf52965c3ae47732a2d164531906d3682d962c`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:01b4921e77406f889d0437125b71bdf5f805cf04641a193eb3c0d5c8699e28dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.0 KB (982001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac5ac88201f97ce5374ce04294cdf1b6c7168970276cc2c99b7e235fff87b1`

```dockerfile
```

-	Layers:
	-	`sha256:3cf4c4489f806262ce791a8d0d075723ec462c1cbe852a02a9de5f768adbdd57`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 967.0 KB (967037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d187a63c79ddb91a2e0179f2797fcea1fa99c3ab862784dcaf7657bb889bd1`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; 386

```console
$ docker pull fluentd@sha256:3b5c41740e127b2f7d11ece929062854204aa3d6fa9f18fd56be996e290be7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12579072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8bc33303f4a49f716042880ea26989704a7fb3f6eec1fa3854dacface2811`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86.tar.gz / # buildkit
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
	-	`sha256:ddad413607a62a4ff60ecbc53c13444783ab17a333628bcce0b2783b8aaea52a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.2 MB (3247827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ebd472c2c4b8c770ef6eebb5cbe24ce510939e072c5f9e54fa3fb8818280cc`  
		Size: 9.3 MB (9329077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7165958473bb23f17c1bcadd899abf68a02c4d2d3c29dbda0587f303f418f361`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429212592506ac6d80c94fc40441c2c47791db0d9c9a294d140516b2544ab19`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2268a222e0dbb04a424d5f4d2e6616909cf3e29903504a3cc4770426e7f6bea0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3529f1fa68c6e021001144d35ec781a3da00c91615ce1f2ff57c99aa415e066e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.6 KB (978642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7484e9ca5a6499c1f1cc83722a881ff38e4b4348bdba4db63635fd47601cbf`

```dockerfile
```

-	Layers:
	-	`sha256:5f0eb9912709e5e6237727b146db6c49cf2d482c306631e667484ed630ea335a`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 963.8 KB (963818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad97972a90445331ceba4e37ee3b6c3d2f4f1252859d36e39a8f984fe8a083d0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8d15fba21b09b17efb24a833ece5a662b154de8dc05073d952579644c84e2b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13217994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abdf903efa8b689278ac12c0253e6c38ed90ab1286a27ed2ddbb80973d9a9bb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:14bbc05bcc91b6abaa1bc3bf5f448fd6260254d09a572cb88c4a8b8b3eaba807`  
		Last Modified: Tue, 07 Jan 2025 02:32:41 GMT  
		Size: 3.4 MB (3362221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a33dfed01d5417a57d4f45cfbe928b58c88eec772bf26ac6e5b6a340464ba3`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 9.9 MB (9853607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a58106e64ea15d2ae20c1eea3281aee6cb3e91b09a3eb406579523c1d407a5`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75268cb14ad8a568e21378f40ce4ea09fb692dcd6aa489c70c60e7a7c8cc856d`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6094d9f76c3cf37404c3e1c5b117c681cc454a3abfaa93e95920d77c6bc23b50`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e31280462d48e1a92de6b71658bd72440fd001c50d05aa67c1400dbf5854461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.5 KB (977494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38bce77f83a6e6328655287ba5ddda0bdb5335c9ce63734f4eaba845480ffbe`

```dockerfile
```

-	Layers:
	-	`sha256:1e6cc067b49ca30756bb9fe2794b8880136938ab5392c453fcf0182581d3ddf1`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 962.6 KB (962601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365d1ee83e9b66c8657c5396285020215532f2d7e13621e289ec5fa32667acc9`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; s390x

```console
$ docker pull fluentd@sha256:7d04fe8d748f98b7f89a69cc5c50c98903dca36d41f88f04ef80be67c60e5ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12878929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8298105f2e4482e393f24f932643016f0c4be4eea2c72a1a5b64071496d534`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-s390x.tar.gz / # buildkit
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
	-	`sha256:c4672aa17160cbc8f6b41aa2f65cabe08127bf890ea6e72064b57e28d86daa7d`  
		Last Modified: Tue, 07 Jan 2025 02:33:22 GMT  
		Size: 3.2 MB (3247312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caad40faeab658b1492659aa8a77d262981dd0068cca18be7f90f410f5fa337`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 9.6 MB (9629450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f4b2df8638dae157f53da71da26e377bb1d2f4d99cd355f7f906bca2f48c1`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634b3e9b2aa7f6500b26fc5705d7153abba5966f1d052a9125d85bcb917e91f5`  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b97bf6e2b56384e1f1fc573163b1908172cb476a538e6bfc9ffe784a679bfde`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:031207cae7590e9bf888427eeb0a07bf194dd73708bc727f6e9cde8b904db72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.8 KB (976838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1500dd0b96d22a47b222742642f7aa6cc6da0748366e60c42e854804b84582`

```dockerfile
```

-	Layers:
	-	`sha256:e325a002bcd4d4c25a459aa84b41cad23d135795b9053ea23bdca9fbdda56a8a`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 962.0 KB (961985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a7a7190a30fee7904cbe99d8c9059425326504ce2d1e6c3a2a620adf1daba2`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-debian-1`

```console
$ docker pull fluentd@sha256:32b7fd76c3cd6d5bfda5a51a16b184b3920aed16cba0a80a2c3ba75311ea095c
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
$ docker pull fluentd@sha256:ac59892a58d3f3eed596214e253fa44c7dda696657e629154083c6a4ec6b9fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0eef2605e81d78c6e842ca518a508ef29d4fbeee1fbfba32593a7d011be1e2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6192766bba5c3464689794dd8795a413e7faa5070ebda6b1758995794f7ce2`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 13.7 MB (13670848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65b87ea982cfdb7796b311117e8d63e47322d8d0f90a9e974623f2fc11dc8e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b11361083bd06be74efb93cfaee92caca7f9a4e60fbe9c951dea9f9bf4f5e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 36.3 MB (36269137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db821620208c36c4857340805266208dc856ce52aa716ef809ecf0edfd8842e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c216769261c83e14558bd38c716d4f575362a0d564776af5b0560e8b23fb4a`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 5.1 MB (5139787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4508b995191c3adcaa82150cf93c499816c53ddd9eb5d00ff88ccea07e6c9`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed168431b9f559ff7472fa10ae251cf2f5e44c8431339e96e53ab57281e902a5`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd9fdcf7f0c674a766dcff0989d776cb078af761fda20539ab8985247cb4451`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f33c0834b6b5d261b81a1aeb83f5d4f9251c3d5fada2aca78c76aaa7011923c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6533c35cd642ddc940888c9cb56e6c3952953f41d44b94b75560648a3f2dc1`

```dockerfile
```

-	Layers:
	-	`sha256:2ac1d2ad90304db34ea37b32e67cdb6a8d5c8e1d636b9b81d2d5f11aa0145a05`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 2.6 MB (2575888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060dbf2741d53d33be82a9c67c972bd4f5fb463ca827a73316d238414237e68d`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3bbd4f7fde5f8556d6e295fb12e5ed27281d87e238f45df99178b013a67cf71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74490176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d42c830d493982ac07d3f4347ddb01303f2d793ef829535d35248c54d251f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c710cd50384381178d4a99b3fba9d2dfa69803556729285a1b50fd8deb12`  
		Last Modified: Wed, 25 Dec 2024 04:16:42 GMT  
		Size: 11.4 MB (11429897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dc8997201556ba03f5167cc7439004539824c7ac936f6fc0474c405d4bc997`  
		Last Modified: Wed, 25 Dec 2024 04:16:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b214593604478100cd665874141b1ad172f1d67397e2a60685aaef9bc432daa`  
		Last Modified: Wed, 25 Dec 2024 04:22:25 GMT  
		Size: 32.2 MB (32241968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a18dfcc4e105b009878324d3b5e5c829c8fa74d4600726658f68ddd462790`  
		Last Modified: Wed, 25 Dec 2024 04:22:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc66dfc3b0e993ad58493dbc28703bdd95f1dac57fb1c1051c1760cf1126bea`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 5.1 MB (5061015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefeb677b49dc31c216efc3be6a1065f45a9c4616d11c5195a8773f25852cef`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed3b177d0b3a875d0d2af93ca979ab316d770a7fe9c76c1ae8869634b77aed4`  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033b659d4d3ea681026df3d7ccd4fd2374ad7ed93d0e8adc62cea8de38face2`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9cf4cec5866c9917e921f62ff58c4ec98f069fc427c6219bde69b9497b3667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37297221133ea0dd781d6c64368982bd739bae813e5836fde702b7b2dd8bdab7`

```dockerfile
```

-	Layers:
	-	`sha256:bc80e9046bfdc845e8dbf44b143dbec5333f1a6ae0e8a90457943c3c3c06fb1e`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 2.6 MB (2579380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947b89242be771bacaaecea04f50c7f0ad9f14eac4cdf5e025f2bc093acbad2b`  
		Last Modified: Wed, 25 Dec 2024 06:31:51 GMT  
		Size: 20.3 KB (20326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:58233ab3bc751312bc3971b26986a0b46a7c0c37d14753449907faf741f309b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71717394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb69093cbfb72c04acd18127491de7e45394ba4fbe49d0a50ebabbf38e1d3f25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d05cb7c792ad963ab034afd2d15f759666da36de314b89fe00a60ccf1416c`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 10.8 MB (10766076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c75dc3e8dde657a75eb239ba3c01bb8fd67cd4c4edc2a7d4fa5b51badea60`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae61764a59ae0274f10a54b02df6b575a4b310e95e0fc9ddb756c26d2402ea0c`  
		Last Modified: Wed, 25 Dec 2024 12:27:52 GMT  
		Size: 32.1 MB (32082882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3a50097f6887ed6f64a61d1b54bb85dd938a22dfea772aa9fd51cfdda6bd5`  
		Last Modified: Wed, 25 Dec 2024 12:27:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e172e670936461cf551852e74835bc1e47dfe1402a54a77edbfd98ea8660c2`  
		Last Modified: Wed, 25 Dec 2024 16:35:14 GMT  
		Size: 4.9 MB (4932521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f495325a174a3e336d2741e3a252da6816ce04912080187fb9b26ec3459cbf`  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a21165534cb1c247153f6bf2f24db7da4c954835c682cabe827d566a2585c1`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be55141fb7d242e4f068d846ef8ab9e9723784b831a3a53a6ce8b7fa7a48b9d8`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:aee0764b162132d37db29c21073a0564dc2eb9553970e65720808c37ffa4e543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b00b6bcc68f96e93abb5c967d8f50048c0fcbf0f3055c7d677333e5dd6cd0`

```dockerfile
```

-	Layers:
	-	`sha256:ace32f8aa351e19f098913c0c9d509513752c39d7dcedb090775c1936aa3e5d7`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 2.6 MB (2578129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f744cf59079f314746a03e62f611a2cb08ce24b7171297a958f4f808627cf52b`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 20.3 KB (20325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b945204b34e5f6102c8b5d535f98416f1b932860c97da9f7dae097648fcd2227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81963469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf77ebe03a81292e701266fe19153717b4e2f0a42f1183e438656f2c03e207`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670f5d8e14300025cf13b44458e85c51bee541e9d990f1e8e30b6a3524c3059`  
		Size: 12.5 MB (12516720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423b11e942a877e3918d0adc5fb8b1fff467ed3585db43efdc3c1638f6db54f`  
		Last Modified: Wed, 25 Dec 2024 06:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff8aa22c0dae194cfd3bbebe2ea2a126863d846aeb0e3f5afb02506c17b9246`  
		Last Modified: Wed, 25 Dec 2024 06:28:09 GMT  
		Size: 36.3 MB (36251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f872efb343a3030f7cf3df15e4730ae7995e23546ec5c40e7d5d4b1edc400`  
		Last Modified: Wed, 25 Dec 2024 06:28:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e51225882ebe256daca074afedf324b8e43d5a2bef2a733768ee9c80cdd969`  
		Last Modified: Wed, 25 Dec 2024 10:56:55 GMT  
		Size: 5.1 MB (5133906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576364f0ec6df680f4c30c1dd2cb272b0e8cb919e0948312a14805aa0fdab75`  
		Last Modified: Wed, 08 Jan 2025 05:32:12 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c4fbac4d4126ba169c3bedb9c10b9dca9ef1555ee6faed89d4b6b63d49d82`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aeba3b787b194c12889a0fc504259afcc7dcada0faf06e56e385fa5b11517d`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ef0a395e2ef4ee848cb383d92d2354a32056cc1d4f0c091ca01d43e346d27cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7316dc3b6c4b4e9bb9f913658154bd84854a3ecabb72b93f8b30a2e785bc6a4`

```dockerfile
```

-	Layers:
	-	`sha256:d0146b5c2bea950035314ef9ffd96004c37e1787761ade648365932fc4adc3c3`  
		Last Modified: Wed, 25 Dec 2024 10:56:55 GMT  
		Size: 2.6 MB (2576133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8639ae836f9abc07826a9f6e6534389cd67645efd74aa883d349de07013d751`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 20.3 KB (20348 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:c0ebd73778a47ba11462ac9f563755411ed0a2040d93be8918d382a94a20c32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79635393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdd8b6d62b7a6797aa8cd9d7783a7b1d95ea4ef054045ef59bd8c74cb9aee26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10752e01b1d65ccc3fe4892885524c7253244c0d05700692c4963c312a828e0`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 13.2 MB (13224941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb2b027029d23a36df20aa6d33d9a01b2d9b6566babd2b308cd26838c6f9d83`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc1b90e59458c949ca171a23e501f88b96941019a9d47b40c362e44ad182f2`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 32.1 MB (32080992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5c988d253d80c0614a4fc3323c1601e309e6ac635bc20d599c6e110354a98`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34058678bc855a13625ea422dfe0b7322548606238bb959c9e4b90bd9c3d3e`  
		Last Modified: Tue, 24 Dec 2024 23:24:16 GMT  
		Size: 5.1 MB (5121681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db7639750b7d1d460e084f1b3b84bc74f236e7c4077d37a3ed2890b8aeee88`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f79b88a21a761d4f5f23b0ab640cb6cb771877711ff7652120cdc41141d833f`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a494c7f918ca1b7c8181a999beb32638ce03b39186541c179bfa2bf9b50769`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8744c1614927254b02e75ba771252e2919233cf72277ce3254d5212a39161aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639d147bd6b0782d06fbcf6a9b8bacb22dabf87423b167f59d5fc80a859df6c6`

```dockerfile
```

-	Layers:
	-	`sha256:978aa0f44c191b166a03974a064c9877b2bd2ea21a978c92867d40038d8f3273`  
		Size: 2.6 MB (2573012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7f88a6dbe422e4ba26fb94da92b1825a167354710ebb9207e1c7327e0ec6b5`  
		Size: 20.2 KB (20229 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:1d88060416ef6190378532ccf6b748e1a7208d6fea567581c443e63789a30afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85660698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5f97152937b86cdc800eaa59dbe3ec7b5abe84a98508f9d70ae91a4cfad33b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3ea8a05c45526233e9213e7f2425280f25b80169948122fa7cfe93cc27458`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 14.4 MB (14402509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb31ee5cbf5a52d5431decdea9b6a5f38d4f650ca23edb6a395971c6231dcf2a`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362979882e32b13f5e21c8d29cd4ce7cc9863c68c688e3496f7b36abf3f127f`  
		Last Modified: Wed, 25 Dec 2024 09:00:36 GMT  
		Size: 33.7 MB (33730252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb364227e0f85d5ca3fb62c8f4d0aee3fea245933199a2f18aaf271468d8dd`  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9700f947e1162b58a59e97ed9ad5f1c4899f5962c6c8ef8f56f9bd1fdc25f2b0`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 5.5 MB (5462306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4851394fcb707c13cd7b2f13781a717d0da8e0007ac03355ac5883cd04b40`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82fd279a5fab969211afbfdc8677e9d4076f0e4bd3bdd89ea09913716c44575`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f396e803d8f71fe2077f253e892d8b4eb76fda305e9c5402ac4ea29a470a1efd`  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0f1b95ace5fe35e9f3cb99c048da83b8ef8d13cd0307852a55310cb25776203a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27e7142dd55c81362adf7de0ce813eaa7d0806257472ba662df3913f7051139`

```dockerfile
```

-	Layers:
	-	`sha256:1e1709ada3e384ce07e0437edcae11ecefa18acfe84a34c2239619e97fb5baea`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 2.6 MB (2580236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8dcbf3e48ef54cda729b4ed0e29707391a40779d76e75da20f2cb88be675ac`  
		Last Modified: Wed, 25 Dec 2024 12:18:02 GMT  
		Size: 20.3 KB (20287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:ded7e725f40e112391cb6d80798e13d11fd7ff2aa74a92ed18a042ce35af5a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76915349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64c7b0557e95e365b31e65ac2e9519826f9dd4b51ac31a7e146e4827040b83`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50be06e5ebedc40968798c3d6b6a09d3c7011f3ca20978a6c6e2a8f05a089d9`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 11.8 MB (11848389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7e7bc1a175ba0bd702f8259a0ace929069093dfd095b7fb5d977eda015a26`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a466601d6790e51cdc4e1d4575bcda2544830e27bcde57beb05638455a65e6`  
		Last Modified: Wed, 25 Dec 2024 02:59:38 GMT  
		Size: 33.0 MB (33014423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390762e91aff3a4bb685f14354e6e1626a8a9f79c28023e83801823963a5444`  
		Last Modified: Wed, 25 Dec 2024 02:59:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0061d913f3953eece65b0d61610e008c16305d73efb9705914875e5c39e36e50`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 5.2 MB (5171244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b450bbbe0bbf4a1cdc82ae487fb2097a6a3c7b6c554efc33117b6579a9b8f6ed`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1da1e409287ee5c44d7ff0d2e2e38fedabaeb71020f4c3b680dbf002fafe5`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153626d0e2847b1801c00d04178f7220a0598a42a06546badb63c3447890618d`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:eff3ea514fdea921c4ce99b79f7b5ab6a1eae63a7a9bcdf5120e9d2b44877f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f5f9a4d0159fabe37ecd59b739dadb88a299b4927e345f37529f7ecd65b82`

```dockerfile
```

-	Layers:
	-	`sha256:03ce88d1681feb827446c0c5e0b6cc664b060153cd6d45f437e8d4d2f43f111e`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 2.6 MB (2575600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b34af974c5764dfc2bb2016ab973e7bbdf8009f8c90add0b181795446d7aac`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-1.0`

```console
$ docker pull fluentd@sha256:24a309c34863c4e97a8e890123fe936ef7779879f90d0e2b3165d61e98483d91
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
$ docker pull fluentd@sha256:4c0a5948bdec411ed6543d46d6896b75b23fdb26c779deb16facff0d5a165260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13486709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b6c77172c0473fd643200caa5c720f03277f583b27dcdb8a81b93dd4fdbb0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd378b01f03e6be712dcfcdb323317cca29acf1ba1e5cfcf4e51a34cd50d49`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 10.1 MB (10071273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aeb3ce22de6a9f47c7553fdb4ec0e782152ede465a8ec31d04870e1ebec4fc`  
		Last Modified: Tue, 07 Jan 2025 03:34:23 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c056cce2ddac76a24273a6be985fe440a9ddcbf652c9a04d7a42aa488fe4e9`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072211c40b59ec7b7c38df6453a207d8645dfe9a21362dce86fd4bbf7c84c2c`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ae7cde16897feb8f9913040d6e0f873a8173e0a11a9e0ca6378419dccb8701c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.8 KB (981752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d3f92390a910c14018c2ad6fde454bb5a0f5dc83a8c8ebedf7ebae7ff574`

```dockerfile
```

-	Layers:
	-	`sha256:940969d9a7406d40753c78203a1ff07ce91da381dcfd4a38efe7f13559bdaaf5`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 966.9 KB (966895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f51382362c1a792939fbcd7505f44969d3c0684f4a6e55fb358f260b83bbab9e`  
		Last Modified: Tue, 07 Jan 2025 03:34:24 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65c9e421ed2513049edf7712c00ec27014a49520c8e8dd0bfa98db48017f2256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12270882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894f9486c3539563d1f402091e22a2c21fedb0fde6567937193a981d4dadddec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
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
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58b9263897cc0e79ef4c6e654d14352ced6a609a760bec255f8f0a2b39e26`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 9.1 MB (9099087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5665918c386010085ebb738d6eb1e7378309c19c6137ed7f582cb5c94a9a1cc`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73443ffa09ef618036cffc98c38421d9ec3fad5a2a4e5d8c386d9cf54ae41e77`  
		Last Modified: Tue, 07 Jan 2025 18:12:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b046d755911d1c8d32e7545f94db43ea045030f91f6e80d997a90bf084352014`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b04b911c8c0e7aaadc86b94e844de8561ce28a1eab56eaff56807535d653901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3bfda6bc781b19a9ee3b2860418e953862c63d3743cdc508e1f34580df957`

```dockerfile
```

-	Layers:
	-	`sha256:4f7b656259434256f0c66a9af2f481098c68c784662073018d1879293387864f`  
		Last Modified: Tue, 07 Jan 2025 18:12:51 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:4276938d2b57b1444d9a9baf1845ed1c71e3f6290f52334f3d5d653c9fee1141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13546606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217f8030ec9be0ea182db5b089659ffba5d3a24636ef97e8af84a38089144059`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1eb4b6684518896815f538154ac77386d0f4e8a5e5a1db410bf766e81c6f1`  
		Last Modified: Tue, 07 Jan 2025 15:35:26 GMT  
		Size: 10.2 MB (10192491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9481ad8fa03c61d0f3f12a5aad626700181a57ab4f9253301a349c8829149e2`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf2598d98331c3efd2672d4adbdc5a071eb9c5deba1ef533d68325a715ed3a`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2616908a602bb3563d13154d1bf52965c3ae47732a2d164531906d3682d962c`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:01b4921e77406f889d0437125b71bdf5f805cf04641a193eb3c0d5c8699e28dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.0 KB (982001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac5ac88201f97ce5374ce04294cdf1b6c7168970276cc2c99b7e235fff87b1`

```dockerfile
```

-	Layers:
	-	`sha256:3cf4c4489f806262ce791a8d0d075723ec462c1cbe852a02a9de5f768adbdd57`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 967.0 KB (967037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d187a63c79ddb91a2e0179f2797fcea1fa99c3ab862784dcaf7657bb889bd1`  
		Last Modified: Tue, 07 Jan 2025 15:35:25 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:3b5c41740e127b2f7d11ece929062854204aa3d6fa9f18fd56be996e290be7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12579072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8bc33303f4a49f716042880ea26989704a7fb3f6eec1fa3854dacface2811`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-x86.tar.gz / # buildkit
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
	-	`sha256:ddad413607a62a4ff60ecbc53c13444783ab17a333628bcce0b2783b8aaea52a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.2 MB (3247827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ebd472c2c4b8c770ef6eebb5cbe24ce510939e072c5f9e54fa3fb8818280cc`  
		Size: 9.3 MB (9329077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7165958473bb23f17c1bcadd899abf68a02c4d2d3c29dbda0587f303f418f361`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429212592506ac6d80c94fc40441c2c47791db0d9c9a294d140516b2544ab19`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2268a222e0dbb04a424d5f4d2e6616909cf3e29903504a3cc4770426e7f6bea0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3529f1fa68c6e021001144d35ec781a3da00c91615ce1f2ff57c99aa415e066e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.6 KB (978642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7484e9ca5a6499c1f1cc83722a881ff38e4b4348bdba4db63635fd47601cbf`

```dockerfile
```

-	Layers:
	-	`sha256:5f0eb9912709e5e6237727b146db6c49cf2d482c306631e667484ed630ea335a`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 963.8 KB (963818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad97972a90445331ceba4e37ee3b6c3d2f4f1252859d36e39a8f984fe8a083d0`  
		Last Modified: Tue, 07 Jan 2025 03:31:35 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8d15fba21b09b17efb24a833ece5a662b154de8dc05073d952579644c84e2b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13217994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abdf903efa8b689278ac12c0253e6c38ed90ab1286a27ed2ddbb80973d9a9bb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:14bbc05bcc91b6abaa1bc3bf5f448fd6260254d09a572cb88c4a8b8b3eaba807`  
		Last Modified: Tue, 07 Jan 2025 02:32:41 GMT  
		Size: 3.4 MB (3362221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a33dfed01d5417a57d4f45cfbe928b58c88eec772bf26ac6e5b6a340464ba3`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 9.9 MB (9853607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a58106e64ea15d2ae20c1eea3281aee6cb3e91b09a3eb406579523c1d407a5`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75268cb14ad8a568e21378f40ce4ea09fb692dcd6aa489c70c60e7a7c8cc856d`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6094d9f76c3cf37404c3e1c5b117c681cc454a3abfaa93e95920d77c6bc23b50`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e31280462d48e1a92de6b71658bd72440fd001c50d05aa67c1400dbf5854461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.5 KB (977494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38bce77f83a6e6328655287ba5ddda0bdb5335c9ce63734f4eaba845480ffbe`

```dockerfile
```

-	Layers:
	-	`sha256:1e6cc067b49ca30756bb9fe2794b8880136938ab5392c453fcf0182581d3ddf1`  
		Last Modified: Tue, 07 Jan 2025 09:44:20 GMT  
		Size: 962.6 KB (962601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365d1ee83e9b66c8657c5396285020215532f2d7e13621e289ec5fa32667acc9`  
		Last Modified: Tue, 07 Jan 2025 09:44:19 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:7d04fe8d748f98b7f89a69cc5c50c98903dca36d41f88f04ef80be67c60e5ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12878929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8298105f2e4482e393f24f932643016f0c4be4eea2c72a1a5b64071496d534`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.5-s390x.tar.gz / # buildkit
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
	-	`sha256:c4672aa17160cbc8f6b41aa2f65cabe08127bf890ea6e72064b57e28d86daa7d`  
		Last Modified: Tue, 07 Jan 2025 02:33:22 GMT  
		Size: 3.2 MB (3247312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caad40faeab658b1492659aa8a77d262981dd0068cca18be7f90f410f5fa337`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 9.6 MB (9629450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f4b2df8638dae157f53da71da26e377bb1d2f4d99cd355f7f906bca2f48c1`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634b3e9b2aa7f6500b26fc5705d7153abba5966f1d052a9125d85bcb917e91f5`  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b97bf6e2b56384e1f1fc573163b1908172cb476a538e6bfc9ffe784a679bfde`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:031207cae7590e9bf888427eeb0a07bf194dd73708bc727f6e9cde8b904db72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.8 KB (976838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1500dd0b96d22a47b222742642f7aa6cc6da0748366e60c42e854804b84582`

```dockerfile
```

-	Layers:
	-	`sha256:e325a002bcd4d4c25a459aa84b41cad23d135795b9053ea23bdca9fbdda56a8a`  
		Last Modified: Tue, 07 Jan 2025 15:26:01 GMT  
		Size: 962.0 KB (961985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a7a7190a30fee7904cbe99d8c9059425326504ce2d1e6c3a2a620adf1daba2`  
		Last Modified: Tue, 07 Jan 2025 15:26:00 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-debian-1.0`

```console
$ docker pull fluentd@sha256:32b7fd76c3cd6d5bfda5a51a16b184b3920aed16cba0a80a2c3ba75311ea095c
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
$ docker pull fluentd@sha256:ac59892a58d3f3eed596214e253fa44c7dda696657e629154083c6a4ec6b9fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83313741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0eef2605e81d78c6e842ca518a508ef29d4fbeee1fbfba32593a7d011be1e2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6192766bba5c3464689794dd8795a413e7faa5070ebda6b1758995794f7ce2`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 13.7 MB (13670848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65b87ea982cfdb7796b311117e8d63e47322d8d0f90a9e974623f2fc11dc8e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b11361083bd06be74efb93cfaee92caca7f9a4e60fbe9c951dea9f9bf4f5e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 36.3 MB (36269137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db821620208c36c4857340805266208dc856ce52aa716ef809ecf0edfd8842e`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c216769261c83e14558bd38c716d4f575362a0d564776af5b0560e8b23fb4a`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 5.1 MB (5139787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4508b995191c3adcaa82150cf93c499816c53ddd9eb5d00ff88ccea07e6c9`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed168431b9f559ff7472fa10ae251cf2f5e44c8431339e96e53ab57281e902a5`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd9fdcf7f0c674a766dcff0989d776cb078af761fda20539ab8985247cb4451`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f33c0834b6b5d261b81a1aeb83f5d4f9251c3d5fada2aca78c76aaa7011923c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6533c35cd642ddc940888c9cb56e6c3952953f41d44b94b75560648a3f2dc1`

```dockerfile
```

-	Layers:
	-	`sha256:2ac1d2ad90304db34ea37b32e67cdb6a8d5c8e1d636b9b81d2d5f11aa0145a05`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 2.6 MB (2575888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060dbf2741d53d33be82a9c67c972bd4f5fb463ca827a73316d238414237e68d`  
		Last Modified: Tue, 24 Dec 2024 23:25:37 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3bbd4f7fde5f8556d6e295fb12e5ed27281d87e238f45df99178b013a67cf71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74490176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d42c830d493982ac07d3f4347ddb01303f2d793ef829535d35248c54d251f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c710cd50384381178d4a99b3fba9d2dfa69803556729285a1b50fd8deb12`  
		Last Modified: Wed, 25 Dec 2024 04:16:42 GMT  
		Size: 11.4 MB (11429897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dc8997201556ba03f5167cc7439004539824c7ac936f6fc0474c405d4bc997`  
		Last Modified: Wed, 25 Dec 2024 04:16:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b214593604478100cd665874141b1ad172f1d67397e2a60685aaef9bc432daa`  
		Last Modified: Wed, 25 Dec 2024 04:22:25 GMT  
		Size: 32.2 MB (32241968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a18dfcc4e105b009878324d3b5e5c829c8fa74d4600726658f68ddd462790`  
		Last Modified: Wed, 25 Dec 2024 04:22:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc66dfc3b0e993ad58493dbc28703bdd95f1dac57fb1c1051c1760cf1126bea`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 5.1 MB (5061015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefeb677b49dc31c216efc3be6a1065f45a9c4616d11c5195a8773f25852cef`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed3b177d0b3a875d0d2af93ca979ab316d770a7fe9c76c1ae8869634b77aed4`  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5033b659d4d3ea681026df3d7ccd4fd2374ad7ed93d0e8adc62cea8de38face2`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9cf4cec5866c9917e921f62ff58c4ec98f069fc427c6219bde69b9497b3667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37297221133ea0dd781d6c64368982bd739bae813e5836fde702b7b2dd8bdab7`

```dockerfile
```

-	Layers:
	-	`sha256:bc80e9046bfdc845e8dbf44b143dbec5333f1a6ae0e8a90457943c3c3c06fb1e`  
		Last Modified: Wed, 25 Dec 2024 06:31:52 GMT  
		Size: 2.6 MB (2579380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947b89242be771bacaaecea04f50c7f0ad9f14eac4cdf5e025f2bc093acbad2b`  
		Last Modified: Wed, 25 Dec 2024 06:31:51 GMT  
		Size: 20.3 KB (20326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:58233ab3bc751312bc3971b26986a0b46a7c0c37d14753449907faf741f309b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71717394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb69093cbfb72c04acd18127491de7e45394ba4fbe49d0a50ebabbf38e1d3f25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d05cb7c792ad963ab034afd2d15f759666da36de314b89fe00a60ccf1416c`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 10.8 MB (10766076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c75dc3e8dde657a75eb239ba3c01bb8fd67cd4c4edc2a7d4fa5b51badea60`  
		Last Modified: Wed, 25 Dec 2024 12:17:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae61764a59ae0274f10a54b02df6b575a4b310e95e0fc9ddb756c26d2402ea0c`  
		Last Modified: Wed, 25 Dec 2024 12:27:52 GMT  
		Size: 32.1 MB (32082882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3a50097f6887ed6f64a61d1b54bb85dd938a22dfea772aa9fd51cfdda6bd5`  
		Last Modified: Wed, 25 Dec 2024 12:27:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e172e670936461cf551852e74835bc1e47dfe1402a54a77edbfd98ea8660c2`  
		Last Modified: Wed, 25 Dec 2024 16:35:14 GMT  
		Size: 4.9 MB (4932521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f495325a174a3e336d2741e3a252da6816ce04912080187fb9b26ec3459cbf`  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a21165534cb1c247153f6bf2f24db7da4c954835c682cabe827d566a2585c1`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be55141fb7d242e4f068d846ef8ab9e9723784b831a3a53a6ce8b7fa7a48b9d8`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:aee0764b162132d37db29c21073a0564dc2eb9553970e65720808c37ffa4e543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b00b6bcc68f96e93abb5c967d8f50048c0fcbf0f3055c7d677333e5dd6cd0`

```dockerfile
```

-	Layers:
	-	`sha256:ace32f8aa351e19f098913c0c9d509513752c39d7dcedb090775c1936aa3e5d7`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 2.6 MB (2578129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f744cf59079f314746a03e62f611a2cb08ce24b7171297a958f4f808627cf52b`  
		Last Modified: Wed, 25 Dec 2024 16:35:13 GMT  
		Size: 20.3 KB (20325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b945204b34e5f6102c8b5d535f98416f1b932860c97da9f7dae097648fcd2227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81963469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf77ebe03a81292e701266fe19153717b4e2f0a42f1183e438656f2c03e207`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670f5d8e14300025cf13b44458e85c51bee541e9d990f1e8e30b6a3524c3059`  
		Size: 12.5 MB (12516720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423b11e942a877e3918d0adc5fb8b1fff467ed3585db43efdc3c1638f6db54f`  
		Last Modified: Wed, 25 Dec 2024 06:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff8aa22c0dae194cfd3bbebe2ea2a126863d846aeb0e3f5afb02506c17b9246`  
		Last Modified: Wed, 25 Dec 2024 06:28:09 GMT  
		Size: 36.3 MB (36251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f872efb343a3030f7cf3df15e4730ae7995e23546ec5c40e7d5d4b1edc400`  
		Last Modified: Wed, 25 Dec 2024 06:28:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e51225882ebe256daca074afedf324b8e43d5a2bef2a733768ee9c80cdd969`  
		Last Modified: Wed, 25 Dec 2024 10:56:55 GMT  
		Size: 5.1 MB (5133906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576364f0ec6df680f4c30c1dd2cb272b0e8cb919e0948312a14805aa0fdab75`  
		Last Modified: Wed, 08 Jan 2025 05:32:12 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c4fbac4d4126ba169c3bedb9c10b9dca9ef1555ee6faed89d4b6b63d49d82`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aeba3b787b194c12889a0fc504259afcc7dcada0faf06e56e385fa5b11517d`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ef0a395e2ef4ee848cb383d92d2354a32056cc1d4f0c091ca01d43e346d27cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7316dc3b6c4b4e9bb9f913658154bd84854a3ecabb72b93f8b30a2e785bc6a4`

```dockerfile
```

-	Layers:
	-	`sha256:d0146b5c2bea950035314ef9ffd96004c37e1787761ade648365932fc4adc3c3`  
		Last Modified: Wed, 25 Dec 2024 10:56:55 GMT  
		Size: 2.6 MB (2576133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8639ae836f9abc07826a9f6e6534389cd67645efd74aa883d349de07013d751`  
		Last Modified: Wed, 25 Dec 2024 10:56:54 GMT  
		Size: 20.3 KB (20348 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c0ebd73778a47ba11462ac9f563755411ed0a2040d93be8918d382a94a20c32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79635393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdd8b6d62b7a6797aa8cd9d7783a7b1d95ea4ef054045ef59bd8c74cb9aee26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10752e01b1d65ccc3fe4892885524c7253244c0d05700692c4963c312a828e0`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 13.2 MB (13224941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb2b027029d23a36df20aa6d33d9a01b2d9b6566babd2b308cd26838c6f9d83`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc1b90e59458c949ca171a23e501f88b96941019a9d47b40c362e44ad182f2`  
		Last Modified: Tue, 24 Dec 2024 22:32:58 GMT  
		Size: 32.1 MB (32080992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5c988d253d80c0614a4fc3323c1601e309e6ac635bc20d599c6e110354a98`  
		Last Modified: Tue, 24 Dec 2024 22:32:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d34058678bc855a13625ea422dfe0b7322548606238bb959c9e4b90bd9c3d3e`  
		Last Modified: Tue, 24 Dec 2024 23:24:16 GMT  
		Size: 5.1 MB (5121681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db7639750b7d1d460e084f1b3b84bc74f236e7c4077d37a3ed2890b8aeee88`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f79b88a21a761d4f5f23b0ab640cb6cb771877711ff7652120cdc41141d833f`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a494c7f918ca1b7c8181a999beb32638ce03b39186541c179bfa2bf9b50769`  
		Last Modified: Tue, 24 Dec 2024 23:24:15 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8744c1614927254b02e75ba771252e2919233cf72277ce3254d5212a39161aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639d147bd6b0782d06fbcf6a9b8bacb22dabf87423b167f59d5fc80a859df6c6`

```dockerfile
```

-	Layers:
	-	`sha256:978aa0f44c191b166a03974a064c9877b2bd2ea21a978c92867d40038d8f3273`  
		Size: 2.6 MB (2573012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7f88a6dbe422e4ba26fb94da92b1825a167354710ebb9207e1c7327e0ec6b5`  
		Size: 20.2 KB (20229 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:1d88060416ef6190378532ccf6b748e1a7208d6fea567581c443e63789a30afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85660698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5f97152937b86cdc800eaa59dbe3ec7b5abe84a98508f9d70ae91a4cfad33b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3ea8a05c45526233e9213e7f2425280f25b80169948122fa7cfe93cc27458`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 14.4 MB (14402509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb31ee5cbf5a52d5431decdea9b6a5f38d4f650ca23edb6a395971c6231dcf2a`  
		Last Modified: Wed, 25 Dec 2024 08:52:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362979882e32b13f5e21c8d29cd4ce7cc9863c68c688e3496f7b36abf3f127f`  
		Last Modified: Wed, 25 Dec 2024 09:00:36 GMT  
		Size: 33.7 MB (33730252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb364227e0f85d5ca3fb62c8f4d0aee3fea245933199a2f18aaf271468d8dd`  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9700f947e1162b58a59e97ed9ad5f1c4899f5962c6c8ef8f56f9bd1fdc25f2b0`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 5.5 MB (5462306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4851394fcb707c13cd7b2f13781a717d0da8e0007ac03355ac5883cd04b40`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82fd279a5fab969211afbfdc8677e9d4076f0e4bd3bdd89ea09913716c44575`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f396e803d8f71fe2077f253e892d8b4eb76fda305e9c5402ac4ea29a470a1efd`  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0f1b95ace5fe35e9f3cb99c048da83b8ef8d13cd0307852a55310cb25776203a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27e7142dd55c81362adf7de0ce813eaa7d0806257472ba662df3913f7051139`

```dockerfile
```

-	Layers:
	-	`sha256:1e1709ada3e384ce07e0437edcae11ecefa18acfe84a34c2239619e97fb5baea`  
		Last Modified: Wed, 25 Dec 2024 12:18:03 GMT  
		Size: 2.6 MB (2580236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8dcbf3e48ef54cda729b4ed0e29707391a40779d76e75da20f2cb88be675ac`  
		Last Modified: Wed, 25 Dec 2024 12:18:02 GMT  
		Size: 20.3 KB (20287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:ded7e725f40e112391cb6d80798e13d11fd7ff2aa74a92ed18a042ce35af5a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76915349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64c7b0557e95e365b31e65ac2e9519826f9dd4b51ac31a7e146e4827040b83`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 02 Dec 2024 04:34:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50be06e5ebedc40968798c3d6b6a09d3c7011f3ca20978a6c6e2a8f05a089d9`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 11.8 MB (11848389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7e7bc1a175ba0bd702f8259a0ace929069093dfd095b7fb5d977eda015a26`  
		Last Modified: Wed, 25 Dec 2024 02:53:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a466601d6790e51cdc4e1d4575bcda2544830e27bcde57beb05638455a65e6`  
		Last Modified: Wed, 25 Dec 2024 02:59:38 GMT  
		Size: 33.0 MB (33014423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390762e91aff3a4bb685f14354e6e1626a8a9f79c28023e83801823963a5444`  
		Last Modified: Wed, 25 Dec 2024 02:59:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0061d913f3953eece65b0d61610e008c16305d73efb9705914875e5c39e36e50`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 5.2 MB (5171244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b450bbbe0bbf4a1cdc82ae487fb2097a6a3c7b6c554efc33117b6579a9b8f6ed`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1da1e409287ee5c44d7ff0d2e2e38fedabaeb71020f4c3b680dbf002fafe5`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153626d0e2847b1801c00d04178f7220a0598a42a06546badb63c3447890618d`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:eff3ea514fdea921c4ce99b79f7b5ab6a1eae63a7a9bcdf5120e9d2b44877f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f5f9a4d0159fabe37ecd59b739dadb88a299b4927e345f37529f7ecd65b82`

```dockerfile
```

-	Layers:
	-	`sha256:03ce88d1681feb827446c0c5e0b6cc664b060153cd6d45f437e8d4d2f43f111e`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 2.6 MB (2575600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b34af974c5764dfc2bb2016ab973e7bbdf8009f8c90add0b181795446d7aac`  
		Last Modified: Wed, 25 Dec 2024 05:25:48 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json
