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
$ docker pull fluentd@sha256:f2e00db9337b6cafd900baefa80d7dc92f7869c9efb9967ace7054fcda60769c
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
$ docker pull fluentd@sha256:1cfeefc63742d9c1e4a0a81bd06c59ac515625e9216bda498d3cbb81ffe5bea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13503116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6726f799691ee19fb45ea27834423e4e9ba5975f3aadd1105eb2206eac2ca730`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88184bdf313262fd2b997ef59a4038d2972f7677bd41e74a4e67e8d30a9f0a`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 10.1 MB (10080707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac64fa66df6e55e2c851cebc50b387f2deac85c2c3f43249487d15c3a777d`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e21b2856c0b6deca9cd7a6ad5dd6eef86bba047016e64a7e2f9814426430b`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc8e49be5aadbe64c8791612a4309696c03c5da139b55fa2f272e6ba98170be`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ef10734f2f1bf9e4e3fca546feb000532c083ec8ec17107db6d15f9243ecd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9c02f1f401c793a3f5e3cc3579b2375936adca4e8f2a524a575a984a4f91fd`

```dockerfile
```

-	Layers:
	-	`sha256:46ffc5122367ac0020f0e1431e2981aa74ea007a16cc57d575a7ade622484e46`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 972.8 KB (972773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf961a846aa828aa17a9eb140c86565feae755052fb2073c6b3d4f86a60cf97f`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:a6edff4227f751a9f6f6d852848b6dcc9fe2b26c9453d38cf83b8040f72aa361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12293968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e774d5a6378801d8ab21db43de16242daede5314be554580a0500582197111f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
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
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1f6328a98409ef7ebdb673a31904f1733fe61a8606be8982970e7d8d8395b`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 9.1 MB (9114798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e6410b03f444c7fb5ffcb5964bc54cfb810a5604717495e1282cd677d2393`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f555b28a58800c180f5aed2d1dbafed5d9077c34b3960486c78b2aca8e5c32`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14dc540a2af8278d681f92d131d33eaf3403587630310486f7a1d9979313a3`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7739f7dc8dc341d9de7bd9d0cd73c05ce5aaaecced57869065ec09751e204cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a096ea30107a537393046263deb7a8e5894f1a38f13f155bc9e968e2730df1`

```dockerfile
```

-	Layers:
	-	`sha256:72a7f2b6b11131276d268b128eb06e6429da4a7eb23d8179876b1c0dbbd44887`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:508fe22601e35eb968eb6fcff8191e4ba2f527ba6df563302ce66f6b3a8e04ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13572944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45b99119b157c2fa1d13773f64320c1576f9255cb257b0b7fe31bb5c5f60d48`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a667ca550d5c342aef10ed2642c61d3f25e721bcf025d041c2985912f17ca63b`  
		Last Modified: Thu, 09 Jan 2025 06:07:42 GMT  
		Size: 10.2 MB (10210246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6868acfd0a2f6827fe612eb47cbc113f32f60001154c030e25bdeb792ed800a2`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b5723c118daaca704e83bbe2e9656bd030da6c8881c6bc63c39c42d87aa83`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff45b09b039e321c1809dbf2117718875281c958eec3fd2a912bd93c105aa8ac`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5634332cc476eff85acaf61f2982edd45dc03a385ef62434e355ed2f6d6b300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417aee84378ab0adbc360e0ab0ca8bce4b2789d13a566164c9b481ebe2de14a4`

```dockerfile
```

-	Layers:
	-	`sha256:71d441fb47540e96c217565ce9b91057e89eb2de76614b088c6a93e89a38b5d3`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 972.9 KB (972915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a310b33534948985d9da53b6bc63e8bb85f0b249a88ae08677e59a5518bc856`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:30a69b73619b02f1569dd23ca4aae6e3feeddac07beeb1af2a916b2b21819944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12604962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffd2f89238e4db7386065072ac31741e899e852e5b974d94da70bd0226a8142`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5185764e58ad06e32da6014fb124dbfdceec809e4039bcc4bd2eca81f8bc23a0`  
		Last Modified: Wed, 08 Jan 2025 18:14:19 GMT  
		Size: 9.3 MB (9348500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd62b18440c9a9eb21772cffabfc56219c5491fb1408bb48a7470ddf29d58bd6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0d601bbff4a60b06bfd718cfdf0b3a8773f1d499e1ee92e5f3ae521f512e7`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476c493b073fba36a24b750ecb784d9ac9593c05b72ee8e6cfeeaa4e5c6d1f3`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:905aaf9db86a1ae5f5f5b27b263d946ca426b178dc4c72dee1e5d591d63e8dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3fd24f9b6a35a9ebc4a91ec2956d643d93182494390ca42232ea3023e2c396`

```dockerfile
```

-	Layers:
	-	`sha256:69177ae6cba5a8318d81e6918989493903af8d2d08ef21219fcdbf685ec955d6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 969.7 KB (969696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3853612e064f202dfe95db7c07b145cb06ba9769e588f5289e06b5b3683ca40b`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2e0eec460a136adf9a6f8aa0369a75bd5ed8331772ffa0fa6e67927aff52c3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13236866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747910d8da73a8a53b54c8cb20cdcae6e5a9a30421593c93a3561b2b5afa752`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ea284016ffcc6a262a497ef4345323d63916db72b1a956f4b2c920120dac12`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 9.9 MB (9869053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5816e0c3bc37f90ea4ed3c1503eb186e3f9395a9f5594cd52fb1a098810f19`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8f63e9a01c37db6303087f6db77a0009f51b9eb55006327ed898a6b015117b`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703b0333c72cad50aca36fcb074517778263f09c3776cdbcd41b65b867384aa`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:9245091845e8a2f6b9454afafc0c754fa90e966a5e94daa1b5851fa46f53ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc0a260581f1c348ba478eeff05775c89bfa90f6fb92a66482245ee516c244`

```dockerfile
```

-	Layers:
	-	`sha256:e1343a6c5ff192e4765a75235d9ada61e87d1f8b6dc3166cb2fff781d9bcacfb`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 968.5 KB (968479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65da8b0bb3bc52944a98b8bf05b31131291f25c3f65255247cf000f91022ea3`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:481699bea13ddaf0bd8e459f1178be92b522f9f123b7bb87463bf2fbeda31ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12897163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095aab6a9f3bb8165dfc0bd4eeeb214f38134f6adb69cd907914461ba86f6613`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36793eda614f3800d8dee66d2397436ab110199dd50deb50f2729d40f2c6da68`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 9.6 MB (9640744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f8ebbc4596a65c46b18e9e93f0ad21cad5abe0e1ce35eb5464c9186f4decce`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aac62a48a860c337b0cceb55c7628552ae6daade7af6616eb92192368717b91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97491580908b3ca7e161ef90a8a9c70f11e086b0b7bb7176262a63dff68550`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:dfb3a2a35fad837e6c243c203a1d99d4c7d12c6d080d664c82242fe0899339f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67faa80a717af387624f796e4488daa141be37dc94c86d4bde786b362bc9896`

```dockerfile
```

-	Layers:
	-	`sha256:915e83825c99fe30464f9b5a97a57e80101160ee4361ca173776e44a29eb3f91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 967.9 KB (967863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83c3ab7a15dce251c9ee2ccfa0eed20017b8c80dd6fb357ac6ecf87a5aa1206`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 14.9 KB (14852 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:1c3b4b63679975af222d97ec67ac6b18158b4ba93ec2d0dea1e072994eafd0bf
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
$ docker pull fluentd@sha256:b621aabd823150352155a8ff11be05a7ef265188502538da2ed4265500c9687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17518495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e16b27db9655ce9a83de6c81426713ac4f342b8bc67c8126ad5a2e604cf78bb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02c32a33ebbf311010cd7257962c604406ca46d9cbedf5725deae826bda3b6`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 14.1 MB (14096085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408f763fb18031d2f3eba7b900fcd96ccc641c0b7001cc157a2aae6ab270e80`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f7df84945fd956eab5b6a28aba274142d6ace116c8be24eb382e2ba9b140f4`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a14e180b0c07fb54a834dba878b09ad84201d17e345ca605964630b4b1a7a2`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:46c48caae66bd179326f6abb3f2e070f7287691aa174d9bb4683714f46a310bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.7 KB (985740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1716d2dfccf2bef10924d14ba5d4080095253709ec20e61c70aeae7ffb87588d`

```dockerfile
```

-	Layers:
	-	`sha256:45da4d20a1d075564c875d49db7f514d47adb45f285371b5cdb092357d8cfd8f`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 972.1 KB (972063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e8e871c18b067fe620111db24445c162d037bb4724c60c438e30ad0590e79a`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:468cd8c329a4c7a4ce6eea5404f33aa4eef927e6b711207cc2081f3115266e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16271041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79281c99cb69b11a3b574dc1ede9f1842de5f7b300378ac53cc7a492997ad1b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff4eab3232fc9a98f819544ad7809463189060fd3013661ee5a65987f30d26e`  
		Last Modified: Mon, 03 Feb 2025 22:27:51 GMT  
		Size: 13.1 MB (13091874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22002924c4d96bbda27181cc5b4c9ea9123accb15553d873ee968721248587d`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774f5225242b24fda7ef533f6001b33e786248b6e67b322dcc033b9cc6b16c9`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471aa05db4bd95456cf4e2bdcb2fab3464e3ef92380f13cff3694151468df666`  
		Last Modified: Mon, 03 Feb 2025 22:27:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:77bc8e0ba8b3359e000390fd7f09889a2f16b31e615810c39a99ee02bbb726c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac64f8f3d800e2a1a5bdabdd2b4823f3e2e9c8f773ddcd499c0cf17d2c5dd1a0`

```dockerfile
```

-	Layers:
	-	`sha256:179ea26d318d93d4fc39bc40793a2ef72bff3cb0812d9d26f1a946ccc728271d`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 13.5 KB (13532 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:db90955a6e69b308660f0b3ce15ff7102379b6c4d05ed40e4e60dc77987afbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17503689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b03b05d0dddb0281f6526a171553a614f195b6885eca5309584b8c18fb1cb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620933fc6d6dd5a4380cc640a9679c625d702d67caf857439c368b82b18be8`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 14.1 MB (14140997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716d15687cec53e91713a097aa9436081931300b54c5b0501eb11dd553764133`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aee685c537c0f1d3b825571dc7f9c82664b149c93aadd715576c842e8e1d400`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722b498299193f9a9ba81ce1e0ac2c03d92473c50365edbb5f9f29721b062458`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:01c932568dd05a986272a0e9651ef2737e660cabd732e0597de9f72f97b7e055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57441a40667e4b3689c30eba225fa0d0b81d150c92848a1a9f720273e470d0c5`

```dockerfile
```

-	Layers:
	-	`sha256:87f352d4bf88dbeb0ec1326c2589b52f24754b12445e0febde739d10f177a717`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 972.2 KB (972193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203a1dea36c579676679c88b9151332010a603fba92016e26ed0d05310147ad5`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:1a095795a5957b3fa06fa7b0e9c7333ff12254449a2e96ffb33a8f574eceff3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16481932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9bc3c953c501272d0ceadc49647d34503977bc3b64f26bd68e62370ec30a3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b98331f3f1b19ae3ed05f0045c0d6826736dde457ad28e38d9c631ad272c6c`  
		Last Modified: Mon, 03 Feb 2025 22:27:47 GMT  
		Size: 13.2 MB (13225472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd72345774c70fa21b988b8f8dd405c6a26e4454c16de87bd065d207f06957`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c9e1c0839afe409e534313a2c34faf07a4c023f9a8ab499c081c3b83cb900`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce00f12691c6b7beb5807422b311e80787c32cd8710b108659d28cef254f31`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:886977715dce9db6886d359642175c5a9d08ed61a7d706ae7d6f3ef834720cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaeed3e84263db724641904fe94169612dbd4a0f98ecb279f6184aba719c552`

```dockerfile
```

-	Layers:
	-	`sha256:cb13bc8c3ee1db3b8c2b5d48382a75446151c38c1f3a9f651ba2d6e6c993ebbb`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 969.0 KB (968991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55c254dc940462ac436eebc3777d13c199f394855701282507fbf053800b0ae`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 13.7 KB (13651 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8c27614478a5ae6e3d731a2a55788ced4baf561e63a4bb617110aeecb9d53f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17071238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e4ce458711b2eb096d761d2237084e997d927ab3912800eb542cfe9c0b5c51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da21706b8d0d36f8a6af9a69ef6e92bd41559f67759ef3db18e2d20875d7adf`  
		Last Modified: Mon, 03 Feb 2025 22:28:05 GMT  
		Size: 13.7 MB (13703423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b247113fb1d3d15747816470256860341b877cdaf7fa44a57b7122487dec276`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6044f59f8641adea4e936ab40bda77953a2adb1f3f864e15a745bc9f226c15f5`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d9d40a29a7c619abaca98bc9d5744757373c8525af5f7a0c8ea2a7286a8e4`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:99b3b00efcd9b61648bd00de15552593cc632a245489b28eac8cc1d3271b8979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683441e432805a2e609afd7ae318366dcb6e6677e1224ba24def9a01b3fc8c69`

```dockerfile
```

-	Layers:
	-	`sha256:6065e357c4bd3b8ad452e9cc4f83b84a398f3c3db0e214d52ed7b7bacb304a87`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 967.8 KB (967763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1d9c7a34716652687771f29d0461afd31ac8fd38906f6f274a6dc832db163c`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:cdc4f73879f7d28685a6777046d8f42a6dd5c1d4d32e78db47e96741efb33d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16923579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b03f7b1519d19d5af9bf068571ae57637a41e50e316d26662e2db5b08f0663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7008e312899e3a6dd2c8bfa5e958b5f0b02280df303b7694f3adc80993b84b`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 13.7 MB (13667162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2196e45d90121f35554a6b51495abd2c5a4b82e438a9ee8931293a1d1c4ad588`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b781d0338eff0ec98085174f2f2095ccd881f7905a83ea536175ea17b392d4`  
		Last Modified: Mon, 03 Feb 2025 22:27:55 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810d5a967180f8b515b2a15c4629eeb9333ecf4749c72ce0c48011aa2cea188`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cbc204caedc2ac9881ea2ab89d2d0e6ee23a2228e1f7a1f21bdd5b82e863aaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b223232e7bfa119a393c39a80af4b7012e6fc7376fe51bea4d028fe574aa6424`

```dockerfile
```

-	Layers:
	-	`sha256:7b5d7b77a9ee9344a1b5ed91252624bce032faacbcbe5479192c7ecf5ed7a894`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 967.2 KB (967153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7323478b29e37b83e552f116eb2ddffdbffaeca3af8c2a2ad736df7d260e4e60`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:d7e26fcf82feae844b8fe4bb2d95f265214be4a8baf66e67c39207547002a06a
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
$ docker pull fluentd@sha256:461c551830ea72fd1870ec4166691a4ef240bb76909f18cd9ac5233665d049af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92156609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea52e6f1918be968ee5c5050d34b12a03d5b6af685fd6924a2655458d3c328a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331c02dcb1fc995541b31ae50dd3a8926876f241eec5b9727179749e8cfdf80`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 3.5 MB (3499361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c353cd4c9298737bd1cef91fe0bddd0af2bcb03fc4926f516c135d3dee33a`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7078735eadfd37aa4f14ef8aec511066ac5d2ba47122695509e7ae36be719`  
		Last Modified: Tue, 04 Feb 2025 04:50:28 GMT  
		Size: 46.2 MB (46231484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad7bdb63007ebe60c30d983e0bd82d62e192786a6d508a9c073e846453da05`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891f38f87256eff75d06254c1f8e97b17108c3bad8f53cd5d78332654533eda4`  
		Last Modified: Tue, 04 Feb 2025 05:30:26 GMT  
		Size: 14.2 MB (14211071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0bcfc919d5b937cef68b7ac618cea9f9e9b1490d0358068576732970123768`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd6aeb946b49cfeda06d1774fa88151b589a82519e2431f4922cd9cfba0b51`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60325860cb77ebc4c852557a676bc5e53cd3f5f9fda54a4f22e6f1849eb5e5`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fe647e92c4bfd821cef7bf23bb1269e88534a850b07f157f51cbd8b2b174ffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed7bfefd78f4dcd475e179e8618a41cade5d7d77d1461228ce3df19cdff8cf`

```dockerfile
```

-	Layers:
	-	`sha256:7d6e0a9437a4add078fae41c055da644609652720a11755e9534d9b199308940`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 2.6 MB (2572052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d20348905baa332d5c13be27931180acfc2e59e6a1dc9882c8d36f015279f24`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c280034f011991378d7118bb409fc123a7da1522eb78efebad2dd0ed7ed6dccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83793461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904111386369f10dd83ef1f51db932bb42d39b675883c774f343964c62d5c2f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d934325bc4b023af5c986fb28122fdea2b662a8442d611b55b0afdcbf5d099`  
		Last Modified: Tue, 04 Feb 2025 09:48:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81cc1dbccf5ce79eae01f7c07bf23a032af1a6cee42e6246d3b1ac2b1c956f`  
		Last Modified: Tue, 04 Feb 2025 09:54:40 GMT  
		Size: 40.8 MB (40779941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2106cd75253171c2bd9a0f4195f303151f08780cabb37a7e11867e74dd0fbc`  
		Last Modified: Tue, 04 Feb 2025 09:54:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f5a92d41c5c0169851f0c4a99517b53a5684056f5691864c10386af2ccab6`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 14.2 MB (14201160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a18f7c61b891c6169fc598c9bc734405ac5e9afc445c84aed36aba5c74180`  
		Last Modified: Tue, 04 Feb 2025 11:51:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1333af2de1ead57247c1ca8fcffbae2b41db875dd48e97f72f59a39ddc335da`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed79ab427a8c7185cfcb00a76d7bbf769e20d9d32f7c2148f67dd536a3ec4a3b`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6fd21dda2cc0c5f25f09adf39cd060b02f0faf0f019cc747a53d9e8cc8977eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6dc81909102313815bcee94b2afabe137693d11454ca8f8a6925866a4596c4`

```dockerfile
```

-	Layers:
	-	`sha256:44d03c62228e74089786c2aa3d82f29abd7089aab13079fe5384ca732e507103`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 2.6 MB (2575544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e88f3da590da21cde4726a4aa417dfc317c13c404a57d5c958b2acf17dfd964`  
		Last Modified: Tue, 04 Feb 2025 11:51:44 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:7e11c925db033c314151a8ef6d977ac5fe744500c776b4ba03ebb95b0ec47a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81060220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e9a157688f7cfc4fb83596acf898a9815f271cbba2972943a093046a783360`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e150ebe0715d085b568881fb745ae6852a33486175a85cd10e8aef763bbe2`  
		Last Modified: Tue, 14 Jan 2025 14:57:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f681e7a3a3a77ea47826710f8eedd797b7bf23e06b51cf04fb1effe23f44ac3`  
		Last Modified: Wed, 15 Jan 2025 20:08:27 GMT  
		Size: 40.1 MB (40116930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec815d6fab44349a0eddc67b01f43007eec296cbc39341305d2edc801eaba2`  
		Last Modified: Wed, 15 Jan 2025 20:08:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188a1993f9ae05356f9aad126d6994009108f005d8a64c67ae987f2406b1d7f`  
		Last Modified: Mon, 03 Feb 2025 22:30:03 GMT  
		Size: 14.1 MB (14118505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5eb47ecfa921d1dc456dbbbf0f41d411c5ce9eb26ffbde2be8b114ea821256`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a8442c8352e145b8b62c2ac7750d2b0132b1dc24abd684569d8989882d58f`  
		Last Modified: Mon, 03 Feb 2025 22:30:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ae1bb5e5aa6084e7dda81323fe324fc132f59130e4246e58c9cbfff55af1e`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:eccb3c2f7f74ed72408b43a85c89055cce4b26e3a6a57be75e6ead1aa59aedca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8315291ab5d18f0f4b0c19d4d09bf1e5f0efd114085c14e7048f7699ca2babde`

```dockerfile
```

-	Layers:
	-	`sha256:30f925928027569493bf32092e27ff8431fbd58db93e9c3ac535dbbcffca5c93`  
		Last Modified: Mon, 03 Feb 2025 22:30:02 GMT  
		Size: 2.6 MB (2574293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c05e47c3de226232adebcca9ba2aaf9a4c3fa94722a344f60005467eb124b77e`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:476022d29ec794e114a6c6d527b3c9e7aaee4e57620919393a22d09eedb4e6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90753547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb713c8cfca9e9749bed3ee258ec6361e2404927d58f1373346e6dcdb0ade10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58416046741782581ba6b478f57f74691b94b4bba6e177c08cb5755d52f7ee38`  
		Last Modified: Tue, 14 Jan 2025 11:27:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383ed55caee07787faa4ec3c9f8a015d187e2e41c38f2e998e1b7c6fe4b05c98`  
		Last Modified: Wed, 15 Jan 2025 20:05:53 GMT  
		Size: 45.2 MB (45172241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba58f57af5993bf899a32367d58eae51512f86b69f531888c98be4e3f3bf131`  
		Last Modified: Wed, 15 Jan 2025 20:05:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdff73295bae40beb474049790d2688e0b7f0562272c605b97c7edd4c813bc8`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 14.2 MB (14215002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1abec911a955cce09c9e7c80bee9a99ed5e4e10dd863e9a3578e8b9616c83c6`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f116f63da49eec930407a32098577cfed77cdc2a00ed4d31770e7239009456ca`  
		Last Modified: Mon, 03 Feb 2025 22:33:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09303825d43ee1a1adcc1d9877ce8b74b07b93875fc6fc00127d00445a5a6fd0`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ac542439ac488d0d5f6080567f7fbb7e2aeddaaa643479864c84b3e1d975bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98106161d03b75e017fc4571d4b705ee5a3c3f4c35243f5c2c2ebf493fc441f5`

```dockerfile
```

-	Layers:
	-	`sha256:73e5e42157fbedafbf26288547bb822fd37f8986e35e65efbc22fa6e6da90d0a`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 2.6 MB (2572297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b611ba44cf537169dd993a586a548ec035438a6c3688894d09a6c9936ed8bb5a`  
		Last Modified: Mon, 03 Feb 2025 22:33:36 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:55c28a36e8be7acc95da5297a713c2bfd4462d5a08658a13d3dc3c031f6bbd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88678261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f3b6a0ca0b8d19ef7b56429cd96d9600bf64a79283921e1f9c77b5345d0e78`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b249856b2bd7df2e0f8ddb14f80a0d356420b051fbb64fb38e7607e063b09`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 3.5 MB (3503410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b99e72709696463474ec292f81f3437debe658e6d744f61627f640e2c4667`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e775bf0fa12d5d5a3a66e563c9d16d2127daf1c2927fa93e4e2a09d86647`  
		Last Modified: Tue, 04 Feb 2025 04:43:43 GMT  
		Size: 42.0 MB (41979266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddacabb7846af3bac7ac8761ea96e499a3a4498c44ccf1fd46e9c354c2e12e0`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93e6188f88edab6dce34c57ecda5365d2ec899dd2a400439a2f8880a887a519`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 14.0 MB (14005738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99737f311e913e99005f9a99a1407e805c9a9c83447a2108c85da1f95c527f`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767baacde2966acdaeff5f968193de636861b226eac2f6f836e4bc04b053acc`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1298e5704e9962e1bf5d27af2afe5c9f2e70d83445ebabd556a71aa2aee3c784`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:34a38440a7be33d9f7490ba8edbdfc5b86dedb3d3a22209d6e12484ec9328835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3444b629e5c5a45f959a488566acdb5f5138c530d90c8badf88538c0dd7b8874`

```dockerfile
```

-	Layers:
	-	`sha256:78f3b27061fdc4a6bc0e3e760690db3271a2e6d3865592edad8222a64f21b85f`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 2.6 MB (2569176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5bf6d617620f69062fc2f0d4d0a47b9fec75b937904310454f4ce4aead51ff`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 21.1 KB (21079 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f3b2dca5fd49c7a1bd0fcfbdb65687f9e9fe80d89dcaac9bcf1db333794fd09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94971869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c248c95aaa82f6bf7b535a85545e2d52c0655d5acce6e259d7c6211433230304`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea4eff7192e8ce52808fb6ab513ad38b48d6931a5571ba83fc8cb74d4f91ff7`  
		Last Modified: Tue, 14 Jan 2025 08:25:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b554468e854a3e4497eec7b1d7d6194a3410c61a276d1d9eb8e56fa14fe206f`  
		Last Modified: Wed, 15 Jan 2025 19:04:28 GMT  
		Size: 44.6 MB (44615901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae7abd9014ac00cdd55280d61b30695c62efe4d5cd02240e28507d7d0c53f`  
		Last Modified: Wed, 15 Jan 2025 19:04:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b638ed45f13f214f1482221e610cc236b40b57bf51ba47e94ff467ea88103`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 14.6 MB (14605814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe72ab5f8ef4318f34b0200a76de356c5304ade9e0b7e9835bf255ee3d53196e`  
		Last Modified: Mon, 03 Feb 2025 22:32:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a221258e2f85b71bb5f032b3dca84dbb611a30e0239c2c610e0a577e05c97c00`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bd98c52dc928e97888eda2da500c5df7f690538c55e9b15ac733d1761eb1ca`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ce70b22f8c958152e3be2b32eb6dad6efae6c18c2f81ae4300af16d797e194b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a56d38b83587b17b599aea154feb322f83a024338f1bdb432e0e236fb6573c`

```dockerfile
```

-	Layers:
	-	`sha256:b6cda368a8a52bb7381a1d86019ed4b107c12f43601b5fc225e6f137e67442ae`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 2.6 MB (2576400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82accb06b83d9ce09c42daf6e38f1cd544b7f00ec0a4e2abfff4f55951e252f`  
		Last Modified: Mon, 03 Feb 2025 22:32:41 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:201360c2c15409ae5bf0b0b281180da89b48aff297933c449f664d09a8eed3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86246877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a40a9edad4f56497f9dd85c00b59250d3f3d7b8ec9d3b8f0d35d3ea880686f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb53c00cc457fdc4bb929f08300df25e06e0b068a3dffb3addb1f41c092f5f4`  
		Last Modified: Tue, 04 Feb 2025 10:53:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fe1bc27e1e69c36aa54c5ff4280a4dfba37d4d962e1a2b5851105cd813366`  
		Last Modified: Tue, 04 Feb 2025 10:59:39 GMT  
		Size: 41.9 MB (41876003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0cc91519f097b09cac7bd36a749caec6b5d576b91ad7e173fa9d0e026e489`  
		Last Modified: Tue, 04 Feb 2025 10:59:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8247fc44136c4135d1cc4807453d7f186fbfab9d4807c67ffba32ea899d269b1`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 14.3 MB (14346492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b950db4d4e193bc857369a3c18af55d22782682ce80dcc8666857e8ef10cc`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41758f1d0ca8e53df68d031e3bad9ae0281c141397067fe31cc667a0641d945`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5052191e7c6ca1139f757d1616754ac387fe6b15e0c50cf2624138257738af71`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0fe3863a61c38aa768b609eb30bb5bbf83b565f7e619ffe67c1638f17cf81dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394a5f27da7f0f9fd0509fc9138c9ae735c8ae40ca0abc2f8dc33b4348d13fc3`

```dockerfile
```

-	Layers:
	-	`sha256:1978d89494002b2e3460a8ede8a4553c1e5b46fccc7d2d7b69410e5e48cbb2b0`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 2.6 MB (2571764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfe382b0a3f9d5a5a4c465118dd86a8c77a7732dba57d26d41d02b086b32e47`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.7-1.0`

```console
$ docker pull fluentd@sha256:1c3b4b63679975af222d97ec67ac6b18158b4ba93ec2d0dea1e072994eafd0bf
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
$ docker pull fluentd@sha256:b621aabd823150352155a8ff11be05a7ef265188502538da2ed4265500c9687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17518495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e16b27db9655ce9a83de6c81426713ac4f342b8bc67c8126ad5a2e604cf78bb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02c32a33ebbf311010cd7257962c604406ca46d9cbedf5725deae826bda3b6`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 14.1 MB (14096085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408f763fb18031d2f3eba7b900fcd96ccc641c0b7001cc157a2aae6ab270e80`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f7df84945fd956eab5b6a28aba274142d6ace116c8be24eb382e2ba9b140f4`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a14e180b0c07fb54a834dba878b09ad84201d17e345ca605964630b4b1a7a2`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:46c48caae66bd179326f6abb3f2e070f7287691aa174d9bb4683714f46a310bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.7 KB (985740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1716d2dfccf2bef10924d14ba5d4080095253709ec20e61c70aeae7ffb87588d`

```dockerfile
```

-	Layers:
	-	`sha256:45da4d20a1d075564c875d49db7f514d47adb45f285371b5cdb092357d8cfd8f`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 972.1 KB (972063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e8e871c18b067fe620111db24445c162d037bb4724c60c438e30ad0590e79a`  
		Last Modified: Mon, 03 Feb 2025 22:27:42 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:468cd8c329a4c7a4ce6eea5404f33aa4eef927e6b711207cc2081f3115266e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16271041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79281c99cb69b11a3b574dc1ede9f1842de5f7b300378ac53cc7a492997ad1b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff4eab3232fc9a98f819544ad7809463189060fd3013661ee5a65987f30d26e`  
		Last Modified: Mon, 03 Feb 2025 22:27:51 GMT  
		Size: 13.1 MB (13091874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22002924c4d96bbda27181cc5b4c9ea9123accb15553d873ee968721248587d`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774f5225242b24fda7ef533f6001b33e786248b6e67b322dcc033b9cc6b16c9`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471aa05db4bd95456cf4e2bdcb2fab3464e3ef92380f13cff3694151468df666`  
		Last Modified: Mon, 03 Feb 2025 22:27:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:77bc8e0ba8b3359e000390fd7f09889a2f16b31e615810c39a99ee02bbb726c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac64f8f3d800e2a1a5bdabdd2b4823f3e2e9c8f773ddcd499c0cf17d2c5dd1a0`

```dockerfile
```

-	Layers:
	-	`sha256:179ea26d318d93d4fc39bc40793a2ef72bff3cb0812d9d26f1a946ccc728271d`  
		Last Modified: Mon, 03 Feb 2025 22:27:50 GMT  
		Size: 13.5 KB (13532 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:db90955a6e69b308660f0b3ce15ff7102379b6c4d05ed40e4e60dc77987afbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17503689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b03b05d0dddb0281f6526a171553a614f195b6885eca5309584b8c18fb1cb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620933fc6d6dd5a4380cc640a9679c625d702d67caf857439c368b82b18be8`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 14.1 MB (14140997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716d15687cec53e91713a097aa9436081931300b54c5b0501eb11dd553764133`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aee685c537c0f1d3b825571dc7f9c82664b149c93aadd715576c842e8e1d400`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722b498299193f9a9ba81ce1e0ac2c03d92473c50365edbb5f9f29721b062458`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:01c932568dd05a986272a0e9651ef2737e660cabd732e0597de9f72f97b7e055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 KB (985965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57441a40667e4b3689c30eba225fa0d0b81d150c92848a1a9f720273e470d0c5`

```dockerfile
```

-	Layers:
	-	`sha256:87f352d4bf88dbeb0ec1326c2589b52f24754b12445e0febde739d10f177a717`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 972.2 KB (972193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203a1dea36c579676679c88b9151332010a603fba92016e26ed0d05310147ad5`  
		Last Modified: Mon, 03 Feb 2025 22:30:23 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:1a095795a5957b3fa06fa7b0e9c7333ff12254449a2e96ffb33a8f574eceff3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16481932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9bc3c953c501272d0ceadc49647d34503977bc3b64f26bd68e62370ec30a3c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b98331f3f1b19ae3ed05f0045c0d6826736dde457ad28e38d9c631ad272c6c`  
		Last Modified: Mon, 03 Feb 2025 22:27:47 GMT  
		Size: 13.2 MB (13225472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd72345774c70fa21b988b8f8dd405c6a26e4454c16de87bd065d207f06957`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c9e1c0839afe409e534313a2c34faf07a4c023f9a8ab499c081c3b83cb900`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce00f12691c6b7beb5807422b311e80787c32cd8710b108659d28cef254f31`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:886977715dce9db6886d359642175c5a9d08ed61a7d706ae7d6f3ef834720cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaeed3e84263db724641904fe94169612dbd4a0f98ecb279f6184aba719c552`

```dockerfile
```

-	Layers:
	-	`sha256:cb13bc8c3ee1db3b8c2b5d48382a75446151c38c1f3a9f651ba2d6e6c993ebbb`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 969.0 KB (968991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55c254dc940462ac436eebc3777d13c199f394855701282507fbf053800b0ae`  
		Last Modified: Mon, 03 Feb 2025 22:27:46 GMT  
		Size: 13.7 KB (13651 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8c27614478a5ae6e3d731a2a55788ced4baf561e63a4bb617110aeecb9d53f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17071238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e4ce458711b2eb096d761d2237084e997d927ab3912800eb542cfe9c0b5c51`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da21706b8d0d36f8a6af9a69ef6e92bd41559f67759ef3db18e2d20875d7adf`  
		Last Modified: Mon, 03 Feb 2025 22:28:05 GMT  
		Size: 13.7 MB (13703423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b247113fb1d3d15747816470256860341b877cdaf7fa44a57b7122487dec276`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6044f59f8641adea4e936ab40bda77953a2adb1f3f864e15a745bc9f226c15f5`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d9d40a29a7c619abaca98bc9d5744757373c8525af5f7a0c8ea2a7286a8e4`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:99b3b00efcd9b61648bd00de15552593cc632a245489b28eac8cc1d3271b8979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.5 KB (981474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683441e432805a2e609afd7ae318366dcb6e6677e1224ba24def9a01b3fc8c69`

```dockerfile
```

-	Layers:
	-	`sha256:6065e357c4bd3b8ad452e9cc4f83b84a398f3c3db0e214d52ed7b7bacb304a87`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 967.8 KB (967763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1d9c7a34716652687771f29d0461afd31ac8fd38906f6f274a6dc832db163c`  
		Last Modified: Mon, 03 Feb 2025 22:28:04 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:cdc4f73879f7d28685a6777046d8f42a6dd5c1d4d32e78db47e96741efb33d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16923579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b03f7b1519d19d5af9bf068571ae57637a41e50e316d26662e2db5b08f0663`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7008e312899e3a6dd2c8bfa5e958b5f0b02280df303b7694f3adc80993b84b`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 13.7 MB (13667162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2196e45d90121f35554a6b51495abd2c5a4b82e438a9ee8931293a1d1c4ad588`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b781d0338eff0ec98085174f2f2095ccd881f7905a83ea536175ea17b392d4`  
		Last Modified: Mon, 03 Feb 2025 22:27:55 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810d5a967180f8b515b2a15c4629eeb9333ecf4749c72ce0c48011aa2cea188`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cbc204caedc2ac9881ea2ab89d2d0e6ee23a2228e1f7a1f21bdd5b82e863aaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b223232e7bfa119a393c39a80af4b7012e6fc7376fe51bea4d028fe574aa6424`

```dockerfile
```

-	Layers:
	-	`sha256:7b5d7b77a9ee9344a1b5ed91252624bce032faacbcbe5479192c7ecf5ed7a894`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 967.2 KB (967153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7323478b29e37b83e552f116eb2ddffdbffaeca3af8c2a2ad736df7d260e4e60`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.7-debian-1.0`

```console
$ docker pull fluentd@sha256:d7e26fcf82feae844b8fe4bb2d95f265214be4a8baf66e67c39207547002a06a
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
$ docker pull fluentd@sha256:461c551830ea72fd1870ec4166691a4ef240bb76909f18cd9ac5233665d049af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92156609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea52e6f1918be968ee5c5050d34b12a03d5b6af685fd6924a2655458d3c328a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331c02dcb1fc995541b31ae50dd3a8926876f241eec5b9727179749e8cfdf80`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 3.5 MB (3499361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c353cd4c9298737bd1cef91fe0bddd0af2bcb03fc4926f516c135d3dee33a`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7078735eadfd37aa4f14ef8aec511066ac5d2ba47122695509e7ae36be719`  
		Last Modified: Tue, 04 Feb 2025 04:50:28 GMT  
		Size: 46.2 MB (46231484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad7bdb63007ebe60c30d983e0bd82d62e192786a6d508a9c073e846453da05`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891f38f87256eff75d06254c1f8e97b17108c3bad8f53cd5d78332654533eda4`  
		Last Modified: Tue, 04 Feb 2025 05:30:26 GMT  
		Size: 14.2 MB (14211071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0bcfc919d5b937cef68b7ac618cea9f9e9b1490d0358068576732970123768`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd6aeb946b49cfeda06d1774fa88151b589a82519e2431f4922cd9cfba0b51`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60325860cb77ebc4c852557a676bc5e53cd3f5f9fda54a4f22e6f1849eb5e5`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fe647e92c4bfd821cef7bf23bb1269e88534a850b07f157f51cbd8b2b174ffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed7bfefd78f4dcd475e179e8618a41cade5d7d77d1461228ce3df19cdff8cf`

```dockerfile
```

-	Layers:
	-	`sha256:7d6e0a9437a4add078fae41c055da644609652720a11755e9534d9b199308940`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 2.6 MB (2572052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d20348905baa332d5c13be27931180acfc2e59e6a1dc9882c8d36f015279f24`  
		Last Modified: Tue, 04 Feb 2025 05:30:25 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c280034f011991378d7118bb409fc123a7da1522eb78efebad2dd0ed7ed6dccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83793461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904111386369f10dd83ef1f51db932bb42d39b675883c774f343964c62d5c2f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d934325bc4b023af5c986fb28122fdea2b662a8442d611b55b0afdcbf5d099`  
		Last Modified: Tue, 04 Feb 2025 09:48:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81cc1dbccf5ce79eae01f7c07bf23a032af1a6cee42e6246d3b1ac2b1c956f`  
		Last Modified: Tue, 04 Feb 2025 09:54:40 GMT  
		Size: 40.8 MB (40779941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2106cd75253171c2bd9a0f4195f303151f08780cabb37a7e11867e74dd0fbc`  
		Last Modified: Tue, 04 Feb 2025 09:54:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877f5a92d41c5c0169851f0c4a99517b53a5684056f5691864c10386af2ccab6`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 14.2 MB (14201160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a18f7c61b891c6169fc598c9bc734405ac5e9afc445c84aed36aba5c74180`  
		Last Modified: Tue, 04 Feb 2025 11:51:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1333af2de1ead57247c1ca8fcffbae2b41db875dd48e97f72f59a39ddc335da`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed79ab427a8c7185cfcb00a76d7bbf769e20d9d32f7c2148f67dd536a3ec4a3b`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6fd21dda2cc0c5f25f09adf39cd060b02f0faf0f019cc747a53d9e8cc8977eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6dc81909102313815bcee94b2afabe137693d11454ca8f8a6925866a4596c4`

```dockerfile
```

-	Layers:
	-	`sha256:44d03c62228e74089786c2aa3d82f29abd7089aab13079fe5384ca732e507103`  
		Last Modified: Tue, 04 Feb 2025 11:51:45 GMT  
		Size: 2.6 MB (2575544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e88f3da590da21cde4726a4aa417dfc317c13c404a57d5c958b2acf17dfd964`  
		Last Modified: Tue, 04 Feb 2025 11:51:44 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:7e11c925db033c314151a8ef6d977ac5fe744500c776b4ba03ebb95b0ec47a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81060220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e9a157688f7cfc4fb83596acf898a9815f271cbba2972943a093046a783360`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e150ebe0715d085b568881fb745ae6852a33486175a85cd10e8aef763bbe2`  
		Last Modified: Tue, 14 Jan 2025 14:57:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f681e7a3a3a77ea47826710f8eedd797b7bf23e06b51cf04fb1effe23f44ac3`  
		Last Modified: Wed, 15 Jan 2025 20:08:27 GMT  
		Size: 40.1 MB (40116930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec815d6fab44349a0eddc67b01f43007eec296cbc39341305d2edc801eaba2`  
		Last Modified: Wed, 15 Jan 2025 20:08:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188a1993f9ae05356f9aad126d6994009108f005d8a64c67ae987f2406b1d7f`  
		Last Modified: Mon, 03 Feb 2025 22:30:03 GMT  
		Size: 14.1 MB (14118505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5eb47ecfa921d1dc456dbbbf0f41d411c5ce9eb26ffbde2be8b114ea821256`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a8442c8352e145b8b62c2ac7750d2b0132b1dc24abd684569d8989882d58f`  
		Last Modified: Mon, 03 Feb 2025 22:30:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ae1bb5e5aa6084e7dda81323fe324fc132f59130e4246e58c9cbfff55af1e`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:eccb3c2f7f74ed72408b43a85c89055cce4b26e3a6a57be75e6ead1aa59aedca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8315291ab5d18f0f4b0c19d4d09bf1e5f0efd114085c14e7048f7699ca2babde`

```dockerfile
```

-	Layers:
	-	`sha256:30f925928027569493bf32092e27ff8431fbd58db93e9c3ac535dbbcffca5c93`  
		Last Modified: Mon, 03 Feb 2025 22:30:02 GMT  
		Size: 2.6 MB (2574293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c05e47c3de226232adebcca9ba2aaf9a4c3fa94722a344f60005467eb124b77e`  
		Last Modified: Mon, 03 Feb 2025 22:30:01 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:476022d29ec794e114a6c6d527b3c9e7aaee4e57620919393a22d09eedb4e6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90753547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb713c8cfca9e9749bed3ee258ec6361e2404927d58f1373346e6dcdb0ade10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58416046741782581ba6b478f57f74691b94b4bba6e177c08cb5755d52f7ee38`  
		Last Modified: Tue, 14 Jan 2025 11:27:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383ed55caee07787faa4ec3c9f8a015d187e2e41c38f2e998e1b7c6fe4b05c98`  
		Last Modified: Wed, 15 Jan 2025 20:05:53 GMT  
		Size: 45.2 MB (45172241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba58f57af5993bf899a32367d58eae51512f86b69f531888c98be4e3f3bf131`  
		Last Modified: Wed, 15 Jan 2025 20:05:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdff73295bae40beb474049790d2688e0b7f0562272c605b97c7edd4c813bc8`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 14.2 MB (14215002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1abec911a955cce09c9e7c80bee9a99ed5e4e10dd863e9a3578e8b9616c83c6`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f116f63da49eec930407a32098577cfed77cdc2a00ed4d31770e7239009456ca`  
		Last Modified: Mon, 03 Feb 2025 22:33:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09303825d43ee1a1adcc1d9877ce8b74b07b93875fc6fc00127d00445a5a6fd0`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ac542439ac488d0d5f6080567f7fbb7e2aeddaaa643479864c84b3e1d975bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98106161d03b75e017fc4571d4b705ee5a3c3f4c35243f5c2c2ebf493fc441f5`

```dockerfile
```

-	Layers:
	-	`sha256:73e5e42157fbedafbf26288547bb822fd37f8986e35e65efbc22fa6e6da90d0a`  
		Last Modified: Mon, 03 Feb 2025 22:33:37 GMT  
		Size: 2.6 MB (2572297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b611ba44cf537169dd993a586a548ec035438a6c3688894d09a6c9936ed8bb5a`  
		Last Modified: Mon, 03 Feb 2025 22:33:36 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:55c28a36e8be7acc95da5297a713c2bfd4462d5a08658a13d3dc3c031f6bbd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88678261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f3b6a0ca0b8d19ef7b56429cd96d9600bf64a79283921e1f9c77b5345d0e78`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b249856b2bd7df2e0f8ddb14f80a0d356420b051fbb64fb38e7607e063b09`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 3.5 MB (3503410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b99e72709696463474ec292f81f3437debe658e6d744f61627f640e2c4667`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e775bf0fa12d5d5a3a66e563c9d16d2127daf1c2927fa93e4e2a09d86647`  
		Last Modified: Tue, 04 Feb 2025 04:43:43 GMT  
		Size: 42.0 MB (41979266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddacabb7846af3bac7ac8761ea96e499a3a4498c44ccf1fd46e9c354c2e12e0`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93e6188f88edab6dce34c57ecda5365d2ec899dd2a400439a2f8880a887a519`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 14.0 MB (14005738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99737f311e913e99005f9a99a1407e805c9a9c83447a2108c85da1f95c527f`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767baacde2966acdaeff5f968193de636861b226eac2f6f836e4bc04b053acc`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1298e5704e9962e1bf5d27af2afe5c9f2e70d83445ebabd556a71aa2aee3c784`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:34a38440a7be33d9f7490ba8edbdfc5b86dedb3d3a22209d6e12484ec9328835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3444b629e5c5a45f959a488566acdb5f5138c530d90c8badf88538c0dd7b8874`

```dockerfile
```

-	Layers:
	-	`sha256:78f3b27061fdc4a6bc0e3e760690db3271a2e6d3865592edad8222a64f21b85f`  
		Last Modified: Tue, 04 Feb 2025 05:25:51 GMT  
		Size: 2.6 MB (2569176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5bf6d617620f69062fc2f0d4d0a47b9fec75b937904310454f4ce4aead51ff`  
		Last Modified: Tue, 04 Feb 2025 05:25:50 GMT  
		Size: 21.1 KB (21079 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f3b2dca5fd49c7a1bd0fcfbdb65687f9e9fe80d89dcaac9bcf1db333794fd09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94971869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c248c95aaa82f6bf7b535a85545e2d52c0655d5acce6e259d7c6211433230304`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea4eff7192e8ce52808fb6ab513ad38b48d6931a5571ba83fc8cb74d4f91ff7`  
		Last Modified: Tue, 14 Jan 2025 08:25:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b554468e854a3e4497eec7b1d7d6194a3410c61a276d1d9eb8e56fa14fe206f`  
		Last Modified: Wed, 15 Jan 2025 19:04:28 GMT  
		Size: 44.6 MB (44615901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae7abd9014ac00cdd55280d61b30695c62efe4d5cd02240e28507d7d0c53f`  
		Last Modified: Wed, 15 Jan 2025 19:04:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496b638ed45f13f214f1482221e610cc236b40b57bf51ba47e94ff467ea88103`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 14.6 MB (14605814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe72ab5f8ef4318f34b0200a76de356c5304ade9e0b7e9835bf255ee3d53196e`  
		Last Modified: Mon, 03 Feb 2025 22:32:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a221258e2f85b71bb5f032b3dca84dbb611a30e0239c2c610e0a577e05c97c00`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bd98c52dc928e97888eda2da500c5df7f690538c55e9b15ac733d1761eb1ca`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ce70b22f8c958152e3be2b32eb6dad6efae6c18c2f81ae4300af16d797e194b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a56d38b83587b17b599aea154feb322f83a024338f1bdb432e0e236fb6573c`

```dockerfile
```

-	Layers:
	-	`sha256:b6cda368a8a52bb7381a1d86019ed4b107c12f43601b5fc225e6f137e67442ae`  
		Last Modified: Mon, 03 Feb 2025 22:32:42 GMT  
		Size: 2.6 MB (2576400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82accb06b83d9ce09c42daf6e38f1cd544b7f00ec0a4e2abfff4f55951e252f`  
		Last Modified: Mon, 03 Feb 2025 22:32:41 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.7-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:201360c2c15409ae5bf0b0b281180da89b48aff297933c449f664d09a8eed3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86246877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a40a9edad4f56497f9dd85c00b59250d3f3d7b8ec9d3b8f0d35d3ea880686f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 14 Jan 2025 19:28:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb53c00cc457fdc4bb929f08300df25e06e0b068a3dffb3addb1f41c092f5f4`  
		Last Modified: Tue, 04 Feb 2025 10:53:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fe1bc27e1e69c36aa54c5ff4280a4dfba37d4d962e1a2b5851105cd813366`  
		Last Modified: Tue, 04 Feb 2025 10:59:39 GMT  
		Size: 41.9 MB (41876003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0cc91519f097b09cac7bd36a749caec6b5d576b91ad7e173fa9d0e026e489`  
		Last Modified: Tue, 04 Feb 2025 10:59:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8247fc44136c4135d1cc4807453d7f186fbfab9d4807c67ffba32ea899d269b1`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 14.3 MB (14346492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b950db4d4e193bc857369a3c18af55d22782682ce80dcc8666857e8ef10cc`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41758f1d0ca8e53df68d031e3bad9ae0281c141397067fe31cc667a0641d945`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5052191e7c6ca1139f757d1616754ac387fe6b15e0c50cf2624138257738af71`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.7-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0fe3863a61c38aa768b609eb30bb5bbf83b565f7e619ffe67c1638f17cf81dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394a5f27da7f0f9fd0509fc9138c9ae735c8ae40ca0abc2f8dc33b4348d13fc3`

```dockerfile
```

-	Layers:
	-	`sha256:1978d89494002b2e3460a8ede8a4553c1e5b46fccc7d2d7b69410e5e48cbb2b0`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 2.6 MB (2571764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfe382b0a3f9d5a5a4c465118dd86a8c77a7732dba57d26d41d02b086b32e47`  
		Last Modified: Tue, 04 Feb 2025 18:20:40 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-1`

```console
$ docker pull fluentd@sha256:f2e00db9337b6cafd900baefa80d7dc92f7869c9efb9967ace7054fcda60769c
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
$ docker pull fluentd@sha256:1cfeefc63742d9c1e4a0a81bd06c59ac515625e9216bda498d3cbb81ffe5bea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13503116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6726f799691ee19fb45ea27834423e4e9ba5975f3aadd1105eb2206eac2ca730`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88184bdf313262fd2b997ef59a4038d2972f7677bd41e74a4e67e8d30a9f0a`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 10.1 MB (10080707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac64fa66df6e55e2c851cebc50b387f2deac85c2c3f43249487d15c3a777d`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e21b2856c0b6deca9cd7a6ad5dd6eef86bba047016e64a7e2f9814426430b`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc8e49be5aadbe64c8791612a4309696c03c5da139b55fa2f272e6ba98170be`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ef10734f2f1bf9e4e3fca546feb000532c083ec8ec17107db6d15f9243ecd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9c02f1f401c793a3f5e3cc3579b2375936adca4e8f2a524a575a984a4f91fd`

```dockerfile
```

-	Layers:
	-	`sha256:46ffc5122367ac0020f0e1431e2981aa74ea007a16cc57d575a7ade622484e46`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 972.8 KB (972773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf961a846aa828aa17a9eb140c86565feae755052fb2073c6b3d4f86a60cf97f`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:a6edff4227f751a9f6f6d852848b6dcc9fe2b26c9453d38cf83b8040f72aa361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12293968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e774d5a6378801d8ab21db43de16242daede5314be554580a0500582197111f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
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
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1f6328a98409ef7ebdb673a31904f1733fe61a8606be8982970e7d8d8395b`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 9.1 MB (9114798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e6410b03f444c7fb5ffcb5964bc54cfb810a5604717495e1282cd677d2393`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f555b28a58800c180f5aed2d1dbafed5d9077c34b3960486c78b2aca8e5c32`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14dc540a2af8278d681f92d131d33eaf3403587630310486f7a1d9979313a3`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7739f7dc8dc341d9de7bd9d0cd73c05ce5aaaecced57869065ec09751e204cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a096ea30107a537393046263deb7a8e5894f1a38f13f155bc9e968e2730df1`

```dockerfile
```

-	Layers:
	-	`sha256:72a7f2b6b11131276d268b128eb06e6429da4a7eb23d8179876b1c0dbbd44887`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:508fe22601e35eb968eb6fcff8191e4ba2f527ba6df563302ce66f6b3a8e04ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13572944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45b99119b157c2fa1d13773f64320c1576f9255cb257b0b7fe31bb5c5f60d48`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a667ca550d5c342aef10ed2642c61d3f25e721bcf025d041c2985912f17ca63b`  
		Last Modified: Thu, 09 Jan 2025 06:07:42 GMT  
		Size: 10.2 MB (10210246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6868acfd0a2f6827fe612eb47cbc113f32f60001154c030e25bdeb792ed800a2`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b5723c118daaca704e83bbe2e9656bd030da6c8881c6bc63c39c42d87aa83`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff45b09b039e321c1809dbf2117718875281c958eec3fd2a912bd93c105aa8ac`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5634332cc476eff85acaf61f2982edd45dc03a385ef62434e355ed2f6d6b300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417aee84378ab0adbc360e0ab0ca8bce4b2789d13a566164c9b481ebe2de14a4`

```dockerfile
```

-	Layers:
	-	`sha256:71d441fb47540e96c217565ce9b91057e89eb2de76614b088c6a93e89a38b5d3`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 972.9 KB (972915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a310b33534948985d9da53b6bc63e8bb85f0b249a88ae08677e59a5518bc856`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; 386

```console
$ docker pull fluentd@sha256:30a69b73619b02f1569dd23ca4aae6e3feeddac07beeb1af2a916b2b21819944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12604962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffd2f89238e4db7386065072ac31741e899e852e5b974d94da70bd0226a8142`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5185764e58ad06e32da6014fb124dbfdceec809e4039bcc4bd2eca81f8bc23a0`  
		Last Modified: Wed, 08 Jan 2025 18:14:19 GMT  
		Size: 9.3 MB (9348500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd62b18440c9a9eb21772cffabfc56219c5491fb1408bb48a7470ddf29d58bd6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0d601bbff4a60b06bfd718cfdf0b3a8773f1d499e1ee92e5f3ae521f512e7`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476c493b073fba36a24b750ecb784d9ac9593c05b72ee8e6cfeeaa4e5c6d1f3`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:905aaf9db86a1ae5f5f5b27b263d946ca426b178dc4c72dee1e5d591d63e8dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3fd24f9b6a35a9ebc4a91ec2956d643d93182494390ca42232ea3023e2c396`

```dockerfile
```

-	Layers:
	-	`sha256:69177ae6cba5a8318d81e6918989493903af8d2d08ef21219fcdbf685ec955d6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 969.7 KB (969696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3853612e064f202dfe95db7c07b145cb06ba9769e588f5289e06b5b3683ca40b`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2e0eec460a136adf9a6f8aa0369a75bd5ed8331772ffa0fa6e67927aff52c3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13236866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747910d8da73a8a53b54c8cb20cdcae6e5a9a30421593c93a3561b2b5afa752`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ea284016ffcc6a262a497ef4345323d63916db72b1a956f4b2c920120dac12`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 9.9 MB (9869053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5816e0c3bc37f90ea4ed3c1503eb186e3f9395a9f5594cd52fb1a098810f19`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8f63e9a01c37db6303087f6db77a0009f51b9eb55006327ed898a6b015117b`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703b0333c72cad50aca36fcb074517778263f09c3776cdbcd41b65b867384aa`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9245091845e8a2f6b9454afafc0c754fa90e966a5e94daa1b5851fa46f53ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc0a260581f1c348ba478eeff05775c89bfa90f6fb92a66482245ee516c244`

```dockerfile
```

-	Layers:
	-	`sha256:e1343a6c5ff192e4765a75235d9ada61e87d1f8b6dc3166cb2fff781d9bcacfb`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 968.5 KB (968479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65da8b0bb3bc52944a98b8bf05b31131291f25c3f65255247cf000f91022ea3`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-1` - linux; s390x

```console
$ docker pull fluentd@sha256:481699bea13ddaf0bd8e459f1178be92b522f9f123b7bb87463bf2fbeda31ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12897163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095aab6a9f3bb8165dfc0bd4eeeb214f38134f6adb69cd907914461ba86f6613`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36793eda614f3800d8dee66d2397436ab110199dd50deb50f2729d40f2c6da68`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 9.6 MB (9640744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f8ebbc4596a65c46b18e9e93f0ad21cad5abe0e1ce35eb5464c9186f4decce`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aac62a48a860c337b0cceb55c7628552ae6daade7af6616eb92192368717b91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97491580908b3ca7e161ef90a8a9c70f11e086b0b7bb7176262a63dff68550`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:dfb3a2a35fad837e6c243c203a1d99d4c7d12c6d080d664c82242fe0899339f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67faa80a717af387624f796e4488daa141be37dc94c86d4bde786b362bc9896`

```dockerfile
```

-	Layers:
	-	`sha256:915e83825c99fe30464f9b5a97a57e80101160ee4361ca173776e44a29eb3f91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 967.9 KB (967863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83c3ab7a15dce251c9ee2ccfa0eed20017b8c80dd6fb357ac6ecf87a5aa1206`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 14.9 KB (14852 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18-debian-1`

```console
$ docker pull fluentd@sha256:59e5add706d19fb2380dc93c697a9dff8bbb9e37a47776b28675baa011c041ed
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
$ docker pull fluentd@sha256:9e7014b563803ec121ed913fb526a6c57772223fba02f2066ff61b2eb8bb41d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83090336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbbdfd8834323acd0ec4f7657f75352ce44b31e432fd563b53c3a0d9965cbcd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331c02dcb1fc995541b31ae50dd3a8926876f241eec5b9727179749e8cfdf80`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 3.5 MB (3499361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c353cd4c9298737bd1cef91fe0bddd0af2bcb03fc4926f516c135d3dee33a`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7078735eadfd37aa4f14ef8aec511066ac5d2ba47122695509e7ae36be719`  
		Last Modified: Tue, 04 Feb 2025 04:50:28 GMT  
		Size: 46.2 MB (46231484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad7bdb63007ebe60c30d983e0bd82d62e192786a6d508a9c073e846453da05`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7655c07c885c0fa246b10bbfb7dd0fba4a643c0e629f88ba9ae1218abc156`  
		Last Modified: Tue, 04 Feb 2025 05:30:38 GMT  
		Size: 5.1 MB (5144797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7291bc86af5fd6c9e13d8f2362fd1986931ee4884d6918b6255955d321033e`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc38bfd3e3dbde29daae3661704d729ca49adc3fdc7ba9484e3ff2e3c52e6c02`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a4d04572195ed648cf3c58d21d8498b711f1094e88ac1a63cb8e6b5598dd8d`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9e3705ce45c4a8df2495689df4dec43349af2202d318ba1af9097f3d9527f598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d6f78983345c4edcb551edee48d77aba11819b25325ba88b22b7f1a49fe001`

```dockerfile
```

-	Layers:
	-	`sha256:3cbdcfbdc703399f4404c9b69e17351b9c64682736613161502aea6be17a66bb`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 2.6 MB (2575888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a18358aa5620746fd411934eaa282b9711464b96d4345574a02e033448fb12`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:bc0b04bdcb3c528e69b0bbe2bdd0b8bd531eb381dd85225c412689acebf73074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74654302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5fac02dc1379a10524c060058ae4e40d77e25068f0224da0a105c09b1a04ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d934325bc4b023af5c986fb28122fdea2b662a8442d611b55b0afdcbf5d099`  
		Last Modified: Tue, 04 Feb 2025 09:48:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81cc1dbccf5ce79eae01f7c07bf23a032af1a6cee42e6246d3b1ac2b1c956f`  
		Last Modified: Tue, 04 Feb 2025 09:54:40 GMT  
		Size: 40.8 MB (40779941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2106cd75253171c2bd9a0f4195f303151f08780cabb37a7e11867e74dd0fbc`  
		Last Modified: Tue, 04 Feb 2025 09:54:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e251f4fd15303aa755bef5ae402ed2d890948d6858b9f17d443420b21c11692d`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 5.1 MB (5062002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7324641fde43d748db58e96e11830358f9372ffb264c67b25cbd11eea17bddf0`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a65785ab5d23ec3ad5a17e40c9e352fed57eb34225df104406c668cee33904d`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5110efad532733de62b68bb2c5ed70d83c988f8462e4649a8e747b6f55325b49`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b32af7e77a66d1eb927345b50562385f21251bf1cff9ae44f5c6cd4ff6e90e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0535d965e159c0472b10724e953cae1ef2390d464090f09c5702317759eaec`

```dockerfile
```

-	Layers:
	-	`sha256:ba98a4b40d450978b42cc76d1014ae672302d5b16063f469ac0f4aab725bd6f8`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 2.6 MB (2579380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a47c098ffe578243d137bf96804846c1ba3bd414de35d09c10980554ea6fc9`  
		Last Modified: Tue, 04 Feb 2025 11:55:06 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:15e699bc5b4eba9f93f478691c72639132ca36aeb281ba66e2b06a93a348a6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71879221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f898fe9d0fccb9c303757eab92c4820d5bd771e3bbc04e43ff6f11ea8181045`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e150ebe0715d085b568881fb745ae6852a33486175a85cd10e8aef763bbe2`  
		Last Modified: Tue, 14 Jan 2025 14:57:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f681e7a3a3a77ea47826710f8eedd797b7bf23e06b51cf04fb1effe23f44ac3`  
		Last Modified: Wed, 15 Jan 2025 20:08:27 GMT  
		Size: 40.1 MB (40116930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec815d6fab44349a0eddc67b01f43007eec296cbc39341305d2edc801eaba2`  
		Last Modified: Wed, 15 Jan 2025 20:08:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177a80764f94e9a3f02d0963f567885f88bcfb73ce707bde0a81aec4010f1d03`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 4.9 MB (4937508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65d9091e286f0e1ed9bb869124177728609d96b58403da51ef564aef571c77`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf8a80d83edbd57b64c6ec5d8dc370befa3ff594fe101da020c4d6253dd907`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540c74ccf0a7de93fcbf1146dca2a8aa7d26c773656e6ee6bf4cf76553c7fedc`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:680a1ca97e26fbf67f3a968f89e1d922ab8a0b01a617dbf8bb938eb77a029a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61987920652caf151106bde09fa4d80578848571973a2815d5766e8bfd841a9a`

```dockerfile
```

-	Layers:
	-	`sha256:11f0ab340994943a1a07adaf404bdea3067b842c1d7d2e290e77fb2204327ce1`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 2.6 MB (2578129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79aef42f0900738ca9c6eae6da6ce2dc4e9e5ec8255538794c5ad9455f29d7e1`  
		Last Modified: Wed, 15 Jan 2025 21:21:01 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7aba43a3eb8bc0e49b8ad876ed853b81404eaa063fca3503cb8e590861af2e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81675924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2da638f2cce4405a7b5d6ec891b786672417608f3d21f1f06e7fdfdd6afd9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58416046741782581ba6b478f57f74691b94b4bba6e177c08cb5755d52f7ee38`  
		Last Modified: Tue, 14 Jan 2025 11:27:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383ed55caee07787faa4ec3c9f8a015d187e2e41c38f2e998e1b7c6fe4b05c98`  
		Last Modified: Wed, 15 Jan 2025 20:05:53 GMT  
		Size: 45.2 MB (45172241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba58f57af5993bf899a32367d58eae51512f86b69f531888c98be4e3f3bf131`  
		Last Modified: Wed, 15 Jan 2025 20:05:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f54332cbd0fd3ea48ca9f835201f3af2babcc54db91714db273a4f0097eefe`  
		Last Modified: Wed, 15 Jan 2025 21:51:25 GMT  
		Size: 5.1 MB (5137377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716a481f1a88679f766822e80d704eac7a820a2196dfe4374a4170658cf248e`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2298c73e42c0f6abf0fd5b20c9717c82207093c869d58670921253b72cdc162`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6471cb5a1365d4c57155bf7f879628ae278a7288113057fb952724ef9f5bc1`  
		Last Modified: Wed, 15 Jan 2025 21:51:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:779d7da8c68ddb047ee3dc2e4820b349ca97f25cdf17397cd3aeb01cd1ea86b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde1ac7e076a825fd8354a18adbad9facd0638c85d7e4d738cdc53b9b99698c3`

```dockerfile
```

-	Layers:
	-	`sha256:f43040dfa2fd33b82a1a29eb286e1622041d7ea9721f9bfcb73fb0f742c38e46`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 2.6 MB (2576133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:969eadb0779170bfc805b6541f79f8f9fe6654db303dd8e3454308532a553883`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:f39c6152f77e3a3460fc28e7f1239529378df150130fa267c5b709f0137420bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79798796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56265780636624b9e5a45d3ce6b1495bfd40673da87662716d349d7a2ee5ece9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b249856b2bd7df2e0f8ddb14f80a0d356420b051fbb64fb38e7607e063b09`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 3.5 MB (3503410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b99e72709696463474ec292f81f3437debe658e6d744f61627f640e2c4667`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e775bf0fa12d5d5a3a66e563c9d16d2127daf1c2927fa93e4e2a09d86647`  
		Last Modified: Tue, 04 Feb 2025 04:43:43 GMT  
		Size: 42.0 MB (41979266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddacabb7846af3bac7ac8761ea96e499a3a4498c44ccf1fd46e9c354c2e12e0`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760394f624b2a302f0190a33d66857de1685deac6f6096e7874fc12918f6934a`  
		Last Modified: Tue, 04 Feb 2025 05:20:14 GMT  
		Size: 5.1 MB (5126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6fa124852d53227d045c25d772552e73c854d0bcee13e96ab3bcb1d1a892e5`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afc77f5089e92c564a35c88d5dec128dba2d05873fd7bb595bedfcfb30ad9d2`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049908c3ec3e17f3c137d478546229b4e3d7d6c847ad3d3f0db64ebc3fe5c76b`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fb2d310e34da8bbdc0fe1f38ad9564b9a1faf41a1376056463e21f95cac9b0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3ef87e42c145ac4b395f9eeee0141c5bdc7cf03e68362f79a6699bcdb069a6`

```dockerfile
```

-	Layers:
	-	`sha256:e5c27da6f0600b917df12f40732a8460dd80ba94aae40fa46df4826d0b868493`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 2.6 MB (2573012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a007097df8d9465935e2ea160cb8022200fed7d5e717068b2f30732e85dc1b63`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a4a7959d92a67ae0b9272e0ea2513edd2a478054d498e7a384fb5fd8a5bd5c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85830955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a126e0a1b90ec5f2f359520017124cec56fdb50a71f961708491b5ee7d8248`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea4eff7192e8ce52808fb6ab513ad38b48d6931a5571ba83fc8cb74d4f91ff7`  
		Last Modified: Tue, 14 Jan 2025 08:25:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b554468e854a3e4497eec7b1d7d6194a3410c61a276d1d9eb8e56fa14fe206f`  
		Last Modified: Wed, 15 Jan 2025 19:04:28 GMT  
		Size: 44.6 MB (44615901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae7abd9014ac00cdd55280d61b30695c62efe4d5cd02240e28507d7d0c53f`  
		Last Modified: Wed, 15 Jan 2025 19:04:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf962d48f8b97c21fc444566c45f175d23c920c1be0d68bfcf0c53e0e9f59e`  
		Last Modified: Wed, 15 Jan 2025 19:33:59 GMT  
		Size: 5.5 MB (5464905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c626c221cd815de80507072ddd76a75053b38aa3152899b73609ad0cb09cdc`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce003ba998cfc17760a49632bb329b9778d1b2ac221e929e114125cce87170e`  
		Last Modified: Wed, 15 Jan 2025 19:33:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f619d4d326682a2fb2e92a90f9b3a4b76f61e66f12b7c05d76dcf4c9bcf99fb6`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6b5921078ab89d2a95fdc0c5d11817a9f3c2deacc6318ead380a2822b12b239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c953ee1a0543394b3c39f2ce0b41ab71a3b62f620987a569eecebb0360166de2`

```dockerfile
```

-	Layers:
	-	`sha256:cd3cf27948b91a20933bf030370c3d7852560be37d1092d8fa9b95d1b6e0a3a3`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 2.6 MB (2580236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7a7d1a82bd2941b1661b850fefc09c16ab6734aa6137da1f5839b0f565d21c`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:36271e3bda93c26cc0e57d9fcb9ecf368b36039708b97ca12edee60a7d3705d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7a4cb7be349dca17ef9d9bed5886a24b50ce3707f9114e9dcbea4916dc17ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb53c00cc457fdc4bb929f08300df25e06e0b068a3dffb3addb1f41c092f5f4`  
		Last Modified: Tue, 04 Feb 2025 10:53:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fe1bc27e1e69c36aa54c5ff4280a4dfba37d4d962e1a2b5851105cd813366`  
		Last Modified: Tue, 04 Feb 2025 10:59:39 GMT  
		Size: 41.9 MB (41876003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0cc91519f097b09cac7bd36a749caec6b5d576b91ad7e173fa9d0e026e489`  
		Last Modified: Tue, 04 Feb 2025 10:59:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec81fe7fa750d50abcb182e96096218e6031543f5212fef62599e2c0f12a85`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 5.2 MB (5175812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c063fb827a64d7f338ec757f2f752c2378548e16e09927bd437f9a734fe937`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfa70ee4b4b3f1f636da7bbbcecc7b25bb94e8d8a74b7de17be643f13d7af90`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6f0aab00b1aaf4c800188a2281816cd376a2e7e6aa6468692b4d05583c490`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3090fbfce5810e9bb6025eb04b2b19ff531377762f31efe43c00c54b60d82a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7b028a25b517e5d7bf35a451412ee5ad0ba93d2b111d5806bb657505acd929`

```dockerfile
```

-	Layers:
	-	`sha256:d2fc64217ee17c8785a16faf7062978cc130b5f26509d564a5054f052d8fa682`  
		Last Modified: Tue, 04 Feb 2025 18:23:51 GMT  
		Size: 2.6 MB (2575600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb3dcafb8f5b369beefa1cc16fd8f72f65029032cc4ae56429fba9f131354e0`  
		Last Modified: Tue, 04 Feb 2025 18:23:51 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-1.0`

```console
$ docker pull fluentd@sha256:f2e00db9337b6cafd900baefa80d7dc92f7869c9efb9967ace7054fcda60769c
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
$ docker pull fluentd@sha256:1cfeefc63742d9c1e4a0a81bd06c59ac515625e9216bda498d3cbb81ffe5bea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13503116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6726f799691ee19fb45ea27834423e4e9ba5975f3aadd1105eb2206eac2ca730`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88184bdf313262fd2b997ef59a4038d2972f7677bd41e74a4e67e8d30a9f0a`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 10.1 MB (10080707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ac64fa66df6e55e2c851cebc50b387f2deac85c2c3f43249487d15c3a777d`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e21b2856c0b6deca9cd7a6ad5dd6eef86bba047016e64a7e2f9814426430b`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc8e49be5aadbe64c8791612a4309696c03c5da139b55fa2f272e6ba98170be`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ef10734f2f1bf9e4e3fca546feb000532c083ec8ec17107db6d15f9243ecd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 KB (987630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9c02f1f401c793a3f5e3cc3579b2375936adca4e8f2a524a575a984a4f91fd`

```dockerfile
```

-	Layers:
	-	`sha256:46ffc5122367ac0020f0e1431e2981aa74ea007a16cc57d575a7ade622484e46`  
		Last Modified: Wed, 08 Jan 2025 18:17:59 GMT  
		Size: 972.8 KB (972773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf961a846aa828aa17a9eb140c86565feae755052fb2073c6b3d4f86a60cf97f`  
		Last Modified: Wed, 08 Jan 2025 18:17:58 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:a6edff4227f751a9f6f6d852848b6dcc9fe2b26c9453d38cf83b8040f72aa361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12293968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e774d5a6378801d8ab21db43de16242daede5314be554580a0500582197111f0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
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
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1f6328a98409ef7ebdb673a31904f1733fe61a8606be8982970e7d8d8395b`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 9.1 MB (9114798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e6410b03f444c7fb5ffcb5964bc54cfb810a5604717495e1282cd677d2393`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f555b28a58800c180f5aed2d1dbafed5d9077c34b3960486c78b2aca8e5c32`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14dc540a2af8278d681f92d131d33eaf3403587630310486f7a1d9979313a3`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7739f7dc8dc341d9de7bd9d0cd73c05ce5aaaecced57869065ec09751e204cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a096ea30107a537393046263deb7a8e5894f1a38f13f155bc9e968e2730df1`

```dockerfile
```

-	Layers:
	-	`sha256:72a7f2b6b11131276d268b128eb06e6429da4a7eb23d8179876b1c0dbbd44887`  
		Last Modified: Thu, 09 Jan 2025 08:49:25 GMT  
		Size: 14.7 KB (14718 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:508fe22601e35eb968eb6fcff8191e4ba2f527ba6df563302ce66f6b3a8e04ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13572944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45b99119b157c2fa1d13773f64320c1576f9255cb257b0b7fe31bb5c5f60d48`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a667ca550d5c342aef10ed2642c61d3f25e721bcf025d041c2985912f17ca63b`  
		Last Modified: Thu, 09 Jan 2025 06:07:42 GMT  
		Size: 10.2 MB (10210246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6868acfd0a2f6827fe612eb47cbc113f32f60001154c030e25bdeb792ed800a2`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b5723c118daaca704e83bbe2e9656bd030da6c8881c6bc63c39c42d87aa83`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff45b09b039e321c1809dbf2117718875281c958eec3fd2a912bd93c105aa8ac`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5634332cc476eff85acaf61f2982edd45dc03a385ef62434e355ed2f6d6b300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417aee84378ab0adbc360e0ab0ca8bce4b2789d13a566164c9b481ebe2de14a4`

```dockerfile
```

-	Layers:
	-	`sha256:71d441fb47540e96c217565ce9b91057e89eb2de76614b088c6a93e89a38b5d3`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 972.9 KB (972915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a310b33534948985d9da53b6bc63e8bb85f0b249a88ae08677e59a5518bc856`  
		Last Modified: Thu, 09 Jan 2025 06:07:41 GMT  
		Size: 15.0 KB (14964 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:30a69b73619b02f1569dd23ca4aae6e3feeddac07beeb1af2a916b2b21819944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12604962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffd2f89238e4db7386065072ac31741e899e852e5b974d94da70bd0226a8142`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5185764e58ad06e32da6014fb124dbfdceec809e4039bcc4bd2eca81f8bc23a0`  
		Last Modified: Wed, 08 Jan 2025 18:14:19 GMT  
		Size: 9.3 MB (9348500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd62b18440c9a9eb21772cffabfc56219c5491fb1408bb48a7470ddf29d58bd6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0d601bbff4a60b06bfd718cfdf0b3a8773f1d499e1ee92e5f3ae521f512e7`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476c493b073fba36a24b750ecb784d9ac9593c05b72ee8e6cfeeaa4e5c6d1f3`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:905aaf9db86a1ae5f5f5b27b263d946ca426b178dc4c72dee1e5d591d63e8dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 KB (984520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3fd24f9b6a35a9ebc4a91ec2956d643d93182494390ca42232ea3023e2c396`

```dockerfile
```

-	Layers:
	-	`sha256:69177ae6cba5a8318d81e6918989493903af8d2d08ef21219fcdbf685ec955d6`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 969.7 KB (969696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3853612e064f202dfe95db7c07b145cb06ba9769e588f5289e06b5b3683ca40b`  
		Last Modified: Wed, 08 Jan 2025 18:14:18 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2e0eec460a136adf9a6f8aa0369a75bd5ed8331772ffa0fa6e67927aff52c3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13236866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747910d8da73a8a53b54c8cb20cdcae6e5a9a30421593c93a3561b2b5afa752`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ea284016ffcc6a262a497ef4345323d63916db72b1a956f4b2c920120dac12`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 9.9 MB (9869053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5816e0c3bc37f90ea4ed3c1503eb186e3f9395a9f5594cd52fb1a098810f19`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8f63e9a01c37db6303087f6db77a0009f51b9eb55006327ed898a6b015117b`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703b0333c72cad50aca36fcb074517778263f09c3776cdbcd41b65b867384aa`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9245091845e8a2f6b9454afafc0c754fa90e966a5e94daa1b5851fa46f53ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc0a260581f1c348ba478eeff05775c89bfa90f6fb92a66482245ee516c244`

```dockerfile
```

-	Layers:
	-	`sha256:e1343a6c5ff192e4765a75235d9ada61e87d1f8b6dc3166cb2fff781d9bcacfb`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 968.5 KB (968479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65da8b0bb3bc52944a98b8bf05b31131291f25c3f65255247cf000f91022ea3`  
		Last Modified: Thu, 09 Jan 2025 00:59:20 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:481699bea13ddaf0bd8e459f1178be92b522f9f123b7bb87463bf2fbeda31ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12897163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095aab6a9f3bb8165dfc0bd4eeeb214f38134f6adb69cd907914461ba86f6613`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36793eda614f3800d8dee66d2397436ab110199dd50deb50f2729d40f2c6da68`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 9.6 MB (9640744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f8ebbc4596a65c46b18e9e93f0ad21cad5abe0e1ce35eb5464c9186f4decce`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aac62a48a860c337b0cceb55c7628552ae6daade7af6616eb92192368717b91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97491580908b3ca7e161ef90a8a9c70f11e086b0b7bb7176262a63dff68550`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:dfb3a2a35fad837e6c243c203a1d99d4c7d12c6d080d664c82242fe0899339f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67faa80a717af387624f796e4488daa141be37dc94c86d4bde786b362bc9896`

```dockerfile
```

-	Layers:
	-	`sha256:915e83825c99fe30464f9b5a97a57e80101160ee4361ca173776e44a29eb3f91`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 967.9 KB (967863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83c3ab7a15dce251c9ee2ccfa0eed20017b8c80dd6fb357ac6ecf87a5aa1206`  
		Last Modified: Thu, 09 Jan 2025 07:13:49 GMT  
		Size: 14.9 KB (14852 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.18.0-debian-1.0`

```console
$ docker pull fluentd@sha256:59e5add706d19fb2380dc93c697a9dff8bbb9e37a47776b28675baa011c041ed
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
$ docker pull fluentd@sha256:9e7014b563803ec121ed913fb526a6c57772223fba02f2066ff61b2eb8bb41d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83090336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbbdfd8834323acd0ec4f7657f75352ce44b31e432fd563b53c3a0d9965cbcd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331c02dcb1fc995541b31ae50dd3a8926876f241eec5b9727179749e8cfdf80`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 3.5 MB (3499361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c353cd4c9298737bd1cef91fe0bddd0af2bcb03fc4926f516c135d3dee33a`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7078735eadfd37aa4f14ef8aec511066ac5d2ba47122695509e7ae36be719`  
		Last Modified: Tue, 04 Feb 2025 04:50:28 GMT  
		Size: 46.2 MB (46231484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad7bdb63007ebe60c30d983e0bd82d62e192786a6d508a9c073e846453da05`  
		Last Modified: Tue, 04 Feb 2025 04:50:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7655c07c885c0fa246b10bbfb7dd0fba4a643c0e629f88ba9ae1218abc156`  
		Last Modified: Tue, 04 Feb 2025 05:30:38 GMT  
		Size: 5.1 MB (5144797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7291bc86af5fd6c9e13d8f2362fd1986931ee4884d6918b6255955d321033e`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc38bfd3e3dbde29daae3661704d729ca49adc3fdc7ba9484e3ff2e3c52e6c02`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a4d04572195ed648cf3c58d21d8498b711f1094e88ac1a63cb8e6b5598dd8d`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9e3705ce45c4a8df2495689df4dec43349af2202d318ba1af9097f3d9527f598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d6f78983345c4edcb551edee48d77aba11819b25325ba88b22b7f1a49fe001`

```dockerfile
```

-	Layers:
	-	`sha256:3cbdcfbdc703399f4404c9b69e17351b9c64682736613161502aea6be17a66bb`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 2.6 MB (2575888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a18358aa5620746fd411934eaa282b9711464b96d4345574a02e033448fb12`  
		Last Modified: Tue, 04 Feb 2025 05:30:37 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:bc0b04bdcb3c528e69b0bbe2bdd0b8bd531eb381dd85225c412689acebf73074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74654302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5fac02dc1379a10524c060058ae4e40d77e25068f0224da0a105c09b1a04ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d934325bc4b023af5c986fb28122fdea2b662a8442d611b55b0afdcbf5d099`  
		Last Modified: Tue, 04 Feb 2025 09:48:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee81cc1dbccf5ce79eae01f7c07bf23a032af1a6cee42e6246d3b1ac2b1c956f`  
		Last Modified: Tue, 04 Feb 2025 09:54:40 GMT  
		Size: 40.8 MB (40779941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2106cd75253171c2bd9a0f4195f303151f08780cabb37a7e11867e74dd0fbc`  
		Last Modified: Tue, 04 Feb 2025 09:54:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e251f4fd15303aa755bef5ae402ed2d890948d6858b9f17d443420b21c11692d`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 5.1 MB (5062002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7324641fde43d748db58e96e11830358f9372ffb264c67b25cbd11eea17bddf0`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a65785ab5d23ec3ad5a17e40c9e352fed57eb34225df104406c668cee33904d`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5110efad532733de62b68bb2c5ed70d83c988f8462e4649a8e747b6f55325b49`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b32af7e77a66d1eb927345b50562385f21251bf1cff9ae44f5c6cd4ff6e90e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0535d965e159c0472b10724e953cae1ef2390d464090f09c5702317759eaec`

```dockerfile
```

-	Layers:
	-	`sha256:ba98a4b40d450978b42cc76d1014ae672302d5b16063f469ac0f4aab725bd6f8`  
		Last Modified: Tue, 04 Feb 2025 11:55:07 GMT  
		Size: 2.6 MB (2579380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a47c098ffe578243d137bf96804846c1ba3bd414de35d09c10980554ea6fc9`  
		Last Modified: Tue, 04 Feb 2025 11:55:06 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:15e699bc5b4eba9f93f478691c72639132ca36aeb281ba66e2b06a93a348a6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71879221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f898fe9d0fccb9c303757eab92c4820d5bd771e3bbc04e43ff6f11ea8181045`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e150ebe0715d085b568881fb745ae6852a33486175a85cd10e8aef763bbe2`  
		Last Modified: Tue, 14 Jan 2025 14:57:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f681e7a3a3a77ea47826710f8eedd797b7bf23e06b51cf04fb1effe23f44ac3`  
		Last Modified: Wed, 15 Jan 2025 20:08:27 GMT  
		Size: 40.1 MB (40116930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec815d6fab44349a0eddc67b01f43007eec296cbc39341305d2edc801eaba2`  
		Last Modified: Wed, 15 Jan 2025 20:08:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177a80764f94e9a3f02d0963f567885f88bcfb73ce707bde0a81aec4010f1d03`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 4.9 MB (4937508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65d9091e286f0e1ed9bb869124177728609d96b58403da51ef564aef571c77`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf8a80d83edbd57b64c6ec5d8dc370befa3ff594fe101da020c4d6253dd907`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540c74ccf0a7de93fcbf1146dca2a8aa7d26c773656e6ee6bf4cf76553c7fedc`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:680a1ca97e26fbf67f3a968f89e1d922ab8a0b01a617dbf8bb938eb77a029a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61987920652caf151106bde09fa4d80578848571973a2815d5766e8bfd841a9a`

```dockerfile
```

-	Layers:
	-	`sha256:11f0ab340994943a1a07adaf404bdea3067b842c1d7d2e290e77fb2204327ce1`  
		Last Modified: Wed, 15 Jan 2025 21:21:02 GMT  
		Size: 2.6 MB (2578129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79aef42f0900738ca9c6eae6da6ce2dc4e9e5ec8255538794c5ad9455f29d7e1`  
		Last Modified: Wed, 15 Jan 2025 21:21:01 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7aba43a3eb8bc0e49b8ad876ed853b81404eaa063fca3503cb8e590861af2e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81675924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2da638f2cce4405a7b5d6ec891b786672417608f3d21f1f06e7fdfdd6afd9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58416046741782581ba6b478f57f74691b94b4bba6e177c08cb5755d52f7ee38`  
		Last Modified: Tue, 14 Jan 2025 11:27:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383ed55caee07787faa4ec3c9f8a015d187e2e41c38f2e998e1b7c6fe4b05c98`  
		Last Modified: Wed, 15 Jan 2025 20:05:53 GMT  
		Size: 45.2 MB (45172241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba58f57af5993bf899a32367d58eae51512f86b69f531888c98be4e3f3bf131`  
		Last Modified: Wed, 15 Jan 2025 20:05:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f54332cbd0fd3ea48ca9f835201f3af2babcc54db91714db273a4f0097eefe`  
		Last Modified: Wed, 15 Jan 2025 21:51:25 GMT  
		Size: 5.1 MB (5137377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716a481f1a88679f766822e80d704eac7a820a2196dfe4374a4170658cf248e`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2298c73e42c0f6abf0fd5b20c9717c82207093c869d58670921253b72cdc162`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6471cb5a1365d4c57155bf7f879628ae278a7288113057fb952724ef9f5bc1`  
		Last Modified: Wed, 15 Jan 2025 21:51:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:779d7da8c68ddb047ee3dc2e4820b349ca97f25cdf17397cd3aeb01cd1ea86b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde1ac7e076a825fd8354a18adbad9facd0638c85d7e4d738cdc53b9b99698c3`

```dockerfile
```

-	Layers:
	-	`sha256:f43040dfa2fd33b82a1a29eb286e1622041d7ea9721f9bfcb73fb0f742c38e46`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 2.6 MB (2576133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:969eadb0779170bfc805b6541f79f8f9fe6654db303dd8e3454308532a553883`  
		Last Modified: Wed, 15 Jan 2025 21:51:24 GMT  
		Size: 20.3 KB (20343 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:f39c6152f77e3a3460fc28e7f1239529378df150130fa267c5b709f0137420bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79798796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56265780636624b9e5a45d3ce6b1495bfd40673da87662716d349d7a2ee5ece9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b249856b2bd7df2e0f8ddb14f80a0d356420b051fbb64fb38e7607e063b09`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 3.5 MB (3503410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b99e72709696463474ec292f81f3437debe658e6d744f61627f640e2c4667`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e775bf0fa12d5d5a3a66e563c9d16d2127daf1c2927fa93e4e2a09d86647`  
		Last Modified: Tue, 04 Feb 2025 04:43:43 GMT  
		Size: 42.0 MB (41979266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddacabb7846af3bac7ac8761ea96e499a3a4498c44ccf1fd46e9c354c2e12e0`  
		Last Modified: Tue, 04 Feb 2025 04:43:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760394f624b2a302f0190a33d66857de1685deac6f6096e7874fc12918f6934a`  
		Last Modified: Tue, 04 Feb 2025 05:20:14 GMT  
		Size: 5.1 MB (5126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6fa124852d53227d045c25d772552e73c854d0bcee13e96ab3bcb1d1a892e5`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afc77f5089e92c564a35c88d5dec128dba2d05873fd7bb595bedfcfb30ad9d2`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049908c3ec3e17f3c137d478546229b4e3d7d6c847ad3d3f0db64ebc3fe5c76b`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fb2d310e34da8bbdc0fe1f38ad9564b9a1faf41a1376056463e21f95cac9b0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3ef87e42c145ac4b395f9eeee0141c5bdc7cf03e68362f79a6699bcdb069a6`

```dockerfile
```

-	Layers:
	-	`sha256:e5c27da6f0600b917df12f40732a8460dd80ba94aae40fa46df4826d0b868493`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 2.6 MB (2573012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a007097df8d9465935e2ea160cb8022200fed7d5e717068b2f30732e85dc1b63`  
		Last Modified: Tue, 04 Feb 2025 05:20:13 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a4a7959d92a67ae0b9272e0ea2513edd2a478054d498e7a384fb5fd8a5bd5c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85830955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a126e0a1b90ec5f2f359520017124cec56fdb50a71f961708491b5ee7d8248`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea4eff7192e8ce52808fb6ab513ad38b48d6931a5571ba83fc8cb74d4f91ff7`  
		Last Modified: Tue, 14 Jan 2025 08:25:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b554468e854a3e4497eec7b1d7d6194a3410c61a276d1d9eb8e56fa14fe206f`  
		Last Modified: Wed, 15 Jan 2025 19:04:28 GMT  
		Size: 44.6 MB (44615901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeae7abd9014ac00cdd55280d61b30695c62efe4d5cd02240e28507d7d0c53f`  
		Last Modified: Wed, 15 Jan 2025 19:04:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf962d48f8b97c21fc444566c45f175d23c920c1be0d68bfcf0c53e0e9f59e`  
		Last Modified: Wed, 15 Jan 2025 19:33:59 GMT  
		Size: 5.5 MB (5464905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c626c221cd815de80507072ddd76a75053b38aa3152899b73609ad0cb09cdc`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce003ba998cfc17760a49632bb329b9778d1b2ac221e929e114125cce87170e`  
		Last Modified: Wed, 15 Jan 2025 19:33:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f619d4d326682a2fb2e92a90f9b3a4b76f61e66f12b7c05d76dcf4c9bcf99fb6`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6b5921078ab89d2a95fdc0c5d11817a9f3c2deacc6318ead380a2822b12b239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c953ee1a0543394b3c39f2ce0b41ab71a3b62f620987a569eecebb0360166de2`

```dockerfile
```

-	Layers:
	-	`sha256:cd3cf27948b91a20933bf030370c3d7852560be37d1092d8fa9b95d1b6e0a3a3`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 2.6 MB (2580236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7a7d1a82bd2941b1661b850fefc09c16ab6734aa6137da1f5839b0f565d21c`  
		Last Modified: Wed, 15 Jan 2025 19:33:58 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.18.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:36271e3bda93c26cc0e57d9fcb9ecf368b36039708b97ca12edee60a7d3705d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7a4cb7be349dca17ef9d9bed5886a24b50ce3707f9114e9dcbea4916dc17ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Dec 2024 04:34:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Mon, 02 Dec 2024 04:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		savedAptMark="$savedAptMark 		bzip2 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	"; 	apt-get install -y --no-install-recommends $savedAptMark; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb53c00cc457fdc4bb929f08300df25e06e0b068a3dffb3addb1f41c092f5f4`  
		Last Modified: Tue, 04 Feb 2025 10:53:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fe1bc27e1e69c36aa54c5ff4280a4dfba37d4d962e1a2b5851105cd813366`  
		Last Modified: Tue, 04 Feb 2025 10:59:39 GMT  
		Size: 41.9 MB (41876003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a0cc91519f097b09cac7bd36a749caec6b5d576b91ad7e173fa9d0e026e489`  
		Last Modified: Tue, 04 Feb 2025 10:59:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec81fe7fa750d50abcb182e96096218e6031543f5212fef62599e2c0f12a85`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 5.2 MB (5175812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c063fb827a64d7f338ec757f2f752c2378548e16e09927bd437f9a734fe937`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfa70ee4b4b3f1f636da7bbbcecc7b25bb94e8d8a74b7de17be643f13d7af90`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6f0aab00b1aaf4c800188a2281816cd376a2e7e6aa6468692b4d05583c490`  
		Last Modified: Tue, 04 Feb 2025 18:23:52 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.18.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3090fbfce5810e9bb6025eb04b2b19ff531377762f31efe43c00c54b60d82a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7b028a25b517e5d7bf35a451412ee5ad0ba93d2b111d5806bb657505acd929`

```dockerfile
```

-	Layers:
	-	`sha256:d2fc64217ee17c8785a16faf7062978cc130b5f26509d564a5054f052d8fa682`  
		Last Modified: Tue, 04 Feb 2025 18:23:51 GMT  
		Size: 2.6 MB (2575600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb3dcafb8f5b369beefa1cc16fd8f72f65029032cc4ae56429fba9f131354e0`  
		Last Modified: Tue, 04 Feb 2025 18:23:51 GMT  
		Size: 20.2 KB (20248 bytes)  
		MIME: application/vnd.in-toto+json
