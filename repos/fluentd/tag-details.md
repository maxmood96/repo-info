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
$ docker pull fluentd@sha256:021de1d5819dbb737438e0bbe2a44f87a27dd905b3b079303c32e3e52bfca359
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
$ docker pull fluentd@sha256:4c326bbff82e9ef026b2727f46a30bbdeaa4acf11bbda9f79ba156d8f7b31cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92231257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c817102de996b9b867b07f668302224e54c5beab8a598428e417150394c9eb9c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac603e3acde9c2e5596ee3ef27767ad3ca9fc39159f9c321addd1eb919a33e51`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 13.9 MB (13862276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293e8c1ee175c3a3a89c4e2a16aa1656adfdeb820f527a6395c34a7ae2f770c`  
		Last Modified: Fri, 27 Sep 2024 06:17:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2631bf1c371b778cc33ce5a5c6b81e65b44093ee038fdcb0b5c815d4f094dbcf`  
		Last Modified: Fri, 27 Sep 2024 06:18:03 GMT  
		Size: 34.9 MB (34903601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1a4a91a396fef1d11f17a3eaa83e97c971cf7ea9cca046957a6e3a9228ede`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7133346ea7b624b884006dc5540ec89d699f2a74a6a871998954e90c0e5189`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 14.3 MB (14336706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfd5e064f761ab13707b85e9ecc8337dae469ce292a3cacf6d29f9049b83cf`  
		Last Modified: Fri, 27 Sep 2024 07:06:43 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac07c41a86ed8f226682a64c7ac6c68b1500e1300a9f6c5d1f9d1fe027bc2e7`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edc21907296cffa26406768c524d9cc0fa628b21d0edbe0ce24f68caf97b97b`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b6167c9b08df362e7f0900d52ac3b4a4dfa058141d9eec2175d68d64d7309740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983f511645ebcdf3dff1ca29ccbb6647185fb8d2f7777bf83d2e57591e867c03`

```dockerfile
```

-	Layers:
	-	`sha256:42fc41dc4f055f8032d442d9809a0bf46af08edf9a4b38c233a915c16a60350b`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 2.5 MB (2548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c8821aeddabdcf3bd629c9650d4549fae2aa9f22262551eb9d5c74605d584d`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:69b4a879eb3953541af941acdc2f299645c4c779efc2299159c64656488363ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83793331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8143c3496203c071fcd13ab0845e3e1795ac143dbd5baafbcb9dc534c7e4c37d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45845df8f6f470d7a059a7929530fe5fe9f9c235b398cc7ca33942bb8a61880`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 11.6 MB (11619729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafdc7b73c599d0ee3cfa9f4b5a540c2c1046536633de446f2f2e502766b47d`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d93e02f376a36b740dc38b1fb2ca43d3bafe3c8a22b5bba0a6716f796bdab2`  
		Last Modified: Fri, 27 Sep 2024 16:27:29 GMT  
		Size: 31.0 MB (30964743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cf82729737584fce4d757d120d529716884b0ae6a2dbd129a68340ca54678`  
		Last Modified: Fri, 27 Sep 2024 16:27:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01eda4eff6d554f82625e41ccd42a612fb85de89c66bc09663a5182b90f3ab`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 14.3 MB (14319150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c21ab13aabdff7f6b0f6a2928f7b6a685c7e9c0e1d7370a5827d06b67bfc6`  
		Last Modified: Fri, 27 Sep 2024 18:10:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4775d3c85d65939db8d0934b011021f7a3b945410abe45ec07add5f0f35250`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c766cd22eb374c4befe448e8f88f5d5a8e76404d815261fa5d5e67dc1a2d59`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d1619558841c6de5a18b1cab8d03e570e9ad07ca80be585a4e2354e1e097389b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1811aa80a45d741fedfc9551aa68a1ffccf01140613c650c2dfe8457b39699e0`

```dockerfile
```

-	Layers:
	-	`sha256:e47d2719ebb9f3fbc73cb53ed5e371ab04b3c13fcea89621627628212f342d44`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 2.6 MB (2551866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98544094124c3d6d5c2ad67eaa9aee9fa367812a150f419fc7af3fe24827a32c`  
		Last Modified: Fri, 27 Sep 2024 18:10:36 GMT  
		Size: 21.2 KB (21178 bytes)  
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
$ docker pull fluentd@sha256:e13fbc2ad25ee980ac73e6b37fad57c64a41fbe28b3f210b8fd54bdc9e50a6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88502808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f887eb123c22da239cae7ffd9cd69194e9f5cae2aead7d51cbe69f05c563c24`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2311d534ce56c21a7a499479c7f9c79e8c270bf304eb0ab12142c09122d27577`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 13.4 MB (13416835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7aec7f52e4f19ff57ca320ed34686668513ad4554f001047df6dfee2fadfe4`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e5e4e419fe1e66bc38ce38c7bbdc395aa7002d4c7c658ea4eb0bdd4a40f607`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 30.8 MB (30809165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f0214ae49c0dcde1cd4cd4a105d68aae76b3be6bf15222d2275a52b5ae1787`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeae5c03e504e9bcdaae0a322d87d1dacc1a99bba3f2fd1419915a2bd0efb70`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 14.1 MB (14130190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b78976e65bdb6307a1fafe82be99e8d37b0f563da523177ffb5cdb01cb0f6e`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719fd1c2f805e501175de95cc3b926ebf3d065888290d5eb661c5cfacd9cd70`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5be5fb7bd5e5902febb2d863d55ac93beb6e10ea2fd8b7525010d86aa932f4b`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e58491b279da6fb1e60c9fc4ab0ca3e483c31f0dd7ebb1dbc5f3adb976a615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d541e9f47f608aa99f70adb10ad1bfce9d519c95e9245de1f7d277d987e59c7`

```dockerfile
```

-	Layers:
	-	`sha256:b44213b03c423b8add4d944e596cf8b34d9a42eb0c16ba5dc35e2e5206a5c17b`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 2.5 MB (2545604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d5cc48ff7971ba7789d92a010071c9f37e6f817419330c23bfab862250e6ed`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 21.1 KB (21050 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ddab9d7a1a1dce178234b1005ef85b412951516af28ff077d0b4f4a2a4694608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94787093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4013e63af1dd7c1c85c956b453ff38b8c0536986232fed89135591aab3086871`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944decc6c885a3cfb18414f7007b22fc8a4b77f4b16c9d881f26c07c4a59167`  
		Last Modified: Sat, 28 Sep 2024 00:51:13 GMT  
		Size: 14.6 MB (14590506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69529784e0f3b0b65d2ec424cdcd4b6997929a1e9900af7d5be09782809f4888`  
		Last Modified: Sat, 28 Sep 2024 00:51:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab681378a03a161e604840dbbfb18199db4422ff0623e5af4b1df3f098613ba`  
		Last Modified: Sat, 28 Sep 2024 01:03:58 GMT  
		Size: 32.3 MB (32337939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c711126121e4549d63a054288a85638b37fce915537843b43daf3854b401c`  
		Last Modified: Sat, 28 Sep 2024 01:03:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d362b85020f4b13957131ed62e93770f304b8b235ec2ce14fa76d1953aa66b`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 14.7 MB (14734083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684878939979fe59f6190c039e61653d557d6afb17f850db5bdc55d03bd7f1e2`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb5e41bcc064bd139c4cc97e0542a3d4b7b5b10a830bce390c271e765f6818f`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47974dfbb883e661c2a906668c0bf1ed73f640247d58bbf0b877371f2b84e360`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:efa5f1c25ae6511a23cda33d24febe4110361d784998223790501323cc7de1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72771adf42675987c0d8a34bfd0c58be662b40f84efab24916a67ee5af0e5180`

```dockerfile
```

-	Layers:
	-	`sha256:f0603cea9e1c341a21140c6a7d9d7679bc2315a83b6641c6ee1af4dcccacc37c`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 2.6 MB (2552828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9691c7e3cd6e2025f1fb0909af5f4f5990d147e86886a7f157dc4f00a523404`  
		Last Modified: Sat, 28 Sep 2024 05:21:17 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:f6a09cc8b93da48caa67b47e0bb225b2407e5a0ad2a1022208eb5341b8e7adc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85614292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a143e6c09a1d17f1aaf40a15e81eafae4b932cbc80fe15b25a657765301f8463`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4964b44d90bb8a258c7d0da09e47f2bc08c5a6a6e0f8a115ee932af6c1846`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 12.0 MB (12040811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9c9b4664bd84b47f7aeb29e34ee545ddc3509c2693234ac7d0748eec301d2`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124c8bc976af5cce1e69a2598f76b68dbb9fc2037142bf553908ff2ee4e4cb8`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 31.6 MB (31610348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d0923518b1d48669040a368d05d833b81740bb9dec6257e085fc79e35cb43e`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff64543b84f526b7e5bb2b22c6d0aca2e252f09966d131aaaf06b4143ba0b8`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 14.5 MB (14470711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4873e299f9161accbf5a05dced7cf435cf0b62f0b15a67aae021ae9af2b712`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e335a11e7850106cab49aaa0933550296a522a4ac7132b93065b9c9b9bf2d`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787f2a7b6277f438834c1f006d5562249a94f5c29577e41f26ff44cd3c9e3460`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f91210c0698d6ad98c6268b057e345c448afafeee61e3c6613c9288ece250b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39413d15ce89341a2370d7548ac547fce88af508055285501c7ece40c1858193`

```dockerfile
```

-	Layers:
	-	`sha256:82cc5efa302cca458cd638e607b8b26fea0cd309e492b5fdad5a8fe4f8791d15`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 2.5 MB (2548300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adff21f06d4ce32a1e1ea09cad42249c1290ab25b87c77c236913f4c4cbbdfb`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 21.1 KB (21105 bytes)  
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
$ docker pull fluentd@sha256:021de1d5819dbb737438e0bbe2a44f87a27dd905b3b079303c32e3e52bfca359
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
$ docker pull fluentd@sha256:4c326bbff82e9ef026b2727f46a30bbdeaa4acf11bbda9f79ba156d8f7b31cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92231257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c817102de996b9b867b07f668302224e54c5beab8a598428e417150394c9eb9c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac603e3acde9c2e5596ee3ef27767ad3ca9fc39159f9c321addd1eb919a33e51`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 13.9 MB (13862276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293e8c1ee175c3a3a89c4e2a16aa1656adfdeb820f527a6395c34a7ae2f770c`  
		Last Modified: Fri, 27 Sep 2024 06:17:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2631bf1c371b778cc33ce5a5c6b81e65b44093ee038fdcb0b5c815d4f094dbcf`  
		Last Modified: Fri, 27 Sep 2024 06:18:03 GMT  
		Size: 34.9 MB (34903601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1a4a91a396fef1d11f17a3eaa83e97c971cf7ea9cca046957a6e3a9228ede`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7133346ea7b624b884006dc5540ec89d699f2a74a6a871998954e90c0e5189`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 14.3 MB (14336706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfd5e064f761ab13707b85e9ecc8337dae469ce292a3cacf6d29f9049b83cf`  
		Last Modified: Fri, 27 Sep 2024 07:06:43 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac07c41a86ed8f226682a64c7ac6c68b1500e1300a9f6c5d1f9d1fe027bc2e7`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edc21907296cffa26406768c524d9cc0fa628b21d0edbe0ce24f68caf97b97b`  
		Last Modified: Fri, 27 Sep 2024 07:06:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b6167c9b08df362e7f0900d52ac3b4a4dfa058141d9eec2175d68d64d7309740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983f511645ebcdf3dff1ca29ccbb6647185fb8d2f7777bf83d2e57591e867c03`

```dockerfile
```

-	Layers:
	-	`sha256:42fc41dc4f055f8032d442d9809a0bf46af08edf9a4b38c233a915c16a60350b`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 2.5 MB (2548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c8821aeddabdcf3bd629c9650d4549fae2aa9f22262551eb9d5c74605d584d`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:69b4a879eb3953541af941acdc2f299645c4c779efc2299159c64656488363ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83793331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8143c3496203c071fcd13ab0845e3e1795ac143dbd5baafbcb9dc534c7e4c37d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45845df8f6f470d7a059a7929530fe5fe9f9c235b398cc7ca33942bb8a61880`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 11.6 MB (11619729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafdc7b73c599d0ee3cfa9f4b5a540c2c1046536633de446f2f2e502766b47d`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d93e02f376a36b740dc38b1fb2ca43d3bafe3c8a22b5bba0a6716f796bdab2`  
		Last Modified: Fri, 27 Sep 2024 16:27:29 GMT  
		Size: 31.0 MB (30964743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cf82729737584fce4d757d120d529716884b0ae6a2dbd129a68340ca54678`  
		Last Modified: Fri, 27 Sep 2024 16:27:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01eda4eff6d554f82625e41ccd42a612fb85de89c66bc09663a5182b90f3ab`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 14.3 MB (14319150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c21ab13aabdff7f6b0f6a2928f7b6a685c7e9c0e1d7370a5827d06b67bfc6`  
		Last Modified: Fri, 27 Sep 2024 18:10:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4775d3c85d65939db8d0934b011021f7a3b945410abe45ec07add5f0f35250`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c766cd22eb374c4befe448e8f88f5d5a8e76404d815261fa5d5e67dc1a2d59`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d1619558841c6de5a18b1cab8d03e570e9ad07ca80be585a4e2354e1e097389b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1811aa80a45d741fedfc9551aa68a1ffccf01140613c650c2dfe8457b39699e0`

```dockerfile
```

-	Layers:
	-	`sha256:e47d2719ebb9f3fbc73cb53ed5e371ab04b3c13fcea89621627628212f342d44`  
		Last Modified: Fri, 27 Sep 2024 18:10:37 GMT  
		Size: 2.6 MB (2551866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98544094124c3d6d5c2ad67eaa9aee9fa367812a150f419fc7af3fe24827a32c`  
		Last Modified: Fri, 27 Sep 2024 18:10:36 GMT  
		Size: 21.2 KB (21178 bytes)  
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
$ docker pull fluentd@sha256:e13fbc2ad25ee980ac73e6b37fad57c64a41fbe28b3f210b8fd54bdc9e50a6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88502808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f887eb123c22da239cae7ffd9cd69194e9f5cae2aead7d51cbe69f05c563c24`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2311d534ce56c21a7a499479c7f9c79e8c270bf304eb0ab12142c09122d27577`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 13.4 MB (13416835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7aec7f52e4f19ff57ca320ed34686668513ad4554f001047df6dfee2fadfe4`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e5e4e419fe1e66bc38ce38c7bbdc395aa7002d4c7c658ea4eb0bdd4a40f607`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 30.8 MB (30809165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f0214ae49c0dcde1cd4cd4a105d68aae76b3be6bf15222d2275a52b5ae1787`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeae5c03e504e9bcdaae0a322d87d1dacc1a99bba3f2fd1419915a2bd0efb70`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 14.1 MB (14130190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b78976e65bdb6307a1fafe82be99e8d37b0f563da523177ffb5cdb01cb0f6e`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719fd1c2f805e501175de95cc3b926ebf3d065888290d5eb661c5cfacd9cd70`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5be5fb7bd5e5902febb2d863d55ac93beb6e10ea2fd8b7525010d86aa932f4b`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e58491b279da6fb1e60c9fc4ab0ca3e483c31f0dd7ebb1dbc5f3adb976a615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2566654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d541e9f47f608aa99f70adb10ad1bfce9d519c95e9245de1f7d277d987e59c7`

```dockerfile
```

-	Layers:
	-	`sha256:b44213b03c423b8add4d944e596cf8b34d9a42eb0c16ba5dc35e2e5206a5c17b`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 2.5 MB (2545604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d5cc48ff7971ba7789d92a010071c9f37e6f817419330c23bfab862250e6ed`  
		Last Modified: Fri, 27 Sep 2024 10:04:54 GMT  
		Size: 21.1 KB (21050 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ddab9d7a1a1dce178234b1005ef85b412951516af28ff077d0b4f4a2a4694608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94787093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4013e63af1dd7c1c85c956b453ff38b8c0536986232fed89135591aab3086871`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944decc6c885a3cfb18414f7007b22fc8a4b77f4b16c9d881f26c07c4a59167`  
		Last Modified: Sat, 28 Sep 2024 00:51:13 GMT  
		Size: 14.6 MB (14590506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69529784e0f3b0b65d2ec424cdcd4b6997929a1e9900af7d5be09782809f4888`  
		Last Modified: Sat, 28 Sep 2024 00:51:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab681378a03a161e604840dbbfb18199db4422ff0623e5af4b1df3f098613ba`  
		Last Modified: Sat, 28 Sep 2024 01:03:58 GMT  
		Size: 32.3 MB (32337939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c711126121e4549d63a054288a85638b37fce915537843b43daf3854b401c`  
		Last Modified: Sat, 28 Sep 2024 01:03:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d362b85020f4b13957131ed62e93770f304b8b235ec2ce14fa76d1953aa66b`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 14.7 MB (14734083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684878939979fe59f6190c039e61653d557d6afb17f850db5bdc55d03bd7f1e2`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb5e41bcc064bd139c4cc97e0542a3d4b7b5b10a830bce390c271e765f6818f`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47974dfbb883e661c2a906668c0bf1ed73f640247d58bbf0b877371f2b84e360`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:efa5f1c25ae6511a23cda33d24febe4110361d784998223790501323cc7de1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72771adf42675987c0d8a34bfd0c58be662b40f84efab24916a67ee5af0e5180`

```dockerfile
```

-	Layers:
	-	`sha256:f0603cea9e1c341a21140c6a7d9d7679bc2315a83b6641c6ee1af4dcccacc37c`  
		Last Modified: Sat, 28 Sep 2024 05:21:18 GMT  
		Size: 2.6 MB (2552828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9691c7e3cd6e2025f1fb0909af5f4f5990d147e86886a7f157dc4f00a523404`  
		Last Modified: Sat, 28 Sep 2024 05:21:17 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.6-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:f6a09cc8b93da48caa67b47e0bb225b2407e5a0ad2a1022208eb5341b8e7adc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85614292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a143e6c09a1d17f1aaf40a15e81eafae4b932cbc80fe15b25a657765301f8463`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4964b44d90bb8a258c7d0da09e47f2bc08c5a6a6e0f8a115ee932af6c1846`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 12.0 MB (12040811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9c9b4664bd84b47f7aeb29e34ee545ddc3509c2693234ac7d0748eec301d2`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124c8bc976af5cce1e69a2598f76b68dbb9fc2037142bf553908ff2ee4e4cb8`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 31.6 MB (31610348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d0923518b1d48669040a368d05d833b81740bb9dec6257e085fc79e35cb43e`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff64543b84f526b7e5bb2b22c6d0aca2e252f09966d131aaaf06b4143ba0b8`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 14.5 MB (14470711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4873e299f9161accbf5a05dced7cf435cf0b62f0b15a67aae021ae9af2b712`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e335a11e7850106cab49aaa0933550296a522a4ac7132b93065b9c9b9bf2d`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787f2a7b6277f438834c1f006d5562249a94f5c29577e41f26ff44cd3c9e3460`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.6-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f91210c0698d6ad98c6268b057e345c448afafeee61e3c6613c9288ece250b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39413d15ce89341a2370d7548ac547fce88af508055285501c7ece40c1858193`

```dockerfile
```

-	Layers:
	-	`sha256:82cc5efa302cca458cd638e607b8b26fea0cd309e492b5fdad5a8fe4f8791d15`  
		Last Modified: Fri, 27 Sep 2024 18:21:05 GMT  
		Size: 2.5 MB (2548300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adff21f06d4ce32a1e1ea09cad42249c1290ab25b87c77c236913f4c4cbbdfb`  
		Last Modified: Fri, 27 Sep 2024 18:21:04 GMT  
		Size: 21.1 KB (21105 bytes)  
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
$ docker pull fluentd@sha256:72d08808420f042f1d1d801c1aabef5ff940fd10802e9929396cc461fd83aae8
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
$ docker pull fluentd@sha256:030d1763e406f8c246d86bd0f6e1e6edb9d701ec06cee43751967095555a5ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91688769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7afbe903c6762ef5d9d111b245b9ef5beeae4b9f028f3b9578dfe5bbac79ee0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac603e3acde9c2e5596ee3ef27767ad3ca9fc39159f9c321addd1eb919a33e51`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 13.9 MB (13862276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293e8c1ee175c3a3a89c4e2a16aa1656adfdeb820f527a6395c34a7ae2f770c`  
		Last Modified: Fri, 27 Sep 2024 06:17:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2631bf1c371b778cc33ce5a5c6b81e65b44093ee038fdcb0b5c815d4f094dbcf`  
		Last Modified: Fri, 27 Sep 2024 06:18:03 GMT  
		Size: 34.9 MB (34903601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1a4a91a396fef1d11f17a3eaa83e97c971cf7ea9cca046957a6e3a9228ede`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b81050ce6b4eac41127f3a87f644b2692879aa507a25332a2fe6827942d742`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 13.8 MB (13794221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed2a924792bb4cdfc86c919dcc9439e795948303f49b18d8c64556e96211c04`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210c1708abbfa5919ea873fdc9955ab86ea6d0673baede087020bbbc07b2968`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02170efd289f80bd99e91d50ed5263528edea4b8de58477c5e9bb125f232eb5f`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1230e04970696bc48022d57a3861696fdecd764f485822c2112b612e72bef07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b9a62b3bfc2f0529197e4e872ed4acb1e42f660d3b4069cd434c2d9d4b0dcf`

```dockerfile
```

-	Layers:
	-	`sha256:c0c0b03308514a248339cb30693fa7f501efa2440a645e776b7e9e883632facf`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 2.6 MB (2551286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d92e7bac3f9926bbf8c290f5e6158d33b4879f71ae32531bc320eec953c94d5`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 21.1 KB (21074 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:494b7a4e3225a537d4e1fe5a86dd51e1dd3a8f33761488713bde50a3fbed49df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83249987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517233f1acc3d9ad0af4672975a66557581136f62c31635f20bb7aad39e1d36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45845df8f6f470d7a059a7929530fe5fe9f9c235b398cc7ca33942bb8a61880`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 11.6 MB (11619729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafdc7b73c599d0ee3cfa9f4b5a540c2c1046536633de446f2f2e502766b47d`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d93e02f376a36b740dc38b1fb2ca43d3bafe3c8a22b5bba0a6716f796bdab2`  
		Last Modified: Fri, 27 Sep 2024 16:27:29 GMT  
		Size: 31.0 MB (30964743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cf82729737584fce4d757d120d529716884b0ae6a2dbd129a68340ca54678`  
		Last Modified: Fri, 27 Sep 2024 16:27:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd46904e7f9af04c0e6f82777db921ffe4230c0a0cf8c5a3edbc5e06002b25c1`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 13.8 MB (13775814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3832e61b3061723dc63ae22f992cd795adb6a89e64194889080ba1e4acdf975`  
		Last Modified: Fri, 27 Sep 2024 18:14:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bf84ee9c0ef7f411bda4f437ea9565471bc4a38d2140f867b369069d28ce26`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021e6137eaffec33e1813e4a08bbb8df98e663c3fddee70025c19bba990d6ee8`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6aaa0930d020499a3501091d11a251706ab488a403c9dfab431d35a99b50261c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c1929b9b7a7afe0a6a8b7c7dc3d91d985f7d558e327d84c8e67574f358f5a6`

```dockerfile
```

-	Layers:
	-	`sha256:3bf507215882800f294358d4206d419fd9cfab644bb47117cf67ac2f28547eea`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 2.6 MB (2554671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3da92d09e8dbbe81a8ba0add13223021451f146f51bcdd3178b276f68e92bc`  
		Last Modified: Fri, 27 Sep 2024 18:14:15 GMT  
		Size: 21.2 KB (21178 bytes)  
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
$ docker pull fluentd@sha256:43925960bb3be81e213cc085758b2413714ef74107ee3861b2efeb0ea9ed3f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87960168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab6b775955d21ea19f94ba05bf930d3281de815e52832fbb10fcad1269ea183`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2311d534ce56c21a7a499479c7f9c79e8c270bf304eb0ab12142c09122d27577`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 13.4 MB (13416835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7aec7f52e4f19ff57ca320ed34686668513ad4554f001047df6dfee2fadfe4`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e5e4e419fe1e66bc38ce38c7bbdc395aa7002d4c7c658ea4eb0bdd4a40f607`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 30.8 MB (30809165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f0214ae49c0dcde1cd4cd4a105d68aae76b3be6bf15222d2275a52b5ae1787`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5838d2a7bd6572955ff6fed347894eb7944e95bd5d7c8f4299ff132ee8e564`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 13.6 MB (13587552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87008a61c354c8b95acea64568255984a441eea14b870a4bfb63c71cdf75ed`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ea18bf93aec0e3ae9d74ee1229f736726196b7336f017abb24e3b482a8e0e7`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b29c896f2710458ecb228fd0c49ce37cd62e43f33809eb593d256c31ec96c6d`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ba4abf24d0240aa2d363ec894935c4791de2adf0a73066df3684d8c2a0bd0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62b039da3be8e9e1122bca0c92f5dcaeb537c969746eeb8268bb08b9362b64`

```dockerfile
```

-	Layers:
	-	`sha256:931cb2681d0f20e8a105194bffb06bfd772bc0ad2915e65af9d32626da0c1b75`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 2.5 MB (2548409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c981bb082f129788559103ad17a80a0d88fc350f60791e79c075ccd3e4e617ed`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 21.1 KB (21051 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:b0877ba732d2242bbeedb0f7c1015948bad4849d51cd515a39ad142343cea41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94250082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ce3a136c56cee5b2aba56ff4b506448a4fe9e941ab6afb4d0c773ea8be222`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944decc6c885a3cfb18414f7007b22fc8a4b77f4b16c9d881f26c07c4a59167`  
		Last Modified: Sat, 28 Sep 2024 00:51:13 GMT  
		Size: 14.6 MB (14590506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69529784e0f3b0b65d2ec424cdcd4b6997929a1e9900af7d5be09782809f4888`  
		Last Modified: Sat, 28 Sep 2024 00:51:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab681378a03a161e604840dbbfb18199db4422ff0623e5af4b1df3f098613ba`  
		Last Modified: Sat, 28 Sep 2024 01:03:58 GMT  
		Size: 32.3 MB (32337939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c711126121e4549d63a054288a85638b37fce915537843b43daf3854b401c`  
		Last Modified: Sat, 28 Sep 2024 01:03:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e978f0617885a2c1f81769b589c63006e07997ba8c8064e5b693f39983258d8`  
		Last Modified: Sat, 28 Sep 2024 05:25:52 GMT  
		Size: 14.2 MB (14197078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc81e3b7a8f449ae6bc217226e8d31740fc8b6189fd7cea3091ccd6d2452753`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa5162d594f3a926472635640c127ee8b0bf7cde18cb3d8190c99d47990c82`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089067c55c93f2dc1dae2100374fb99f9b2d195c8947277daf9e7dd82e5c4f5`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:780ba1a5471b3e86a3663800456e76f1a4d69e595c810117bf56cfa875b2fe73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2576772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d48841db50113b4d54e03d6f40007873a61e6280c85b5c7f0a4b8907faf518d`

```dockerfile
```

-	Layers:
	-	`sha256:b2998ccc36a23cc45b40c0f79eb306b6f51e7af1a85411bf0c5a3f5c8b67be7c`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 2.6 MB (2555633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928f830d1d8479b3107a4fb5124011ee7bd446d3721e2942be78be3ecba4d19c`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:e53809c832c73ad4f94456ffff8940b85aff7f94fa2224feb01aa08c12a15854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85073002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c425017d926da68bbe9d3802379c4c02b5af9c14f149bf884e1f047da8405f7a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4964b44d90bb8a258c7d0da09e47f2bc08c5a6a6e0f8a115ee932af6c1846`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 12.0 MB (12040811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9c9b4664bd84b47f7aeb29e34ee545ddc3509c2693234ac7d0748eec301d2`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124c8bc976af5cce1e69a2598f76b68dbb9fc2037142bf553908ff2ee4e4cb8`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 31.6 MB (31610348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d0923518b1d48669040a368d05d833b81740bb9dec6257e085fc79e35cb43e`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781438db1ac41ab8c83597663d9a78d2a6cc188a60a8b0ea598a400c775faced`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 13.9 MB (13929419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0adf3aaea967c172b546b4218f9dc5e121a37f4bc25f95a80d794edaaa7e959`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6171f4192e8d9a6279557856f55efce1e0c74f583c169cce585b44a64f482c`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cd1e7b92a3ad5ee0564354f0e8183ac043ca265a2d6e0eb83fa0965d43e02d`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2fa72be0a4893dbf3302ba2614eed263a0bebfc43bc5935888d26ed9c4894933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e91a8604e0e5dceba34b80faf23a60ed26bc1d1252af8c5bbbd4a4086be046`

```dockerfile
```

-	Layers:
	-	`sha256:94ae1e029ff1fa3aef766937cf62741b57f5d9c5e5722235eff5bfbb64107802`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 2.6 MB (2551105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6135eb1668e858240cb42d0cf6cfab605c47ef8136a6853fbafc61cf7c83a864`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 21.1 KB (21104 bytes)  
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
$ docker pull fluentd@sha256:72d08808420f042f1d1d801c1aabef5ff940fd10802e9929396cc461fd83aae8
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
$ docker pull fluentd@sha256:030d1763e406f8c246d86bd0f6e1e6edb9d701ec06cee43751967095555a5ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91688769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7afbe903c6762ef5d9d111b245b9ef5beeae4b9f028f3b9578dfe5bbac79ee0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac603e3acde9c2e5596ee3ef27767ad3ca9fc39159f9c321addd1eb919a33e51`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 13.9 MB (13862276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293e8c1ee175c3a3a89c4e2a16aa1656adfdeb820f527a6395c34a7ae2f770c`  
		Last Modified: Fri, 27 Sep 2024 06:17:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2631bf1c371b778cc33ce5a5c6b81e65b44093ee038fdcb0b5c815d4f094dbcf`  
		Last Modified: Fri, 27 Sep 2024 06:18:03 GMT  
		Size: 34.9 MB (34903601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1a4a91a396fef1d11f17a3eaa83e97c971cf7ea9cca046957a6e3a9228ede`  
		Last Modified: Fri, 27 Sep 2024 06:18:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b81050ce6b4eac41127f3a87f644b2692879aa507a25332a2fe6827942d742`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 13.8 MB (13794221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed2a924792bb4cdfc86c919dcc9439e795948303f49b18d8c64556e96211c04`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210c1708abbfa5919ea873fdc9955ab86ea6d0673baede087020bbbc07b2968`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02170efd289f80bd99e91d50ed5263528edea4b8de58477c5e9bb125f232eb5f`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1230e04970696bc48022d57a3861696fdecd764f485822c2112b612e72bef07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b9a62b3bfc2f0529197e4e872ed4acb1e42f660d3b4069cd434c2d9d4b0dcf`

```dockerfile
```

-	Layers:
	-	`sha256:c0c0b03308514a248339cb30693fa7f501efa2440a645e776b7e9e883632facf`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 2.6 MB (2551286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d92e7bac3f9926bbf8c290f5e6158d33b4879f71ae32531bc320eec953c94d5`  
		Last Modified: Fri, 27 Sep 2024 07:06:42 GMT  
		Size: 21.1 KB (21074 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:494b7a4e3225a537d4e1fe5a86dd51e1dd3a8f33761488713bde50a3fbed49df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83249987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517233f1acc3d9ad0af4672975a66557581136f62c31635f20bb7aad39e1d36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45845df8f6f470d7a059a7929530fe5fe9f9c235b398cc7ca33942bb8a61880`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 11.6 MB (11619729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafdc7b73c599d0ee3cfa9f4b5a540c2c1046536633de446f2f2e502766b47d`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d93e02f376a36b740dc38b1fb2ca43d3bafe3c8a22b5bba0a6716f796bdab2`  
		Last Modified: Fri, 27 Sep 2024 16:27:29 GMT  
		Size: 31.0 MB (30964743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cf82729737584fce4d757d120d529716884b0ae6a2dbd129a68340ca54678`  
		Last Modified: Fri, 27 Sep 2024 16:27:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd46904e7f9af04c0e6f82777db921ffe4230c0a0cf8c5a3edbc5e06002b25c1`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 13.8 MB (13775814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3832e61b3061723dc63ae22f992cd795adb6a89e64194889080ba1e4acdf975`  
		Last Modified: Fri, 27 Sep 2024 18:14:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bf84ee9c0ef7f411bda4f437ea9565471bc4a38d2140f867b369069d28ce26`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021e6137eaffec33e1813e4a08bbb8df98e663c3fddee70025c19bba990d6ee8`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6aaa0930d020499a3501091d11a251706ab488a403c9dfab431d35a99b50261c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c1929b9b7a7afe0a6a8b7c7dc3d91d985f7d558e327d84c8e67574f358f5a6`

```dockerfile
```

-	Layers:
	-	`sha256:3bf507215882800f294358d4206d419fd9cfab644bb47117cf67ac2f28547eea`  
		Last Modified: Fri, 27 Sep 2024 18:14:16 GMT  
		Size: 2.6 MB (2554671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3da92d09e8dbbe81a8ba0add13223021451f146f51bcdd3178b276f68e92bc`  
		Last Modified: Fri, 27 Sep 2024 18:14:15 GMT  
		Size: 21.2 KB (21178 bytes)  
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
$ docker pull fluentd@sha256:43925960bb3be81e213cc085758b2413714ef74107ee3861b2efeb0ea9ed3f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87960168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab6b775955d21ea19f94ba05bf930d3281de815e52832fbb10fcad1269ea183`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2311d534ce56c21a7a499479c7f9c79e8c270bf304eb0ab12142c09122d27577`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 13.4 MB (13416835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7aec7f52e4f19ff57ca320ed34686668513ad4554f001047df6dfee2fadfe4`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e5e4e419fe1e66bc38ce38c7bbdc395aa7002d4c7c658ea4eb0bdd4a40f607`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 30.8 MB (30809165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f0214ae49c0dcde1cd4cd4a105d68aae76b3be6bf15222d2275a52b5ae1787`  
		Last Modified: Fri, 27 Sep 2024 09:15:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5838d2a7bd6572955ff6fed347894eb7944e95bd5d7c8f4299ff132ee8e564`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 13.6 MB (13587552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87008a61c354c8b95acea64568255984a441eea14b870a4bfb63c71cdf75ed`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ea18bf93aec0e3ae9d74ee1229f736726196b7336f017abb24e3b482a8e0e7`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b29c896f2710458ecb228fd0c49ce37cd62e43f33809eb593d256c31ec96c6d`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0ba4abf24d0240aa2d363ec894935c4791de2adf0a73066df3684d8c2a0bd0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2569460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62b039da3be8e9e1122bca0c92f5dcaeb537c969746eeb8268bb08b9362b64`

```dockerfile
```

-	Layers:
	-	`sha256:931cb2681d0f20e8a105194bffb06bfd772bc0ad2915e65af9d32626da0c1b75`  
		Last Modified: Fri, 27 Sep 2024 10:05:05 GMT  
		Size: 2.5 MB (2548409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c981bb082f129788559103ad17a80a0d88fc350f60791e79c075ccd3e4e617ed`  
		Last Modified: Fri, 27 Sep 2024 10:05:04 GMT  
		Size: 21.1 KB (21051 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:b0877ba732d2242bbeedb0f7c1015948bad4849d51cd515a39ad142343cea41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94250082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ce3a136c56cee5b2aba56ff4b506448a4fe9e941ab6afb4d0c773ea8be222`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944decc6c885a3cfb18414f7007b22fc8a4b77f4b16c9d881f26c07c4a59167`  
		Last Modified: Sat, 28 Sep 2024 00:51:13 GMT  
		Size: 14.6 MB (14590506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69529784e0f3b0b65d2ec424cdcd4b6997929a1e9900af7d5be09782809f4888`  
		Last Modified: Sat, 28 Sep 2024 00:51:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab681378a03a161e604840dbbfb18199db4422ff0623e5af4b1df3f098613ba`  
		Last Modified: Sat, 28 Sep 2024 01:03:58 GMT  
		Size: 32.3 MB (32337939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2c711126121e4549d63a054288a85638b37fce915537843b43daf3854b401c`  
		Last Modified: Sat, 28 Sep 2024 01:03:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e978f0617885a2c1f81769b589c63006e07997ba8c8064e5b693f39983258d8`  
		Last Modified: Sat, 28 Sep 2024 05:25:52 GMT  
		Size: 14.2 MB (14197078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc81e3b7a8f449ae6bc217226e8d31740fc8b6189fd7cea3091ccd6d2452753`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa5162d594f3a926472635640c127ee8b0bf7cde18cb3d8190c99d47990c82`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089067c55c93f2dc1dae2100374fb99f9b2d195c8947277daf9e7dd82e5c4f5`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:780ba1a5471b3e86a3663800456e76f1a4d69e595c810117bf56cfa875b2fe73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2576772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d48841db50113b4d54e03d6f40007873a61e6280c85b5c7f0a4b8907faf518d`

```dockerfile
```

-	Layers:
	-	`sha256:b2998ccc36a23cc45b40c0f79eb306b6f51e7af1a85411bf0c5a3f5c8b67be7c`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 2.6 MB (2555633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928f830d1d8479b3107a4fb5124011ee7bd446d3721e2942be78be3ecba4d19c`  
		Last Modified: Sat, 28 Sep 2024 05:25:51 GMT  
		Size: 21.1 KB (21139 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.17.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:e53809c832c73ad4f94456ffff8940b85aff7f94fa2224feb01aa08c12a15854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85073002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c425017d926da68bbe9d3802379c4c02b5af9c14f149bf884e1f047da8405f7a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 26 Jul 2024 16:23:41 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4964b44d90bb8a258c7d0da09e47f2bc08c5a6a6e0f8a115ee932af6c1846`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 12.0 MB (12040811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9c9b4664bd84b47f7aeb29e34ee545ddc3509c2693234ac7d0748eec301d2`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124c8bc976af5cce1e69a2598f76b68dbb9fc2037142bf553908ff2ee4e4cb8`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 31.6 MB (31610348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d0923518b1d48669040a368d05d833b81740bb9dec6257e085fc79e35cb43e`  
		Last Modified: Fri, 27 Sep 2024 17:33:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781438db1ac41ab8c83597663d9a78d2a6cc188a60a8b0ea598a400c775faced`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 13.9 MB (13929419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0adf3aaea967c172b546b4218f9dc5e121a37f4bc25f95a80d794edaaa7e959`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6171f4192e8d9a6279557856f55efce1e0c74f583c169cce585b44a64f482c`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cd1e7b92a3ad5ee0564354f0e8183ac043ca265a2d6e0eb83fa0965d43e02d`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.17.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2fa72be0a4893dbf3302ba2614eed263a0bebfc43bc5935888d26ed9c4894933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e91a8604e0e5dceba34b80faf23a60ed26bc1d1252af8c5bbbd4a4086be046`

```dockerfile
```

-	Layers:
	-	`sha256:94ae1e029ff1fa3aef766937cf62741b57f5d9c5e5722235eff5bfbb64107802`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 2.6 MB (2551105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6135eb1668e858240cb42d0cf6cfab605c47ef8136a6853fbafc61cf7c83a864`  
		Last Modified: Fri, 27 Sep 2024 18:23:59 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json
