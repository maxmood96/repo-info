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
$ docker pull fluentd@sha256:185044381c7079505a3a4d2df10e0951d20ae4b036f1dcd85894add73afd631b
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
$ docker pull fluentd@sha256:9d8731ddcb491fa1b58cb0d5eec46028644dfc2a2158d64d11be0a8ece0523b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17539168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7177a0baf62585066bb57462a07622ceec99e1d8737f6ea507f4722f14bb12ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65d9421a6cf6af10f0d7efb81d38105099b7be31305ccfaaba28d380ea11c1f`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 14.2 MB (14177898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474e9013dbd28cc17bb843e54193c514cdbcd9505fbd75a5a54b1a8b252136e5`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5c0a178cd0cebd8004d4f550414c570c6533ffc36b2850aeaec23e7aa71242`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db843133adeb4397f9cc17ee9fbd4d0e145a63113fd3122ee1a9611bb58105`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:d907b289cb67872bc0a1e74604ec56f7dc8ae249856336ef98d4b1d3038fb300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.4 KB (984405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b8f5cc66aeef3f6fe22961ab8cd8a45cf4313b9c15328d3107e831b33f62b`

```dockerfile
```

-	Layers:
	-	`sha256:3e6d4bb274d92d0fa4be0e8013180cdb835f2297341da2eb6f124bc2c8a2f1d9`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 970.4 KB (970369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883b941daba7313bfee0ee5c95c9d7a96f8cda81effd1c653af564c7ab2f0767`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 14.0 KB (14036 bytes)  
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
$ docker pull fluentd@sha256:117344aa852133fe9c9416b4c3b862d8ea47156469079917b89e99b9bf776773
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
$ docker pull fluentd@sha256:83aae31b2a3489f4a45f2f5cf8545e22f46f14ce0f89d158beed02dc1929f856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b04a2aea360fd7e27f17b08daa36fe3cbfc96f809a35252250d598ef51f364`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425e7a28e3eb3b2e903e3820e27ccbf6b7394aef31d39cd5edc673b817dbc3b8`  
		Last Modified: Sat, 07 Sep 2024 12:19:35 GMT  
		Size: 14.1 MB (14135705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfeff0ee1df7e53f9c9e1f13dceeff686b9183144df8d82a5453a2f0632fc6f`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708337bab8c95d7220d40787232afb2550f89f890d3429e69f6e475b4e23f041`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db6ef513149c1dbdd10ced86efdd01c6a840e91377d4cc711d5fe56deb483d`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b5ea461d5703d947e3eced352212b0b1208a8aa256b863c89d17a4e3ac8b4471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.0 KB (980964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d46bfa908b60f83810534fa2ee9e9462ef19afd057e85673fd2a0b112cf0f63`

```dockerfile
```

-	Layers:
	-	`sha256:774dc52d7be13d1e88c96591aaa8e2ad6aee4bbefeac51ec0a702e67ca0ecc94`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 967.2 KB (967238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b54499f65299860a91eb342736d9ef90bc2c538502e3c4a2f971efabd5b18d`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 13.7 KB (13726 bytes)  
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
$ docker pull fluentd@sha256:bdd92d6edc1ac6d202e3cd31dbc7865dc497b568649faed0e550af52be620f4d
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
$ docker pull fluentd@sha256:9da62dfaf1f141ab79b60ff4d5c2da63753e34df033d328c151ebf45b5ceb97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93442482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c7386b124ff6784a982e8dac2b622d932ccad68438b8b68cf429da27254456`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7012cfae44fce24d2ce87b1df401456980e1e80d0bee35658df2d8f1808721`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 13.9 MB (13862683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8433d702d5ea937ff393f1d72a225ea1ece977860e78a82cb7ea86288c8180`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080b50a59c1101198321da9ca33b8a8a2bbc065b8d6ca91461398d6bcd64498`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 36.3 MB (36268931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c3535124be18673a2aa4e532798fb8102d65056fb528a79d10a77c0e0296cb`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1927e6fc42facfdbaa76624d1e65919811578a24b0423727c3e8960057d79a0`  
		Last Modified: Tue, 12 Nov 2024 03:20:40 GMT  
		Size: 14.2 MB (14180477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f078f819da02eb9bff44b3149d5846de67ad2b71f7f76d6322967b72aa747e`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d71c28bf81a4316b3cf4763990281bebe3a94bd3e0cdbd7323c0e3bc994357`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06efdf902ca533ce544c244e5755a8b46bc6bc65d6a302a9012f48345f095a4a`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfc8bb1687c8c641462c80c22e3ad9029c624f3a986e6392fa58d02c14102f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5aa7eb4bada9598dd87e98518ef047e0e9e80f3ca287e77fdb0960341d1ba1`

```dockerfile
```

-	Layers:
	-	`sha256:362a168462864382e853204300602cba248e914b9f3aea5048315277a45824ae`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 2.6 MB (2572958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee768fc44b088c5e34c7fb7e78c6d201ef15163d8a0c4db753779094fd6c6e44`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 21.1 KB (21109 bytes)  
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
$ docker pull fluentd@sha256:564ac8e0583f421346736f177cd63b236f5c4ed2955fc3cb127bf23aca8067aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81852665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d113ada12fdc1b0e5acfe1404c60b23222113bdf5bdbef395418253e97a9b29`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad165fb974bace21f0a023b5b89416ab63e61be2107ec588eb1e3237717f2848`  
		Last Modified: Fri, 18 Oct 2024 01:28:48 GMT  
		Size: 11.0 MB (10960451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56512ba6b2a6c37a25326a81238b0efa1d28a20513e43854cb3a8fb21267af`  
		Last Modified: Fri, 18 Oct 2024 01:28:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3545c4b2a964c6385519f5ebdfc110f670a59349b8c5eaaf5bf904919195630`  
		Last Modified: Tue, 05 Nov 2024 21:31:52 GMT  
		Size: 32.1 MB (32082341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bd711a6e07a75055f2d01100ec86ec8cf1cd1d86dc92f31a043dd39e0e2e5`  
		Last Modified: Tue, 05 Nov 2024 21:31:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cfea4c1fab45c88e7a6fe84f6993173ed83ea187e121d7edda11a6420a162e`  
		Last Modified: Tue, 05 Nov 2024 21:53:29 GMT  
		Size: 14.1 MB (14089267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0088b647c0146a60b53c5aa08b2c47b66435b3eba378e7ac43c9136a7360054`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8286d8c8561a2c0e4bc2e8250f43ada539397eb6a861ff0b554b72e582e11`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53d04e17c697ac1c99dcb22a52ba7ac05b243312a7af26a7e2ddb1ccd5c6b5e`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:caad970f1e08934b1455e230bf9d54e9a165f358a5482b0aa83e210d9f8c6c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87256ae8b95f1afb64e06cae3508ba8b4e69bfd54f91cc768cf2b387338f93de`

```dockerfile
```

-	Layers:
	-	`sha256:16d90a0c8ccc53652985f8eab3a1ab86d6b43a5083a71dbefe6a6ea9704c77f4`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 2.6 MB (2575198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8357c6dbb70dc6853479b2f1a97aed2ed8e32249e1f2be6145a3396514a25dd3`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:9ed6a59c166e7d61a6d48d8ee53b02ea6a5320eb8bab305c7a84207af20b8039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92301693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d01083a504ef623cb26c1633ca015d1353d362b53a20f6fb04c1bdd83600ba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15fa32e5c8f64ba8c5dc13eeb40a1f4b4139996b89fa1ff32fdbd39d393ee13`  
		Last Modified: Wed, 30 Oct 2024 19:10:25 GMT  
		Size: 12.7 MB (12705660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dcf4909f6f483e882642f22161f8fc2dfcf3a570e53433d1479bd85ea99340`  
		Last Modified: Wed, 30 Oct 2024 19:10:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478d67e130011c48845bca1140e27bcf71b2a3872fbe7a079581663b39921de`  
		Last Modified: Tue, 05 Nov 2024 20:51:22 GMT  
		Size: 36.3 MB (36252077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dd28dbda175405a8ac35c24dd24def830939114acc3a4c406fccf4b6bd418f`  
		Last Modified: Tue, 05 Nov 2024 20:51:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb600779c326d31d4dfc9c8de0bb7381005238d81971442aeec95524824f619`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 14.2 MB (14185210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675a560e81ddfdab5c4aa812a77b2da8b2f081948891b787315ced271f55e0`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77550c0f03ff328448113f56264b4deecffb3ae11b21f7a645342a43fcbe146`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772e515ce4579bbf74ecd1aa4c0a5364fb6cfced777bb22759c73eaebad3326`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0470850fd934b63a5c78e3863ebf75eaeda0cd98f424033c7a3d65bf66ddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61fe7d1689a5aad8c919b61bcb7fc0630de1615f8c0c3e7bdfa2aba8d6f8878`

```dockerfile
```

-	Layers:
	-	`sha256:36cccb967e52961197cda16c820ceeb19700af7a3e60078cd858a5d6b9933295`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 2.6 MB (2573202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ec0d4e47e9f99b77f2e917ce5332ce1c52aac67664530ae67223e2fa680006`  
		Last Modified: Tue, 05 Nov 2024 21:15:23 GMT  
		Size: 21.2 KB (21234 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:4959dc1d89dcd7957c5d9fd13994250f2afe666ff74498a33b64cd984f06344e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89618087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cd68f720e333e91f2dbf1d8a35025f297f040090d6d1fa9a7e52a63ec64aef`
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
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4245327d61bc8a47aa32a35e0b565a00fca8b812cc08b0e6fd9df212136f2a`  
		Last Modified: Tue, 12 Nov 2024 02:50:32 GMT  
		Size: 13.4 MB (13417468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dd6ca6cbd0df95e8c863eae285f59aad7421ebaf596cf4d22f25c0ea193e5f`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d29fce25c598912474e45ef412227a32adaff4417d617a11de3b43cd08517`  
		Last Modified: Tue, 12 Nov 2024 02:50:33 GMT  
		Size: 32.1 MB (32080803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb7beb5b8baae0c59dd1eb873ca5200b6c79cbce90ac08f54db3f4dea8b530`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b512b77c4c20aa3221e05a0874c182432488fa3e0481486edbfca59b1dd0fa`  
		Last Modified: Tue, 12 Nov 2024 03:20:58 GMT  
		Size: 14.0 MB (13971964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d50f6fcf12e0b366f3817b538c5b97dca020bb26a8a7a47c47b14e28b4fb6b`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eeacd44fee2d442b0230f788de9cb785f95a6cc7d24ddab5c318079eddc780`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7255b3aca7e06c72403719eac6e8375c469e2c3486bbe47032c41db00cebb9`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9babb62777d0df9415e6d0188c437cf492ea801e405ad9284fc4c8c7c1f4aa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d080e3e6fec4cd9a30a0a64c290ec8887f4c784ae776675b88f40cb1f5c6e237`

```dockerfile
```

-	Layers:
	-	`sha256:979269186a3f7ad9d0ea25a4a5ceff0cb1c25b7dd2076eb342d28f90efa7f27f`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 2.6 MB (2570081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6aceef15d582dc263a3a3a5357e1e2873601f335dcc16da109316a487b55aad`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
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
$ docker pull fluentd@sha256:eb1c10f8069692314635945781bb59a07d22e01488ae7d602fc396009d4e8267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86863104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d064b480b2678ce0606aa863884466195ea32dc25dd6da46256ab82a255b4912`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf62e0109103a0f4111ef4c0c7a451f221c717e4371b21f8c5dbd53f766d93`  
		Last Modified: Wed, 30 Oct 2024 18:37:17 GMT  
		Size: 12.0 MB (12041273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34458864c6076d695a68c5f4e6a0976af64a04a40b45a7583b69ad5811fb7b`  
		Last Modified: Wed, 30 Oct 2024 18:37:16 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecdfb9898838579b71ee3abda85e4aafaf7d3cdcde3555fd78360f0fd154256`  
		Last Modified: Tue, 05 Nov 2024 21:26:08 GMT  
		Size: 33.0 MB (33015239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8def241b7f3b5f6e35e526d4db55532ff0a04378092c6104a3ef999e9efe58`  
		Last Modified: Tue, 05 Nov 2024 21:26:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a456228a413614973439c63fde2fe7000843866a8abbfe32084d78816b561`  
		Last Modified: Tue, 05 Nov 2024 21:50:48 GMT  
		Size: 14.3 MB (14314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a4fad3372cbdfcf9378aaf4e2ff969f6a2cc5080db68fd20cdc9170a382d`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c723286d6a90de0884877a18facf9ddb125a3163d4d630558c051ba75dc99df9`  
		Last Modified: Tue, 05 Nov 2024 21:50:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79fd52850ec8960bbfd31715d894b1c3df20671e66f90928ee9bd3affefe84`  
		Last Modified: Tue, 05 Nov 2024 21:50:46 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd87b378b3532a988f61e8ba5dd5b892f58da4d025b76132d0c76959aee1dcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4a807cca6780dfa0b570c15d2c4b17649dd24938015677585452d9753e9ff`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3ffc21f2e52e85390e599e9cab998c158b6c9b5ba55589c6b660cadbcf9e5`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 2.6 MB (2572671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4095d9c3387c5f2105b4ff4f9b37315ff80e9fc48bcb6782942fb7c5d113e6bf`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-1.0`

```console
$ docker pull fluentd@sha256:117344aa852133fe9c9416b4c3b862d8ea47156469079917b89e99b9bf776773
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
$ docker pull fluentd@sha256:83aae31b2a3489f4a45f2f5cf8545e22f46f14ce0f89d158beed02dc1929f856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b04a2aea360fd7e27f17b08daa36fe3cbfc96f809a35252250d598ef51f364`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425e7a28e3eb3b2e903e3820e27ccbf6b7394aef31d39cd5edc673b817dbc3b8`  
		Last Modified: Sat, 07 Sep 2024 12:19:35 GMT  
		Size: 14.1 MB (14135705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfeff0ee1df7e53f9c9e1f13dceeff686b9183144df8d82a5453a2f0632fc6f`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708337bab8c95d7220d40787232afb2550f89f890d3429e69f6e475b4e23f041`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db6ef513149c1dbdd10ced86efdd01c6a840e91377d4cc711d5fe56deb483d`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b5ea461d5703d947e3eced352212b0b1208a8aa256b863c89d17a4e3ac8b4471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.0 KB (980964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d46bfa908b60f83810534fa2ee9e9462ef19afd057e85673fd2a0b112cf0f63`

```dockerfile
```

-	Layers:
	-	`sha256:774dc52d7be13d1e88c96591aaa8e2ad6aee4bbefeac51ec0a702e67ca0ecc94`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 967.2 KB (967238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b54499f65299860a91eb342736d9ef90bc2c538502e3c4a2f971efabd5b18d`  
		Last Modified: Sat, 07 Sep 2024 12:19:34 GMT  
		Size: 13.7 KB (13726 bytes)  
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
$ docker pull fluentd@sha256:bdd92d6edc1ac6d202e3cd31dbc7865dc497b568649faed0e550af52be620f4d
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
$ docker pull fluentd@sha256:9da62dfaf1f141ab79b60ff4d5c2da63753e34df033d328c151ebf45b5ceb97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93442482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c7386b124ff6784a982e8dac2b622d932ccad68438b8b68cf429da27254456`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7012cfae44fce24d2ce87b1df401456980e1e80d0bee35658df2d8f1808721`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 13.9 MB (13862683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8433d702d5ea937ff393f1d72a225ea1ece977860e78a82cb7ea86288c8180`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080b50a59c1101198321da9ca33b8a8a2bbc065b8d6ca91461398d6bcd64498`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 36.3 MB (36268931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c3535124be18673a2aa4e532798fb8102d65056fb528a79d10a77c0e0296cb`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1927e6fc42facfdbaa76624d1e65919811578a24b0423727c3e8960057d79a0`  
		Last Modified: Tue, 12 Nov 2024 03:20:40 GMT  
		Size: 14.2 MB (14180477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f078f819da02eb9bff44b3149d5846de67ad2b71f7f76d6322967b72aa747e`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d71c28bf81a4316b3cf4763990281bebe3a94bd3e0cdbd7323c0e3bc994357`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06efdf902ca533ce544c244e5755a8b46bc6bc65d6a302a9012f48345f095a4a`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cfc8bb1687c8c641462c80c22e3ad9029c624f3a986e6392fa58d02c14102f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5aa7eb4bada9598dd87e98518ef047e0e9e80f3ca287e77fdb0960341d1ba1`

```dockerfile
```

-	Layers:
	-	`sha256:362a168462864382e853204300602cba248e914b9f3aea5048315277a45824ae`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 2.6 MB (2572958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee768fc44b088c5e34c7fb7e78c6d201ef15163d8a0c4db753779094fd6c6e44`  
		Last Modified: Tue, 12 Nov 2024 03:20:39 GMT  
		Size: 21.1 KB (21109 bytes)  
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
$ docker pull fluentd@sha256:564ac8e0583f421346736f177cd63b236f5c4ed2955fc3cb127bf23aca8067aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81852665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d113ada12fdc1b0e5acfe1404c60b23222113bdf5bdbef395418253e97a9b29`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad165fb974bace21f0a023b5b89416ab63e61be2107ec588eb1e3237717f2848`  
		Last Modified: Fri, 18 Oct 2024 01:28:48 GMT  
		Size: 11.0 MB (10960451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56512ba6b2a6c37a25326a81238b0efa1d28a20513e43854cb3a8fb21267af`  
		Last Modified: Fri, 18 Oct 2024 01:28:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3545c4b2a964c6385519f5ebdfc110f670a59349b8c5eaaf5bf904919195630`  
		Last Modified: Tue, 05 Nov 2024 21:31:52 GMT  
		Size: 32.1 MB (32082341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bd711a6e07a75055f2d01100ec86ec8cf1cd1d86dc92f31a043dd39e0e2e5`  
		Last Modified: Tue, 05 Nov 2024 21:31:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cfea4c1fab45c88e7a6fe84f6993173ed83ea187e121d7edda11a6420a162e`  
		Last Modified: Tue, 05 Nov 2024 21:53:29 GMT  
		Size: 14.1 MB (14089267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0088b647c0146a60b53c5aa08b2c47b66435b3eba378e7ac43c9136a7360054`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8286d8c8561a2c0e4bc2e8250f43ada539397eb6a861ff0b554b72e582e11`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53d04e17c697ac1c99dcb22a52ba7ac05b243312a7af26a7e2ddb1ccd5c6b5e`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:caad970f1e08934b1455e230bf9d54e9a165f358a5482b0aa83e210d9f8c6c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87256ae8b95f1afb64e06cae3508ba8b4e69bfd54f91cc768cf2b387338f93de`

```dockerfile
```

-	Layers:
	-	`sha256:16d90a0c8ccc53652985f8eab3a1ab86d6b43a5083a71dbefe6a6ea9704c77f4`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 2.6 MB (2575198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8357c6dbb70dc6853479b2f1a97aed2ed8e32249e1f2be6145a3396514a25dd3`  
		Last Modified: Tue, 05 Nov 2024 21:53:28 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:9ed6a59c166e7d61a6d48d8ee53b02ea6a5320eb8bab305c7a84207af20b8039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92301693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d01083a504ef623cb26c1633ca015d1353d362b53a20f6fb04c1bdd83600ba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15fa32e5c8f64ba8c5dc13eeb40a1f4b4139996b89fa1ff32fdbd39d393ee13`  
		Last Modified: Wed, 30 Oct 2024 19:10:25 GMT  
		Size: 12.7 MB (12705660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dcf4909f6f483e882642f22161f8fc2dfcf3a570e53433d1479bd85ea99340`  
		Last Modified: Wed, 30 Oct 2024 19:10:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478d67e130011c48845bca1140e27bcf71b2a3872fbe7a079581663b39921de`  
		Last Modified: Tue, 05 Nov 2024 20:51:22 GMT  
		Size: 36.3 MB (36252077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dd28dbda175405a8ac35c24dd24def830939114acc3a4c406fccf4b6bd418f`  
		Last Modified: Tue, 05 Nov 2024 20:51:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb600779c326d31d4dfc9c8de0bb7381005238d81971442aeec95524824f619`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 14.2 MB (14185210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675a560e81ddfdab5c4aa812a77b2da8b2f081948891b787315ced271f55e0`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77550c0f03ff328448113f56264b4deecffb3ae11b21f7a645342a43fcbe146`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772e515ce4579bbf74ecd1aa4c0a5364fb6cfced777bb22759c73eaebad3326`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0470850fd934b63a5c78e3863ebf75eaeda0cd98f424033c7a3d65bf66ddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61fe7d1689a5aad8c919b61bcb7fc0630de1615f8c0c3e7bdfa2aba8d6f8878`

```dockerfile
```

-	Layers:
	-	`sha256:36cccb967e52961197cda16c820ceeb19700af7a3e60078cd858a5d6b9933295`  
		Last Modified: Tue, 05 Nov 2024 21:15:24 GMT  
		Size: 2.6 MB (2573202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ec0d4e47e9f99b77f2e917ce5332ce1c52aac67664530ae67223e2fa680006`  
		Last Modified: Tue, 05 Nov 2024 21:15:23 GMT  
		Size: 21.2 KB (21234 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:4959dc1d89dcd7957c5d9fd13994250f2afe666ff74498a33b64cd984f06344e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89618087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cd68f720e333e91f2dbf1d8a35025f297f040090d6d1fa9a7e52a63ec64aef`
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
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4245327d61bc8a47aa32a35e0b565a00fca8b812cc08b0e6fd9df212136f2a`  
		Last Modified: Tue, 12 Nov 2024 02:50:32 GMT  
		Size: 13.4 MB (13417468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dd6ca6cbd0df95e8c863eae285f59aad7421ebaf596cf4d22f25c0ea193e5f`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d29fce25c598912474e45ef412227a32adaff4417d617a11de3b43cd08517`  
		Last Modified: Tue, 12 Nov 2024 02:50:33 GMT  
		Size: 32.1 MB (32080803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb7beb5b8baae0c59dd1eb873ca5200b6c79cbce90ac08f54db3f4dea8b530`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b512b77c4c20aa3221e05a0874c182432488fa3e0481486edbfca59b1dd0fa`  
		Last Modified: Tue, 12 Nov 2024 03:20:58 GMT  
		Size: 14.0 MB (13971964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d50f6fcf12e0b366f3817b538c5b97dca020bb26a8a7a47c47b14e28b4fb6b`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eeacd44fee2d442b0230f788de9cb785f95a6cc7d24ddab5c318079eddc780`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7255b3aca7e06c72403719eac6e8375c469e2c3486bbe47032c41db00cebb9`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9babb62777d0df9415e6d0188c437cf492ea801e405ad9284fc4c8c7c1f4aa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d080e3e6fec4cd9a30a0a64c290ec8887f4c784ae776675b88f40cb1f5c6e237`

```dockerfile
```

-	Layers:
	-	`sha256:979269186a3f7ad9d0ea25a4a5ceff0cb1c25b7dd2076eb342d28f90efa7f27f`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 2.6 MB (2570081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6aceef15d582dc263a3a3a5357e1e2873601f335dcc16da109316a487b55aad`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
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
$ docker pull fluentd@sha256:eb1c10f8069692314635945781bb59a07d22e01488ae7d602fc396009d4e8267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86863104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d064b480b2678ce0606aa863884466195ea32dc25dd6da46256ab82a255b4912`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf62e0109103a0f4111ef4c0c7a451f221c717e4371b21f8c5dbd53f766d93`  
		Last Modified: Wed, 30 Oct 2024 18:37:17 GMT  
		Size: 12.0 MB (12041273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34458864c6076d695a68c5f4e6a0976af64a04a40b45a7583b69ad5811fb7b`  
		Last Modified: Wed, 30 Oct 2024 18:37:16 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecdfb9898838579b71ee3abda85e4aafaf7d3cdcde3555fd78360f0fd154256`  
		Last Modified: Tue, 05 Nov 2024 21:26:08 GMT  
		Size: 33.0 MB (33015239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8def241b7f3b5f6e35e526d4db55532ff0a04378092c6104a3ef999e9efe58`  
		Last Modified: Tue, 05 Nov 2024 21:26:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a456228a413614973439c63fde2fe7000843866a8abbfe32084d78816b561`  
		Last Modified: Tue, 05 Nov 2024 21:50:48 GMT  
		Size: 14.3 MB (14314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a4fad3372cbdfcf9378aaf4e2ff969f6a2cc5080db68fd20cdc9170a382d`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c723286d6a90de0884877a18facf9ddb125a3163d4d630558c051ba75dc99df9`  
		Last Modified: Tue, 05 Nov 2024 21:50:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79fd52850ec8960bbfd31715d894b1c3df20671e66f90928ee9bd3affefe84`  
		Last Modified: Tue, 05 Nov 2024 21:50:46 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd87b378b3532a988f61e8ba5dd5b892f58da4d025b76132d0c76959aee1dcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4a807cca6780dfa0b570c15d2c4b17649dd24938015677585452d9753e9ff`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3ffc21f2e52e85390e599e9cab998c158b6c9b5ba55589c6b660cadbcf9e5`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 2.6 MB (2572671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4095d9c3387c5f2105b4ff4f9b37315ff80e9fc48bcb6782942fb7c5d113e6bf`  
		Last Modified: Tue, 05 Nov 2024 21:50:45 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17-1`

```console
$ docker pull fluentd@sha256:185044381c7079505a3a4d2df10e0951d20ae4b036f1dcd85894add73afd631b
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
$ docker pull fluentd@sha256:9d8731ddcb491fa1b58cb0d5eec46028644dfc2a2158d64d11be0a8ece0523b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17539168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7177a0baf62585066bb57462a07622ceec99e1d8737f6ea507f4722f14bb12ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65d9421a6cf6af10f0d7efb81d38105099b7be31305ccfaaba28d380ea11c1f`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 14.2 MB (14177898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474e9013dbd28cc17bb843e54193c514cdbcd9505fbd75a5a54b1a8b252136e5`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5c0a178cd0cebd8004d4f550414c570c6533ffc36b2850aeaec23e7aa71242`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db843133adeb4397f9cc17ee9fbd4d0e145a63113fd3122ee1a9611bb58105`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d907b289cb67872bc0a1e74604ec56f7dc8ae249856336ef98d4b1d3038fb300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.4 KB (984405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b8f5cc66aeef3f6fe22961ab8cd8a45cf4313b9c15328d3107e831b33f62b`

```dockerfile
```

-	Layers:
	-	`sha256:3e6d4bb274d92d0fa4be0e8013180cdb835f2297341da2eb6f124bc2c8a2f1d9`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 970.4 KB (970369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883b941daba7313bfee0ee5c95c9d7a96f8cda81effd1c653af564c7ab2f0767`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 14.0 KB (14036 bytes)  
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
$ docker pull fluentd@sha256:4d8a996ba4a46289320086ea6b9af24a570515de63c678aeb096be61c70de8e6
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
$ docker pull fluentd@sha256:4250840d60353e3fb244419400d2ab14169541d8eae49925676b8c7c8ffaf562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92900843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95ae18818a519e21180f0c5042569d488b50a041fbca6671f961325655ad5ec`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7012cfae44fce24d2ce87b1df401456980e1e80d0bee35658df2d8f1808721`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 13.9 MB (13862683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8433d702d5ea937ff393f1d72a225ea1ece977860e78a82cb7ea86288c8180`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080b50a59c1101198321da9ca33b8a8a2bbc065b8d6ca91461398d6bcd64498`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 36.3 MB (36268931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c3535124be18673a2aa4e532798fb8102d65056fb528a79d10a77c0e0296cb`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfed7103f9b17b839fb0070c31ac4c61b40ffbcf4a342a47c7b8380daa98a50`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 13.6 MB (13638835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841fd3e951ecca3de5545a9b59b56ea6e460be6cc87c6ce8406848700196ec8`  
		Last Modified: Tue, 12 Nov 2024 03:20:45 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d4de5e9e4c8bde25c3afd7ed72b6e0999af97621ffd61783ad29e36a70fb0`  
		Last Modified: Tue, 12 Nov 2024 03:20:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8135a5299ec3227978169b0831485d7642f177eb79cd5eeb2e1c79157d8ee71`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1eff35becfa2d0e808ab05dafcd8ebefbbd1422d1ab641d5dfaa5041b472ccfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c27eb31cca6395a52aab798a07cffecbd9e6937558120152c2e85a716b3e03`

```dockerfile
```

-	Layers:
	-	`sha256:fa9aa7969a4b33f749d57bf0b8b8333dd39be35d23262fab188796971bdb511d`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 2.6 MB (2575975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ddb7d788bbd7182d705fdb548bd895638a50d80221155d912d3a95962299f9e`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
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
$ docker pull fluentd@sha256:95c039650b21990c71229140fb61a3e4f8f8a8c8a0c3346db93bfa438e893b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81305376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bfb58bab5ec06dbdfaa05a3c17d4509e3d30f992f2e5adba7bb3805476c873`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad165fb974bace21f0a023b5b89416ab63e61be2107ec588eb1e3237717f2848`  
		Last Modified: Fri, 18 Oct 2024 01:28:48 GMT  
		Size: 11.0 MB (10960451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56512ba6b2a6c37a25326a81238b0efa1d28a20513e43854cb3a8fb21267af`  
		Last Modified: Fri, 18 Oct 2024 01:28:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3545c4b2a964c6385519f5ebdfc110f670a59349b8c5eaaf5bf904919195630`  
		Last Modified: Tue, 05 Nov 2024 21:31:52 GMT  
		Size: 32.1 MB (32082341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bd711a6e07a75055f2d01100ec86ec8cf1cd1d86dc92f31a043dd39e0e2e5`  
		Last Modified: Tue, 05 Nov 2024 21:31:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f5ebd5cbb233f19e7bda71fb776ee530f78a03bf05914c044b87fac3e563a`  
		Last Modified: Tue, 05 Nov 2024 21:56:58 GMT  
		Size: 13.5 MB (13541978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec72ec9c322251e7cd7a2ab4fd25108a43d343e89928cd11a2b3864db909f35`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24c46557b71193bb4b20b96e50b4c9683d3fc79f9a06caf1a616db805edd63`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562a57cc9426ac51b5cc8bfac484ccb7f316d95455a07966427d928becf2ded`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:023e745d0c285b0fd836158952e7b303e552af3a97d6e3e542acf6b7a56c0656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfa2767a07964fcb1acb22e65edaf5519ebd04a3d4c87b74bf3a5fe431ca51f`

```dockerfile
```

-	Layers:
	-	`sha256:0acb2a52665ded2cc936a566467f2e77c54c181c6e5855217e4cd2c80422e1d3`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 2.6 MB (2578215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be062fca62a8ecbd77bf47df27f2061dba531fb97f3626104e06157564e7c2e`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:af2d393bda6796d501920e2f75b6467adcf2ac268458d1f91e63ab2e9c66dc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9987d71a60c22821a4a7213e32e05d1309843349594eadd75c088a5dc860e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15fa32e5c8f64ba8c5dc13eeb40a1f4b4139996b89fa1ff32fdbd39d393ee13`  
		Last Modified: Wed, 30 Oct 2024 19:10:25 GMT  
		Size: 12.7 MB (12705660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dcf4909f6f483e882642f22161f8fc2dfcf3a570e53433d1479bd85ea99340`  
		Last Modified: Wed, 30 Oct 2024 19:10:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478d67e130011c48845bca1140e27bcf71b2a3872fbe7a079581663b39921de`  
		Last Modified: Tue, 05 Nov 2024 20:51:22 GMT  
		Size: 36.3 MB (36252077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dd28dbda175405a8ac35c24dd24def830939114acc3a4c406fccf4b6bd418f`  
		Last Modified: Tue, 05 Nov 2024 20:51:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c501b7706b5e4a81771e5f68a9c7e396b46b2ccb8511a2ebe0e98a0c695d5ad`  
		Last Modified: Tue, 05 Nov 2024 21:18:23 GMT  
		Size: 13.6 MB (13645105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf160732ab706ab06d9a708b192a9a1a8a1a56d96fc6c3bc555b8a519028af`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb50cc6c16e269e831751340b67c9aec2f3349af9d1b7a30c87c5324bf8871b4`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac23610ab8b59465f4d2bf1b0816bb507412e98259183351dab55ab811a8c4a`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a3e7fc0f62165fc780a88c002e4fd84cf2bd332baae2962e813063e60f494fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d11f2d8ce905384d28599cacddc621444c4d3f1e41e96d14ad40c11c50fd173`

```dockerfile
```

-	Layers:
	-	`sha256:0e29229c8ff7fa0172f90c5eaa02e762eb48a70bf62fdaafc113008dcbad1a38`  
		Last Modified: Tue, 05 Nov 2024 21:18:23 GMT  
		Size: 2.6 MB (2576219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cf49d27f8f78424e462b175cde54c2175e2cdacbc76c056b2b9b818bf42dba`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:d07a7fed374b3280d7b1e834d794f148d011da72cf70dac5fb3855c02f0b06af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89075048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64b6834996386d8f32c40f87a1cfdffa50eb9b777e4b2541bb740a79b63caad`
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
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4245327d61bc8a47aa32a35e0b565a00fca8b812cc08b0e6fd9df212136f2a`  
		Last Modified: Tue, 12 Nov 2024 02:50:32 GMT  
		Size: 13.4 MB (13417468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dd6ca6cbd0df95e8c863eae285f59aad7421ebaf596cf4d22f25c0ea193e5f`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d29fce25c598912474e45ef412227a32adaff4417d617a11de3b43cd08517`  
		Last Modified: Tue, 12 Nov 2024 02:50:33 GMT  
		Size: 32.1 MB (32080803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb7beb5b8baae0c59dd1eb873ca5200b6c79cbce90ac08f54db3f4dea8b530`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d12cf739b4cbe4c461d0871c034c3a44b103da3eedccfd6f16c65154cf8f5a2`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 13.4 MB (13428926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0592fb4815f28a59861f94f6b58489f3bd71718a472a3fc01524fc80a5d33278`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb9450a722db51731f66700d766cc4c29655271a94c4a2db06313683e0c45a`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60874e351c6a72dfb8e30c4a77f27bbff1eecaebc076c699de35cfec8e30fd`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:04779930844ce04243287d6c40b3935ad4b9061702c5cc850eb168cf146bab6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb642152672e5d3227f8b688ff00b245e1dca3c484469120117154cb7b476e7`

```dockerfile
```

-	Layers:
	-	`sha256:0b223593e97f6af2dcef9b1d4dc3a539f2a8545f78b8a518f131037f451702b1`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 2.6 MB (2573098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85abe3a6c6758417faeb2e9ad0b92e4141078d9db7ea82bb1c96c8158df47f48`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
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
$ docker pull fluentd@sha256:b40c9bb133ef2e7a43c8c1e7d643e366fc1901567b449a8ef93e7a3ac2066141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86326787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1211a167aea00df7ce4d3c35665d40b66b5ad2fc057d16ece2612f89789aa213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf62e0109103a0f4111ef4c0c7a451f221c717e4371b21f8c5dbd53f766d93`  
		Last Modified: Wed, 30 Oct 2024 18:37:17 GMT  
		Size: 12.0 MB (12041273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34458864c6076d695a68c5f4e6a0976af64a04a40b45a7583b69ad5811fb7b`  
		Last Modified: Wed, 30 Oct 2024 18:37:16 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecdfb9898838579b71ee3abda85e4aafaf7d3cdcde3555fd78360f0fd154256`  
		Last Modified: Tue, 05 Nov 2024 21:26:08 GMT  
		Size: 33.0 MB (33015239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8def241b7f3b5f6e35e526d4db55532ff0a04378092c6104a3ef999e9efe58`  
		Last Modified: Tue, 05 Nov 2024 21:26:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cb4934feb4e6756ca8a116e9520ce17cf7dc67f9e60995dc014adfc188244`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 13.8 MB (13777787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f933c8fe9ff511526242b066dd806e61fd88876c71261a5f0c1e022bdc5e8fb9`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcea4313f3ad9ab763db49523e8e5cdfa9d22044858e9612ec11007cd125ab`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3c426ecb445a700a7eb1784495fed15dbefd29e54b40ac480115e08d7d1a5d`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3017c7a5e3ed4085debaddab2d23fdb6f57e78d489ab093a3d1d22a7cdbe754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a556930d363926f2d96d1c1227b809b07f17a38d16014d02d8f3c4db7ded9b1`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd0ccfa423b021e544af83a4e816df3bba529849aa0c80333a28160457807c`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 2.6 MB (2575688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339046ec481a7aeafb726e9a5608b5c73c7a3e368a6c58dc2a2fd8745fb3b7a7`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17.1-1.0`

```console
$ docker pull fluentd@sha256:185044381c7079505a3a4d2df10e0951d20ae4b036f1dcd85894add73afd631b
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
$ docker pull fluentd@sha256:9d8731ddcb491fa1b58cb0d5eec46028644dfc2a2158d64d11be0a8ece0523b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17539168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7177a0baf62585066bb57462a07622ceec99e1d8737f6ea507f4722f14bb12ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65d9421a6cf6af10f0d7efb81d38105099b7be31305ccfaaba28d380ea11c1f`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 14.2 MB (14177898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474e9013dbd28cc17bb843e54193c514cdbcd9505fbd75a5a54b1a8b252136e5`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5c0a178cd0cebd8004d4f550414c570c6533ffc36b2850aeaec23e7aa71242`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db843133adeb4397f9cc17ee9fbd4d0e145a63113fd3122ee1a9611bb58105`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d907b289cb67872bc0a1e74604ec56f7dc8ae249856336ef98d4b1d3038fb300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.4 KB (984405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b8f5cc66aeef3f6fe22961ab8cd8a45cf4313b9c15328d3107e831b33f62b`

```dockerfile
```

-	Layers:
	-	`sha256:3e6d4bb274d92d0fa4be0e8013180cdb835f2297341da2eb6f124bc2c8a2f1d9`  
		Last Modified: Sat, 07 Sep 2024 12:20:42 GMT  
		Size: 970.4 KB (970369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883b941daba7313bfee0ee5c95c9d7a96f8cda81effd1c653af564c7ab2f0767`  
		Last Modified: Sat, 07 Sep 2024 12:20:41 GMT  
		Size: 14.0 KB (14036 bytes)  
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
$ docker pull fluentd@sha256:4d8a996ba4a46289320086ea6b9af24a570515de63c678aeb096be61c70de8e6
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
$ docker pull fluentd@sha256:4250840d60353e3fb244419400d2ab14169541d8eae49925676b8c7c8ffaf562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92900843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95ae18818a519e21180f0c5042569d488b50a041fbca6671f961325655ad5ec`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7012cfae44fce24d2ce87b1df401456980e1e80d0bee35658df2d8f1808721`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 13.9 MB (13862683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8433d702d5ea937ff393f1d72a225ea1ece977860e78a82cb7ea86288c8180`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080b50a59c1101198321da9ca33b8a8a2bbc065b8d6ca91461398d6bcd64498`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 36.3 MB (36268931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c3535124be18673a2aa4e532798fb8102d65056fb528a79d10a77c0e0296cb`  
		Last Modified: Tue, 12 Nov 2024 02:50:22 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfed7103f9b17b839fb0070c31ac4c61b40ffbcf4a342a47c7b8380daa98a50`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 13.6 MB (13638835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841fd3e951ecca3de5545a9b59b56ea6e460be6cc87c6ce8406848700196ec8`  
		Last Modified: Tue, 12 Nov 2024 03:20:45 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8d4de5e9e4c8bde25c3afd7ed72b6e0999af97621ffd61783ad29e36a70fb0`  
		Last Modified: Tue, 12 Nov 2024 03:20:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8135a5299ec3227978169b0831485d7642f177eb79cd5eeb2e1c79157d8ee71`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1eff35becfa2d0e808ab05dafcd8ebefbbd1422d1ab641d5dfaa5041b472ccfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c27eb31cca6395a52aab798a07cffecbd9e6937558120152c2e85a716b3e03`

```dockerfile
```

-	Layers:
	-	`sha256:fa9aa7969a4b33f749d57bf0b8b8333dd39be35d23262fab188796971bdb511d`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
		Size: 2.6 MB (2575975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ddb7d788bbd7182d705fdb548bd895638a50d80221155d912d3a95962299f9e`  
		Last Modified: Tue, 12 Nov 2024 03:20:46 GMT  
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
$ docker pull fluentd@sha256:95c039650b21990c71229140fb61a3e4f8f8a8c8a0c3346db93bfa438e893b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81305376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bfb58bab5ec06dbdfaa05a3c17d4509e3d30f992f2e5adba7bb3805476c873`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad165fb974bace21f0a023b5b89416ab63e61be2107ec588eb1e3237717f2848`  
		Last Modified: Fri, 18 Oct 2024 01:28:48 GMT  
		Size: 11.0 MB (10960451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56512ba6b2a6c37a25326a81238b0efa1d28a20513e43854cb3a8fb21267af`  
		Last Modified: Fri, 18 Oct 2024 01:28:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3545c4b2a964c6385519f5ebdfc110f670a59349b8c5eaaf5bf904919195630`  
		Last Modified: Tue, 05 Nov 2024 21:31:52 GMT  
		Size: 32.1 MB (32082341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bd711a6e07a75055f2d01100ec86ec8cf1cd1d86dc92f31a043dd39e0e2e5`  
		Last Modified: Tue, 05 Nov 2024 21:31:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f5ebd5cbb233f19e7bda71fb776ee530f78a03bf05914c044b87fac3e563a`  
		Last Modified: Tue, 05 Nov 2024 21:56:58 GMT  
		Size: 13.5 MB (13541978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec72ec9c322251e7cd7a2ab4fd25108a43d343e89928cd11a2b3864db909f35`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24c46557b71193bb4b20b96e50b4c9683d3fc79f9a06caf1a616db805edd63`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562a57cc9426ac51b5cc8bfac484ccb7f316d95455a07966427d928becf2ded`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:023e745d0c285b0fd836158952e7b303e552af3a97d6e3e542acf6b7a56c0656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfa2767a07964fcb1acb22e65edaf5519ebd04a3d4c87b74bf3a5fe431ca51f`

```dockerfile
```

-	Layers:
	-	`sha256:0acb2a52665ded2cc936a566467f2e77c54c181c6e5855217e4cd2c80422e1d3`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 2.6 MB (2578215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be062fca62a8ecbd77bf47df27f2061dba531fb97f3626104e06157564e7c2e`  
		Last Modified: Tue, 05 Nov 2024 21:56:57 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:af2d393bda6796d501920e2f75b6467adcf2ac268458d1f91e63ab2e9c66dc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c9987d71a60c22821a4a7213e32e05d1309843349594eadd75c088a5dc860e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15fa32e5c8f64ba8c5dc13eeb40a1f4b4139996b89fa1ff32fdbd39d393ee13`  
		Last Modified: Wed, 30 Oct 2024 19:10:25 GMT  
		Size: 12.7 MB (12705660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dcf4909f6f483e882642f22161f8fc2dfcf3a570e53433d1479bd85ea99340`  
		Last Modified: Wed, 30 Oct 2024 19:10:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478d67e130011c48845bca1140e27bcf71b2a3872fbe7a079581663b39921de`  
		Last Modified: Tue, 05 Nov 2024 20:51:22 GMT  
		Size: 36.3 MB (36252077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dd28dbda175405a8ac35c24dd24def830939114acc3a4c406fccf4b6bd418f`  
		Last Modified: Tue, 05 Nov 2024 20:51:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c501b7706b5e4a81771e5f68a9c7e396b46b2ccb8511a2ebe0e98a0c695d5ad`  
		Last Modified: Tue, 05 Nov 2024 21:18:23 GMT  
		Size: 13.6 MB (13645105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf160732ab706ab06d9a708b192a9a1a8a1a56d96fc6c3bc555b8a519028af`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb50cc6c16e269e831751340b67c9aec2f3349af9d1b7a30c87c5324bf8871b4`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac23610ab8b59465f4d2bf1b0816bb507412e98259183351dab55ab811a8c4a`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a3e7fc0f62165fc780a88c002e4fd84cf2bd332baae2962e813063e60f494fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d11f2d8ce905384d28599cacddc621444c4d3f1e41e96d14ad40c11c50fd173`

```dockerfile
```

-	Layers:
	-	`sha256:0e29229c8ff7fa0172f90c5eaa02e762eb48a70bf62fdaafc113008dcbad1a38`  
		Last Modified: Tue, 05 Nov 2024 21:18:23 GMT  
		Size: 2.6 MB (2576219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cf49d27f8f78424e462b175cde54c2175e2cdacbc76c056b2b9b818bf42dba`  
		Last Modified: Tue, 05 Nov 2024 21:18:22 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d07a7fed374b3280d7b1e834d794f148d011da72cf70dac5fb3855c02f0b06af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89075048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64b6834996386d8f32c40f87a1cfdffa50eb9b777e4b2541bb740a79b63caad`
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
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4245327d61bc8a47aa32a35e0b565a00fca8b812cc08b0e6fd9df212136f2a`  
		Last Modified: Tue, 12 Nov 2024 02:50:32 GMT  
		Size: 13.4 MB (13417468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dd6ca6cbd0df95e8c863eae285f59aad7421ebaf596cf4d22f25c0ea193e5f`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d29fce25c598912474e45ef412227a32adaff4417d617a11de3b43cd08517`  
		Last Modified: Tue, 12 Nov 2024 02:50:33 GMT  
		Size: 32.1 MB (32080803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb7beb5b8baae0c59dd1eb873ca5200b6c79cbce90ac08f54db3f4dea8b530`  
		Last Modified: Tue, 12 Nov 2024 02:50:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d12cf739b4cbe4c461d0871c034c3a44b103da3eedccfd6f16c65154cf8f5a2`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 13.4 MB (13428926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0592fb4815f28a59861f94f6b58489f3bd71718a472a3fc01524fc80a5d33278`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb9450a722db51731f66700d766cc4c29655271a94c4a2db06313683e0c45a`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60874e351c6a72dfb8e30c4a77f27bbff1eecaebc076c699de35cfec8e30fd`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:04779930844ce04243287d6c40b3935ad4b9061702c5cc850eb168cf146bab6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb642152672e5d3227f8b688ff00b245e1dca3c484469120117154cb7b476e7`

```dockerfile
```

-	Layers:
	-	`sha256:0b223593e97f6af2dcef9b1d4dc3a539f2a8545f78b8a518f131037f451702b1`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
		Size: 2.6 MB (2573098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85abe3a6c6758417faeb2e9ad0b92e4141078d9db7ea82bb1c96c8158df47f48`  
		Last Modified: Tue, 12 Nov 2024 03:20:57 GMT  
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
$ docker pull fluentd@sha256:b40c9bb133ef2e7a43c8c1e7d643e366fc1901567b449a8ef93e7a3ac2066141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86326787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1211a167aea00df7ce4d3c35665d40b66b5ad2fc057d16ece2612f89789aa213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf62e0109103a0f4111ef4c0c7a451f221c717e4371b21f8c5dbd53f766d93`  
		Last Modified: Wed, 30 Oct 2024 18:37:17 GMT  
		Size: 12.0 MB (12041273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34458864c6076d695a68c5f4e6a0976af64a04a40b45a7583b69ad5811fb7b`  
		Last Modified: Wed, 30 Oct 2024 18:37:16 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecdfb9898838579b71ee3abda85e4aafaf7d3cdcde3555fd78360f0fd154256`  
		Last Modified: Tue, 05 Nov 2024 21:26:08 GMT  
		Size: 33.0 MB (33015239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8def241b7f3b5f6e35e526d4db55532ff0a04378092c6104a3ef999e9efe58`  
		Last Modified: Tue, 05 Nov 2024 21:26:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cb4934feb4e6756ca8a116e9520ce17cf7dc67f9e60995dc014adfc188244`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 13.8 MB (13777787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f933c8fe9ff511526242b066dd806e61fd88876c71261a5f0c1e022bdc5e8fb9`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcea4313f3ad9ab763db49523e8e5cdfa9d22044858e9612ec11007cd125ab`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3c426ecb445a700a7eb1784495fed15dbefd29e54b40ac480115e08d7d1a5d`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3017c7a5e3ed4085debaddab2d23fdb6f57e78d489ab093a3d1d22a7cdbe754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a556930d363926f2d96d1c1227b809b07f17a38d16014d02d8f3c4db7ded9b1`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd0ccfa423b021e544af83a4e816df3bba529849aa0c80333a28160457807c`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 2.6 MB (2575688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339046ec481a7aeafb726e9a5608b5c73c7a3e368a6c58dc2a2fd8745fb3b7a7`  
		Last Modified: Tue, 05 Nov 2024 21:55:14 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json
