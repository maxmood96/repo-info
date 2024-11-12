## `fluentd:latest`

```console
$ docker pull fluentd@sha256:3d86b077cd2a983b4e7058d63e0a90944b70ee66f441c1f5c46b5fa42c9f17d4
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
