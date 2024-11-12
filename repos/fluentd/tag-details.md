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
$ docker pull fluentd@sha256:2761de005481ec6f9904caf8ef3becb2263aefccdeea5a19659aaf9049fdaf9c
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
$ docker pull fluentd@sha256:1745a5a982cef63bd21c66b9b137a9762c4faab8cd298694a00fb28c1e17aa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16297518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891664aa169ab161981a30b3b62de4ca81510b685c55b6880764c0450a02febc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b10f5d96e97ceb3b758054e5f53fce3b6bbad9ea0e052366d7b8449216d9f`  
		Last Modified: Sat, 07 Sep 2024 12:53:44 GMT  
		Size: 13.1 MB (13118953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391fe9e5281d4bde619c7e5c71d92fb9e031be3e0b4af6fe016f8fb22a3fd1ff`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6887733c66c8f64b90ce5c1947f14605123431c739f1d110f2679830dca811`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35204c5e77d28136d6633a0f9fff8653fb7bf9aa307668e00a4393d2eef88991`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:573cc73ea2911e43d8b8a879bbf71edf8942cbef351126bd9480140c8d2eb9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792c5be09495ab2f023412f9d696660b66a2764e27ff756e982b3cd9b976afb4`

```dockerfile
```

-	Layers:
	-	`sha256:ab4b17c3b9b1c5cdea7b419e9002925e13303b3bf54c86451ac9222c56d53af5`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 13.6 KB (13606 bytes)  
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
$ docker pull fluentd@sha256:0e7abc99a8ea730b7bd16c91cbd7e29fe766cf3eca91e637cd5f72e4ba83a5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17102936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530ec17be88bc608a200cda549e2896830ea433b6d9282fe3adf127f9a0e497`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d0d10ad20b971eeab4a17882bee29d98ed6638ec90cd586f26760b1cc4d6e`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 13.7 MB (13736301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619aebff2e97d98bc39dea9d791d86aaf29000789d90443831cb8d7135e2203b`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aece3d2bd1e2e1850105fa9d0201f6fc47602739717d9343ff02918ab02cc0e`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85db083a94520ef6e956c6a76cc8457242133e1dbc2d7abc2d9eb43cce076bd5`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:e245200af63b58345451973f001d1da552a71192d3f891d61aded848229563c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.7 KB (979710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932295115b06403597a65638457a265a4a63e03d9ba592958df100892da53ae4`

```dockerfile
```

-	Layers:
	-	`sha256:54cc512c7e9dd36755e70ce43ce86b34bee28c9900ad0b351309a655a5fb3851`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 965.9 KB (965927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1db62231943df6cefd36defbec4ecf6f6364dd228a08042f25681fdc47d19a`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 13.8 KB (13783 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:59606cc1af3633db661c63439f0fce618bd1992b79ae61487b3e5cf804e34dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e772a58a5fc32d69a2142f36b23c99240b8c5119e4cccf786c3df56130d3b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f5006dbaca93167284eb6968f33d7f724cc31e4d8c3ad3e2288d6d2f2beaac`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.7 MB (13711443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f737ed55fe73feed661a95901572355d7a835ba7ba533b0bf60f6a73a46f992`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95087696a6d3f004d6c34f39ea01a1da1f1788aec2a4317244f6873254b105b9`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78193fbe6f5065a08da16003fcbaf57fa023e8cce820a0011492614b658845`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:64b22645d0bccf7ab31d797cd9778ce32ca7fff05dbe6b6e77e91716ecbf0e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72dfa68e09f181c01d535a903dd2bed4156adae6da8199ffe54252a1dbc611f`

```dockerfile
```

-	Layers:
	-	`sha256:cec50a8d3e056ac5b69b56737d850fb338e47e987a9ad0872109a187aff9101a`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 965.3 KB (965311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217bb467f557c0df3252b9a5c783f298f333e52ef5ff3b62ea045c644a6fbc7`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.8 KB (13750 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:9959f463a584188289b19b76413294b235ac1c735742241b285f9f40f938b250
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
$ docker pull fluentd@sha256:1e78eb8aee3e5a76c6d6815a33d7998f54c61c1accd2fad3f165bb67782c0fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16260846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8244a24ea1c3a4808b70e145ce586705fae68959c19462c1375b29e6ad187163`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2cd7fe8f1de9884f22795ca45632e187747b7aefa6f1a5c1377ccb1938ffe`  
		Last Modified: Sat, 07 Sep 2024 12:52:17 GMT  
		Size: 13.1 MB (13082281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe7026aeca4c2328e6412b8113a08647bebc634e65a242513f5b15e2134ea6d`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1769e1f71c3e7a082e4fb04f89da371d97c438ed41766677350aeb9365fc355a`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6dd50c3d51f54060a9a2a4f050b2b36dceeed4abf4c16b2119ddb468a47fdc`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47078f1974754332e43fd82b3fcf47d4a62d5295174ee3fa01846069ab1b5f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30177d209a111c3e9312ea2024e67095e4b114abe293c7f29c22b28b3249e3a1`

```dockerfile
```

-	Layers:
	-	`sha256:fd68f1cfaecae64620a7bac8d83024aa0c934fe6a5706ad64283b8cd119315ba`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 13.3 KB (13298 bytes)  
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
$ docker pull fluentd@sha256:333729a8d31520345903bb9350f85d9cf6c27fffade3825eb59a96c8a7ba0c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb424c58e9f98a3023e732c645f672657244db1e3f8a55584f796cb4b5655b0a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4608275635b6fa74d16034f0d731b4f3635758a4df2f9f3aaf74cc4c036020f8`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 13.7 MB (13692126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46532fb86ead1127bef8554b6c4c4b29fcdd4326fc2d0e7a5f30f9044c4b84ed`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a6f7157b234218a0b240baa2dc1410c01fcbb72c2802e2d5a3e974bfc5cbba`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331acaa2c00a65c97c3ebe8bd1eb1e72d9027d85700ec28a605c3a8b7db7f821`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:54ed76a81b14dcaa70eeefd4b644f79668e788616851cb5323b878601b60f10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.3 KB (976280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206a898bd98f2a6b40338abc668e7e9d4e7a37628c78c081ba8605fb36760302`

```dockerfile
```

-	Layers:
	-	`sha256:bb620b2b08716c7090fd82e19e8c59ad8ca470900adfced39d6c2cc71cd66fe8`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 962.8 KB (962802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef51158407f734ac1a7694ece3e67d078894d878c4f39d8e7001f6a4eb10e7fe`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:b8de037f23db00379f1f2e342b7303fff3ca538539723ea6742350d181359536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16913302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3843c92e9f595939a73ee343bebdaef7ebc7dfe9adba5380c82702cf3f40ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e22fa78e7b3688a87b1ecb7f50561e4824ed71d09537112a25d9af1bd828a`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 13.7 MB (13657780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3fbe9895b24f8ff481bee977d9fa49cd43ff9dfc97af53cbcd99347611486`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3b37bbf4c26673f13ec29b90591d52c0f4f32f5c76b94b07b6e0a004fa8059`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f302b312acba8684469744ad90c2d11994d675cb2f2f47b961843aec54671`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:dd827d9aac3102cabb9d15d670c0a5c00cbd858008be3858efd9c8a1f33a2c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.6 KB (975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc4e98f831f180134fd47b0b32f06c4ff996cd7c2abaf4936814affd4ebcccc`

```dockerfile
```

-	Layers:
	-	`sha256:5f3ceda5459f0a12e6d2d8ea31248db48a8f58eb7e9f411bda9b89529b7f5906`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 962.2 KB (962192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aaa8f8866b792b2079d01306a4f3d0bbc0d9f808d0ba3f10d068b1576c27df`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 13.4 KB (13450 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:85a47321aa3b7bde00d6478469e94d5b1bc33628ab6e2c3e8f3f2246d74b8ff3
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
$ docker pull fluentd@sha256:231d0ac4df3ac277950174fbb64f862b23d1889c4f0a3c4c21ad78621fc4702c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84918748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16f1abe381f720e215f56ed6d72966d630ee427c70c80a145cbe52a88b310e2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
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
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ce1f192165e9a7ce336963643a944c339a24427a87c96c3698d3d6641f348`  
		Last Modified: Thu, 17 Oct 2024 09:49:24 GMT  
		Size: 11.6 MB (11620510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1368a401dd210cbfccceb2812e7b128f261e2e405f473856acb05966577669e`  
		Last Modified: Thu, 17 Oct 2024 09:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857dac63f10e78cb54f4c34b160b2b0998eabff35096a85be0e24aa2bb58f449`  
		Last Modified: Tue, 05 Nov 2024 21:17:52 GMT  
		Size: 32.2 MB (32241644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6f09195a593207ce75d9be73f751e6ce6ef99a38be15b4360b8cf0d34ac10`  
		Last Modified: Tue, 05 Nov 2024 21:17:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34c5cac0ff08dac4acb9e125f969ba763ea37ae10faec9a96c95cf5a8626cdb`  
		Last Modified: Tue, 05 Nov 2024 21:50:52 GMT  
		Size: 14.2 MB (14166880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6d60c0133d0ea00af7ce2d3c9831b178f0ec0f957aa80b758778de1ac6dc0`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860c74d31add72d58972b3f7ae2e29fba4b62133f5f370a8483bf378edd0aec4`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0330ac842842828606a99a36c5132b7120243e4992f3aca8fb06140a6b28188`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8db7bf25ee7dc64cc52ceb4e3d9481d9a35ea98fad9191ef090ff2848472d508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6df48c885d0bcf219dd98737951702ab0725a74743ec6bb56aba02eeaeef74c`

```dockerfile
```

-	Layers:
	-	`sha256:24a7601a04624f468f7cf2b9cf40e485e87a9240f8edf38230b7fb536cea581b`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 2.6 MB (2576449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c2eb5546adc2c85b29a0524d95017996507cc94ede52c7165083aa97eca96a`  
		Last Modified: Tue, 05 Nov 2024 21:50:50 GMT  
		Size: 21.2 KB (21212 bytes)  
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
$ docker pull fluentd@sha256:79a7bbdd55dac4b41b88b444e08cc054d8ab65e9bdef54f565498830ebf98d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96019733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daed8cb29782b5538250f9dfeaaa60b9681bfe3cbac0f7086d36339f6e602ed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2085a9bf6425e1db4aceff65b459218746f21da3a2b2bc7c609f6e7f3bc13cc`  
		Last Modified: Wed, 30 Oct 2024 18:29:41 GMT  
		Size: 14.6 MB (14591140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d294ef697680ab988c128a54b9e09239e2b59f695cf8665e799a6dae10a3d05`  
		Last Modified: Wed, 30 Oct 2024 18:29:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5ec399be8a51eb991e23efe52aaca4a9322ad460d8209b3baf7b5769b863f`  
		Last Modified: Tue, 05 Nov 2024 21:03:50 GMT  
		Size: 33.7 MB (33729980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f064f984c52c7846f6af551962186edc1e252975cedcd5d437809ac1feb63a`  
		Last Modified: Tue, 05 Nov 2024 21:03:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae667c5f01e82dddec16681d5bd733b1a3d2840e197fc1d71a6b67e14408fa91`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 14.6 MB (14574004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001cd3cfe7c27863df85c44726db8fd99b421dbab2da58db8f15613f1233456`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cf32d020778a6770ae8aea497fa97882f6840a4f32db8961720a82f2cedd6d`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a92da717e605af8c28011da2d009df6b2e1b33a1f5a15d8fada5b4f04994f1`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3d2f7731846d6a20006530e51ee960f85770fb57ab20f699dc5a6c4f1897aeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc2a7459849b0ec6a160f5a77b3585d236563d4aacad458de82e34243b165a8`

```dockerfile
```

-	Layers:
	-	`sha256:9acf68f560572211dfb2ff28aab2aef2d04bc935c2be5ab83891cc3a531b053f`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 2.6 MB (2577305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ef117fda372a757229c726d1f01f04f88f19c9846295e4cf5612aac687c5d`  
		Last Modified: Tue, 05 Nov 2024 21:51:30 GMT  
		Size: 21.2 KB (21173 bytes)  
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
$ docker pull fluentd@sha256:9959f463a584188289b19b76413294b235ac1c735742241b285f9f40f938b250
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
$ docker pull fluentd@sha256:1e78eb8aee3e5a76c6d6815a33d7998f54c61c1accd2fad3f165bb67782c0fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16260846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8244a24ea1c3a4808b70e145ce586705fae68959c19462c1375b29e6ad187163`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2cd7fe8f1de9884f22795ca45632e187747b7aefa6f1a5c1377ccb1938ffe`  
		Last Modified: Sat, 07 Sep 2024 12:52:17 GMT  
		Size: 13.1 MB (13082281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe7026aeca4c2328e6412b8113a08647bebc634e65a242513f5b15e2134ea6d`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1769e1f71c3e7a082e4fb04f89da371d97c438ed41766677350aeb9365fc355a`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6dd50c3d51f54060a9a2a4f050b2b36dceeed4abf4c16b2119ddb468a47fdc`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:47078f1974754332e43fd82b3fcf47d4a62d5295174ee3fa01846069ab1b5f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30177d209a111c3e9312ea2024e67095e4b114abe293c7f29c22b28b3249e3a1`

```dockerfile
```

-	Layers:
	-	`sha256:fd68f1cfaecae64620a7bac8d83024aa0c934fe6a5706ad64283b8cd119315ba`  
		Last Modified: Sat, 07 Sep 2024 12:52:16 GMT  
		Size: 13.3 KB (13298 bytes)  
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
$ docker pull fluentd@sha256:333729a8d31520345903bb9350f85d9cf6c27fffade3825eb59a96c8a7ba0c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb424c58e9f98a3023e732c645f672657244db1e3f8a55584f796cb4b5655b0a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4608275635b6fa74d16034f0d731b4f3635758a4df2f9f3aaf74cc4c036020f8`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 13.7 MB (13692126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46532fb86ead1127bef8554b6c4c4b29fcdd4326fc2d0e7a5f30f9044c4b84ed`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a6f7157b234218a0b240baa2dc1410c01fcbb72c2802e2d5a3e974bfc5cbba`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331acaa2c00a65c97c3ebe8bd1eb1e72d9027d85700ec28a605c3a8b7db7f821`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:54ed76a81b14dcaa70eeefd4b644f79668e788616851cb5323b878601b60f10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.3 KB (976280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206a898bd98f2a6b40338abc668e7e9d4e7a37628c78c081ba8605fb36760302`

```dockerfile
```

-	Layers:
	-	`sha256:bb620b2b08716c7090fd82e19e8c59ad8ca470900adfced39d6c2cc71cd66fe8`  
		Last Modified: Sat, 07 Sep 2024 11:54:33 GMT  
		Size: 962.8 KB (962802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef51158407f734ac1a7694ece3e67d078894d878c4f39d8e7001f6a4eb10e7fe`  
		Last Modified: Sat, 07 Sep 2024 11:54:32 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:b8de037f23db00379f1f2e342b7303fff3ca538539723ea6742350d181359536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16913302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3843c92e9f595939a73ee343bebdaef7ebc7dfe9adba5380c82702cf3f40ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e22fa78e7b3688a87b1ecb7f50561e4824ed71d09537112a25d9af1bd828a`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 13.7 MB (13657780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3fbe9895b24f8ff481bee977d9fa49cd43ff9dfc97af53cbcd99347611486`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3b37bbf4c26673f13ec29b90591d52c0f4f32f5c76b94b07b6e0a004fa8059`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f302b312acba8684469744ad90c2d11994d675cb2f2f47b961843aec54671`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:dd827d9aac3102cabb9d15d670c0a5c00cbd858008be3858efd9c8a1f33a2c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.6 KB (975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc4e98f831f180134fd47b0b32f06c4ff996cd7c2abaf4936814affd4ebcccc`

```dockerfile
```

-	Layers:
	-	`sha256:5f3ceda5459f0a12e6d2d8ea31248db48a8f58eb7e9f411bda9b89529b7f5906`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 962.2 KB (962192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aaa8f8866b792b2079d01306a4f3d0bbc0d9f808d0ba3f10d068b1576c27df`  
		Last Modified: Sat, 07 Sep 2024 11:00:38 GMT  
		Size: 13.4 KB (13450 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-debian-1.0`

```console
$ docker pull fluentd@sha256:85a47321aa3b7bde00d6478469e94d5b1bc33628ab6e2c3e8f3f2246d74b8ff3
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
$ docker pull fluentd@sha256:231d0ac4df3ac277950174fbb64f862b23d1889c4f0a3c4c21ad78621fc4702c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84918748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16f1abe381f720e215f56ed6d72966d630ee427c70c80a145cbe52a88b310e2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
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
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ce1f192165e9a7ce336963643a944c339a24427a87c96c3698d3d6641f348`  
		Last Modified: Thu, 17 Oct 2024 09:49:24 GMT  
		Size: 11.6 MB (11620510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1368a401dd210cbfccceb2812e7b128f261e2e405f473856acb05966577669e`  
		Last Modified: Thu, 17 Oct 2024 09:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857dac63f10e78cb54f4c34b160b2b0998eabff35096a85be0e24aa2bb58f449`  
		Last Modified: Tue, 05 Nov 2024 21:17:52 GMT  
		Size: 32.2 MB (32241644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6f09195a593207ce75d9be73f751e6ce6ef99a38be15b4360b8cf0d34ac10`  
		Last Modified: Tue, 05 Nov 2024 21:17:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34c5cac0ff08dac4acb9e125f969ba763ea37ae10faec9a96c95cf5a8626cdb`  
		Last Modified: Tue, 05 Nov 2024 21:50:52 GMT  
		Size: 14.2 MB (14166880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6d60c0133d0ea00af7ce2d3c9831b178f0ec0f957aa80b758778de1ac6dc0`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860c74d31add72d58972b3f7ae2e29fba4b62133f5f370a8483bf378edd0aec4`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0330ac842842828606a99a36c5132b7120243e4992f3aca8fb06140a6b28188`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8db7bf25ee7dc64cc52ceb4e3d9481d9a35ea98fad9191ef090ff2848472d508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6df48c885d0bcf219dd98737951702ab0725a74743ec6bb56aba02eeaeef74c`

```dockerfile
```

-	Layers:
	-	`sha256:24a7601a04624f468f7cf2b9cf40e485e87a9240f8edf38230b7fb536cea581b`  
		Last Modified: Tue, 05 Nov 2024 21:50:51 GMT  
		Size: 2.6 MB (2576449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c2eb5546adc2c85b29a0524d95017996507cc94ede52c7165083aa97eca96a`  
		Last Modified: Tue, 05 Nov 2024 21:50:50 GMT  
		Size: 21.2 KB (21212 bytes)  
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
$ docker pull fluentd@sha256:79a7bbdd55dac4b41b88b444e08cc054d8ab65e9bdef54f565498830ebf98d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96019733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daed8cb29782b5538250f9dfeaaa60b9681bfe3cbac0f7086d36339f6e602ed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2085a9bf6425e1db4aceff65b459218746f21da3a2b2bc7c609f6e7f3bc13cc`  
		Last Modified: Wed, 30 Oct 2024 18:29:41 GMT  
		Size: 14.6 MB (14591140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d294ef697680ab988c128a54b9e09239e2b59f695cf8665e799a6dae10a3d05`  
		Last Modified: Wed, 30 Oct 2024 18:29:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5ec399be8a51eb991e23efe52aaca4a9322ad460d8209b3baf7b5769b863f`  
		Last Modified: Tue, 05 Nov 2024 21:03:50 GMT  
		Size: 33.7 MB (33729980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f064f984c52c7846f6af551962186edc1e252975cedcd5d437809ac1feb63a`  
		Last Modified: Tue, 05 Nov 2024 21:03:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae667c5f01e82dddec16681d5bd733b1a3d2840e197fc1d71a6b67e14408fa91`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 14.6 MB (14574004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001cd3cfe7c27863df85c44726db8fd99b421dbab2da58db8f15613f1233456`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cf32d020778a6770ae8aea497fa97882f6840a4f32db8961720a82f2cedd6d`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a92da717e605af8c28011da2d009df6b2e1b33a1f5a15d8fada5b4f04994f1`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3d2f7731846d6a20006530e51ee960f85770fb57ab20f699dc5a6c4f1897aeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2598478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc2a7459849b0ec6a160f5a77b3585d236563d4aacad458de82e34243b165a8`

```dockerfile
```

-	Layers:
	-	`sha256:9acf68f560572211dfb2ff28aab2aef2d04bc935c2be5ab83891cc3a531b053f`  
		Last Modified: Tue, 05 Nov 2024 21:51:31 GMT  
		Size: 2.6 MB (2577305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764ef117fda372a757229c726d1f01f04f88f19c9846295e4cf5612aac687c5d`  
		Last Modified: Tue, 05 Nov 2024 21:51:30 GMT  
		Size: 21.2 KB (21173 bytes)  
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
$ docker pull fluentd@sha256:2761de005481ec6f9904caf8ef3becb2263aefccdeea5a19659aaf9049fdaf9c
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
$ docker pull fluentd@sha256:1745a5a982cef63bd21c66b9b137a9762c4faab8cd298694a00fb28c1e17aa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16297518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891664aa169ab161981a30b3b62de4ca81510b685c55b6880764c0450a02febc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b10f5d96e97ceb3b758054e5f53fce3b6bbad9ea0e052366d7b8449216d9f`  
		Last Modified: Sat, 07 Sep 2024 12:53:44 GMT  
		Size: 13.1 MB (13118953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391fe9e5281d4bde619c7e5c71d92fb9e031be3e0b4af6fe016f8fb22a3fd1ff`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6887733c66c8f64b90ce5c1947f14605123431c739f1d110f2679830dca811`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35204c5e77d28136d6633a0f9fff8653fb7bf9aa307668e00a4393d2eef88991`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:573cc73ea2911e43d8b8a879bbf71edf8942cbef351126bd9480140c8d2eb9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792c5be09495ab2f023412f9d696660b66a2764e27ff756e982b3cd9b976afb4`

```dockerfile
```

-	Layers:
	-	`sha256:ab4b17c3b9b1c5cdea7b419e9002925e13303b3bf54c86451ac9222c56d53af5`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 13.6 KB (13606 bytes)  
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
$ docker pull fluentd@sha256:0e7abc99a8ea730b7bd16c91cbd7e29fe766cf3eca91e637cd5f72e4ba83a5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17102936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530ec17be88bc608a200cda549e2896830ea433b6d9282fe3adf127f9a0e497`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d0d10ad20b971eeab4a17882bee29d98ed6638ec90cd586f26760b1cc4d6e`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 13.7 MB (13736301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619aebff2e97d98bc39dea9d791d86aaf29000789d90443831cb8d7135e2203b`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aece3d2bd1e2e1850105fa9d0201f6fc47602739717d9343ff02918ab02cc0e`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85db083a94520ef6e956c6a76cc8457242133e1dbc2d7abc2d9eb43cce076bd5`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e245200af63b58345451973f001d1da552a71192d3f891d61aded848229563c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.7 KB (979710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932295115b06403597a65638457a265a4a63e03d9ba592958df100892da53ae4`

```dockerfile
```

-	Layers:
	-	`sha256:54cc512c7e9dd36755e70ce43ce86b34bee28c9900ad0b351309a655a5fb3851`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 965.9 KB (965927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1db62231943df6cefd36defbec4ecf6f6364dd228a08042f25681fdc47d19a`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 13.8 KB (13783 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-1` - linux; s390x

```console
$ docker pull fluentd@sha256:59606cc1af3633db661c63439f0fce618bd1992b79ae61487b3e5cf804e34dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e772a58a5fc32d69a2142f36b23c99240b8c5119e4cccf786c3df56130d3b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f5006dbaca93167284eb6968f33d7f724cc31e4d8c3ad3e2288d6d2f2beaac`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.7 MB (13711443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f737ed55fe73feed661a95901572355d7a835ba7ba533b0bf60f6a73a46f992`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95087696a6d3f004d6c34f39ea01a1da1f1788aec2a4317244f6873254b105b9`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78193fbe6f5065a08da16003fcbaf57fa023e8cce820a0011492614b658845`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:64b22645d0bccf7ab31d797cd9778ce32ca7fff05dbe6b6e77e91716ecbf0e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72dfa68e09f181c01d535a903dd2bed4156adae6da8199ffe54252a1dbc611f`

```dockerfile
```

-	Layers:
	-	`sha256:cec50a8d3e056ac5b69b56737d850fb338e47e987a9ad0872109a187aff9101a`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 965.3 KB (965311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217bb467f557c0df3252b9a5c783f298f333e52ef5ff3b62ea045c644a6fbc7`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.8 KB (13750 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17-debian-1`

```console
$ docker pull fluentd@sha256:745730a8a6eb29f33058004ace50970a740a068c64aa62f62654f039cf95d7fe
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
$ docker pull fluentd@sha256:cbd4748d65d744441c7dae3f345b9b64dc88b3cd9cd00b400c879acf2035ccc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84373802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc5bc4ac729ead4f59797a300df858eb2ca63348177deda1d2c6148f6c8ed94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
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
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ce1f192165e9a7ce336963643a944c339a24427a87c96c3698d3d6641f348`  
		Last Modified: Thu, 17 Oct 2024 09:49:24 GMT  
		Size: 11.6 MB (11620510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1368a401dd210cbfccceb2812e7b128f261e2e405f473856acb05966577669e`  
		Last Modified: Thu, 17 Oct 2024 09:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857dac63f10e78cb54f4c34b160b2b0998eabff35096a85be0e24aa2bb58f449`  
		Last Modified: Tue, 05 Nov 2024 21:17:52 GMT  
		Size: 32.2 MB (32241644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6f09195a593207ce75d9be73f751e6ce6ef99a38be15b4360b8cf0d34ac10`  
		Last Modified: Tue, 05 Nov 2024 21:17:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88415b68ddd65f1576192b0202a994597af5b68e7bca583c3bd60ad6149bd184`  
		Last Modified: Tue, 05 Nov 2024 21:54:20 GMT  
		Size: 13.6 MB (13621933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556df879cab03f3f89c3f38763d416ed94a34868c881661c24730515669c7e1`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43282acfe8bc3378cdee8449c9f279b3c0416b577a8e569f5b6b046496e5ac1`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88b0b3ab7bc7035b605dc96649148617766ec0803ef2de2dcac003716f7295`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:da696bc97d7a9da806411ef957260a321e8430d2b60c75c1ec04f0357113acdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5a1f8afaaa8a1a80afbc43179c8b9b1d2513e38b18fffd794f71f3512dfbb7`

```dockerfile
```

-	Layers:
	-	`sha256:f39ca08e5c34bc53823afd2307a5ef086fb15047356a6ffcebaba4ceae2e955e`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 2.6 MB (2579466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c94f67b72bf9fb1773ae41bf3f42f0b1dc0aac24df4d21c01af6c1e9abdedbb`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 21.2 KB (21212 bytes)  
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
$ docker pull fluentd@sha256:6984bbd16d264b481d2cea3b33e558f5fdbf970ca349d2f5f27451bf07426639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95481145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfb1631b81cc2305fc9ce102c6976f61153bf96fbbb91932dff533880f1db91`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2085a9bf6425e1db4aceff65b459218746f21da3a2b2bc7c609f6e7f3bc13cc`  
		Last Modified: Wed, 30 Oct 2024 18:29:41 GMT  
		Size: 14.6 MB (14591140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d294ef697680ab988c128a54b9e09239e2b59f695cf8665e799a6dae10a3d05`  
		Last Modified: Wed, 30 Oct 2024 18:29:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5ec399be8a51eb991e23efe52aaca4a9322ad460d8209b3baf7b5769b863f`  
		Last Modified: Tue, 05 Nov 2024 21:03:50 GMT  
		Size: 33.7 MB (33729980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f064f984c52c7846f6af551962186edc1e252975cedcd5d437809ac1feb63a`  
		Last Modified: Tue, 05 Nov 2024 21:03:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1761fa9d906a33cf8ba7f88931e5721cd66ba221bfe6bad0393807b695b94`  
		Last Modified: Tue, 05 Nov 2024 21:55:42 GMT  
		Size: 14.0 MB (14035413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5212700fef51cbf7c2e730abd98296a3692effe23f3a0a717bd37ee77a16c01`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247548c94e2052ba7c1a6c3c8b1716d26bf605a0222b30b634c5b8583c5b1746`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e3fcd011126cd33b8bea28f2a6efebef9a3bf3e4cd7516321e45b1fb95e99e`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a238039a647cb1129f11bb47ee8c326a61ca8830d315f5a22fd358bd9091acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9defaaa3c9f73b2eb0cb4e031e598c2117dc88454703ed2016a090f501d78a7`

```dockerfile
```

-	Layers:
	-	`sha256:0d0049973796f5933be2b8e38e1747b02bc7cc4d690cbcc191d92c8517dea6a3`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 2.6 MB (2580322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9584581dd6596d518fd6c6e723be1ccc2442c2dc45b552b2201b76c68f7449c`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 21.2 KB (21173 bytes)  
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
$ docker pull fluentd@sha256:2761de005481ec6f9904caf8ef3becb2263aefccdeea5a19659aaf9049fdaf9c
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
$ docker pull fluentd@sha256:1745a5a982cef63bd21c66b9b137a9762c4faab8cd298694a00fb28c1e17aa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16297518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891664aa169ab161981a30b3b62de4ca81510b685c55b6880764c0450a02febc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b10f5d96e97ceb3b758054e5f53fce3b6bbad9ea0e052366d7b8449216d9f`  
		Last Modified: Sat, 07 Sep 2024 12:53:44 GMT  
		Size: 13.1 MB (13118953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391fe9e5281d4bde619c7e5c71d92fb9e031be3e0b4af6fe016f8fb22a3fd1ff`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6887733c66c8f64b90ce5c1947f14605123431c739f1d110f2679830dca811`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35204c5e77d28136d6633a0f9fff8653fb7bf9aa307668e00a4393d2eef88991`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:573cc73ea2911e43d8b8a879bbf71edf8942cbef351126bd9480140c8d2eb9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792c5be09495ab2f023412f9d696660b66a2764e27ff756e982b3cd9b976afb4`

```dockerfile
```

-	Layers:
	-	`sha256:ab4b17c3b9b1c5cdea7b419e9002925e13303b3bf54c86451ac9222c56d53af5`  
		Last Modified: Sat, 07 Sep 2024 12:53:43 GMT  
		Size: 13.6 KB (13606 bytes)  
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
$ docker pull fluentd@sha256:0e7abc99a8ea730b7bd16c91cbd7e29fe766cf3eca91e637cd5f72e4ba83a5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17102936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530ec17be88bc608a200cda549e2896830ea433b6d9282fe3adf127f9a0e497`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439d0d10ad20b971eeab4a17882bee29d98ed6638ec90cd586f26760b1cc4d6e`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 13.7 MB (13736301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619aebff2e97d98bc39dea9d791d86aaf29000789d90443831cb8d7135e2203b`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aece3d2bd1e2e1850105fa9d0201f6fc47602739717d9343ff02918ab02cc0e`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85db083a94520ef6e956c6a76cc8457242133e1dbc2d7abc2d9eb43cce076bd5`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e245200af63b58345451973f001d1da552a71192d3f891d61aded848229563c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.7 KB (979710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932295115b06403597a65638457a265a4a63e03d9ba592958df100892da53ae4`

```dockerfile
```

-	Layers:
	-	`sha256:54cc512c7e9dd36755e70ce43ce86b34bee28c9900ad0b351309a655a5fb3851`  
		Last Modified: Sat, 07 Sep 2024 11:56:04 GMT  
		Size: 965.9 KB (965927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1db62231943df6cefd36defbec4ecf6f6364dd228a08042f25681fdc47d19a`  
		Last Modified: Sat, 07 Sep 2024 11:56:03 GMT  
		Size: 13.8 KB (13783 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:59606cc1af3633db661c63439f0fce618bd1992b79ae61487b3e5cf804e34dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e772a58a5fc32d69a2142f36b23c99240b8c5119e4cccf786c3df56130d3b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f5006dbaca93167284eb6968f33d7f724cc31e4d8c3ad3e2288d6d2f2beaac`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.7 MB (13711443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f737ed55fe73feed661a95901572355d7a835ba7ba533b0bf60f6a73a46f992`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95087696a6d3f004d6c34f39ea01a1da1f1788aec2a4317244f6873254b105b9`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78193fbe6f5065a08da16003fcbaf57fa023e8cce820a0011492614b658845`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:64b22645d0bccf7ab31d797cd9778ce32ca7fff05dbe6b6e77e91716ecbf0e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72dfa68e09f181c01d535a903dd2bed4156adae6da8199ffe54252a1dbc611f`

```dockerfile
```

-	Layers:
	-	`sha256:cec50a8d3e056ac5b69b56737d850fb338e47e987a9ad0872109a187aff9101a`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 965.3 KB (965311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217bb467f557c0df3252b9a5c783f298f333e52ef5ff3b62ea045c644a6fbc7`  
		Last Modified: Sat, 07 Sep 2024 11:01:54 GMT  
		Size: 13.8 KB (13750 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17.1-debian-1.0`

```console
$ docker pull fluentd@sha256:745730a8a6eb29f33058004ace50970a740a068c64aa62f62654f039cf95d7fe
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
$ docker pull fluentd@sha256:cbd4748d65d744441c7dae3f345b9b64dc88b3cd9cd00b400c879acf2035ccc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84373802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc5bc4ac729ead4f59797a300df858eb2ca63348177deda1d2c6148f6c8ed94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
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
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ce1f192165e9a7ce336963643a944c339a24427a87c96c3698d3d6641f348`  
		Last Modified: Thu, 17 Oct 2024 09:49:24 GMT  
		Size: 11.6 MB (11620510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1368a401dd210cbfccceb2812e7b128f261e2e405f473856acb05966577669e`  
		Last Modified: Thu, 17 Oct 2024 09:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857dac63f10e78cb54f4c34b160b2b0998eabff35096a85be0e24aa2bb58f449`  
		Last Modified: Tue, 05 Nov 2024 21:17:52 GMT  
		Size: 32.2 MB (32241644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6f09195a593207ce75d9be73f751e6ce6ef99a38be15b4360b8cf0d34ac10`  
		Last Modified: Tue, 05 Nov 2024 21:17:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88415b68ddd65f1576192b0202a994597af5b68e7bca583c3bd60ad6149bd184`  
		Last Modified: Tue, 05 Nov 2024 21:54:20 GMT  
		Size: 13.6 MB (13621933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556df879cab03f3f89c3f38763d416ed94a34868c881661c24730515669c7e1`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43282acfe8bc3378cdee8449c9f279b3c0416b577a8e569f5b6b046496e5ac1`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88b0b3ab7bc7035b605dc96649148617766ec0803ef2de2dcac003716f7295`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:da696bc97d7a9da806411ef957260a321e8430d2b60c75c1ec04f0357113acdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5a1f8afaaa8a1a80afbc43179c8b9b1d2513e38b18fffd794f71f3512dfbb7`

```dockerfile
```

-	Layers:
	-	`sha256:f39ca08e5c34bc53823afd2307a5ef086fb15047356a6ffcebaba4ceae2e955e`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 2.6 MB (2579466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c94f67b72bf9fb1773ae41bf3f42f0b1dc0aac24df4d21c01af6c1e9abdedbb`  
		Last Modified: Tue, 05 Nov 2024 21:54:19 GMT  
		Size: 21.2 KB (21212 bytes)  
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
$ docker pull fluentd@sha256:6984bbd16d264b481d2cea3b33e558f5fdbf970ca349d2f5f27451bf07426639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95481145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfb1631b81cc2305fc9ce102c6976f61153bf96fbbb91932dff533880f1db91`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
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
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2085a9bf6425e1db4aceff65b459218746f21da3a2b2bc7c609f6e7f3bc13cc`  
		Last Modified: Wed, 30 Oct 2024 18:29:41 GMT  
		Size: 14.6 MB (14591140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d294ef697680ab988c128a54b9e09239e2b59f695cf8665e799a6dae10a3d05`  
		Last Modified: Wed, 30 Oct 2024 18:29:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5ec399be8a51eb991e23efe52aaca4a9322ad460d8209b3baf7b5769b863f`  
		Last Modified: Tue, 05 Nov 2024 21:03:50 GMT  
		Size: 33.7 MB (33729980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f064f984c52c7846f6af551962186edc1e252975cedcd5d437809ac1feb63a`  
		Last Modified: Tue, 05 Nov 2024 21:03:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1761fa9d906a33cf8ba7f88931e5721cd66ba221bfe6bad0393807b695b94`  
		Last Modified: Tue, 05 Nov 2024 21:55:42 GMT  
		Size: 14.0 MB (14035413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5212700fef51cbf7c2e730abd98296a3692effe23f3a0a717bd37ee77a16c01`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247548c94e2052ba7c1a6c3c8b1716d26bf605a0222b30b634c5b8583c5b1746`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e3fcd011126cd33b8bea28f2a6efebef9a3bf3e4cd7516321e45b1fb95e99e`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a238039a647cb1129f11bb47ee8c326a61ca8830d315f5a22fd358bd9091acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9defaaa3c9f73b2eb0cb4e031e598c2117dc88454703ed2016a090f501d78a7`

```dockerfile
```

-	Layers:
	-	`sha256:0d0049973796f5933be2b8e38e1747b02bc7cc4d690cbcc191d92c8517dea6a3`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 2.6 MB (2580322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9584581dd6596d518fd6c6e723be1ccc2442c2dc45b552b2201b76c68f7449c`  
		Last Modified: Tue, 05 Nov 2024 21:55:41 GMT  
		Size: 21.2 KB (21173 bytes)  
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
