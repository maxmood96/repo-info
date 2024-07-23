## `fluentd:latest`

```console
$ docker pull fluentd@sha256:7176e039844f8340068724ff2356ede171643a989d94139baac0dd8fb9b85846
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
$ docker pull fluentd@sha256:dcb1ccc0866dd5e7af111c32e00b8fc5f54ffd34669811f7f9c2bd311b258715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25143434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5538cac257c740096d04f6592fb2175271c620ab05027a38d81daae3053994`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a3461f6adfa6064f1adb962e6d5719e4a2b74ced1344cf3675348a3b60981`  
		Last Modified: Mon, 22 Jul 2024 23:08:16 GMT  
		Size: 21.7 MB (21749287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de83259d6f0c718e1221511b87004dabdbfdedc59855e328e7974e0f77cdce9`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8909dce1b0f370d9a6acc53231f05348048b8d82a5d6dfb373382d2da179f9c5`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a5567e0ce6a6a44ed033dd7f707279296b7abf8246f9c2c4ceb142457d44`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:e3a22c83c5be945bfadac065de63192efe294714f241ee0fb89c868194f07317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **931.3 KB (931277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c1173c6fc4951ff3ca6b8012c4c8f3ff2bdffcb2d5b4eff9c125f76cdb5cd5`

```dockerfile
```

-	Layers:
	-	`sha256:d6f7295b2777b74726220adb446255affd4fe17e45ff359c08732c5798dad5eb`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 917.5 KB (917462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ac286772f01a44cf36697920a0f2e6012cddb49b4fb45ed5b33170edc5a040`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:3ff859e6977284729f111e2a7f43a58bbd84f3a8e42afa857a85769cff9c96c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23819435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d4c8cb26041864d8c47a7fbb53972f18c025002f059cbe071f4f6478a0d7f1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:3e38b93a27dbde320d7c2878b42367f4d6e05d5c98ed33e8cc6560695658fe60 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:40c65822f1dcb1824485b1caa8304dbaf79b9173eab1a2f5b4624015b240e1e5`  
		Last Modified: Thu, 20 Jun 2024 17:50:06 GMT  
		Size: 3.1 MB (3123326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc34fd347f60c1676bbc6efc2be23ff19ff585820d35649f1244766cfe82280`  
		Last Modified: Fri, 21 Jun 2024 05:21:54 GMT  
		Size: 20.7 MB (20693941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80945faf163b04cfb5b0cc0fb73382bf409dc1b4cd8521038e73ba3a62ee3769`  
		Last Modified: Fri, 21 Jun 2024 05:21:53 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d61a794d3c6d8e4f6e3c74bc4c38e39ea7f2d03c33d8c77ac7f65acbf0b0fc3`  
		Last Modified: Fri, 21 Jun 2024 05:21:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba0e5ab2bb06d2b6934f3d668a671e6efa0b13933b2859cd983ce5d12216e`  
		Last Modified: Fri, 21 Jun 2024 05:21:54 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:eda6d0e363ae0e336fdc1035621aad1cff1545434d5fbe60d9acb7db0cfa3180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d612d3e33765da03cd16faf180d14de7aaa7d9a92b2accaea611d0f5c806d26`

```dockerfile
```

-	Layers:
	-	`sha256:c4953716dab3e2098d0dbf35c8fd726ec6db8770787dc82cf42b57e3d2315f59`  
		Last Modified: Fri, 21 Jun 2024 05:21:53 GMT  
		Size: 13.7 KB (13671 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:70480f05afb8097bda048403b6b366417f0666fdeaeb6de260526ab91c59de61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24611914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f77afda1a61231d485931674a4f31611743be7446c6edca70ebf99a0a4e7172`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21005e8bb4992960342580d056a7becf9ca706ba12e6efe6425bfe9567cd9ddb`  
		Last Modified: Fri, 21 Jun 2024 07:04:05 GMT  
		Size: 21.3 MB (21337155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8e46ea0c9dc9fc1f47d4d16bb22c2c47493be9398509bc7ba1efed6e29b289`  
		Last Modified: Fri, 21 Jun 2024 07:04:04 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d47b2f90e10b17417c7ad1d1219fdca06016464041bbf491f60f1a3891e778b`  
		Last Modified: Fri, 21 Jun 2024 07:04:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4ab8b4a316bbf7ff70bfb4a91ea6eb446a70f318925b948b4dbbd0c174dbbc`  
		Last Modified: Fri, 21 Jun 2024 07:04:04 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:44040963a8c5ac327fb878a1c0d14e5c9e23d82a3dc7e021b30ffdb7d654a0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **912.4 KB (912429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429033a2c2341d0c49cad227484b17177f2a35b6207fd1e0e1cb0b7c7e7abad9`

```dockerfile
```

-	Layers:
	-	`sha256:e2d5fbd653f2e62f1c9b79db04e11ac1de61f20116c6ba1372f98b0c5c0898d2`  
		Last Modified: Fri, 21 Jun 2024 07:04:04 GMT  
		Size: 898.3 KB (898326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a83a055bf59a1ec272a10212448177adea85b56fc2a38af6e9545227c6ad42`  
		Last Modified: Fri, 21 Jun 2024 07:04:04 GMT  
		Size: 14.1 KB (14103 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:0b7728994241bf01d17ccddadb0bad352bf32a0d377cec648649a20320931471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24405917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409fcc64772a27d939b3c4b929b5cf0efa4f8ae298b1c03e4754589a5b59f143`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:98651bffed57a34c4c4de527ea06f09258bc6b9c3fe3d50b1db311c1deca1435 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f51faebf7e0e923e97e24fee855c0662aa8549334180fc1acd4e7be320323c72`  
		Last Modified: Mon, 22 Jul 2024 21:39:23 GMT  
		Size: 3.4 MB (3426046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3bfd13d42920ec20134e3a409f78cb7f29194d68d9d4e5683b141ba703f91a`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 21.0 MB (20977703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82785355eef72faae6c336906631f8e43396bf2677b01adbf9ddcc9e7b3b9c91`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369d6084aab5d81329a1c45c05fab11aa496033bd5a5f308c4828907d5ebc866`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559261397f509be36809a70e580793b5d8fbdbd26204a8f059a3cd3880ebeb`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7f73078dfa9dc8eaa777b370b8d16bb9fc475b0f2c65c1d63cd203e86b6e53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **931.0 KB (931037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d2148e8956642fb803ec532f20a4db55a4aecd6008d1ef6dd004890cf72ee9`

```dockerfile
```

-	Layers:
	-	`sha256:2734d34b0c868f77dd78f07078c1641557a1beb699d2e87d91eec7de6f6d6731`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 917.2 KB (917248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5ad0a16ad1e8020b4f9822c385e40907b405d1dd2d8fff7664b466932c108e`  
		Last Modified: Mon, 22 Jul 2024 22:12:37 GMT  
		Size: 13.8 KB (13789 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:45349e5872c622b4fd19135ab522f7848ae3fb3413b34764d769f96e7b8df71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24990584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b349552b317c9e8c33b0e9662d0e7783070ce2a102e6019a1c554d5111c3e252`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83490f1f4fd472e367e9d0f5b8197bb03458a6ae455038e200248d9eb8e8cd9c`  
		Last Modified: Fri, 21 Jun 2024 03:19:35 GMT  
		Size: 21.6 MB (21586604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e027842e9dfca65b237184bbaff7e6c502e22c4e42219366f23b8b2dbc93c15b`  
		Last Modified: Fri, 21 Jun 2024 03:19:34 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f7eb7c0cb2daf45600a1eeae5953c2538208ba6e7bc90d9e0b3acce6270fd`  
		Last Modified: Fri, 21 Jun 2024 03:19:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7929982e87d166e1a62f209edb21a11dfcadbdfa9e9e2dfc58273f536030488`  
		Last Modified: Fri, 21 Jun 2024 03:19:34 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:d8a0a12c689a612b29e3f3a54287c0ee8197002eca07dd4126e4a804fbe9816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.6 KB (910593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c210219b4e965d6c594160e11d256dc5931aff5e89e73ce33e9dddd8aa9f1e`

```dockerfile
```

-	Layers:
	-	`sha256:f7b74068d3fe7ec66c643a7c9a3a0802332919594b7cfb7557fc46ebde6fdb0c`  
		Last Modified: Fri, 21 Jun 2024 03:19:34 GMT  
		Size: 896.7 KB (896744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7107fca2a9c87b8c016403f64c1432f840c3dd52f490762b2c27999a3a24c6b3`  
		Last Modified: Fri, 21 Jun 2024 03:19:34 GMT  
		Size: 13.8 KB (13849 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:5a5806d4ac882c227f0ad5bd1364b8c6ec64175a185c795d13eef2ef192790a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24364627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acab8e1f5aab6ad028c32f1629f6af70aaedf42daba1ffb1b68cb816be59ccab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a9c4d6f5823b30643d4636be2b440b50deb92a2d19765e0428420a1309bfb0d1 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bc4c034c86cf8d5ea77b49537505f7600ac0422e88fc3d77b3ba3b3f0c9dc564`  
		Last Modified: Thu, 20 Jun 2024 17:43:33 GMT  
		Size: 3.2 MB (3183597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba89a7861f727ac059f7fde03212ae1652f8be9d02be00db6b34098f0d6512a`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 21.2 MB (21178861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b924f3b36febfed7a4763869c21391891ff8fcdea666e65b791d0b3e0bbe18`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92738662e31cf77b2844dc0f81409e747662884245ec1238a5ab048cb86f5410`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb8f9abe80ccf90cf9e75bc9cfd6f8f104565f33d790e69412899b67b414b29`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:2c2f4e05dc175d05189af7b3751bae21fab472ab5249d86652d41df20c7a6e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.9 KB (909949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687ff810a1849d027ab4221d408dd13b8d32a9935682fc4a83ad34c2ed24f84`

```dockerfile
```

-	Layers:
	-	`sha256:fe61bf1a815a3241a9670f9b06c8395b93f1bb47a61cdb1ff07509b22de95903`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 896.1 KB (896134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faff62cd469d35d11a8476d3b27cab41719fd5aad87b18083b5fd5a14e570d15`  
		Last Modified: Fri, 21 Jun 2024 06:08:06 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json
