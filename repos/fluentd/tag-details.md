<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.6-1.0`](#fluentdv1166-10)
-	[`fluentd:v1.16.6-debian-1.0`](#fluentdv1166-debian-10)
-	[`fluentd:v1.17-1`](#fluentdv117-1)
-	[`fluentd:v1.17-debian-1`](#fluentdv117-debian-1)
-	[`fluentd:v1.17.1-1.0`](#fluentdv1171-10)
-	[`fluentd:v1.17.1-debian-1.0`](#fluentdv1171-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:f1125bb64c7bb45881d97adaa9c64cade20b5e394e01d9a76d0fd149f29f4d14
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
$ docker pull fluentd@sha256:69a66ab121b1c527705ca5b0b3f2107ca64ca8837f9313dfd26bcaf1c34b7a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17541449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a570051e688f5f0a0e0cd20067931161c8859d7021664f26eec1ba1949f8b1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26fb14d9f03d80d6a351c8550f2b721cba57c484408e56a16406f701ed4672`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.1 MB (14119554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd7f3a2916614f7b93545575db2733e723a11faf4b012a4271c0b6dac5ced5`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3312511bfca0ab90a65ac84d3255bbbe430cb65b07bcc84a9a18e12886f8c89`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d7888aff12cdd446d772795473f6f803c4ea88b2f52f65c2d73cf699a11f5`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:f441cec2661401f3b0defc276f752d7104b921399e0a87ecd701c4dc16ab2e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.0 KB (986965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a66d2e9a4c9656e4d0cf33c63e6214bb3f48231e0c74c6ddd27cbe5420c3ae`

```dockerfile
```

-	Layers:
	-	`sha256:47fa7b08e14e13c09b23916953413440102c1d855613216c69d157e0f2071387`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 973.0 KB (972988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75406e0a4cac9a4904e647135877a3955d994a25b1a4e708914bfa1f1d0e72bc`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.0 KB (13977 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:ae4dbc2f60917c89ed8eee5140631b544868c0fa6f81ec2cb2b6f4317994b43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16288945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea28d6a7fa01283ab0091b2449868428f3a4c76acd1265ad777481d56d4d9b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e4314d14cdd1eab8c7bd7d04b4eb840e07e311b92701b05033f050a760fccf`  
		Last Modified: Tue, 12 Nov 2024 15:36:22 GMT  
		Size: 13.1 MB (13110344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05b8d3d3ead4020f38f21a2f5310ef4cfc5edb8d7877580a3cf051b2ae22ac`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7378acf6b163022743991c358880d6cd9ee61a81c2c5fd0b90090e436e78f`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dabe2c07d5b74dfdc5507b8187937b350e8c1492e06c6c03e6420d42a7ae26d`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:a9df060029e06b23528cb4d159a6021b506153b0b9fb7dff25f8f8d9d2edd2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78e5474b3e5ff8af95f2c94de1176b441d1e184a3128f348cf51dd6384f78bb`

```dockerfile
```

-	Layers:
	-	`sha256:9144eba8609d3c066ea7ce9eaef02cc3ffbd3c4f8c7ad172b838d623540f9b13`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 13.8 KB (13843 bytes)  
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
$ docker pull fluentd@sha256:675ae0809bb2f2507b64d66c3c9294d9068269debdf988cc40262b6e9852180d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16500851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037ce743da24f109c1d2c1667da51ac4620871dfadde6bb4194bcda14f8bab16`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60bff5f2253ae5f6f66c00e94b366cb468c9dd4c6c4f97cabecc78fa7911b`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 13.2 MB (13245018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3005876d18c66acf8e80ebdedd8005b1c4a497ed6188cddd46ee88cba3dc5dad`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81f31a82e9c7c5431efec55f0f8fdce58b98ecea931d8aa5e6d9ce688cc81b`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5125f347be85a89f1ed0a15d204b9cd49a55bd49eacba23e8d17e55ce4c7c96`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c9b4fb31fb184fe2289b230466690a777e815553b73a2decf419474529a04de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 KB (983856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913899d5a3ec637e5a675b073be05c722cb2a88306c9131784e353e21308e14`

```dockerfile
```

-	Layers:
	-	`sha256:f551dda615cf4d2b56cd2c7b66efd5854bdc3cb22fc7575eb6e150f0373cf1d3`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 969.9 KB (969908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f266dace64c0749591687a9008547941918fb0be233c0051c1024fa800a5f1a7`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 13.9 KB (13948 bytes)  
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

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:f8617b7144d5598a19475b1148d78576498b903a1c801e60e680de1b8b1dd198
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
$ docker pull fluentd@sha256:de7f2b470a5aa1839b88d1a6d356cb216fd4e3cec5b8f7436b4cbb7c244071a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17500754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa143d7c6eecb27e51444f79cd2fb7d5bf306c55f9a3b8a94c072fd68eb4d7f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03641aeb8487523c7557972c6511abb652f675a8a765620e1fb5d5b427eb8ab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 14.1 MB (14078862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb70e9a7cf252f51c69f58040fee493434c3225d154250faa22f9dde6000c76`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a935d220d11a5de7fb09b611fad2ddea6f99eaee887d69a7cca3b226e1c56f31`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892898ae358c92a59eb961338015d38b9ffa6bc34c38557304ce5742dc6d1b58`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c25323a850aa8fc3b60db7b6f9fa36a5da2aa4f545c1f1f39dca9e03e28193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.3 KB (983334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b6728df6c69cb3d78a6b393273af5d50dc492228e3e04950b1baa94a06ef4`

```dockerfile
```

-	Layers:
	-	`sha256:1f076be1586d715022168f1d93306a92fb19700d34ce7f869953282f0b063d69`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 969.7 KB (969657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b9d1a7fc7196f27b8dca7a78a9059eb3623e33c3b7122e3dcdccd29faf88db`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:b90fffb9caeb6dfa5148a8aa1d93e97ebf15e6f546ed4bfee6c0fbf11c61b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16249953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247cb9c0d2332aa78766bcd355b7dbff88e8a437fbb2f26c8c32171318af9795`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a137212c82376d24e903c744caca7e2a9d045b04027583162cebd79d074a34`  
		Last Modified: Tue, 12 Nov 2024 15:34:51 GMT  
		Size: 13.1 MB (13071353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a7bcf0d170c6cfa424680bff249c56dcc1cd13485f93b9606cd198edca806`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2af3e4f074465e23c2dc98db0d76824b13c89e3529a769ea830ff2515b5dce`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aed04ce0ab3b7686f54f8fb77b0cf6824087dfabb686e7535bde97ac536573`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c413d6623822df7a470fdd386d964200dd800688348d5bd6f5b57073652c5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f760e68145be2fa93a5790b01fbb0293e7cb3524154f70ce7ce3ffcf53c77bfd`

```dockerfile
```

-	Layers:
	-	`sha256:c056af5ec9594afb77ae52bcc5cbe7b93247a9538512dcedcdb5d18e74517f6b`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 13.5 KB (13533 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2d66f7fd4262b7663eccf4880d263833ff6927006f6e1473f5349d087b9b4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17483875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981f22752bcd0108721527a5c1bcf7d69568689f77ce09e6363f9c54ad07c80a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2edce25880d7cabc493be5a926661b3d5968abb8644f08cbe77417b9eeab5f9`  
		Last Modified: Wed, 13 Nov 2024 01:42:07 GMT  
		Size: 14.1 MB (14122459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f7b79eb872b316bb439f4fc558ebf5dffce72816c8b11d4ff1a6f2adf40c4`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10a38889725963cefe622795097205c6ecba2ebd4963aaedae5bc4eda7b14d`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a6d89f20fbfe383f01f73ee53a40f67ef0fdf8c39f225ace14a25820a2291`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7d3958bd8af52b4633fda4572cdba2b9a4a87a21ad3810bee1db42300541007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.6 KB (983558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd3a08fdc1a3d2e79b971151eb10f3fd13e8279ff8776079410b1db5f02172e`

```dockerfile
```

-	Layers:
	-	`sha256:00960a9f0196875b4f3f71807f6e37102e47eb255d2224ea23f0111f52b9b33d`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 969.8 KB (969787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d676dd06b29ba72c8229a11fb205987ea6290c79f02e81768f046fc42630b805`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:129d1f0274285b657427b655dd7a1e1a7b15b136f05d5040cc502666db4138ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16457092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd32b64afd7e3abd8b2f32c4041cc79ef9ac8d897d5d89dcc1d84878fcd0aef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de2501f0638fb1825bfa3cd5528a4ef79593a2d8dd2920f645d023f6b8ea460`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 13.2 MB (13201260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cbca890db0eda508f438975ae9cb52ac4fe4d51e6f2d60e1674c79d82dcbc1`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3312511bfca0ab90a65ac84d3255bbbe430cb65b07bcc84a9a18e12886f8c89`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d7888aff12cdd446d772795473f6f803c4ea88b2f52f65c2d73cf699a11f5`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:28fec255d83e725e41dcc05a47494cd6dc7effc4d2dc91a3483745ed9843ffe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.2 KB (980235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb3b3b2b9de0b2e5dffec31e6e6a59af172b0e883770aabcecb08af438e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:941551f158457265f17f9fb98b40a1f75930060668156dbb68bb074ab99cf7a2`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 966.6 KB (966582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691ad8f14775bc9b667b1b4b49380611c49b99b7a53caf2363330496c61ffe1f`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7720a20f726d3e22630c6a279ffc91525850f3b348daaa59a0c012cc7f30e0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffa1612724ccf90daa43116353b4508ffc06d155fea9fe2497df9e05f81fc81`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86615fa6317b3080aeff3038928587d4efd4853ad311cb77bbe9ccea62fb39b`  
		Last Modified: Tue, 12 Nov 2024 14:59:00 GMT  
		Size: 13.7 MB (13684370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396205a671deaa675898069a51c8265ff555108e7804e65029727248482ea114`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c505d257f4da424c5b9bdf9c0adecc893c46a1b87cb928962a0b6cfad71c7d5e`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cc99c342fe219810afa0a89232bed051f7ebb977fe0f1266fc48090ba2cb56`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:432c39e1e5824abc9758289a93a64c9ef5b7b43eea15c4874959675b90769139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65f4db6cb5ab36c3c473c9cefc1546d7257df636ca653a121d0d56cb62face1`

```dockerfile
```

-	Layers:
	-	`sha256:df2a772c1c4eef6371f21254ca41d5eb0371d4b4c290947b9ddc9d44b455957d`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 965.4 KB (965351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bbf015a43c99a5ce1d0282630c36de55c543bbefc35c367ab52a0aa7bb9cfe`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:4153a0ca6dbf827b942065a3e863913538e0d7ddb2060b3493d569040a1aaae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7b00286be8f5078a0faf743739504fddfae478159ea260162dd848e0114046`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
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
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95aa75a013c883c3c2183016bbde406128defbc1f8249fe42abbbf7985575359`  
		Last Modified: Tue, 12 Nov 2024 22:31:19 GMT  
		Size: 13.7 MB (13651889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e678b44ed64915bfda888b997b3efd985d3f708f88bf46989a7f16c86a1bf8`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd845673731e045b3a4805a2c79928e5a2cdf35cbb22d8457e352eefa902e84`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a73234b6a3edab5c451d8e45b93c365272b7040f4c44fca5b0add4e93d4cfe6`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9f7e2f6395d7c48db009202306b54cb0280c2c095000fbf860d8c924012bf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.4 KB (978418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f198834a86d812cb947f18525038288e9ae90dac324ada0bf52435a284a606`

```dockerfile
```

-	Layers:
	-	`sha256:2edd6bebb903cbdb26ea1b8673bba667839babea7740f5cad7b3a07248caaea6`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 964.7 KB (964741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae62c50f15a9e60099b508f4210c892718086b8eaba9053abfcec1a10b966fcf`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:2ddd8f4624148eaa1cb19585b810546b21d5c9ab4224f50124912998356a5d76
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
$ docker pull fluentd@sha256:20b7318587d8406361e3da1d46fb6a03b635f85afb76aaa86757cd3830d92fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92354390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb963ba47026f88e61311fa798a70fcf15f0554f0cbe5f4b9dbd80e47407f919`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9bd057b20c983b5a5dd8b564012305ce511f4ebff62eee5d8ac1d04cf1462`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 13.7 MB (13670850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8fdfd86caf97edf6997707bbcc1011d128817492895e1bdc876b63d3cb41e0`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e05ab4b441b1d9d89c3d83a1d31b891d35db0f2545110649fa0bd4edf8ff7f`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 36.3 MB (36269278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792437d29c94c8908444f5d7bac3ab137a97dcc35d3b2e747a7e9bc5ac2ef62`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff945995e60d5cd72315513731d9373ac4e86e3b44e8b2dbbf795f6002d994`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 14.2 MB (14180279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384b70ff2016a63d22c4184bbc9d9a5e8e37ddf166ef6c0b90ba6c1c93ef330`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be965902c2fad22771261c6003692d4a016ed60e69965d4fcfd8b2151530b85`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522ee64ce7c540f31a936f0abdf74c4d2da79fb74463973c748b87ca74f24fe`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0dd0e50252769f64ddf91327db9a8ac5a0e69beb57981ebcaed7daa899f86968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21429cda5b858ab027425bbceb9e3bc633b63e5d330ea728bf8c869fa869ed7b`

```dockerfile
```

-	Layers:
	-	`sha256:a4b9f8453493bc459c5eb4939c7892a6399b78c556a1b6c31c4a96c6aadedb1a`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 2.6 MB (2571710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:449fb225448fcde46c06a120d2b7cb04f6e8c54799d6836c4b04ce8949cef2cc`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:6b607317da3014414a7842df80a6fb241883422776fad4114498e9b70c517e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84921642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc8847838a8a08dc6ec830976de32dfe3bcd589a90024019203bdea7d47cba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5906fa7115993d82b85acc6fb1a97330d8d2028c1d03cacfbec9beb9a42f3b`  
		Last Modified: Tue, 12 Nov 2024 10:25:37 GMT  
		Size: 11.6 MB (11622109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8481e9180c726b2560a58bf3316e9de05c4da0fc2c7bc68a6914fd4af014d`  
		Last Modified: Tue, 12 Nov 2024 10:25:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93f039578dba536a7a557378fc930028e2b97150782e70f610ef34bd26f0a2`  
		Last Modified: Tue, 12 Nov 2024 10:35:55 GMT  
		Size: 32.2 MB (32242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20643bc812a5fe537cc0b9ebcce343c2d62a2374d111d658ff729761198f70`  
		Last Modified: Tue, 12 Nov 2024 10:35:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b84ec87544cbbffea868c968be40e06e353a635b139dbdb1b15cc995d38eaa`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 14.2 MB (14165036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6d1616b7bde4c9301e0f68d13137af7e2f5eca7141679afaf7d6a8237b93c`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb713cdeb75228820c14aed371772e0c8086a239a337145d84d28e48fd870752`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2bcfbf6e686427042203e9682915fff4eba7b33d11bcda0b91e6f9df3257a`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fde6621a7e49f63e7eebd75c9f0d614590bcbc2c882bcb6e12855e19a5d4f798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9f7c682177588b9bd95a1debce573ef4c4bc45809ee562e2a2c3100b3a5ed9`

```dockerfile
```

-	Layers:
	-	`sha256:a29d98d20453062db89c66ff23a7dd11d1f4996613c0a3b03c77c9f9c0cb2f87`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 2.6 MB (2576449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32d1927eeb7574414cc514f470f934454db5704a71ee5493e7f724ceaab0f6d`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:689d47e3e8054aa50374dddb8d6ccfc9c3488f2e7e47c19ede33458f51294e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81850102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffd980a15db19bd4803a0eb9666fbccd528c487f0873b8a03be2f7d4e1df67f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f34fa6d5f96840b646a0c90acc1554160d7f199183ba7b17e5795aa4677d7d`  
		Last Modified: Wed, 13 Nov 2024 06:05:11 GMT  
		Size: 11.0 MB (10961903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c784f7d0f43345e4b550058872fc4197d6190db00a868aaaeb4f9a3ef00f81`  
		Last Modified: Wed, 13 Nov 2024 06:05:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d82171d3440b57cc9c19aecd47a0c585772cb7f202274d0b897726f224ddde`  
		Last Modified: Wed, 13 Nov 2024 06:26:33 GMT  
		Size: 32.1 MB (32082572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6d4b99eb8601f8a8997376ad8a6552260aeb2cc949711d3e6e908bb43893d5`  
		Last Modified: Wed, 13 Nov 2024 06:26:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7e53c5fc339fe8682f4677637769d739bd21c9b01127075ca28870cdc79a55`  
		Last Modified: Wed, 13 Nov 2024 14:24:21 GMT  
		Size: 14.1 MB (14084312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f3e986cf1338ccb9abcfff173a396cca682a5dbc432076553b5ea1e250e7ea`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78821b0b7c20d1449f3454c5112a3e80a00236786dbdeefaaf2f2a4290f5bf97`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6cccd5f15f633c6fe2f36ba7e23e856049f1e312c72162ee377262cfbd10`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0a83a02e990e17062cfe621dbdd85b14da6b88e83f443323b86377ed3c05a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dd7da5c9b1a2731bbc84667c09e37e486d1c3890034da2ad09b28c5dcb4779`

```dockerfile
```

-	Layers:
	-	`sha256:93cd2c8e0c022f370a1fa0142045f66d577847312bc487617e7afcfb91593abc`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 2.6 MB (2575198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2738fcaaf876ce5b1d318cea76748c32c4218b0df07b91dfeccf31f19691f05a`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:c8160f241e8b889bceb5b73d5c53d1752cdc9ec549d37b16617ee21ca78e53ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92300044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9793d40704b4c44470ab0912ede0b1591934a5f77dcef335a176c394a2b1345`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb695f97103470e35fb2e70d0232e5b648afc2b6ebd4bc359837bac092f7680`  
		Last Modified: Tue, 12 Nov 2024 23:54:57 GMT  
		Size: 12.7 MB (12708339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be1fb58a40d407f9d681171188cf062bcef1801a011a0ecb20893051ca1364e`  
		Last Modified: Tue, 12 Nov 2024 23:54:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0446da4693731cf3d730a62992e39cce6bcb01a9af0b44452dfd73dd9c2e0`  
		Last Modified: Wed, 13 Nov 2024 00:16:48 GMT  
		Size: 36.3 MB (36251966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922d82cfa1682c028f8df64b92ea109ed9e2355f22bba4b9b01ec0730abe02e`  
		Last Modified: Wed, 13 Nov 2024 00:16:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90060460a6d50faa1ddf3f0a60d1f33d258858d5d291d8b124ca01a94e2e6d`  
		Last Modified: Wed, 13 Nov 2024 07:07:58 GMT  
		Size: 14.2 MB (14179979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40ed001d20e1e460289df04266f6cf657cc4a7be7c645353ae0285ed1f5fef0`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead5fed6fb144ef1c11ef5fee346f650859df9394fcf61d38d3c34ffef4d495`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fad3a6a8eb0e057b06c013fad1122797cbad92fc62a63459f5ee47ca89dd8d`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6b160cad31ad3185db5064b479563bca64fe2a4fcd99bf59200d9bde93af8f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f2eff8e85456461dccf53375dc84e477c862b2bee60eac7f71822e3a09d211`

```dockerfile
```

-	Layers:
	-	`sha256:5d762f275ebbe5f7d3ef388f2f57ba3952669bc548faeead11867f7fb4181c95`  
		Last Modified: Wed, 13 Nov 2024 07:07:58 GMT  
		Size: 2.6 MB (2573202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05942c79f67e0d734c7a9b0ff1912cc30814fe29128c7991e68766f4ad321b77`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:298a736b41999a6094b646b74c72170ac89f5dacbb0d01544636d8cc9cfed3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88485940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ac90be5336ae05aabbec6b377c4bc9144f57f3c81e008bdf9d03b920af4d2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93bfd42dab87128d6ad5008b29506784eeb8c0cb5902904b319665c5f6b428`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 13.2 MB (13224995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdc371f408e37970b1431a564ba75d58f8c150a0271708fc1bed842e5805223`  
		Last Modified: Tue, 03 Dec 2024 02:33:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2535b3fd053a5cc5e3ba5cec933296609ca88ab8c0145acdec5adc355de541df`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 32.1 MB (32081003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31ef648709524c35c3c8809900ed1c9ae4bc938b086b54c11dcb2fc8003e60`  
		Last Modified: Tue, 03 Dec 2024 02:34:04 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365166989b81f281b3aef724a72524f9ce3130eece0de0c2a906a3dd4526c8cc`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 14.0 MB (13972052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba2e7e33ea33c25d08a1999140ab0076daf4d89890bfcb4c6d9c35f454bb03`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b927287c9e11f7673b697115ede99e73dd5b336626dc8516d3d88f17b3eafa`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e9b5b9309be97c04f733ba060bf913180986ef9456c5fc1d44106ee9b97716`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fad708008d3f69cf0b0e7e9bd18d2fb5db52a43acd8d2e788ac16ad60d41a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b639cf2e4486303575d5cc94fbf00a062721ad809e97a965ad7d1de8fd55d301`

```dockerfile
```

-	Layers:
	-	`sha256:cafff90b6e2c1495a0672718b8ec3a95eab06c56d0cd83284994fa906c0a59cb`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 2.6 MB (2568833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db409ee4123a23fd8817f8d8233bd7443f2b20d14cdda55bc1adeb283bd3c758`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f45fd6c123b77d2f841e994959567d5212afd33f1aaa315f2643f6d5b8ec324c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96024614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147092562cf8c120467063bce3b53c3e454b607e561df85a067df379288421f4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b133fb4fe27d1b5712d5d7520c0fdb58781d30453ef001d30434cc9420b5581`  
		Last Modified: Tue, 12 Nov 2024 14:10:32 GMT  
		Size: 14.6 MB (14594671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55aa781775efd2072960cdae59b014cbf4e391a2963e2a696e14988419d75e6`  
		Last Modified: Tue, 12 Nov 2024 14:10:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64fe4f911cedf6a3c1b1fdaf98f430db917a7de9e7c185c65283631badea7b`  
		Last Modified: Tue, 12 Nov 2024 14:29:45 GMT  
		Size: 33.7 MB (33730042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81625df79783eb5159909e2be2f22c0cde69d091d34d548db6f4f68698fcfd45`  
		Last Modified: Tue, 12 Nov 2024 14:29:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b434bb88f5800b1cda8962c6454b6481815bbef5a87c53f2d6148623e0a2b5e`  
		Last Modified: Tue, 12 Nov 2024 22:59:46 GMT  
		Size: 14.6 MB (14572148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5f7ca2b5604f7c75b5c70fac368edb79ba8aa0d4105dd685da3a54e2861a4d`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e36c6f27a961fad705c6c45dbe4ad3a18a9b05848d568e04dc984b3611cbf`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5364fd33a353ebc86476409bab9f0139122060ae09a8c3c6e89d71c30584a7a9`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ad38b4d1cb2a41c8fa1a130149b051fbcdf2e1c98fac501b9150296c2252ad19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6113376bd6e0be719f6d6c16e462697833954adb8d8927a55af2deb2cbdb79`

```dockerfile
```

-	Layers:
	-	`sha256:25c2c52c01147036ad0b18fc8a9167cacbe7d5deae5b750e107415d1a8b9301e`  
		Last Modified: Tue, 12 Nov 2024 22:59:46 GMT  
		Size: 2.6 MB (2577305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e465a5c2efa78ac6eff9ef305184456599c2b3c79d3e9509dac50faedd3d360`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:508044ee4101784dfe6ec4b77de1f14a627036ae643296d68351bea1f5b77577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86863571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fc3904b3d031bbe0cf88ac435ae55d4be8bf1bff2f463619e1a0a714ae19b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35582e0be2a8a6ac4177a3ba2b91a8c95996c721c8fe3ed562416edbb4b0c491`  
		Last Modified: Tue, 12 Nov 2024 21:34:02 GMT  
		Size: 12.0 MB (12042758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82736cf35477bdcd28547bfae52af65b613fcd12765ac421680d293cddfc479`  
		Last Modified: Tue, 12 Nov 2024 21:34:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1f591e44e311f3c5809e8aef25afbf5a1148589b01be62022ab2679c5d64a`  
		Last Modified: Tue, 12 Nov 2024 21:55:47 GMT  
		Size: 33.0 MB (33014634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d918453e85e18b6f87cd660f71c9c767cd46df1baa296a59130c0face46b8`  
		Last Modified: Tue, 12 Nov 2024 21:55:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04225f4917db82d8f85a0033a28fd4f7ba7f51c657bfdf45fb30a48690377756`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 14.3 MB (14312148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262b8df0f26952daa6038e3c5277a8e4191992b868479f7ed014ca28b0b6637`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb16777eefbe9d69becd1f82a1f9ae6cdb3598833ebe33bfa978599435a024`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03832765ca7c748ba3b785669c23f3b56edafa4d1e2484ee0b701fef60425ef4`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6e07646e4af02c57a818938e34ca75205fd2aad5ee8ed938d00fd129b76ef6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d9af06129525b271bfb80f7b8d94d807b6ec2a6c7e1d96a01e1387a8ef257`

```dockerfile
```

-	Layers:
	-	`sha256:c0c0044afec568368bd82008c2a5a1279bbb8251f744a976f4f8bc0fc9340632`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 2.6 MB (2572671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac996e6624eca4fbda45d0bd92db53472a7fbe1e525198ba14e9e6a5f3e414a`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 21.1 KB (21108 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-1.0`

```console
$ docker pull fluentd@sha256:f8617b7144d5598a19475b1148d78576498b903a1c801e60e680de1b8b1dd198
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
$ docker pull fluentd@sha256:de7f2b470a5aa1839b88d1a6d356cb216fd4e3cec5b8f7436b4cbb7c244071a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17500754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa143d7c6eecb27e51444f79cd2fb7d5bf306c55f9a3b8a94c072fd68eb4d7f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03641aeb8487523c7557972c6511abb652f675a8a765620e1fb5d5b427eb8ab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 14.1 MB (14078862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb70e9a7cf252f51c69f58040fee493434c3225d154250faa22f9dde6000c76`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a935d220d11a5de7fb09b611fad2ddea6f99eaee887d69a7cca3b226e1c56f31`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892898ae358c92a59eb961338015d38b9ffa6bc34c38557304ce5742dc6d1b58`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1c25323a850aa8fc3b60db7b6f9fa36a5da2aa4f545c1f1f39dca9e03e28193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.3 KB (983334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b6728df6c69cb3d78a6b393273af5d50dc492228e3e04950b1baa94a06ef4`

```dockerfile
```

-	Layers:
	-	`sha256:1f076be1586d715022168f1d93306a92fb19700d34ce7f869953282f0b063d69`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 969.7 KB (969657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b9d1a7fc7196f27b8dca7a78a9059eb3623e33c3b7122e3dcdccd29faf88db`  
		Last Modified: Tue, 12 Nov 2024 02:50:40 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:b90fffb9caeb6dfa5148a8aa1d93e97ebf15e6f546ed4bfee6c0fbf11c61b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16249953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247cb9c0d2332aa78766bcd355b7dbff88e8a437fbb2f26c8c32171318af9795`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a137212c82376d24e903c744caca7e2a9d045b04027583162cebd79d074a34`  
		Last Modified: Tue, 12 Nov 2024 15:34:51 GMT  
		Size: 13.1 MB (13071353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a7bcf0d170c6cfa424680bff249c56dcc1cd13485f93b9606cd198edca806`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2af3e4f074465e23c2dc98db0d76824b13c89e3529a769ea830ff2515b5dce`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aed04ce0ab3b7686f54f8fb77b0cf6824087dfabb686e7535bde97ac536573`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c413d6623822df7a470fdd386d964200dd800688348d5bd6f5b57073652c5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f760e68145be2fa93a5790b01fbb0293e7cb3524154f70ce7ce3ffcf53c77bfd`

```dockerfile
```

-	Layers:
	-	`sha256:c056af5ec9594afb77ae52bcc5cbe7b93247a9538512dcedcdb5d18e74517f6b`  
		Last Modified: Tue, 12 Nov 2024 15:34:50 GMT  
		Size: 13.5 KB (13533 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2d66f7fd4262b7663eccf4880d263833ff6927006f6e1473f5349d087b9b4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17483875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981f22752bcd0108721527a5c1bcf7d69568689f77ce09e6363f9c54ad07c80a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2edce25880d7cabc493be5a926661b3d5968abb8644f08cbe77417b9eeab5f9`  
		Last Modified: Wed, 13 Nov 2024 01:42:07 GMT  
		Size: 14.1 MB (14122459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f7b79eb872b316bb439f4fc558ebf5dffce72816c8b11d4ff1a6f2adf40c4`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10a38889725963cefe622795097205c6ecba2ebd4963aaedae5bc4eda7b14d`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a6d89f20fbfe383f01f73ee53a40f67ef0fdf8c39f225ace14a25820a2291`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7d3958bd8af52b4633fda4572cdba2b9a4a87a21ad3810bee1db42300541007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.6 KB (983558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd3a08fdc1a3d2e79b971151eb10f3fd13e8279ff8776079410b1db5f02172e`

```dockerfile
```

-	Layers:
	-	`sha256:00960a9f0196875b4f3f71807f6e37102e47eb255d2224ea23f0111f52b9b33d`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 969.8 KB (969787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d676dd06b29ba72c8229a11fb205987ea6290c79f02e81768f046fc42630b805`  
		Last Modified: Wed, 13 Nov 2024 01:42:06 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:129d1f0274285b657427b655dd7a1e1a7b15b136f05d5040cc502666db4138ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16457092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd32b64afd7e3abd8b2f32c4041cc79ef9ac8d897d5d89dcc1d84878fcd0aef`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de2501f0638fb1825bfa3cd5528a4ef79593a2d8dd2920f645d023f6b8ea460`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 13.2 MB (13201260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cbca890db0eda508f438975ae9cb52ac4fe4d51e6f2d60e1674c79d82dcbc1`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3312511bfca0ab90a65ac84d3255bbbe430cb65b07bcc84a9a18e12886f8c89`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d7888aff12cdd446d772795473f6f803c4ea88b2f52f65c2d73cf699a11f5`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:28fec255d83e725e41dcc05a47494cd6dc7effc4d2dc91a3483745ed9843ffe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.2 KB (980235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb3b3b2b9de0b2e5dffec31e6e6a59af172b0e883770aabcecb08af438e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:941551f158457265f17f9fb98b40a1f75930060668156dbb68bb074ab99cf7a2`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 966.6 KB (966582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691ad8f14775bc9b667b1b4b49380611c49b99b7a53caf2363330496c61ffe1f`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7720a20f726d3e22630c6a279ffc91525850f3b348daaa59a0c012cc7f30e0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffa1612724ccf90daa43116353b4508ffc06d155fea9fe2497df9e05f81fc81`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86615fa6317b3080aeff3038928587d4efd4853ad311cb77bbe9ccea62fb39b`  
		Last Modified: Tue, 12 Nov 2024 14:59:00 GMT  
		Size: 13.7 MB (13684370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396205a671deaa675898069a51c8265ff555108e7804e65029727248482ea114`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c505d257f4da424c5b9bdf9c0adecc893c46a1b87cb928962a0b6cfad71c7d5e`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cc99c342fe219810afa0a89232bed051f7ebb977fe0f1266fc48090ba2cb56`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:432c39e1e5824abc9758289a93a64c9ef5b7b43eea15c4874959675b90769139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65f4db6cb5ab36c3c473c9cefc1546d7257df636ca653a121d0d56cb62face1`

```dockerfile
```

-	Layers:
	-	`sha256:df2a772c1c4eef6371f21254ca41d5eb0371d4b4c290947b9ddc9d44b455957d`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 965.4 KB (965351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bbf015a43c99a5ce1d0282630c36de55c543bbefc35c367ab52a0aa7bb9cfe`  
		Last Modified: Tue, 12 Nov 2024 14:58:59 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:4153a0ca6dbf827b942065a3e863913538e0d7ddb2060b3493d569040a1aaae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7b00286be8f5078a0faf743739504fddfae478159ea260162dd848e0114046`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
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
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95aa75a013c883c3c2183016bbde406128defbc1f8249fe42abbbf7985575359`  
		Last Modified: Tue, 12 Nov 2024 22:31:19 GMT  
		Size: 13.7 MB (13651889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e678b44ed64915bfda888b997b3efd985d3f708f88bf46989a7f16c86a1bf8`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd845673731e045b3a4805a2c79928e5a2cdf35cbb22d8457e352eefa902e84`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a73234b6a3edab5c451d8e45b93c365272b7040f4c44fca5b0add4e93d4cfe6`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9f7e2f6395d7c48db009202306b54cb0280c2c095000fbf860d8c924012bf14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.4 KB (978418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f198834a86d812cb947f18525038288e9ae90dac324ada0bf52435a284a606`

```dockerfile
```

-	Layers:
	-	`sha256:2edd6bebb903cbdb26ea1b8673bba667839babea7740f5cad7b3a07248caaea6`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 964.7 KB (964741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae62c50f15a9e60099b508f4210c892718086b8eaba9053abfcec1a10b966fcf`  
		Last Modified: Tue, 12 Nov 2024 22:31:17 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-debian-1.0`

```console
$ docker pull fluentd@sha256:2ddd8f4624148eaa1cb19585b810546b21d5c9ab4224f50124912998356a5d76
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
$ docker pull fluentd@sha256:20b7318587d8406361e3da1d46fb6a03b635f85afb76aaa86757cd3830d92fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92354390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb963ba47026f88e61311fa798a70fcf15f0554f0cbe5f4b9dbd80e47407f919`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9bd057b20c983b5a5dd8b564012305ce511f4ebff62eee5d8ac1d04cf1462`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 13.7 MB (13670850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8fdfd86caf97edf6997707bbcc1011d128817492895e1bdc876b63d3cb41e0`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e05ab4b441b1d9d89c3d83a1d31b891d35db0f2545110649fa0bd4edf8ff7f`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 36.3 MB (36269278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792437d29c94c8908444f5d7bac3ab137a97dcc35d3b2e747a7e9bc5ac2ef62`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff945995e60d5cd72315513731d9373ac4e86e3b44e8b2dbbf795f6002d994`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 14.2 MB (14180279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384b70ff2016a63d22c4184bbc9d9a5e8e37ddf166ef6c0b90ba6c1c93ef330`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be965902c2fad22771261c6003692d4a016ed60e69965d4fcfd8b2151530b85`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522ee64ce7c540f31a936f0abdf74c4d2da79fb74463973c748b87ca74f24fe`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0dd0e50252769f64ddf91327db9a8ac5a0e69beb57981ebcaed7daa899f86968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21429cda5b858ab027425bbceb9e3bc633b63e5d330ea728bf8c869fa869ed7b`

```dockerfile
```

-	Layers:
	-	`sha256:a4b9f8453493bc459c5eb4939c7892a6399b78c556a1b6c31c4a96c6aadedb1a`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 2.6 MB (2571710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:449fb225448fcde46c06a120d2b7cb04f6e8c54799d6836c4b04ce8949cef2cc`  
		Last Modified: Tue, 03 Dec 2024 03:28:33 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:6b607317da3014414a7842df80a6fb241883422776fad4114498e9b70c517e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84921642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc8847838a8a08dc6ec830976de32dfe3bcd589a90024019203bdea7d47cba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5906fa7115993d82b85acc6fb1a97330d8d2028c1d03cacfbec9beb9a42f3b`  
		Last Modified: Tue, 12 Nov 2024 10:25:37 GMT  
		Size: 11.6 MB (11622109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8481e9180c726b2560a58bf3316e9de05c4da0fc2c7bc68a6914fd4af014d`  
		Last Modified: Tue, 12 Nov 2024 10:25:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93f039578dba536a7a557378fc930028e2b97150782e70f610ef34bd26f0a2`  
		Last Modified: Tue, 12 Nov 2024 10:35:55 GMT  
		Size: 32.2 MB (32242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20643bc812a5fe537cc0b9ebcce343c2d62a2374d111d658ff729761198f70`  
		Last Modified: Tue, 12 Nov 2024 10:35:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b84ec87544cbbffea868c968be40e06e353a635b139dbdb1b15cc995d38eaa`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 14.2 MB (14165036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6d1616b7bde4c9301e0f68d13137af7e2f5eca7141679afaf7d6a8237b93c`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb713cdeb75228820c14aed371772e0c8086a239a337145d84d28e48fd870752`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2bcfbf6e686427042203e9682915fff4eba7b33d11bcda0b91e6f9df3257a`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fde6621a7e49f63e7eebd75c9f0d614590bcbc2c882bcb6e12855e19a5d4f798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9f7c682177588b9bd95a1debce573ef4c4bc45809ee562e2a2c3100b3a5ed9`

```dockerfile
```

-	Layers:
	-	`sha256:a29d98d20453062db89c66ff23a7dd11d1f4996613c0a3b03c77c9f9c0cb2f87`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 2.6 MB (2576449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32d1927eeb7574414cc514f470f934454db5704a71ee5493e7f724ceaab0f6d`  
		Last Modified: Tue, 12 Nov 2024 14:07:17 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:689d47e3e8054aa50374dddb8d6ccfc9c3488f2e7e47c19ede33458f51294e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81850102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffd980a15db19bd4803a0eb9666fbccd528c487f0873b8a03be2f7d4e1df67f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f34fa6d5f96840b646a0c90acc1554160d7f199183ba7b17e5795aa4677d7d`  
		Last Modified: Wed, 13 Nov 2024 06:05:11 GMT  
		Size: 11.0 MB (10961903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c784f7d0f43345e4b550058872fc4197d6190db00a868aaaeb4f9a3ef00f81`  
		Last Modified: Wed, 13 Nov 2024 06:05:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d82171d3440b57cc9c19aecd47a0c585772cb7f202274d0b897726f224ddde`  
		Last Modified: Wed, 13 Nov 2024 06:26:33 GMT  
		Size: 32.1 MB (32082572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6d4b99eb8601f8a8997376ad8a6552260aeb2cc949711d3e6e908bb43893d5`  
		Last Modified: Wed, 13 Nov 2024 06:26:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7e53c5fc339fe8682f4677637769d739bd21c9b01127075ca28870cdc79a55`  
		Last Modified: Wed, 13 Nov 2024 14:24:21 GMT  
		Size: 14.1 MB (14084312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f3e986cf1338ccb9abcfff173a396cca682a5dbc432076553b5ea1e250e7ea`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78821b0b7c20d1449f3454c5112a3e80a00236786dbdeefaaf2f2a4290f5bf97`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6cccd5f15f633c6fe2f36ba7e23e856049f1e312c72162ee377262cfbd10`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0a83a02e990e17062cfe621dbdd85b14da6b88e83f443323b86377ed3c05a705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dd7da5c9b1a2731bbc84667c09e37e486d1c3890034da2ad09b28c5dcb4779`

```dockerfile
```

-	Layers:
	-	`sha256:93cd2c8e0c022f370a1fa0142045f66d577847312bc487617e7afcfb91593abc`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 2.6 MB (2575198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2738fcaaf876ce5b1d318cea76748c32c4218b0df07b91dfeccf31f19691f05a`  
		Last Modified: Wed, 13 Nov 2024 14:24:20 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:c8160f241e8b889bceb5b73d5c53d1752cdc9ec549d37b16617ee21ca78e53ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92300044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9793d40704b4c44470ab0912ede0b1591934a5f77dcef335a176c394a2b1345`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb695f97103470e35fb2e70d0232e5b648afc2b6ebd4bc359837bac092f7680`  
		Last Modified: Tue, 12 Nov 2024 23:54:57 GMT  
		Size: 12.7 MB (12708339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be1fb58a40d407f9d681171188cf062bcef1801a011a0ecb20893051ca1364e`  
		Last Modified: Tue, 12 Nov 2024 23:54:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0446da4693731cf3d730a62992e39cce6bcb01a9af0b44452dfd73dd9c2e0`  
		Last Modified: Wed, 13 Nov 2024 00:16:48 GMT  
		Size: 36.3 MB (36251966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922d82cfa1682c028f8df64b92ea109ed9e2355f22bba4b9b01ec0730abe02e`  
		Last Modified: Wed, 13 Nov 2024 00:16:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90060460a6d50faa1ddf3f0a60d1f33d258858d5d291d8b124ca01a94e2e6d`  
		Last Modified: Wed, 13 Nov 2024 07:07:58 GMT  
		Size: 14.2 MB (14179979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40ed001d20e1e460289df04266f6cf657cc4a7be7c645353ae0285ed1f5fef0`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead5fed6fb144ef1c11ef5fee346f650859df9394fcf61d38d3c34ffef4d495`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fad3a6a8eb0e057b06c013fad1122797cbad92fc62a63459f5ee47ca89dd8d`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6b160cad31ad3185db5064b479563bca64fe2a4fcd99bf59200d9bde93af8f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f2eff8e85456461dccf53375dc84e477c862b2bee60eac7f71822e3a09d211`

```dockerfile
```

-	Layers:
	-	`sha256:5d762f275ebbe5f7d3ef388f2f57ba3952669bc548faeead11867f7fb4181c95`  
		Last Modified: Wed, 13 Nov 2024 07:07:58 GMT  
		Size: 2.6 MB (2573202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05942c79f67e0d734c7a9b0ff1912cc30814fe29128c7991e68766f4ad321b77`  
		Last Modified: Wed, 13 Nov 2024 07:07:57 GMT  
		Size: 21.2 KB (21203 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:298a736b41999a6094b646b74c72170ac89f5dacbb0d01544636d8cc9cfed3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88485940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ac90be5336ae05aabbec6b377c4bc9144f57f3c81e008bdf9d03b920af4d2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93bfd42dab87128d6ad5008b29506784eeb8c0cb5902904b319665c5f6b428`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 13.2 MB (13224995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdc371f408e37970b1431a564ba75d58f8c150a0271708fc1bed842e5805223`  
		Last Modified: Tue, 03 Dec 2024 02:33:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2535b3fd053a5cc5e3ba5cec933296609ca88ab8c0145acdec5adc355de541df`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 32.1 MB (32081003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31ef648709524c35c3c8809900ed1c9ae4bc938b086b54c11dcb2fc8003e60`  
		Last Modified: Tue, 03 Dec 2024 02:34:04 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365166989b81f281b3aef724a72524f9ce3130eece0de0c2a906a3dd4526c8cc`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 14.0 MB (13972052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba2e7e33ea33c25d08a1999140ab0076daf4d89890bfcb4c6d9c35f454bb03`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b927287c9e11f7673b697115ede99e73dd5b336626dc8516d3d88f17b3eafa`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e9b5b9309be97c04f733ba060bf913180986ef9456c5fc1d44106ee9b97716`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8fad708008d3f69cf0b0e7e9bd18d2fb5db52a43acd8d2e788ac16ad60d41a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b639cf2e4486303575d5cc94fbf00a062721ad809e97a965ad7d1de8fd55d301`

```dockerfile
```

-	Layers:
	-	`sha256:cafff90b6e2c1495a0672718b8ec3a95eab06c56d0cd83284994fa906c0a59cb`  
		Last Modified: Tue, 03 Dec 2024 03:24:44 GMT  
		Size: 2.6 MB (2568833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db409ee4123a23fd8817f8d8233bd7443f2b20d14cdda55bc1adeb283bd3c758`  
		Last Modified: Tue, 03 Dec 2024 03:24:43 GMT  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f45fd6c123b77d2f841e994959567d5212afd33f1aaa315f2643f6d5b8ec324c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96024614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147092562cf8c120467063bce3b53c3e454b607e561df85a067df379288421f4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b133fb4fe27d1b5712d5d7520c0fdb58781d30453ef001d30434cc9420b5581`  
		Last Modified: Tue, 12 Nov 2024 14:10:32 GMT  
		Size: 14.6 MB (14594671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55aa781775efd2072960cdae59b014cbf4e391a2963e2a696e14988419d75e6`  
		Last Modified: Tue, 12 Nov 2024 14:10:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64fe4f911cedf6a3c1b1fdaf98f430db917a7de9e7c185c65283631badea7b`  
		Last Modified: Tue, 12 Nov 2024 14:29:45 GMT  
		Size: 33.7 MB (33730042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81625df79783eb5159909e2be2f22c0cde69d091d34d548db6f4f68698fcfd45`  
		Last Modified: Tue, 12 Nov 2024 14:29:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b434bb88f5800b1cda8962c6454b6481815bbef5a87c53f2d6148623e0a2b5e`  
		Last Modified: Tue, 12 Nov 2024 22:59:46 GMT  
		Size: 14.6 MB (14572148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5f7ca2b5604f7c75b5c70fac368edb79ba8aa0d4105dd685da3a54e2861a4d`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e36c6f27a961fad705c6c45dbe4ad3a18a9b05848d568e04dc984b3611cbf`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5364fd33a353ebc86476409bab9f0139122060ae09a8c3c6e89d71c30584a7a9`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ad38b4d1cb2a41c8fa1a130149b051fbcdf2e1c98fac501b9150296c2252ad19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6113376bd6e0be719f6d6c16e462697833954adb8d8927a55af2deb2cbdb79`

```dockerfile
```

-	Layers:
	-	`sha256:25c2c52c01147036ad0b18fc8a9167cacbe7d5deae5b750e107415d1a8b9301e`  
		Last Modified: Tue, 12 Nov 2024 22:59:46 GMT  
		Size: 2.6 MB (2577305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e465a5c2efa78ac6eff9ef305184456599c2b3c79d3e9509dac50faedd3d360`  
		Last Modified: Tue, 12 Nov 2024 22:59:45 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:508044ee4101784dfe6ec4b77de1f14a627036ae643296d68351bea1f5b77577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86863571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fc3904b3d031bbe0cf88ac435ae55d4be8bf1bff2f463619e1a0a714ae19b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 02:52:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
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
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35582e0be2a8a6ac4177a3ba2b91a8c95996c721c8fe3ed562416edbb4b0c491`  
		Last Modified: Tue, 12 Nov 2024 21:34:02 GMT  
		Size: 12.0 MB (12042758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82736cf35477bdcd28547bfae52af65b613fcd12765ac421680d293cddfc479`  
		Last Modified: Tue, 12 Nov 2024 21:34:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1f591e44e311f3c5809e8aef25afbf5a1148589b01be62022ab2679c5d64a`  
		Last Modified: Tue, 12 Nov 2024 21:55:47 GMT  
		Size: 33.0 MB (33014634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d918453e85e18b6f87cd660f71c9c767cd46df1baa296a59130c0face46b8`  
		Last Modified: Tue, 12 Nov 2024 21:55:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04225f4917db82d8f85a0033a28fd4f7ba7f51c657bfdf45fb30a48690377756`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 14.3 MB (14312148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262b8df0f26952daa6038e3c5277a8e4191992b868479f7ed014ca28b0b6637`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb16777eefbe9d69becd1f82a1f9ae6cdb3598833ebe33bfa978599435a024`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03832765ca7c748ba3b785669c23f3b56edafa4d1e2484ee0b701fef60425ef4`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6e07646e4af02c57a818938e34ca75205fd2aad5ee8ed938d00fd129b76ef6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d9af06129525b271bfb80f7b8d94d807b6ec2a6c7e1d96a01e1387a8ef257`

```dockerfile
```

-	Layers:
	-	`sha256:c0c0044afec568368bd82008c2a5a1279bbb8251f744a976f4f8bc0fc9340632`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 2.6 MB (2572671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac996e6624eca4fbda45d0bd92db53472a7fbe1e525198ba14e9e6a5f3e414a`  
		Last Modified: Wed, 13 Nov 2024 03:49:54 GMT  
		Size: 21.1 KB (21108 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17-1`

```console
$ docker pull fluentd@sha256:f1125bb64c7bb45881d97adaa9c64cade20b5e394e01d9a76d0fd149f29f4d14
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

### `fluentd:v1.17-1` - linux; amd64

```console
$ docker pull fluentd@sha256:69a66ab121b1c527705ca5b0b3f2107ca64ca8837f9313dfd26bcaf1c34b7a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17541449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a570051e688f5f0a0e0cd20067931161c8859d7021664f26eec1ba1949f8b1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26fb14d9f03d80d6a351c8550f2b721cba57c484408e56a16406f701ed4672`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.1 MB (14119554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd7f3a2916614f7b93545575db2733e723a11faf4b012a4271c0b6dac5ced5`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3312511bfca0ab90a65ac84d3255bbbe430cb65b07bcc84a9a18e12886f8c89`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d7888aff12cdd446d772795473f6f803c4ea88b2f52f65c2d73cf699a11f5`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f441cec2661401f3b0defc276f752d7104b921399e0a87ecd701c4dc16ab2e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.0 KB (986965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a66d2e9a4c9656e4d0cf33c63e6214bb3f48231e0c74c6ddd27cbe5420c3ae`

```dockerfile
```

-	Layers:
	-	`sha256:47fa7b08e14e13c09b23916953413440102c1d855613216c69d157e0f2071387`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 973.0 KB (972988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75406e0a4cac9a4904e647135877a3955d994a25b1a4e708914bfa1f1d0e72bc`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.0 KB (13977 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:ae4dbc2f60917c89ed8eee5140631b544868c0fa6f81ec2cb2b6f4317994b43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16288945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea28d6a7fa01283ab0091b2449868428f3a4c76acd1265ad777481d56d4d9b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e4314d14cdd1eab8c7bd7d04b4eb840e07e311b92701b05033f050a760fccf`  
		Last Modified: Tue, 12 Nov 2024 15:36:22 GMT  
		Size: 13.1 MB (13110344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05b8d3d3ead4020f38f21a2f5310ef4cfc5edb8d7877580a3cf051b2ae22ac`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7378acf6b163022743991c358880d6cd9ee61a81c2c5fd0b90090e436e78f`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dabe2c07d5b74dfdc5507b8187937b350e8c1492e06c6c03e6420d42a7ae26d`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a9df060029e06b23528cb4d159a6021b506153b0b9fb7dff25f8f8d9d2edd2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78e5474b3e5ff8af95f2c94de1176b441d1e184a3128f348cf51dd6384f78bb`

```dockerfile
```

-	Layers:
	-	`sha256:9144eba8609d3c066ea7ce9eaef02cc3ffbd3c4f8c7ad172b838d623540f9b13`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 13.8 KB (13843 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-1` - linux; arm64 variant v8

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

### `fluentd:v1.17-1` - unknown; unknown

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

### `fluentd:v1.17-1` - linux; 386

```console
$ docker pull fluentd@sha256:675ae0809bb2f2507b64d66c3c9294d9068269debdf988cc40262b6e9852180d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16500851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037ce743da24f109c1d2c1667da51ac4620871dfadde6bb4194bcda14f8bab16`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60bff5f2253ae5f6f66c00e94b366cb468c9dd4c6c4f97cabecc78fa7911b`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 13.2 MB (13245018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3005876d18c66acf8e80ebdedd8005b1c4a497ed6188cddd46ee88cba3dc5dad`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81f31a82e9c7c5431efec55f0f8fdce58b98ecea931d8aa5e6d9ce688cc81b`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5125f347be85a89f1ed0a15d204b9cd49a55bd49eacba23e8d17e55ce4c7c96`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c9b4fb31fb184fe2289b230466690a777e815553b73a2decf419474529a04de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 KB (983856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913899d5a3ec637e5a675b073be05c722cb2a88306c9131784e353e21308e14`

```dockerfile
```

-	Layers:
	-	`sha256:f551dda615cf4d2b56cd2c7b66efd5854bdc3cb22fc7575eb6e150f0373cf1d3`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 969.9 KB (969908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f266dace64c0749591687a9008547941918fb0be233c0051c1024fa800a5f1a7`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 13.9 KB (13948 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-1` - linux; ppc64le

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

### `fluentd:v1.17-1` - unknown; unknown

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

### `fluentd:v1.17-1` - linux; s390x

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

### `fluentd:v1.17-1` - unknown; unknown

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

## `fluentd:v1.17-debian-1`

```console
$ docker pull fluentd@sha256:81d407c945128660c4dfb6106dcd9e70b35328901e7009234fea7f4cd2d5b205
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

### `fluentd:v1.17-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:c0abfeee85925fa04744f51c28785bd2e06b962af917a2f053b9f2dfcd7f8fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91815579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183ccfbfa0e34a8e8fd331ad31b68a8e8fd3a416165d8da6d280c29cb2bce9ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9bd057b20c983b5a5dd8b564012305ce511f4ebff62eee5d8ac1d04cf1462`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 13.7 MB (13670850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8fdfd86caf97edf6997707bbcc1011d128817492895e1bdc876b63d3cb41e0`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e05ab4b441b1d9d89c3d83a1d31b891d35db0f2545110649fa0bd4edf8ff7f`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 36.3 MB (36269278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792437d29c94c8908444f5d7bac3ab137a97dcc35d3b2e747a7e9bc5ac2ef62`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a703dac3db1741b65bb0643c53abe492aef421a603a5c5e39be96e87458231`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 13.6 MB (13641468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac802c32c71adbfe9c2fb54c6c50883e2ea6467a086d0cf7182167b7156d0723`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ff6f83ede3edd25640c0ab8beae96fa4708c1ade30a6c505fd63b89433d60d`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d7674b0a6e409e456f3c58c60bb1b3855670c6c5ede16735542c1d9283040`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:15a357cb45ab43fdcc4dbd8bf9948d3e53bd814875eab786519007828184467e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9c69754fe1f5212862f245042cc2999a02e6fb598cff7a43834179dc8d899`

```dockerfile
```

-	Layers:
	-	`sha256:734ceb9b74d879ef592dd7577e5360292e2779af80e2a9a3a46591cf908a91ef`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 2.6 MB (2574727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2cda60dca58d2bc093f0ed2fca95ecd4663d0ae7728ecd93f9cac2d88d30a8`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0ae1390f6ece2c73210f954e1ffd11bade0849deec9e7ac0d12c082a258892e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84377138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987095234204683acbb9a832eea5bbb8cc8cd6b2a1d461638ffb32f579ff5198`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5906fa7115993d82b85acc6fb1a97330d8d2028c1d03cacfbec9beb9a42f3b`  
		Last Modified: Tue, 12 Nov 2024 10:25:37 GMT  
		Size: 11.6 MB (11622109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8481e9180c726b2560a58bf3316e9de05c4da0fc2c7bc68a6914fd4af014d`  
		Last Modified: Tue, 12 Nov 2024 10:25:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93f039578dba536a7a557378fc930028e2b97150782e70f610ef34bd26f0a2`  
		Last Modified: Tue, 12 Nov 2024 10:35:55 GMT  
		Size: 32.2 MB (32242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20643bc812a5fe537cc0b9ebcce343c2d62a2374d111d658ff729761198f70`  
		Last Modified: Tue, 12 Nov 2024 10:35:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49863caaed3ff5adad2fa0c1664d2ea7a109c3ccceb2125fbda5efff32075b18`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 13.6 MB (13620531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6c3eee0a4cd3078bb3dd889d62d51ee09e817f6896faaa26f5a364a33c5db5`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63131b37798bed9cccffcd3284937a529f8b2b92b584d6db6cd240bf0f7aee8`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8decb2a9071d6c68b49d7581fe143cf774e73783d5096c7726010106fda50`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bb3ca5eaaf0c42308b14377ab4947e1db2a84afd81671754675a2e2197b7b880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df77d6d1f998f50334fa1616554341d8dab183111394397233e4a78f717fe2`

```dockerfile
```

-	Layers:
	-	`sha256:c34a09284ea4986fa1387fa6aace646c51220b59931c91f3e6c1b62382d0ab1f`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 2.6 MB (2579466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab7f2baf2a12718c65e2b362ec8fd45ba09c4451e355ed82f81931b5023c944`  
		Last Modified: Tue, 12 Nov 2024 14:10:56 GMT  
		Size: 21.2 KB (21181 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:6827f451a162d0c57f5568433d219dc365653181330db36491270c4b9155da97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81304269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a25bec73754088f436db02737d900da787c2cc9edcad331ccfb27ad804f665`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f34fa6d5f96840b646a0c90acc1554160d7f199183ba7b17e5795aa4677d7d`  
		Last Modified: Wed, 13 Nov 2024 06:05:11 GMT  
		Size: 11.0 MB (10961903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c784f7d0f43345e4b550058872fc4197d6190db00a868aaaeb4f9a3ef00f81`  
		Last Modified: Wed, 13 Nov 2024 06:05:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d82171d3440b57cc9c19aecd47a0c585772cb7f202274d0b897726f224ddde`  
		Last Modified: Wed, 13 Nov 2024 06:26:33 GMT  
		Size: 32.1 MB (32082572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6d4b99eb8601f8a8997376ad8a6552260aeb2cc949711d3e6e908bb43893d5`  
		Last Modified: Wed, 13 Nov 2024 06:26:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca514934ac73cdbad67f114f5572daca6ad03090ea7a2ca8d8ae9e7cf67a51af`  
		Last Modified: Wed, 13 Nov 2024 14:27:52 GMT  
		Size: 13.5 MB (13538481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2d8b982f6f9b3981f9416bbbeb96f2e505813a17f39afaa6943e5215c47705`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1871b8e17d4fe7a6b89b956f5e4a33394aaaa4dce112468c1134a0383e323c1`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32425604064268b4f676d86c97a6caedc29a44486a9ebf2914b17a8b3de3a170`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:edacb71a608a9a7a18bcd8f07df4f04a715a34160608b38939f29d7cdeb9a683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2e1dccc79b98f6ddfdd23b6f574ae26397e1e7e1d37d3525b45f4c3fb310c6`

```dockerfile
```

-	Layers:
	-	`sha256:34b185732a5ea15b2ab5011e73ff43422efc50baa7f13037b1421159f114ab9b`  
		Last Modified: Wed, 13 Nov 2024 14:27:50 GMT  
		Size: 2.6 MB (2578215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4eb114653c11cd9bfdb83b64b7cf707e464fd7cf14491c4e0f9a9c0fae8a6d`  
		Last Modified: Wed, 13 Nov 2024 14:27:50 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d16262617442429081f3a2a0f755432b0481948ce64e6b8d1e5ed70de1e721f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91761015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd26e344799e4c6bfb831ebf4f9640d01b9be3c8f29b7bfa9d34f625518a4ced`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb695f97103470e35fb2e70d0232e5b648afc2b6ebd4bc359837bac092f7680`  
		Last Modified: Tue, 12 Nov 2024 23:54:57 GMT  
		Size: 12.7 MB (12708339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be1fb58a40d407f9d681171188cf062bcef1801a011a0ecb20893051ca1364e`  
		Last Modified: Tue, 12 Nov 2024 23:54:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0446da4693731cf3d730a62992e39cce6bcb01a9af0b44452dfd73dd9c2e0`  
		Last Modified: Wed, 13 Nov 2024 00:16:48 GMT  
		Size: 36.3 MB (36251966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922d82cfa1682c028f8df64b92ea109ed9e2355f22bba4b9b01ec0730abe02e`  
		Last Modified: Wed, 13 Nov 2024 00:16:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c31c1c783edbe0362525fccbc1dde6019a5bbba73924d4026d66b697bd408`  
		Last Modified: Wed, 13 Nov 2024 07:11:14 GMT  
		Size: 13.6 MB (13640952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55664192bdbda9034851709c0c3776ab681282fa95ce7697abaf385b349c7b2`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cabc54da637ee2fafbf4b093576747c08a2d477effc296761f537348958b3f`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1a2a01f474823c809d3157559ad9e606dff76ba339b468a6814d65c62052a7`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ee51504c1eb542626a5367892255590cc91860a5795c86d1f51da3e91a0c5743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a4522ce705f07ed8b68b219cc3088d5e3d8655799f4e1f6f7a8034f2a9d66c`

```dockerfile
```

-	Layers:
	-	`sha256:cec18e891583619b2becf9ca168f62cd40cf7d72df5c34f19ade4d856c74fccd`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 2.6 MB (2576219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e6d43fb776bc582d38efca5043625cb5cbd1079a70eb044ceb9cca0d8d873e`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:da679419a190509ce37474e42c2bc8d1a103b75a26a40664423b71a9998d6619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87946191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd7c3b9b1c68d62f366d88ea5230db9106f6ebcd7089595ba821aa351808e1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93bfd42dab87128d6ad5008b29506784eeb8c0cb5902904b319665c5f6b428`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 13.2 MB (13224995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdc371f408e37970b1431a564ba75d58f8c150a0271708fc1bed842e5805223`  
		Last Modified: Tue, 03 Dec 2024 02:33:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2535b3fd053a5cc5e3ba5cec933296609ca88ab8c0145acdec5adc355de541df`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 32.1 MB (32081003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31ef648709524c35c3c8809900ed1c9ae4bc938b086b54c11dcb2fc8003e60`  
		Last Modified: Tue, 03 Dec 2024 02:34:04 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb31506684aeb5255c200a9646977fae9eb0aec57c8187fb55a92bde4f44cb`  
		Last Modified: Tue, 03 Dec 2024 03:25:14 GMT  
		Size: 13.4 MB (13432302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ce73a97c28321e9586537e12e9f0c6b1ad389a236d4588d87e031c2f5a13d3`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e5c51c774251056934b40380c105e66637a269bb596e2c5293b06ddcf3963`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba75199b00a1b1d875fbca9f007d98623c8cd31c0918fa9fe7402ff7423893c2`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5b591833a45a32115183f8783e7643d8fc6686cbd16a3226f964ff100e1507b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c782cd2ac2b6e509616e682958e1bbd52f84544224ef3b4dc5fb5bbf545c9548`

```dockerfile
```

-	Layers:
	-	`sha256:dab8ef2f27b579bab356b52161975281cd9f95442462e5c5ec1dfc6d6af1f102`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 2.6 MB (2571850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7962cb8617a0c47d2a1081f773dcb6f8a9a3a2d0d5efdd66f657e9a698416b8b`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:dd8dc90e1a9e84260adc6d08b537f3ef1ac9d428b93edf8ff09283244f3d9a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95486365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83eb0676c789c777979f8628f9eca9c927a1c18f6d0d29970d2f636efeef1fa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b133fb4fe27d1b5712d5d7520c0fdb58781d30453ef001d30434cc9420b5581`  
		Last Modified: Tue, 12 Nov 2024 14:10:32 GMT  
		Size: 14.6 MB (14594671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55aa781775efd2072960cdae59b014cbf4e391a2963e2a696e14988419d75e6`  
		Last Modified: Tue, 12 Nov 2024 14:10:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64fe4f911cedf6a3c1b1fdaf98f430db917a7de9e7c185c65283631badea7b`  
		Last Modified: Tue, 12 Nov 2024 14:29:45 GMT  
		Size: 33.7 MB (33730042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81625df79783eb5159909e2be2f22c0cde69d091d34d548db6f4f68698fcfd45`  
		Last Modified: Tue, 12 Nov 2024 14:29:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37842465be26d03b8a800f4a257588d6f825e84935ecbaa82edaea416b2af942`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 14.0 MB (14033897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9407640565ac09f29c251dc3b580bc5257af5c4f3bd450b4b52a2fe5ccdbce`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3d3402280c8d40ee2fc7e41ff0a33b1e5170889a9235f03b157fc3f4686208`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f589ac6366ec696249fdb808789771f48966e475c3c0159474fb302008959f`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:eca1071b9e5aa204a9447147813ce05a5888b4a0528c8666bcb121ae33042c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7eba2c29d9add9ecca6de5b62352ddf267ad229d919938cf22b20e1ef15a494`

```dockerfile
```

-	Layers:
	-	`sha256:2c2fbbe19a1447dffa9fb0766350df0f9bf0d43f12ae8321da7dd398ec42c3da`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 2.6 MB (2580322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea771bdfe3d4386152efcff836deac9c76fc6909165e1878623d4cf41e293aaf`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:7b58d9f60eb8b00e97c025ef95826e3c034f32bf18219f4f1695797ee683f51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86325921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0779e3c60fc0e12043427f2d5ce6030428ab328cfa32038cf6ba57cb7eec9870`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35582e0be2a8a6ac4177a3ba2b91a8c95996c721c8fe3ed562416edbb4b0c491`  
		Last Modified: Tue, 12 Nov 2024 21:34:02 GMT  
		Size: 12.0 MB (12042758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82736cf35477bdcd28547bfae52af65b613fcd12765ac421680d293cddfc479`  
		Last Modified: Tue, 12 Nov 2024 21:34:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1f591e44e311f3c5809e8aef25afbf5a1148589b01be62022ab2679c5d64a`  
		Last Modified: Tue, 12 Nov 2024 21:55:47 GMT  
		Size: 33.0 MB (33014634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d918453e85e18b6f87cd660f71c9c767cd46df1baa296a59130c0face46b8`  
		Last Modified: Tue, 12 Nov 2024 21:55:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222448a0447d04f50fb1dc01c43646c32ec3573211a224beb0212fbdc79f2b49`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 13.8 MB (13774494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995aa7c27ca53f47a94181de9b1d046b8e47b97bc867f845ac95a3dfc82b95a3`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da4f0d2d62b2f10acedfbaddf695b452fd06f3e6e0339f4a17f2528c4f11de9`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a63518302187597a2cfc691f81515cec5179943869be9ba9c2bc4de38d79d`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b7dbd3b0245775708ba00580e05c8b45f00ac8a49fc0818745670cfa18f0ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38eb4056aaa790649db4cb1a394c24d4f01ab8fda1f9b2d38d23e917b76c1eca`

```dockerfile
```

-	Layers:
	-	`sha256:b0ff34e85f298d790e57252193c105a1925b1ac66d92d97814d835a1d764647f`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 2.6 MB (2575688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fc3397b924a0c4428499178cf340254f2dce771eeeab8b642558e2bd8830ca`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 21.1 KB (21108 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17.1-1.0`

```console
$ docker pull fluentd@sha256:f1125bb64c7bb45881d97adaa9c64cade20b5e394e01d9a76d0fd149f29f4d14
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

### `fluentd:v1.17.1-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:69a66ab121b1c527705ca5b0b3f2107ca64ca8837f9313dfd26bcaf1c34b7a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17541449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a570051e688f5f0a0e0cd20067931161c8859d7021664f26eec1ba1949f8b1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26fb14d9f03d80d6a351c8550f2b721cba57c484408e56a16406f701ed4672`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.1 MB (14119554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd7f3a2916614f7b93545575db2733e723a11faf4b012a4271c0b6dac5ced5`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3312511bfca0ab90a65ac84d3255bbbe430cb65b07bcc84a9a18e12886f8c89`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d7888aff12cdd446d772795473f6f803c4ea88b2f52f65c2d73cf699a11f5`  
		Last Modified: Tue, 12 Nov 2024 02:50:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f441cec2661401f3b0defc276f752d7104b921399e0a87ecd701c4dc16ab2e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.0 KB (986965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a66d2e9a4c9656e4d0cf33c63e6214bb3f48231e0c74c6ddd27cbe5420c3ae`

```dockerfile
```

-	Layers:
	-	`sha256:47fa7b08e14e13c09b23916953413440102c1d855613216c69d157e0f2071387`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 973.0 KB (972988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75406e0a4cac9a4904e647135877a3955d994a25b1a4e708914bfa1f1d0e72bc`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 14.0 KB (13977 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:ae4dbc2f60917c89ed8eee5140631b544868c0fa6f81ec2cb2b6f4317994b43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16288945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea28d6a7fa01283ab0091b2449868428f3a4c76acd1265ad777481d56d4d9b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e4314d14cdd1eab8c7bd7d04b4eb840e07e311b92701b05033f050a760fccf`  
		Last Modified: Tue, 12 Nov 2024 15:36:22 GMT  
		Size: 13.1 MB (13110344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05b8d3d3ead4020f38f21a2f5310ef4cfc5edb8d7877580a3cf051b2ae22ac`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7378acf6b163022743991c358880d6cd9ee61a81c2c5fd0b90090e436e78f`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dabe2c07d5b74dfdc5507b8187937b350e8c1492e06c6c03e6420d42a7ae26d`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a9df060029e06b23528cb4d159a6021b506153b0b9fb7dff25f8f8d9d2edd2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78e5474b3e5ff8af95f2c94de1176b441d1e184a3128f348cf51dd6384f78bb`

```dockerfile
```

-	Layers:
	-	`sha256:9144eba8609d3c066ea7ce9eaef02cc3ffbd3c4f8c7ad172b838d623540f9b13`  
		Last Modified: Tue, 12 Nov 2024 15:36:21 GMT  
		Size: 13.8 KB (13843 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.17.1-1.0` - unknown; unknown

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

### `fluentd:v1.17.1-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:675ae0809bb2f2507b64d66c3c9294d9068269debdf988cc40262b6e9852180d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16500851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037ce743da24f109c1d2c1667da51ac4620871dfadde6bb4194bcda14f8bab16`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60bff5f2253ae5f6f66c00e94b366cb468c9dd4c6c4f97cabecc78fa7911b`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 13.2 MB (13245018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3005876d18c66acf8e80ebdedd8005b1c4a497ed6188cddd46ee88cba3dc5dad`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81f31a82e9c7c5431efec55f0f8fdce58b98ecea931d8aa5e6d9ce688cc81b`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5125f347be85a89f1ed0a15d204b9cd49a55bd49eacba23e8d17e55ce4c7c96`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c9b4fb31fb184fe2289b230466690a777e815553b73a2decf419474529a04de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 KB (983856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913899d5a3ec637e5a675b073be05c722cb2a88306c9131784e353e21308e14`

```dockerfile
```

-	Layers:
	-	`sha256:f551dda615cf4d2b56cd2c7b66efd5854bdc3cb22fc7575eb6e150f0373cf1d3`  
		Last Modified: Tue, 12 Nov 2024 02:51:04 GMT  
		Size: 969.9 KB (969908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f266dace64c0749591687a9008547941918fb0be233c0051c1024fa800a5f1a7`  
		Last Modified: Tue, 12 Nov 2024 02:51:03 GMT  
		Size: 13.9 KB (13948 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-1.0` - linux; ppc64le

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

### `fluentd:v1.17.1-1.0` - unknown; unknown

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

### `fluentd:v1.17.1-1.0` - linux; s390x

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

### `fluentd:v1.17.1-1.0` - unknown; unknown

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

## `fluentd:v1.17.1-debian-1.0`

```console
$ docker pull fluentd@sha256:81d407c945128660c4dfb6106dcd9e70b35328901e7009234fea7f4cd2d5b205
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

### `fluentd:v1.17.1-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:c0abfeee85925fa04744f51c28785bd2e06b962af917a2f053b9f2dfcd7f8fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91815579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183ccfbfa0e34a8e8fd331ad31b68a8e8fd3a416165d8da6d280c29cb2bce9ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9bd057b20c983b5a5dd8b564012305ce511f4ebff62eee5d8ac1d04cf1462`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 13.7 MB (13670850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8fdfd86caf97edf6997707bbcc1011d128817492895e1bdc876b63d3cb41e0`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e05ab4b441b1d9d89c3d83a1d31b891d35db0f2545110649fa0bd4edf8ff7f`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 36.3 MB (36269278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792437d29c94c8908444f5d7bac3ab137a97dcc35d3b2e747a7e9bc5ac2ef62`  
		Last Modified: Tue, 03 Dec 2024 02:37:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a703dac3db1741b65bb0643c53abe492aef421a603a5c5e39be96e87458231`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 13.6 MB (13641468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac802c32c71adbfe9c2fb54c6c50883e2ea6467a086d0cf7182167b7156d0723`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ff6f83ede3edd25640c0ab8beae96fa4708c1ade30a6c505fd63b89433d60d`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d7674b0a6e409e456f3c58c60bb1b3855670c6c5ede16735542c1d9283040`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:15a357cb45ab43fdcc4dbd8bf9948d3e53bd814875eab786519007828184467e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9c69754fe1f5212862f245042cc2999a02e6fb598cff7a43834179dc8d899`

```dockerfile
```

-	Layers:
	-	`sha256:734ceb9b74d879ef592dd7577e5360292e2779af80e2a9a3a46591cf908a91ef`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 2.6 MB (2574727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2cda60dca58d2bc093f0ed2fca95ecd4663d0ae7728ecd93f9cac2d88d30a8`  
		Last Modified: Tue, 03 Dec 2024 03:28:47 GMT  
		Size: 21.1 KB (21109 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0ae1390f6ece2c73210f954e1ffd11bade0849deec9e7ac0d12c082a258892e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84377138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987095234204683acbb9a832eea5bbb8cc8cd6b2a1d461638ffb32f579ff5198`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5906fa7115993d82b85acc6fb1a97330d8d2028c1d03cacfbec9beb9a42f3b`  
		Last Modified: Tue, 12 Nov 2024 10:25:37 GMT  
		Size: 11.6 MB (11622109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8481e9180c726b2560a58bf3316e9de05c4da0fc2c7bc68a6914fd4af014d`  
		Last Modified: Tue, 12 Nov 2024 10:25:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93f039578dba536a7a557378fc930028e2b97150782e70f610ef34bd26f0a2`  
		Last Modified: Tue, 12 Nov 2024 10:35:55 GMT  
		Size: 32.2 MB (32242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20643bc812a5fe537cc0b9ebcce343c2d62a2374d111d658ff729761198f70`  
		Last Modified: Tue, 12 Nov 2024 10:35:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49863caaed3ff5adad2fa0c1664d2ea7a109c3ccceb2125fbda5efff32075b18`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 13.6 MB (13620531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6c3eee0a4cd3078bb3dd889d62d51ee09e817f6896faaa26f5a364a33c5db5`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63131b37798bed9cccffcd3284937a529f8b2b92b584d6db6cd240bf0f7aee8`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8decb2a9071d6c68b49d7581fe143cf774e73783d5096c7726010106fda50`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bb3ca5eaaf0c42308b14377ab4947e1db2a84afd81671754675a2e2197b7b880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df77d6d1f998f50334fa1616554341d8dab183111394397233e4a78f717fe2`

```dockerfile
```

-	Layers:
	-	`sha256:c34a09284ea4986fa1387fa6aace646c51220b59931c91f3e6c1b62382d0ab1f`  
		Last Modified: Tue, 12 Nov 2024 14:10:57 GMT  
		Size: 2.6 MB (2579466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab7f2baf2a12718c65e2b362ec8fd45ba09c4451e355ed82f81931b5023c944`  
		Last Modified: Tue, 12 Nov 2024 14:10:56 GMT  
		Size: 21.2 KB (21181 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:6827f451a162d0c57f5568433d219dc365653181330db36491270c4b9155da97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81304269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a25bec73754088f436db02737d900da787c2cc9edcad331ccfb27ad804f665`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f34fa6d5f96840b646a0c90acc1554160d7f199183ba7b17e5795aa4677d7d`  
		Last Modified: Wed, 13 Nov 2024 06:05:11 GMT  
		Size: 11.0 MB (10961903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c784f7d0f43345e4b550058872fc4197d6190db00a868aaaeb4f9a3ef00f81`  
		Last Modified: Wed, 13 Nov 2024 06:05:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d82171d3440b57cc9c19aecd47a0c585772cb7f202274d0b897726f224ddde`  
		Last Modified: Wed, 13 Nov 2024 06:26:33 GMT  
		Size: 32.1 MB (32082572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6d4b99eb8601f8a8997376ad8a6552260aeb2cc949711d3e6e908bb43893d5`  
		Last Modified: Wed, 13 Nov 2024 06:26:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca514934ac73cdbad67f114f5572daca6ad03090ea7a2ca8d8ae9e7cf67a51af`  
		Last Modified: Wed, 13 Nov 2024 14:27:52 GMT  
		Size: 13.5 MB (13538481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2d8b982f6f9b3981f9416bbbeb96f2e505813a17f39afaa6943e5215c47705`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1871b8e17d4fe7a6b89b956f5e4a33394aaaa4dce112468c1134a0383e323c1`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32425604064268b4f676d86c97a6caedc29a44486a9ebf2914b17a8b3de3a170`  
		Last Modified: Wed, 13 Nov 2024 14:27:51 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:edacb71a608a9a7a18bcd8f07df4f04a715a34160608b38939f29d7cdeb9a683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2e1dccc79b98f6ddfdd23b6f574ae26397e1e7e1d37d3525b45f4c3fb310c6`

```dockerfile
```

-	Layers:
	-	`sha256:34b185732a5ea15b2ab5011e73ff43422efc50baa7f13037b1421159f114ab9b`  
		Last Modified: Wed, 13 Nov 2024 14:27:50 GMT  
		Size: 2.6 MB (2578215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4eb114653c11cd9bfdb83b64b7cf707e464fd7cf14491c4e0f9a9c0fae8a6d`  
		Last Modified: Wed, 13 Nov 2024 14:27:50 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d16262617442429081f3a2a0f755432b0481948ce64e6b8d1e5ed70de1e721f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91761015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd26e344799e4c6bfb831ebf4f9640d01b9be3c8f29b7bfa9d34f625518a4ced`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb695f97103470e35fb2e70d0232e5b648afc2b6ebd4bc359837bac092f7680`  
		Last Modified: Tue, 12 Nov 2024 23:54:57 GMT  
		Size: 12.7 MB (12708339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be1fb58a40d407f9d681171188cf062bcef1801a011a0ecb20893051ca1364e`  
		Last Modified: Tue, 12 Nov 2024 23:54:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0446da4693731cf3d730a62992e39cce6bcb01a9af0b44452dfd73dd9c2e0`  
		Last Modified: Wed, 13 Nov 2024 00:16:48 GMT  
		Size: 36.3 MB (36251966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f922d82cfa1682c028f8df64b92ea109ed9e2355f22bba4b9b01ec0730abe02e`  
		Last Modified: Wed, 13 Nov 2024 00:16:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c31c1c783edbe0362525fccbc1dde6019a5bbba73924d4026d66b697bd408`  
		Last Modified: Wed, 13 Nov 2024 07:11:14 GMT  
		Size: 13.6 MB (13640952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55664192bdbda9034851709c0c3776ab681282fa95ce7697abaf385b349c7b2`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cabc54da637ee2fafbf4b093576747c08a2d477effc296761f537348958b3f`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1a2a01f474823c809d3157559ad9e606dff76ba339b468a6814d65c62052a7`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ee51504c1eb542626a5367892255590cc91860a5795c86d1f51da3e91a0c5743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a4522ce705f07ed8b68b219cc3088d5e3d8655799f4e1f6f7a8034f2a9d66c`

```dockerfile
```

-	Layers:
	-	`sha256:cec18e891583619b2becf9ca168f62cd40cf7d72df5c34f19ade4d856c74fccd`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 2.6 MB (2576219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e6d43fb776bc582d38efca5043625cb5cbd1079a70eb044ceb9cca0d8d873e`  
		Last Modified: Wed, 13 Nov 2024 07:11:13 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:da679419a190509ce37474e42c2bc8d1a103b75a26a40664423b71a9998d6619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87946191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd7c3b9b1c68d62f366d88ea5230db9106f6ebcd7089595ba821aa351808e1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93bfd42dab87128d6ad5008b29506784eeb8c0cb5902904b319665c5f6b428`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 13.2 MB (13224995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdc371f408e37970b1431a564ba75d58f8c150a0271708fc1bed842e5805223`  
		Last Modified: Tue, 03 Dec 2024 02:33:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2535b3fd053a5cc5e3ba5cec933296609ca88ab8c0145acdec5adc355de541df`  
		Last Modified: Tue, 03 Dec 2024 02:34:05 GMT  
		Size: 32.1 MB (32081003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31ef648709524c35c3c8809900ed1c9ae4bc938b086b54c11dcb2fc8003e60`  
		Last Modified: Tue, 03 Dec 2024 02:34:04 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb31506684aeb5255c200a9646977fae9eb0aec57c8187fb55a92bde4f44cb`  
		Last Modified: Tue, 03 Dec 2024 03:25:14 GMT  
		Size: 13.4 MB (13432302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ce73a97c28321e9586537e12e9f0c6b1ad389a236d4588d87e031c2f5a13d3`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e5c51c774251056934b40380c105e66637a269bb596e2c5293b06ddcf3963`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba75199b00a1b1d875fbca9f007d98623c8cd31c0918fa9fe7402ff7423893c2`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5b591833a45a32115183f8783e7643d8fc6686cbd16a3226f964ff100e1507b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c782cd2ac2b6e509616e682958e1bbd52f84544224ef3b4dc5fb5bbf545c9548`

```dockerfile
```

-	Layers:
	-	`sha256:dab8ef2f27b579bab356b52161975281cd9f95442462e5c5ec1dfc6d6af1f102`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 2.6 MB (2571850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7962cb8617a0c47d2a1081f773dcb6f8a9a3a2d0d5efdd66f657e9a698416b8b`  
		Last Modified: Tue, 03 Dec 2024 03:25:13 GMT  
		Size: 21.1 KB (21085 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:dd8dc90e1a9e84260adc6d08b537f3ef1ac9d428b93edf8ff09283244f3d9a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95486365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83eb0676c789c777979f8628f9eca9c927a1c18f6d0d29970d2f636efeef1fa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b133fb4fe27d1b5712d5d7520c0fdb58781d30453ef001d30434cc9420b5581`  
		Last Modified: Tue, 12 Nov 2024 14:10:32 GMT  
		Size: 14.6 MB (14594671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55aa781775efd2072960cdae59b014cbf4e391a2963e2a696e14988419d75e6`  
		Last Modified: Tue, 12 Nov 2024 14:10:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64fe4f911cedf6a3c1b1fdaf98f430db917a7de9e7c185c65283631badea7b`  
		Last Modified: Tue, 12 Nov 2024 14:29:45 GMT  
		Size: 33.7 MB (33730042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81625df79783eb5159909e2be2f22c0cde69d091d34d548db6f4f68698fcfd45`  
		Last Modified: Tue, 12 Nov 2024 14:29:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37842465be26d03b8a800f4a257588d6f825e84935ecbaa82edaea416b2af942`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 14.0 MB (14033897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9407640565ac09f29c251dc3b580bc5257af5c4f3bd450b4b52a2fe5ccdbce`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3d3402280c8d40ee2fc7e41ff0a33b1e5170889a9235f03b157fc3f4686208`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f589ac6366ec696249fdb808789771f48966e475c3c0159474fb302008959f`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:eca1071b9e5aa204a9447147813ce05a5888b4a0528c8666bcb121ae33042c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7eba2c29d9add9ecca6de5b62352ddf267ad229d919938cf22b20e1ef15a494`

```dockerfile
```

-	Layers:
	-	`sha256:2c2fbbe19a1447dffa9fb0766350df0f9bf0d43f12ae8321da7dd398ec42c3da`  
		Last Modified: Tue, 12 Nov 2024 23:04:30 GMT  
		Size: 2.6 MB (2580322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea771bdfe3d4386152efcff836deac9c76fc6909165e1878623d4cf41e293aaf`  
		Last Modified: Tue, 12 Nov 2024 23:04:29 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:7b58d9f60eb8b00e97c025ef95826e3c034f32bf18219f4f1695797ee683f51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86325921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0779e3c60fc0e12043427f2d5ce6030428ab328cfa32038cf6ba57cb7eec9870`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 20 Aug 2024 02:01:21 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Aug 2024 02:01:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 02:01:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["irb"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
ENV TINI_VERSION=0.18.0
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35582e0be2a8a6ac4177a3ba2b91a8c95996c721c8fe3ed562416edbb4b0c491`  
		Last Modified: Tue, 12 Nov 2024 21:34:02 GMT  
		Size: 12.0 MB (12042758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82736cf35477bdcd28547bfae52af65b613fcd12765ac421680d293cddfc479`  
		Last Modified: Tue, 12 Nov 2024 21:34:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1f591e44e311f3c5809e8aef25afbf5a1148589b01be62022ab2679c5d64a`  
		Last Modified: Tue, 12 Nov 2024 21:55:47 GMT  
		Size: 33.0 MB (33014634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d918453e85e18b6f87cd660f71c9c767cd46df1baa296a59130c0face46b8`  
		Last Modified: Tue, 12 Nov 2024 21:55:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222448a0447d04f50fb1dc01c43646c32ec3573211a224beb0212fbdc79f2b49`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 13.8 MB (13774494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995aa7c27ca53f47a94181de9b1d046b8e47b97bc867f845ac95a3dfc82b95a3`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da4f0d2d62b2f10acedfbaddf695b452fd06f3e6e0339f4a17f2528c4f11de9`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a63518302187597a2cfc691f81515cec5179943869be9ba9c2bc4de38d79d`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b7dbd3b0245775708ba00580e05c8b45f00ac8a49fc0818745670cfa18f0ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38eb4056aaa790649db4cb1a394c24d4f01ab8fda1f9b2d38d23e917b76c1eca`

```dockerfile
```

-	Layers:
	-	`sha256:b0ff34e85f298d790e57252193c105a1925b1ac66d92d97814d835a1d764647f`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 2.6 MB (2575688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fc3397b924a0c4428499178cf340254f2dce771eeeab8b642558e2bd8830ca`  
		Last Modified: Wed, 13 Nov 2024 03:52:55 GMT  
		Size: 21.1 KB (21108 bytes)  
		MIME: application/vnd.in-toto+json
