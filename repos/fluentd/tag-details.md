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
$ docker pull fluentd@sha256:8a73a3b60b58336dc1e9aecdda6dcd2478cc6db0fef22466fcb4e0f2d18d1fc0
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
$ docker pull fluentd@sha256:06ba48efc78f94aa227db8e6702a559fe0818cfb607510b8e40f933a66092001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17547145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68fa270df800fba908fafe09411210c40196d3c28848d1f5c5d0c4fa569a2e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142073ae05f89188ef6b19da0e8f307181c78560881cd714f13194837a12be71`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 14.1 MB (14125272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153d663aeaed981219366ac194d2d358f40ca20c2832a6cee5407e0fc8a504e`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00be0c886bdc5511031794a42b5dd1b4b59ed735cd22dadca4a2cd0d236651`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e192ea9505785b51e9ec63f17f4c5c388cca5d6e865311b035f48dd36c15eaa`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ee2c8724b9bcc487cc46ea731eacde8ff3cd3773e055bcc87baa9c1ce70a517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 KB (983977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188bbd2103d2f9534d5320be4087da7d597f1a50bbb7e2cf905a69408c5d8b3a`

```dockerfile
```

-	Layers:
	-	`sha256:46ea48c4284410cf7f93cf8881510daa3bc41574a51f2a5ccf404aeba7b28984`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 970.2 KB (970227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1988f1297412d365e44a402b7f6c777c3a57f619df2c542fd0c243b66fa939`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 13.8 KB (13750 bytes)  
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
$ docker pull fluentd@sha256:46c5cd0d2c67bcaeb5eae4bb699b082213bcd21cc001f7ebfc8032c2c947c458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16508107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822df8e9466b20769bc93fe0cb4beb9dd7cb99bee2b85705369293a69ef9e86e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb23f276a4aaa12fb21b10fee8e6c432039e552dc52906ff21ad079b47c493`  
		Last Modified: Fri, 06 Sep 2024 23:19:16 GMT  
		Size: 13.3 MB (13252342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89021af5e07f2e8f6a1301eb4e3754e53993d29a347aed1a90a7d1021fcf785b`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc201f04644a3c4169fdadabde6d84b708a9aef664ca2b0cfc4da52b976db4`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f060475812c2371f316d9a29a7508f7d4aecbfeb978349835b8cc52cf7b67f`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:27f552f8c3c5f5114458e3ed2969db3666cc5a993260f7d00d220176f8ed7674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.9 KB (980871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db9f7c9dcbdd4674795017459eb84fcf0069b1cb9f9ee1af5232e5a865e6e85`

```dockerfile
```

-	Layers:
	-	`sha256:0614ffa77e02e25955d633f28cc84bd143b92b5ee8cd29b336c2d16f41051966`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 967.1 KB (967147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4eeeb07d1daedce55a60f4b93ba410e951cbbf553068589581fa99b13f452e`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 13.7 KB (13724 bytes)  
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
$ docker pull fluentd@sha256:adb4ac6d46c9a2aa0905f949dc25cdb7e94bce62e891ed924a12981d3899538f
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
$ docker pull fluentd@sha256:577730ac8f0ee2e721e7680daf98e81149d2f117fe48af6ff7b1cca7eceada7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17507096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a0429ca0dd7cdf703915e489f98bb9f860590149e4cc9a93985d242bcd74dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e10c0fd773853990bd67b9a1205c78c9c4af6eb4e4de1f7dcebbf2bd3da6a1a`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 14.1 MB (14085222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2d0b839384afaa0efd0ba2c0eb97c9ed7b3dd3078a011b8fdde45794866087`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095a71b2d4eca389c5dbea8258c4c0e21b7654512e263fa444725e635b8f8fa`  
		Last Modified: Fri, 06 Sep 2024 23:18:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed246c6f6298c8c37c59bad0c8f8d007b161631c8f4dd67345167a8f240627a1`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:87f2d7207c0f13374c5dc7bcc28bff184c47af97ca931cb435d3d02feadd4df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.6 KB (980558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e865bdf94b38414fd49859de00eaead351c18acadd6ae379d8a9a0903724e6`

```dockerfile
```

-	Layers:
	-	`sha256:3d4613618f973fd1949f0bcd4c385db37444be3f2dd495c794b1b4bb5425dd29`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 967.1 KB (967108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11b8e1fb391f3d72ab946b8d291d7c452b71c4bad1fcd28f51c16d181704303`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 13.4 KB (13450 bytes)  
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
$ docker pull fluentd@sha256:16a5c81f5668664c6dc95c06cb228712d42632295f5819741bd410ba00413b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16469247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925d2916a9b257d73a4275e5a83c10d61cee5432255d229d3397d67d7f3e1205`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f047225343ccfdb71245c8aa8694607122e9c7142280985095e902dda76eea`  
		Last Modified: Fri, 06 Sep 2024 23:19:10 GMT  
		Size: 13.2 MB (13213476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa8d66f005d127f3a4b1b8cb0c6ff58e354816606005a10e835108f42ea7a24`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f25306560657630e268b2e9a58b52d9631e5febfae4a7e9ab49ddaa505ecb80`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2bb3917e7cd362321c13984140bce2afa32963093c605a999fcb400b4a0ba`  
		Last Modified: Fri, 06 Sep 2024 23:19:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0a4e0c021e5b3831c38597705e695ec445ce6ce12de496d790c689ca8e6f80db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.5 KB (977462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c7d00cb1e34375e74d7fc13a73cc17eb9f715b39765dc7c26a8a01f808cd76`

```dockerfile
```

-	Layers:
	-	`sha256:cc1ddd48495047dba39bb30fe468e9794f15b1fd1201961696067521fa3f56c2`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 964.0 KB (964033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058d15c4d0af372c5350765ba7e2c71e6e50b03b002e6f4ec50f470b009bd84f`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 13.4 KB (13429 bytes)  
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
$ docker pull fluentd@sha256:8e2f16ca630049c68022b7285fb2738cf14f061a078dc00cb1941f7be05ae484
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
$ docker pull fluentd@sha256:3753454524bb6d0e26a8a8e93639185bf72576e8c437d8f704262a91d3b13480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92045924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e7d8fef92a67058f19f9fd4e34f89366e478744fabc44c249c9c910a25694`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b018291468867ef31745a1bd24eb8ced14622ffab396d720dc4a652974fa78`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 13.9 MB (13861897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7481b8293e89f061160042411c8362728a0dace4229634ed67742cdd7b4c7e`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f26dc88f3d3398ed8ea5fc582c108c402a4cc28d75558325cd968a178f657e`  
		Last Modified: Thu, 17 Oct 2024 01:30:26 GMT  
		Size: 34.9 MB (34903558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96e584bc30d61e91e33d430b597a63ff5a1e159fd79bd1f16797507c926aea`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac2396c2d82f50160382784667af3bd4d869411e8a6a042d07d8c4fe8403b5`  
		Last Modified: Thu, 17 Oct 2024 03:11:45 GMT  
		Size: 14.2 MB (14151780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90717fdeb066bdd485a40e82df0163264777a9b9ce793e40c9ffa0238d52f717`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ae803880b9e6c3e35ee1bb8f2503be6c077216c26dac815573faca629facb`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2e5026a601a38e5dd451a3b94b6726bf2fbbcc58489ddff470dafcbe430e1`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:96a4c259e64509afaa9045574068d956f23c03084a17c18ce272deda14141377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e51ffb9ec0101b6abe2202395f4db4087c81c8a747ee11ee4cc087ca754e9b0`

```dockerfile
```

-	Layers:
	-	`sha256:7e37829df66c270bcb205c3216a86dfba19012ec30d1e839a8ce0149e5ee2ff1`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 2.5 MB (2547319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e38c5ef12be3ce3e1755cb3e86a6e9fc960fdec8b05ef63be1aea7e983b16c`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 21.1 KB (21113 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0fcf5f159f933e9f78089f935f5ca9e512fd0bc16b1ba1c7cbd1a576d45d83db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dde9df656077543b2b05f8651b5731aa522f863d8bc827925c4290d0d530f35`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:375e6c3a6d524df34141daa07cd3856bbd0b557d8b491141f233390299a83ea1`  
		Last Modified: Thu, 17 Oct 2024 09:58:34 GMT  
		Size: 31.0 MB (30965168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c4459c5fab9d7b59863d5de1f82575c5ed9b229dc8aea660eb33eac3d193f`  
		Last Modified: Thu, 17 Oct 2024 09:58:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572d9d0c31f8b2ee6f33a4547e76153f1ca0ae0744a29f59d83dffafa0c2a08`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 14.1 MB (14142492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e648955937e6e0416c483f00069bb3893b01d6e60d8b11816045f783301d02`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a4b486069f716a47adc738fe7502ac98acbdd6ce9fc573f26a53ef7f2a971`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2436b204bb5648941782b5b567482d33f684593c2b83c941af68a698bf407554`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7f60230c4b21c5b94a6e44a4e066ba21f0d87db2e56648ad36e21e21288d9f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48b13d48dc0e7a6eea4cdedcdad499c3e7163793556be2f6fa53d446e69fcc2`

```dockerfile
```

-	Layers:
	-	`sha256:fb9a0793c3ed797134f9e22f9bf32b7986d2ca227cd7b296d79fc2e9cd994ffe`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 2.6 MB (2550704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368dcf7e6acc004501b6309e2b0444b340e0c8ef398cd5c3f9ad841671b5a49d`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5006b50b87258c0f28d5cd2fe260cffcdc16e1c6976e19a3425c4406d31f1fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80728428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96bacac5bf8ab20c11994abf75119c6a3849c359826d73caf92311139c78895`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005f2a876bff1ca6153e9909b25938fb86673586af00dbd8d16eb6781a3be0b`  
		Last Modified: Fri, 27 Sep 2024 18:17:59 GMT  
		Size: 11.0 MB (10959430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a99331e9d3b665abd563c84ab3ce402febb0735ccc148da2ff4054e0350a2`  
		Last Modified: Fri, 27 Sep 2024 18:17:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63934f08dcc44ed337c396e33174b7a86a3ce3b6b227ebb050aacefb5277b5dd`  
		Last Modified: Fri, 27 Sep 2024 18:29:42 GMT  
		Size: 30.8 MB (30810569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df498d2490a44bdeea06a59922eb712a9782846d1fa813df14217986420fef96`  
		Last Modified: Fri, 27 Sep 2024 18:29:41 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e1933ad0223313f68932befc9a1ccd56fc1b414a4d949c9dad7096e446b101`  
		Last Modified: Sat, 28 Sep 2024 06:13:47 GMT  
		Size: 14.2 MB (14237889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3321cc5334f9c6ae0f82198d3e4caf0d0911394c68c94b17776bbffc76e60bc`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a3c67044a98de8818b971d43c58729cfa18ddbb3a0ed672c5665f31625b302`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023df2227481abacdf6405ddf005e7177b374568817b4969b29cc2a61e36cb7d`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9538471ec507d97f955153679584e609f540f348a8ec4b72ea644df12bfb111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2195fe06a88b80664bc63693f9855cabde1b055adfc5fb94e867a1b6c576360b`

```dockerfile
```

-	Layers:
	-	`sha256:db464dd2a029e1800bb20dd196ad7ecd51fdc0b4802e8aaa79e9763f49b70256`  
		Last Modified: Sat, 28 Sep 2024 06:13:47 GMT  
		Size: 2.6 MB (2550721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8df66a96c9f4836bf4e0ef825d372c4c4c997e8339d2cc159fb562207e4bd4`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 21.2 KB (21178 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:6e81809d3df6bc4e49230817bc9a6d3f68f6e4b5bbad20fbfd9cb7fed3aaf8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91066921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b2194109c3b8a3bc2945b400d2d28c537b976a1fcdcd346a7ae9903545e977`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b94787adb8320baa3fe59801066b99684da9616d417863e36c8872528b750b5`  
		Last Modified: Fri, 27 Sep 2024 22:50:09 GMT  
		Size: 12.7 MB (12705350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ae70a92988259064119f85dfc37f2050ebfb8f74934c72a724141eef6d242`  
		Last Modified: Fri, 27 Sep 2024 22:50:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a3116d8c8c3ef4ea597c354181cf10a164b3acf14851378f1091ee1e3a6f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:46 GMT  
		Size: 34.9 MB (34859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f141a20bba990b3c31271b615a6b7628b450ba068a35f333956c203b2e98f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef1200821d58ffdf50b33e319b0ad0cab3198a1ff667204948ab857288c4a0`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 14.3 MB (14343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a4f9385733bdaac97c8631bb5470fa992cf198a0e0697f640e7d019272185d`  
		Last Modified: Sat, 28 Sep 2024 02:03:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11d40b6a5caf9c3768400fd5494fc3bec24fc677814e3f058f6800689eaab6`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3b8a2fb6716a5c8d2137292f98cc5c37b9a5aefdcff8ec51a74d3d4f42e7d1`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:31a8f668b5bb1ecd8a83bdaa6983dde2865710372161c861911779c9178e5cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0f29db5f9b840ba0948b977d4e43b0342002fe6f25033a0df00b69dec2245d`

```dockerfile
```

-	Layers:
	-	`sha256:ef05bda78fca26bf98180e2b32cf2cf785cee87758f9d6c32c1477d3a3fb0db7`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f047d6f9a5a59cf8746973334a38869285c80561e8e54d9fe027fd9403b1671f`  
		Last Modified: Sat, 28 Sep 2024 02:03:36 GMT  
		Size: 21.5 KB (21466 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:62638dd1d60422287791cc6bd96747e207f58aa62ed36b770cdcc2c978c21fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88319296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69082c3e0a6becc1c9fdeec7dcafde23da04fe18bc961f3f60cc3857bd1a7e69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05ffe0f4cbfb58547209577ac3932e587586aa5b43d0aea584478c3b35c29f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 13.4 MB (13417145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03c46221a99f4ecf7545993dbe51e289473289415deedae04101d79fd3359e4`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65643aefe7688dcfbd5880ea936ae6e955bbd63de4b249636e724c620380d56f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 30.8 MB (30809295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd77b7e70b238f9ee726ddb2593be45daa74e8c5921725fbc70d327406f687`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb9ae2dd6b77ebd9d4642eda8ff543177327add5279dfeb026df730fdaa621`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 13.9 MB (13946185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d5775782ba7b787be4494b7551dad085c4d8805d27d66a6ffe1a6232cd8e1`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87665c7aa3efa3954e1e7a5a306870e06ea53661b57e61519189da1e1d179165`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91792300de8f8474fd3444c71127ea41c8aef212e3c7e53dbf670f522eae44e9`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47e4e6b921c4c6870a3f2973d75053e93eadf84dde32e4f6afce0e928d1f6e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdafa7af0490c80a206c97627c4883074e08cf3d6ac2e8124a5e82e40f1e4c6f`

```dockerfile
```

-	Layers:
	-	`sha256:615bb4240a04844abf777c0f5ad7e10d50f423dbe06c5f398d2dd502e2d5ccbe`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 2.5 MB (2544442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a01aea9720b13ef27e906d9087f5afeee8da50555270995672ee209e0c888b`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 21.1 KB (21089 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:80117fafcd9a40bc4f54841e40ac9ef7853ea78051b09742ceb4aac5b7dd0f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94599715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced13e287dd7432ef17b28941df25ad41b61b19a33acfb3efa6e3564758a9696`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:b18ba81a996aee835b99f9746116b7662342396fcbf0fa95a963a31969ab9720`  
		Last Modified: Thu, 17 Oct 2024 13:29:35 GMT  
		Size: 14.6 MB (14591066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda835d95772998115abd86dfa88c03d37b547892247d7ab65bf5703c36157b0`  
		Last Modified: Thu, 17 Oct 2024 13:29:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cd50573cf3da5ce8b4c4105e92d6695fec7cb755c89ef5351a338d5480c1`  
		Last Modified: Thu, 17 Oct 2024 13:43:12 GMT  
		Size: 32.3 MB (32337814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53a6dbd455e1f2c425e9d4f8a67699871eae70f29114397b60d4f48a9a124e`  
		Last Modified: Thu, 17 Oct 2024 13:43:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6a95b7d037311cbdf6ccd9e3376fde7232b5ef960762b19985c7860a535b88`  
		Last Modified: Thu, 17 Oct 2024 15:40:27 GMT  
		Size: 14.5 MB (14546232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb703d82073dc02cfe0cc080eb2c62ed3f655aca86e13f1ac1a48440d047a2d`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5827250f0669f058899560d82a9db239f176822b9ff64f63fd0703c6bc806d`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a24e071c75b2e3d2356e45cdd70be6d131cc71ca856691920e5ae743b25ef5`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e83a9b07073cfc66a752173436d0c9ce7d7dbb90c008a78321ec5ecbee69d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323088ca81e145bbc6ff1260118142a5010388cd35e29f99f33372294efaecaf`

```dockerfile
```

-	Layers:
	-	`sha256:27825581899d78844830a6e4895f227f5eeb890174a7a0a18f64279e183a8448`  
		Last Modified: Thu, 17 Oct 2024 15:40:27 GMT  
		Size: 2.6 MB (2551666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964fa27e6b2df7b8b6a4d6c48485e51aa90142581a252d9b3bd30010dcd2aa11`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:05a3072c0f303dbb5ec1fafb75cad752bb6b8da753582d8c60325fa95e4a9999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85432499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a231284601635638667654dc8870685cbe5f049af3e0d4de2f761751ee75a2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:328bf0e6f36016514cbf3cd2b761769d331632390cdca7902634f8b1181dcf30`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 12.0 MB (12041280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3048dcc1de351b3be6f52baa2abb9c7d3acdc56e8c2357fd5b75aa7b8087e14`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738b6177d31663738d6e9505d211ac67ed2ee505983fdf6fb589d65c47a39080`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 31.6 MB (31610658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ac0692aadcc039d4a1c82b0c464c62ce0d881d9eda6e876525acdaee59a8c2`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a39120248ff9ed528f12af46ebaf7e3c306a7852fc4600dbd47e68ecc8260a`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 14.3 MB (14288079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dc709bae542f1b3922af8f42948551aa518b114a4c2d60a208afc5046fdcef`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36954972ee92d9cd43abe028203a0cbb94b5661b07933eef525f1f5563bdf289`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f815dce462b9ab3bfee3c2eef5100fd9046199ba1f78897a1be2b06704be0a4`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:213bd76c446821b74430f0acbfafe366ddc6a416b5866c522dcad964359db4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071a04a05165fe3c0e7f63e86157db9f35b55ddbabad1b39dd3a29b4f3c2b4e9`

```dockerfile
```

-	Layers:
	-	`sha256:2bc4ebb893759f0bafac8fb8a2f7d85d60663f7f6c4b27cf59d7e07bb9b9a2e2`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 2.5 MB (2547138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa5ee28eb19c44391834d6b77cec153c881a8b8432e639cd900446104d6836c`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.6-1.0`

```console
$ docker pull fluentd@sha256:adb4ac6d46c9a2aa0905f949dc25cdb7e94bce62e891ed924a12981d3899538f
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
$ docker pull fluentd@sha256:577730ac8f0ee2e721e7680daf98e81149d2f117fe48af6ff7b1cca7eceada7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17507096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a0429ca0dd7cdf703915e489f98bb9f860590149e4cc9a93985d242bcd74dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e10c0fd773853990bd67b9a1205c78c9c4af6eb4e4de1f7dcebbf2bd3da6a1a`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 14.1 MB (14085222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2d0b839384afaa0efd0ba2c0eb97c9ed7b3dd3078a011b8fdde45794866087`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095a71b2d4eca389c5dbea8258c4c0e21b7654512e263fa444725e635b8f8fa`  
		Last Modified: Fri, 06 Sep 2024 23:18:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed246c6f6298c8c37c59bad0c8f8d007b161631c8f4dd67345167a8f240627a1`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:87f2d7207c0f13374c5dc7bcc28bff184c47af97ca931cb435d3d02feadd4df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.6 KB (980558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e865bdf94b38414fd49859de00eaead351c18acadd6ae379d8a9a0903724e6`

```dockerfile
```

-	Layers:
	-	`sha256:3d4613618f973fd1949f0bcd4c385db37444be3f2dd495c794b1b4bb5425dd29`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 967.1 KB (967108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11b8e1fb391f3d72ab946b8d291d7c452b71c4bad1fcd28f51c16d181704303`  
		Last Modified: Fri, 06 Sep 2024 23:18:57 GMT  
		Size: 13.4 KB (13450 bytes)  
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
$ docker pull fluentd@sha256:16a5c81f5668664c6dc95c06cb228712d42632295f5819741bd410ba00413b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16469247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925d2916a9b257d73a4275e5a83c10d61cee5432255d229d3397d67d7f3e1205`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Aug 2024 02:52:20 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f047225343ccfdb71245c8aa8694607122e9c7142280985095e902dda76eea`  
		Last Modified: Fri, 06 Sep 2024 23:19:10 GMT  
		Size: 13.2 MB (13213476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa8d66f005d127f3a4b1b8cb0c6ff58e354816606005a10e835108f42ea7a24`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f25306560657630e268b2e9a58b52d9631e5febfae4a7e9ab49ddaa505ecb80`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2bb3917e7cd362321c13984140bce2afa32963093c605a999fcb400b4a0ba`  
		Last Modified: Fri, 06 Sep 2024 23:19:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0a4e0c021e5b3831c38597705e695ec445ce6ce12de496d790c689ca8e6f80db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.5 KB (977462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c7d00cb1e34375e74d7fc13a73cc17eb9f715b39765dc7c26a8a01f808cd76`

```dockerfile
```

-	Layers:
	-	`sha256:cc1ddd48495047dba39bb30fe468e9794f15b1fd1201961696067521fa3f56c2`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 964.0 KB (964033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058d15c4d0af372c5350765ba7e2c71e6e50b03b002e6f4ec50f470b009bd84f`  
		Last Modified: Fri, 06 Sep 2024 23:19:09 GMT  
		Size: 13.4 KB (13429 bytes)  
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
$ docker pull fluentd@sha256:8e2f16ca630049c68022b7285fb2738cf14f061a078dc00cb1941f7be05ae484
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
$ docker pull fluentd@sha256:3753454524bb6d0e26a8a8e93639185bf72576e8c437d8f704262a91d3b13480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92045924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e7d8fef92a67058f19f9fd4e34f89366e478744fabc44c249c9c910a25694`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b018291468867ef31745a1bd24eb8ced14622ffab396d720dc4a652974fa78`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 13.9 MB (13861897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7481b8293e89f061160042411c8362728a0dace4229634ed67742cdd7b4c7e`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f26dc88f3d3398ed8ea5fc582c108c402a4cc28d75558325cd968a178f657e`  
		Last Modified: Thu, 17 Oct 2024 01:30:26 GMT  
		Size: 34.9 MB (34903558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96e584bc30d61e91e33d430b597a63ff5a1e159fd79bd1f16797507c926aea`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac2396c2d82f50160382784667af3bd4d869411e8a6a042d07d8c4fe8403b5`  
		Last Modified: Thu, 17 Oct 2024 03:11:45 GMT  
		Size: 14.2 MB (14151780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90717fdeb066bdd485a40e82df0163264777a9b9ce793e40c9ffa0238d52f717`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8ae803880b9e6c3e35ee1bb8f2503be6c077216c26dac815573faca629facb`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2e5026a601a38e5dd451a3b94b6726bf2fbbcc58489ddff470dafcbe430e1`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:96a4c259e64509afaa9045574068d956f23c03084a17c18ce272deda14141377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e51ffb9ec0101b6abe2202395f4db4087c81c8a747ee11ee4cc087ca754e9b0`

```dockerfile
```

-	Layers:
	-	`sha256:7e37829df66c270bcb205c3216a86dfba19012ec30d1e839a8ce0149e5ee2ff1`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 2.5 MB (2547319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e38c5ef12be3ce3e1755cb3e86a6e9fc960fdec8b05ef63be1aea7e983b16c`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 21.1 KB (21113 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0fcf5f159f933e9f78089f935f5ca9e512fd0bc16b1ba1c7cbd1a576d45d83db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83617875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dde9df656077543b2b05f8651b5731aa522f863d8bc827925c4290d0d530f35`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:375e6c3a6d524df34141daa07cd3856bbd0b557d8b491141f233390299a83ea1`  
		Last Modified: Thu, 17 Oct 2024 09:58:34 GMT  
		Size: 31.0 MB (30965168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c4459c5fab9d7b59863d5de1f82575c5ed9b229dc8aea660eb33eac3d193f`  
		Last Modified: Thu, 17 Oct 2024 09:58:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d572d9d0c31f8b2ee6f33a4547e76153f1ca0ae0744a29f59d83dffafa0c2a08`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 14.1 MB (14142492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e648955937e6e0416c483f00069bb3893b01d6e60d8b11816045f783301d02`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a4b486069f716a47adc738fe7502ac98acbdd6ce9fc573f26a53ef7f2a971`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2436b204bb5648941782b5b567482d33f684593c2b83c941af68a698bf407554`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7f60230c4b21c5b94a6e44a4e066ba21f0d87db2e56648ad36e21e21288d9f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48b13d48dc0e7a6eea4cdedcdad499c3e7163793556be2f6fa53d446e69fcc2`

```dockerfile
```

-	Layers:
	-	`sha256:fb9a0793c3ed797134f9e22f9bf32b7986d2ca227cd7b296d79fc2e9cd994ffe`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 2.6 MB (2550704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368dcf7e6acc004501b6309e2b0444b340e0c8ef398cd5c3f9ad841671b5a49d`  
		Last Modified: Thu, 17 Oct 2024 17:12:41 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5006b50b87258c0f28d5cd2fe260cffcdc16e1c6976e19a3425c4406d31f1fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80728428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96bacac5bf8ab20c11994abf75119c6a3849c359826d73caf92311139c78895`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005f2a876bff1ca6153e9909b25938fb86673586af00dbd8d16eb6781a3be0b`  
		Last Modified: Fri, 27 Sep 2024 18:17:59 GMT  
		Size: 11.0 MB (10959430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a99331e9d3b665abd563c84ab3ce402febb0735ccc148da2ff4054e0350a2`  
		Last Modified: Fri, 27 Sep 2024 18:17:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63934f08dcc44ed337c396e33174b7a86a3ce3b6b227ebb050aacefb5277b5dd`  
		Last Modified: Fri, 27 Sep 2024 18:29:42 GMT  
		Size: 30.8 MB (30810569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df498d2490a44bdeea06a59922eb712a9782846d1fa813df14217986420fef96`  
		Last Modified: Fri, 27 Sep 2024 18:29:41 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e1933ad0223313f68932befc9a1ccd56fc1b414a4d949c9dad7096e446b101`  
		Last Modified: Sat, 28 Sep 2024 06:13:47 GMT  
		Size: 14.2 MB (14237889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3321cc5334f9c6ae0f82198d3e4caf0d0911394c68c94b17776bbffc76e60bc`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a3c67044a98de8818b971d43c58729cfa18ddbb3a0ed672c5665f31625b302`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023df2227481abacdf6405ddf005e7177b374568817b4969b29cc2a61e36cb7d`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9538471ec507d97f955153679584e609f540f348a8ec4b72ea644df12bfb111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2195fe06a88b80664bc63693f9855cabde1b055adfc5fb94e867a1b6c576360b`

```dockerfile
```

-	Layers:
	-	`sha256:db464dd2a029e1800bb20dd196ad7ecd51fdc0b4802e8aaa79e9763f49b70256`  
		Last Modified: Sat, 28 Sep 2024 06:13:47 GMT  
		Size: 2.6 MB (2550721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8df66a96c9f4836bf4e0ef825d372c4c4c997e8339d2cc159fb562207e4bd4`  
		Last Modified: Sat, 28 Sep 2024 06:13:46 GMT  
		Size: 21.2 KB (21178 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:6e81809d3df6bc4e49230817bc9a6d3f68f6e4b5bbad20fbfd9cb7fed3aaf8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91066921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b2194109c3b8a3bc2945b400d2d28c537b976a1fcdcd346a7ae9903545e977`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b94787adb8320baa3fe59801066b99684da9616d417863e36c8872528b750b5`  
		Last Modified: Fri, 27 Sep 2024 22:50:09 GMT  
		Size: 12.7 MB (12705350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ae70a92988259064119f85dfc37f2050ebfb8f74934c72a724141eef6d242`  
		Last Modified: Fri, 27 Sep 2024 22:50:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a3116d8c8c3ef4ea597c354181cf10a164b3acf14851378f1091ee1e3a6f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:46 GMT  
		Size: 34.9 MB (34859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f141a20bba990b3c31271b615a6b7628b450ba068a35f333956c203b2e98f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef1200821d58ffdf50b33e319b0ad0cab3198a1ff667204948ab857288c4a0`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 14.3 MB (14343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a4f9385733bdaac97c8631bb5470fa992cf198a0e0697f640e7d019272185d`  
		Last Modified: Sat, 28 Sep 2024 02:03:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11d40b6a5caf9c3768400fd5494fc3bec24fc677814e3f058f6800689eaab6`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3b8a2fb6716a5c8d2137292f98cc5c37b9a5aefdcff8ec51a74d3d4f42e7d1`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:31a8f668b5bb1ecd8a83bdaa6983dde2865710372161c861911779c9178e5cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2570191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0f29db5f9b840ba0948b977d4e43b0342002fe6f25033a0df00b69dec2245d`

```dockerfile
```

-	Layers:
	-	`sha256:ef05bda78fca26bf98180e2b32cf2cf785cee87758f9d6c32c1477d3a3fb0db7`  
		Last Modified: Sat, 28 Sep 2024 02:03:37 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f047d6f9a5a59cf8746973334a38869285c80561e8e54d9fe027fd9403b1671f`  
		Last Modified: Sat, 28 Sep 2024 02:03:36 GMT  
		Size: 21.5 KB (21466 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:62638dd1d60422287791cc6bd96747e207f58aa62ed36b770cdcc2c978c21fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88319296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69082c3e0a6becc1c9fdeec7dcafde23da04fe18bc961f3f60cc3857bd1a7e69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05ffe0f4cbfb58547209577ac3932e587586aa5b43d0aea584478c3b35c29f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 13.4 MB (13417145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03c46221a99f4ecf7545993dbe51e289473289415deedae04101d79fd3359e4`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65643aefe7688dcfbd5880ea936ae6e955bbd63de4b249636e724c620380d56f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 30.8 MB (30809295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd77b7e70b238f9ee726ddb2593be45daa74e8c5921725fbc70d327406f687`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb9ae2dd6b77ebd9d4642eda8ff543177327add5279dfeb026df730fdaa621`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 13.9 MB (13946185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d5775782ba7b787be4494b7551dad085c4d8805d27d66a6ffe1a6232cd8e1`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87665c7aa3efa3954e1e7a5a306870e06ea53661b57e61519189da1e1d179165`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91792300de8f8474fd3444c71127ea41c8aef212e3c7e53dbf670f522eae44e9`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:47e4e6b921c4c6870a3f2973d75053e93eadf84dde32e4f6afce0e928d1f6e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdafa7af0490c80a206c97627c4883074e08cf3d6ac2e8124a5e82e40f1e4c6f`

```dockerfile
```

-	Layers:
	-	`sha256:615bb4240a04844abf777c0f5ad7e10d50f423dbe06c5f398d2dd502e2d5ccbe`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 2.5 MB (2544442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a01aea9720b13ef27e906d9087f5afeee8da50555270995672ee209e0c888b`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 21.1 KB (21089 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:80117fafcd9a40bc4f54841e40ac9ef7853ea78051b09742ceb4aac5b7dd0f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94599715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced13e287dd7432ef17b28941df25ad41b61b19a33acfb3efa6e3564758a9696`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:b18ba81a996aee835b99f9746116b7662342396fcbf0fa95a963a31969ab9720`  
		Last Modified: Thu, 17 Oct 2024 13:29:35 GMT  
		Size: 14.6 MB (14591066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda835d95772998115abd86dfa88c03d37b547892247d7ab65bf5703c36157b0`  
		Last Modified: Thu, 17 Oct 2024 13:29:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cd50573cf3da5ce8b4c4105e92d6695fec7cb755c89ef5351a338d5480c1`  
		Last Modified: Thu, 17 Oct 2024 13:43:12 GMT  
		Size: 32.3 MB (32337814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53a6dbd455e1f2c425e9d4f8a67699871eae70f29114397b60d4f48a9a124e`  
		Last Modified: Thu, 17 Oct 2024 13:43:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6a95b7d037311cbdf6ccd9e3376fde7232b5ef960762b19985c7860a535b88`  
		Last Modified: Thu, 17 Oct 2024 15:40:27 GMT  
		Size: 14.5 MB (14546232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb703d82073dc02cfe0cc080eb2c62ed3f655aca86e13f1ac1a48440d047a2d`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5827250f0669f058899560d82a9db239f176822b9ff64f63fd0703c6bc806d`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a24e071c75b2e3d2356e45cdd70be6d131cc71ca856691920e5ae743b25ef5`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e83a9b07073cfc66a752173436d0c9ce7d7dbb90c008a78321ec5ecbee69d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323088ca81e145bbc6ff1260118142a5010388cd35e29f99f33372294efaecaf`

```dockerfile
```

-	Layers:
	-	`sha256:27825581899d78844830a6e4895f227f5eeb890174a7a0a18f64279e183a8448`  
		Last Modified: Thu, 17 Oct 2024 15:40:27 GMT  
		Size: 2.6 MB (2551666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964fa27e6b2df7b8b6a4d6c48485e51aa90142581a252d9b3bd30010dcd2aa11`  
		Last Modified: Thu, 17 Oct 2024 15:40:26 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:05a3072c0f303dbb5ec1fafb75cad752bb6b8da753582d8c60325fa95e4a9999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85432499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a231284601635638667654dc8870685cbe5f049af3e0d4de2f761751ee75a2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:328bf0e6f36016514cbf3cd2b761769d331632390cdca7902634f8b1181dcf30`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 12.0 MB (12041280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3048dcc1de351b3be6f52baa2abb9c7d3acdc56e8c2357fd5b75aa7b8087e14`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738b6177d31663738d6e9505d211ac67ed2ee505983fdf6fb589d65c47a39080`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 31.6 MB (31610658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ac0692aadcc039d4a1c82b0c464c62ce0d881d9eda6e876525acdaee59a8c2`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a39120248ff9ed528f12af46ebaf7e3c306a7852fc4600dbd47e68ecc8260a`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 14.3 MB (14288079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dc709bae542f1b3922af8f42948551aa518b114a4c2d60a208afc5046fdcef`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36954972ee92d9cd43abe028203a0cbb94b5661b07933eef525f1f5563bdf289`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f815dce462b9ab3bfee3c2eef5100fd9046199ba1f78897a1be2b06704be0a4`  
		Last Modified: Thu, 17 Oct 2024 19:35:34 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:213bd76c446821b74430f0acbfafe366ddc6a416b5866c522dcad964359db4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071a04a05165fe3c0e7f63e86157db9f35b55ddbabad1b39dd3a29b4f3c2b4e9`

```dockerfile
```

-	Layers:
	-	`sha256:2bc4ebb893759f0bafac8fb8a2f7d85d60663f7f6c4b27cf59d7e07bb9b9a2e2`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 2.5 MB (2547138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa5ee28eb19c44391834d6b77cec153c881a8b8432e639cd900446104d6836c`  
		Last Modified: Thu, 17 Oct 2024 19:35:33 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17-1`

```console
$ docker pull fluentd@sha256:8a73a3b60b58336dc1e9aecdda6dcd2478cc6db0fef22466fcb4e0f2d18d1fc0
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
$ docker pull fluentd@sha256:06ba48efc78f94aa227db8e6702a559fe0818cfb607510b8e40f933a66092001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17547145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68fa270df800fba908fafe09411210c40196d3c28848d1f5c5d0c4fa569a2e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142073ae05f89188ef6b19da0e8f307181c78560881cd714f13194837a12be71`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 14.1 MB (14125272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153d663aeaed981219366ac194d2d358f40ca20c2832a6cee5407e0fc8a504e`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00be0c886bdc5511031794a42b5dd1b4b59ed735cd22dadca4a2cd0d236651`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e192ea9505785b51e9ec63f17f4c5c388cca5d6e865311b035f48dd36c15eaa`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ee2c8724b9bcc487cc46ea731eacde8ff3cd3773e055bcc87baa9c1ce70a517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 KB (983977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188bbd2103d2f9534d5320be4087da7d597f1a50bbb7e2cf905a69408c5d8b3a`

```dockerfile
```

-	Layers:
	-	`sha256:46ea48c4284410cf7f93cf8881510daa3bc41574a51f2a5ccf404aeba7b28984`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 970.2 KB (970227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1988f1297412d365e44a402b7f6c777c3a57f619df2c542fd0c243b66fa939`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 13.8 KB (13750 bytes)  
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
$ docker pull fluentd@sha256:46c5cd0d2c67bcaeb5eae4bb699b082213bcd21cc001f7ebfc8032c2c947c458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16508107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822df8e9466b20769bc93fe0cb4beb9dd7cb99bee2b85705369293a69ef9e86e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb23f276a4aaa12fb21b10fee8e6c432039e552dc52906ff21ad079b47c493`  
		Last Modified: Fri, 06 Sep 2024 23:19:16 GMT  
		Size: 13.3 MB (13252342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89021af5e07f2e8f6a1301eb4e3754e53993d29a347aed1a90a7d1021fcf785b`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc201f04644a3c4169fdadabde6d84b708a9aef664ca2b0cfc4da52b976db4`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f060475812c2371f316d9a29a7508f7d4aecbfeb978349835b8cc52cf7b67f`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:27f552f8c3c5f5114458e3ed2969db3666cc5a993260f7d00d220176f8ed7674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.9 KB (980871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db9f7c9dcbdd4674795017459eb84fcf0069b1cb9f9ee1af5232e5a865e6e85`

```dockerfile
```

-	Layers:
	-	`sha256:0614ffa77e02e25955d633f28cc84bd143b92b5ee8cd29b336c2d16f41051966`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 967.1 KB (967147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4eeeb07d1daedce55a60f4b93ba410e951cbbf553068589581fa99b13f452e`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 13.7 KB (13724 bytes)  
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
$ docker pull fluentd@sha256:1d150c9ed908a9a8f3dc98956e4583cc878fe30ddf9987ce9ab31a0b8008da61
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
$ docker pull fluentd@sha256:40856f48aebd424775f5d6a45c031fc089121fe7e46faa7872bf12704ad333a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91503087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3c68eceee00879e3c9c95f621888ac809c4c17ef70d928bf9bd57da8a2d83`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b018291468867ef31745a1bd24eb8ced14622ffab396d720dc4a652974fa78`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 13.9 MB (13861897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7481b8293e89f061160042411c8362728a0dace4229634ed67742cdd7b4c7e`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f26dc88f3d3398ed8ea5fc582c108c402a4cc28d75558325cd968a178f657e`  
		Last Modified: Thu, 17 Oct 2024 01:30:26 GMT  
		Size: 34.9 MB (34903558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96e584bc30d61e91e33d430b597a63ff5a1e159fd79bd1f16797507c926aea`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c80baf6961c226c504e3ce8365d987c3b08febe1a62594e88b603ad9c1ae9`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 13.6 MB (13608944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62efc075df3326b4e439297f23359cf9ef49636abb444f9b5a99eba64076a55`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c3fc6e4d2cd496d8d98119410785656feaf827ea79f3ce78ea476f559b622b`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c4c3261f5c5115d12e7aaab44e81251fb9d05c5a73c2bf162832905c327e6d`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:943370333878e7ab911a0afefe2ca11e6ee19c9424431fe8ff37efd75e56d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005426ee1d942db763090db7ebd9581d4b19a612a44379116a1572f19db49594`

```dockerfile
```

-	Layers:
	-	`sha256:9103c077012367e5be989807747f3d9f684b8c2f90c299ed8ff01236ee2a60fc`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 2.6 MB (2550124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d554d18e9c217ef76d8dd291ba637d5d0754357842f548866442de10ee1ac4`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 21.1 KB (21112 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e5e42a530ad984a695a5c06a8cf50ae1807c9233728633d6d954afaff4b9eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83075760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3c019a5cc35ddbca21bd11ff835344b928de10d58e95d52ce7908c0a7f6814`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:375e6c3a6d524df34141daa07cd3856bbd0b557d8b491141f233390299a83ea1`  
		Last Modified: Thu, 17 Oct 2024 09:58:34 GMT  
		Size: 31.0 MB (30965168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c4459c5fab9d7b59863d5de1f82575c5ed9b229dc8aea660eb33eac3d193f`  
		Last Modified: Thu, 17 Oct 2024 09:58:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bdfa77205a677144cdf484c6ef0a2e891681a39d3ad14da6a64a7e0b7d1d4a`  
		Last Modified: Thu, 17 Oct 2024 17:16:14 GMT  
		Size: 13.6 MB (13600376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0df7c7c2e63bac8e715dcafe7e46ef430af37615a6a8b69d3548dff3017bfb`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a122b4dba26e711162b2068e483dd4ac9fd38820830d91794cc3d58b8b51cb`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675808f1d1b084a33895d602d5765b9c887bdd75e52b4c43caa5b1bb0001997f`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:da7680d8d3c36939be496973f20c6807c5f9e50da5f3b21dfdfd631dd192d7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed426c4a7f46d03baa22c956c6a3c1514eafe14fda2c787a15db2498c69c7f43`

```dockerfile
```

-	Layers:
	-	`sha256:12b2423db92c4f9aea6dc68d499e2b22676b977c05b619deb7574e0300bfb456`  
		Last Modified: Thu, 17 Oct 2024 17:16:14 GMT  
		Size: 2.6 MB (2553509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db263aee34805003233d9e6a035238d558ea6cfa8befd0df583fa2ff80503cb1`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:7ed2bbeeb80d565a3ab3be4acec40350cb228d6cf4ad67d2ec76b135f2fc41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80183122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2222b2becdf9da5fb40ff13040219a256db79e1155c3bf6e14e81f0ccbf5ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005f2a876bff1ca6153e9909b25938fb86673586af00dbd8d16eb6781a3be0b`  
		Last Modified: Fri, 27 Sep 2024 18:17:59 GMT  
		Size: 11.0 MB (10959430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a99331e9d3b665abd563c84ab3ce402febb0735ccc148da2ff4054e0350a2`  
		Last Modified: Fri, 27 Sep 2024 18:17:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63934f08dcc44ed337c396e33174b7a86a3ce3b6b227ebb050aacefb5277b5dd`  
		Last Modified: Fri, 27 Sep 2024 18:29:42 GMT  
		Size: 30.8 MB (30810569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df498d2490a44bdeea06a59922eb712a9782846d1fa813df14217986420fef96`  
		Last Modified: Fri, 27 Sep 2024 18:29:41 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52dfd7be29ece5a6e87ec0ac658efea72b074aa06790f415ca67682b1025b82`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 13.7 MB (13692580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28309c1765baa55416b43c60209f723ad2db002eb358fbfeb4abb110617b3b39`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59fc62b120dc2aeeab51b22525ac372df7e2aa463596b4011df093ae2782ce5`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afb4b0e0ec1b238110cbd2da0beda7456e0316219f0662db04b75e5d512fc37`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc0958f29025342426930f93673af42a31bd3ebe3251f1f30ef5215fcdf0c351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb64c29401bb5b904c09f186d896bdaeb592ad89402533db36badf13bb28fd2`

```dockerfile
```

-	Layers:
	-	`sha256:98d04c648dbc62b35f8e9ce0f64a188cba35c02df9f106868dcd3d530299e140`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 2.6 MB (2553526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0747c15bdac5f83e883536a2d90c09cad9def3bbab1bed77386ab1869cc3ba76`  
		Last Modified: Sat, 28 Sep 2024 06:17:10 GMT  
		Size: 21.2 KB (21178 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cd021185acfbbd5021ce7b67878f305b80d0cf06534d9daf2e7a611d5ee7b7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90521070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3225cd75112d59aebfa1db5b11ed5d3be45a4dab3ab27b1d08c700394c17ce2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b94787adb8320baa3fe59801066b99684da9616d417863e36c8872528b750b5`  
		Last Modified: Fri, 27 Sep 2024 22:50:09 GMT  
		Size: 12.7 MB (12705350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ae70a92988259064119f85dfc37f2050ebfb8f74934c72a724141eef6d242`  
		Last Modified: Fri, 27 Sep 2024 22:50:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a3116d8c8c3ef4ea597c354181cf10a164b3acf14851378f1091ee1e3a6f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:46 GMT  
		Size: 34.9 MB (34859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f141a20bba990b3c31271b615a6b7628b450ba068a35f333956c203b2e98f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6533dd416bf0d20087bc7c4222278906a30cfff9aa03db310d867e2bd28d194d`  
		Last Modified: Sat, 28 Sep 2024 02:06:41 GMT  
		Size: 13.8 MB (13797281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1990af05d9a960423fcf12d6294b1bb59b493dd75e09ba54f2616e429a2a3455`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa0fd66e988b44f9e790d3d423303d3e11d67e405fda59e77d7abd356a6179c`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e03a91d5fbab2df3b4c8131e6dd3ca7e8afea2fe63d548e7b7c55ef9d79af`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c0ea3c2c30a7641df44634bd3bd5c07af74e746559cadfc52bbb7929e39c8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f17ebefe7b15ad5b81ac904604edbf85d0092f848a9786e3e439c43a50e2804`

```dockerfile
```

-	Layers:
	-	`sha256:87878016e12e7f546f7cc4503ab22d48f693510ae67d17cc20e67907a8efc7f3`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 2.6 MB (2551530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ed4a1a024b360a477769b12ad28ebd53e8870ab9474146d24e5d5deb95a3cb`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 21.5 KB (21466 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:ee72a5a09760560beefeec08fa03c57d1a2ccbfc8cc5eb2adfdfc1b9008c4742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87776809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c5484468257bff146a4cfb833b95892ab2aa214c9fedb86aa9607a63b57c9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05ffe0f4cbfb58547209577ac3932e587586aa5b43d0aea584478c3b35c29f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 13.4 MB (13417145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03c46221a99f4ecf7545993dbe51e289473289415deedae04101d79fd3359e4`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65643aefe7688dcfbd5880ea936ae6e955bbd63de4b249636e724c620380d56f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 30.8 MB (30809295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd77b7e70b238f9ee726ddb2593be45daa74e8c5921725fbc70d327406f687`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e76ef92476be4eab9cce5be807ed48ddf00de16c28f65f76c8e51cbf5a0211`  
		Last Modified: Thu, 17 Oct 2024 03:12:23 GMT  
		Size: 13.4 MB (13403695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd189252fdd28bd81eb35608128dc1b48abb7a7828f4575acd2d3bace9e7f6ea`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e139ab87df7f0841a50b996178b13f56e6b1f15ed15dcf4c7d04acfa20b1b5`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a52ae5cab7799dc3f940aee6d586a1aba070e4b469ccca925cbd4056433728a`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b34429369cb782fd4514f8f12568b87bf916ca3adbb9e27112ab0b7d96ee09e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0666838c8c972a91e45effe35d899c74cb977ecc9879b602723dc528f8d8730f`

```dockerfile
```

-	Layers:
	-	`sha256:e77b8818430037b1087908b63c0d89e6ef44a552c7b9493ed6aabff42b759080`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 2.5 MB (2547247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a169e56021d476091e0ffaf4fb41427762b56496716cdfc15ade31e4429c84`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 21.1 KB (21089 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5f52bed7878e0c48ff246344764c2f1cb02ff77d54a4364ae76286a30ec53a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94059660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b432d5b0b2c84a3806dfad29f5bb8ac1ae1d386e995c45cf32a89829e80bc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:b18ba81a996aee835b99f9746116b7662342396fcbf0fa95a963a31969ab9720`  
		Last Modified: Thu, 17 Oct 2024 13:29:35 GMT  
		Size: 14.6 MB (14591066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda835d95772998115abd86dfa88c03d37b547892247d7ab65bf5703c36157b0`  
		Last Modified: Thu, 17 Oct 2024 13:29:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cd50573cf3da5ce8b4c4105e92d6695fec7cb755c89ef5351a338d5480c1`  
		Last Modified: Thu, 17 Oct 2024 13:43:12 GMT  
		Size: 32.3 MB (32337814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53a6dbd455e1f2c425e9d4f8a67699871eae70f29114397b60d4f48a9a124e`  
		Last Modified: Thu, 17 Oct 2024 13:43:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32171978740a409fb1890f6adaabcdb96fe1ceca8d5203033460cd31c0050adb`  
		Last Modified: Thu, 17 Oct 2024 15:45:08 GMT  
		Size: 14.0 MB (14006175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57f7d825222fe696200d6ff1c63bf84afe68123975b5091cf81990da8a9527`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0844998a05d36c92aa56cc603c2475e1b7a9f0e5570bb23f0dc01f3e29469`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d31eac7a4bed07101e7c418557c5505274eb6df972e43fc7716c9f09f02258`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e37d3a75f37fa5c51e5349ae89cdc6dbe02f1a2bbb70fa1d405911b8588ce087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856423bd93bf44d6ea012df644e57259e7f5840dc2d985d838a9e6ae279751d`

```dockerfile
```

-	Layers:
	-	`sha256:cf7bc5f26cbce6bf08095a850b06ba961074d0dfaa2258d7c5f3b5128526049a`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 2.6 MB (2554471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a590fcd56a242532b1e7f63362a10d5562836526b272aca4f8402dd1d00de8`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:95f2944061b66bc8f61985d1a87e1d714e6071a8d6fc9a21ee031de6a418797e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84892118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a644b5682c71a6c6e29a4997204cb7715342b0786f5f630cc527b8268fd01d3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:328bf0e6f36016514cbf3cd2b761769d331632390cdca7902634f8b1181dcf30`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 12.0 MB (12041280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3048dcc1de351b3be6f52baa2abb9c7d3acdc56e8c2357fd5b75aa7b8087e14`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738b6177d31663738d6e9505d211ac67ed2ee505983fdf6fb589d65c47a39080`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 31.6 MB (31610658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ac0692aadcc039d4a1c82b0c464c62ce0d881d9eda6e876525acdaee59a8c2`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae7c49dab2fb1ced409410f20c16ac11193e5dc05ce9720c47ef26d2316255`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 13.7 MB (13747696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aa13c6aea287bd00d3fb4fe04b3a8e07a6469f9bff1b644599fc9e960765e5`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63067704673879f651174df028af993decdc57888af7b5eee8c5fabf59b23bdc`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906a0c7e7e7d4e6643ebd69d40ad9f7149c3f0d1de25f44bbea6397176dd4313`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f2a9b500e83e1e003d94647f9d262e00c3e9bd4cdae0552edd6083ad56967ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d59b4e62e5a9cc322d57e1eb34edbbdc8155b005ebfee529ac92659f7eae6`

```dockerfile
```

-	Layers:
	-	`sha256:78efbbd88f485f419eb22bb9833be6a06b5477173db72434b6dd6f8ac2c03b8d`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 2.5 MB (2549943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4c63605d2f900b26f47a1411e192a32f39fbb1882e0c4218c6bd14bc6302a9`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.17.1-1.0`

```console
$ docker pull fluentd@sha256:8a73a3b60b58336dc1e9aecdda6dcd2478cc6db0fef22466fcb4e0f2d18d1fc0
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
$ docker pull fluentd@sha256:06ba48efc78f94aa227db8e6702a559fe0818cfb607510b8e40f933a66092001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17547145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68fa270df800fba908fafe09411210c40196d3c28848d1f5c5d0c4fa569a2e3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142073ae05f89188ef6b19da0e8f307181c78560881cd714f13194837a12be71`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 14.1 MB (14125272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153d663aeaed981219366ac194d2d358f40ca20c2832a6cee5407e0fc8a504e`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00be0c886bdc5511031794a42b5dd1b4b59ed735cd22dadca4a2cd0d236651`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e192ea9505785b51e9ec63f17f4c5c388cca5d6e865311b035f48dd36c15eaa`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ee2c8724b9bcc487cc46ea731eacde8ff3cd3773e055bcc87baa9c1ce70a517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 KB (983977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188bbd2103d2f9534d5320be4087da7d597f1a50bbb7e2cf905a69408c5d8b3a`

```dockerfile
```

-	Layers:
	-	`sha256:46ea48c4284410cf7f93cf8881510daa3bc41574a51f2a5ccf404aeba7b28984`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 970.2 KB (970227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1988f1297412d365e44a402b7f6c777c3a57f619df2c542fd0c243b66fa939`  
		Last Modified: Fri, 06 Sep 2024 23:19:00 GMT  
		Size: 13.8 KB (13750 bytes)  
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
$ docker pull fluentd@sha256:46c5cd0d2c67bcaeb5eae4bb699b082213bcd21cc001f7ebfc8032c2c947c458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16508107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822df8e9466b20769bc93fe0cb4beb9dd7cb99bee2b85705369293a69ef9e86e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb23f276a4aaa12fb21b10fee8e6c432039e552dc52906ff21ad079b47c493`  
		Last Modified: Fri, 06 Sep 2024 23:19:16 GMT  
		Size: 13.3 MB (13252342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89021af5e07f2e8f6a1301eb4e3754e53993d29a347aed1a90a7d1021fcf785b`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc201f04644a3c4169fdadabde6d84b708a9aef664ca2b0cfc4da52b976db4`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f060475812c2371f316d9a29a7508f7d4aecbfeb978349835b8cc52cf7b67f`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:27f552f8c3c5f5114458e3ed2969db3666cc5a993260f7d00d220176f8ed7674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.9 KB (980871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db9f7c9dcbdd4674795017459eb84fcf0069b1cb9f9ee1af5232e5a865e6e85`

```dockerfile
```

-	Layers:
	-	`sha256:0614ffa77e02e25955d633f28cc84bd143b92b5ee8cd29b336c2d16f41051966`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 967.1 KB (967147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4eeeb07d1daedce55a60f4b93ba410e951cbbf553068589581fa99b13f452e`  
		Last Modified: Fri, 06 Sep 2024 23:19:15 GMT  
		Size: 13.7 KB (13724 bytes)  
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
$ docker pull fluentd@sha256:1d150c9ed908a9a8f3dc98956e4583cc878fe30ddf9987ce9ab31a0b8008da61
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
$ docker pull fluentd@sha256:40856f48aebd424775f5d6a45c031fc089121fe7e46faa7872bf12704ad333a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91503087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3c68eceee00879e3c9c95f621888ac809c4c17ef70d928bf9bd57da8a2d83`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b018291468867ef31745a1bd24eb8ced14622ffab396d720dc4a652974fa78`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 13.9 MB (13861897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7481b8293e89f061160042411c8362728a0dace4229634ed67742cdd7b4c7e`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f26dc88f3d3398ed8ea5fc582c108c402a4cc28d75558325cd968a178f657e`  
		Last Modified: Thu, 17 Oct 2024 01:30:26 GMT  
		Size: 34.9 MB (34903558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96e584bc30d61e91e33d430b597a63ff5a1e159fd79bd1f16797507c926aea`  
		Last Modified: Thu, 17 Oct 2024 01:30:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c80baf6961c226c504e3ce8365d987c3b08febe1a62594e88b603ad9c1ae9`  
		Last Modified: Thu, 17 Oct 2024 03:11:44 GMT  
		Size: 13.6 MB (13608944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62efc075df3326b4e439297f23359cf9ef49636abb444f9b5a99eba64076a55`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c3fc6e4d2cd496d8d98119410785656feaf827ea79f3ce78ea476f559b622b`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c4c3261f5c5115d12e7aaab44e81251fb9d05c5a73c2bf162832905c327e6d`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:943370333878e7ab911a0afefe2ca11e6ee19c9424431fe8ff37efd75e56d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005426ee1d942db763090db7ebd9581d4b19a612a44379116a1572f19db49594`

```dockerfile
```

-	Layers:
	-	`sha256:9103c077012367e5be989807747f3d9f684b8c2f90c299ed8ff01236ee2a60fc`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 2.6 MB (2550124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d554d18e9c217ef76d8dd291ba637d5d0754357842f548866442de10ee1ac4`  
		Last Modified: Thu, 17 Oct 2024 03:11:43 GMT  
		Size: 21.1 KB (21112 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e5e42a530ad984a695a5c06a8cf50ae1807c9233728633d6d954afaff4b9eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83075760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3c019a5cc35ddbca21bd11ff835344b928de10d58e95d52ce7908c0a7f6814`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:375e6c3a6d524df34141daa07cd3856bbd0b557d8b491141f233390299a83ea1`  
		Last Modified: Thu, 17 Oct 2024 09:58:34 GMT  
		Size: 31.0 MB (30965168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c4459c5fab9d7b59863d5de1f82575c5ed9b229dc8aea660eb33eac3d193f`  
		Last Modified: Thu, 17 Oct 2024 09:58:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bdfa77205a677144cdf484c6ef0a2e891681a39d3ad14da6a64a7e0b7d1d4a`  
		Last Modified: Thu, 17 Oct 2024 17:16:14 GMT  
		Size: 13.6 MB (13600376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0df7c7c2e63bac8e715dcafe7e46ef430af37615a6a8b69d3548dff3017bfb`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a122b4dba26e711162b2068e483dd4ac9fd38820830d91794cc3d58b8b51cb`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675808f1d1b084a33895d602d5765b9c887bdd75e52b4c43caa5b1bb0001997f`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:da7680d8d3c36939be496973f20c6807c5f9e50da5f3b21dfdfd631dd192d7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed426c4a7f46d03baa22c956c6a3c1514eafe14fda2c787a15db2498c69c7f43`

```dockerfile
```

-	Layers:
	-	`sha256:12b2423db92c4f9aea6dc68d499e2b22676b977c05b619deb7574e0300bfb456`  
		Last Modified: Thu, 17 Oct 2024 17:16:14 GMT  
		Size: 2.6 MB (2553509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db263aee34805003233d9e6a035238d558ea6cfa8befd0df583fa2ff80503cb1`  
		Last Modified: Thu, 17 Oct 2024 17:16:13 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:7ed2bbeeb80d565a3ab3be4acec40350cb228d6cf4ad67d2ec76b135f2fc41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80183122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2222b2becdf9da5fb40ff13040219a256db79e1155c3bf6e14e81f0ccbf5ae`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005f2a876bff1ca6153e9909b25938fb86673586af00dbd8d16eb6781a3be0b`  
		Last Modified: Fri, 27 Sep 2024 18:17:59 GMT  
		Size: 11.0 MB (10959430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a99331e9d3b665abd563c84ab3ce402febb0735ccc148da2ff4054e0350a2`  
		Last Modified: Fri, 27 Sep 2024 18:17:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63934f08dcc44ed337c396e33174b7a86a3ce3b6b227ebb050aacefb5277b5dd`  
		Last Modified: Fri, 27 Sep 2024 18:29:42 GMT  
		Size: 30.8 MB (30810569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df498d2490a44bdeea06a59922eb712a9782846d1fa813df14217986420fef96`  
		Last Modified: Fri, 27 Sep 2024 18:29:41 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52dfd7be29ece5a6e87ec0ac658efea72b074aa06790f415ca67682b1025b82`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 13.7 MB (13692580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28309c1765baa55416b43c60209f723ad2db002eb358fbfeb4abb110617b3b39`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59fc62b120dc2aeeab51b22525ac372df7e2aa463596b4011df093ae2782ce5`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afb4b0e0ec1b238110cbd2da0beda7456e0316219f0662db04b75e5d512fc37`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc0958f29025342426930f93673af42a31bd3ebe3251f1f30ef5215fcdf0c351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2574704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb64c29401bb5b904c09f186d896bdaeb592ad89402533db36badf13bb28fd2`

```dockerfile
```

-	Layers:
	-	`sha256:98d04c648dbc62b35f8e9ce0f64a188cba35c02df9f106868dcd3d530299e140`  
		Last Modified: Sat, 28 Sep 2024 06:17:11 GMT  
		Size: 2.6 MB (2553526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0747c15bdac5f83e883536a2d90c09cad9def3bbab1bed77386ab1869cc3ba76`  
		Last Modified: Sat, 28 Sep 2024 06:17:10 GMT  
		Size: 21.2 KB (21178 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:cd021185acfbbd5021ce7b67878f305b80d0cf06534d9daf2e7a611d5ee7b7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90521070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3225cd75112d59aebfa1db5b11ed5d3be45a4dab3ab27b1d08c700394c17ce2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b94787adb8320baa3fe59801066b99684da9616d417863e36c8872528b750b5`  
		Last Modified: Fri, 27 Sep 2024 22:50:09 GMT  
		Size: 12.7 MB (12705350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ae70a92988259064119f85dfc37f2050ebfb8f74934c72a724141eef6d242`  
		Last Modified: Fri, 27 Sep 2024 22:50:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a3116d8c8c3ef4ea597c354181cf10a164b3acf14851378f1091ee1e3a6f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:46 GMT  
		Size: 34.9 MB (34859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f141a20bba990b3c31271b615a6b7628b450ba068a35f333956c203b2e98f4`  
		Last Modified: Fri, 27 Sep 2024 23:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6533dd416bf0d20087bc7c4222278906a30cfff9aa03db310d867e2bd28d194d`  
		Last Modified: Sat, 28 Sep 2024 02:06:41 GMT  
		Size: 13.8 MB (13797281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1990af05d9a960423fcf12d6294b1bb59b493dd75e09ba54f2616e429a2a3455`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa0fd66e988b44f9e790d3d423303d3e11d67e405fda59e77d7abd356a6179c`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e03a91d5fbab2df3b4c8131e6dd3ca7e8afea2fe63d548e7b7c55ef9d79af`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c0ea3c2c30a7641df44634bd3bd5c07af74e746559cadfc52bbb7929e39c8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f17ebefe7b15ad5b81ac904604edbf85d0092f848a9786e3e439c43a50e2804`

```dockerfile
```

-	Layers:
	-	`sha256:87878016e12e7f546f7cc4503ab22d48f693510ae67d17cc20e67907a8efc7f3`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 2.6 MB (2551530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ed4a1a024b360a477769b12ad28ebd53e8870ab9474146d24e5d5deb95a3cb`  
		Last Modified: Sat, 28 Sep 2024 02:06:40 GMT  
		Size: 21.5 KB (21466 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:ee72a5a09760560beefeec08fa03c57d1a2ccbfc8cc5eb2adfdfc1b9008c4742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87776809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c5484468257bff146a4cfb833b95892ab2aa214c9fedb86aa9607a63b57c9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05ffe0f4cbfb58547209577ac3932e587586aa5b43d0aea584478c3b35c29f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 13.4 MB (13417145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03c46221a99f4ecf7545993dbe51e289473289415deedae04101d79fd3359e4`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65643aefe7688dcfbd5880ea936ae6e955bbd63de4b249636e724c620380d56f`  
		Last Modified: Thu, 17 Oct 2024 01:31:50 GMT  
		Size: 30.8 MB (30809295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd77b7e70b238f9ee726ddb2593be45daa74e8c5921725fbc70d327406f687`  
		Last Modified: Thu, 17 Oct 2024 01:31:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e76ef92476be4eab9cce5be807ed48ddf00de16c28f65f76c8e51cbf5a0211`  
		Last Modified: Thu, 17 Oct 2024 03:12:23 GMT  
		Size: 13.4 MB (13403695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd189252fdd28bd81eb35608128dc1b48abb7a7828f4575acd2d3bace9e7f6ea`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e139ab87df7f0841a50b996178b13f56e6b1f15ed15dcf4c7d04acfa20b1b5`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a52ae5cab7799dc3f940aee6d586a1aba070e4b469ccca925cbd4056433728a`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b34429369cb782fd4514f8f12568b87bf916ca3adbb9e27112ab0b7d96ee09e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2568336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0666838c8c972a91e45effe35d899c74cb977ecc9879b602723dc528f8d8730f`

```dockerfile
```

-	Layers:
	-	`sha256:e77b8818430037b1087908b63c0d89e6ef44a552c7b9493ed6aabff42b759080`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 2.5 MB (2547247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a169e56021d476091e0ffaf4fb41427762b56496716cdfc15ade31e4429c84`  
		Last Modified: Thu, 17 Oct 2024 03:12:22 GMT  
		Size: 21.1 KB (21089 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5f52bed7878e0c48ff246344764c2f1cb02ff77d54a4364ae76286a30ec53a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94059660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b432d5b0b2c84a3806dfad29f5bb8ac1ae1d386e995c45cf32a89829e80bc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:b18ba81a996aee835b99f9746116b7662342396fcbf0fa95a963a31969ab9720`  
		Last Modified: Thu, 17 Oct 2024 13:29:35 GMT  
		Size: 14.6 MB (14591066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda835d95772998115abd86dfa88c03d37b547892247d7ab65bf5703c36157b0`  
		Last Modified: Thu, 17 Oct 2024 13:29:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7cd50573cf3da5ce8b4c4105e92d6695fec7cb755c89ef5351a338d5480c1`  
		Last Modified: Thu, 17 Oct 2024 13:43:12 GMT  
		Size: 32.3 MB (32337814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53a6dbd455e1f2c425e9d4f8a67699871eae70f29114397b60d4f48a9a124e`  
		Last Modified: Thu, 17 Oct 2024 13:43:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32171978740a409fb1890f6adaabcdb96fe1ceca8d5203033460cd31c0050adb`  
		Last Modified: Thu, 17 Oct 2024 15:45:08 GMT  
		Size: 14.0 MB (14006175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57f7d825222fe696200d6ff1c63bf84afe68123975b5091cf81990da8a9527`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0844998a05d36c92aa56cc603c2475e1b7a9f0e5570bb23f0dc01f3e29469`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d31eac7a4bed07101e7c418557c5505274eb6df972e43fc7716c9f09f02258`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e37d3a75f37fa5c51e5349ae89cdc6dbe02f1a2bbb70fa1d405911b8588ce087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856423bd93bf44d6ea012df644e57259e7f5840dc2d985d838a9e6ae279751d`

```dockerfile
```

-	Layers:
	-	`sha256:cf7bc5f26cbce6bf08095a850b06ba961074d0dfaa2258d7c5f3b5128526049a`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 2.6 MB (2554471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a590fcd56a242532b1e7f63362a10d5562836526b272aca4f8402dd1d00de8`  
		Last Modified: Thu, 17 Oct 2024 15:45:07 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:95f2944061b66bc8f61985d1a87e1d714e6071a8d6fc9a21ee031de6a418797e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84892118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a644b5682c71a6c6e29a4997204cb7715342b0786f5f630cc527b8268fd01d3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 26 Jul 2024 16:23:41 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_VERSION=3.2.5
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.5.tar.xz
# Fri, 26 Jul 2024 16:23:41 GMT
ENV RUBY_DOWNLOAD_SHA256=7780d91130139406d39b29ed8fe16bba350d8fa00e510c76bef9b8ec1340903c
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jul 2024 16:23:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 16:23:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 26 Jul 2024 16:23:41 GMT
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
	-	`sha256:328bf0e6f36016514cbf3cd2b761769d331632390cdca7902634f8b1181dcf30`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 12.0 MB (12041280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3048dcc1de351b3be6f52baa2abb9c7d3acdc56e8c2357fd5b75aa7b8087e14`  
		Last Modified: Thu, 17 Oct 2024 18:03:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738b6177d31663738d6e9505d211ac67ed2ee505983fdf6fb589d65c47a39080`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 31.6 MB (31610658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ac0692aadcc039d4a1c82b0c464c62ce0d881d9eda6e876525acdaee59a8c2`  
		Last Modified: Thu, 17 Oct 2024 18:15:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae7c49dab2fb1ced409410f20c16ac11193e5dc05ce9720c47ef26d2316255`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 13.7 MB (13747696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aa13c6aea287bd00d3fb4fe04b3a8e07a6469f9bff1b644599fc9e960765e5`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63067704673879f651174df028af993decdc57888af7b5eee8c5fabf59b23bdc`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906a0c7e7e7d4e6643ebd69d40ad9f7149c3f0d1de25f44bbea6397176dd4313`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f2a9b500e83e1e003d94647f9d262e00c3e9bd4cdae0552edd6083ad56967ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d59b4e62e5a9cc322d57e1eb34edbbdc8155b005ebfee529ac92659f7eae6`

```dockerfile
```

-	Layers:
	-	`sha256:78efbbd88f485f419eb22bb9833be6a06b5477173db72434b6dd6f8ac2c03b8d`  
		Last Modified: Thu, 17 Oct 2024 19:38:43 GMT  
		Size: 2.5 MB (2549943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4c63605d2f900b26f47a1411e192a32f39fbb1882e0c4218c6bd14bc6302a9`  
		Last Modified: Thu, 17 Oct 2024 19:38:42 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json
