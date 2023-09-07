<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.0-1.0`](#fluentdv1160-10)
-	[`fluentd:v1.16.0-debian-1.0`](#fluentdv1160-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:3b5e8bb493f277c0e04a5ff6f48a4a72fd13083a6ff09ac98527bec1c2f9d73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:56c9a79408eb21afe816f7f596cd14c3414bbc1ab216a554194d58ade0318aad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25150972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd0325e67fca65a5c1b19f78bd50b1111fa5725360ebac717b5df77354ef856`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:09:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:09:24 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:09:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:09:24 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:09:25 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:09:25 GMT
USER fluent
# Wed, 09 Aug 2023 10:09:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:09:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e3f26392ec29ada78eeb1c98c2df3f8422b5a581376a4093d8c80c36869b40`  
		Last Modified: Wed, 09 Aug 2023 10:09:41 GMT  
		Size: 21.8 MB (21770144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f2007908d1df8b7db8a7456ff60be7e7b78d2d8f4a8186aaf6ff7d8a2a8fd7`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c1ad76bab10bdb4aef989acd8a09c31f24ebf092418e7c95662a42e7b6c7d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87c4c99fc1a28b6b71ed4b5656764fd53617c4af8a1e7ccc54d90541648b62d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1f96095b93b01bf118f591bf8ddc437903590d141135fe4e8a8170c0fffe6673
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23826878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b69c435230370d631790a81bff0db94ef91908e5d79620ffa8f58cadfcdc1ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 22:15:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 22:15:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 22:15:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 22:15:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 22:15:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 22:15:03 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 22:15:03 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 22:15:03 GMT
USER fluent
# Mon, 07 Aug 2023 22:15:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 22:15:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35333f35db5b3a8277ad49e8df6a413f1d2aa4bc9d4f8f9a1a9e50dc1af890fa`  
		Last Modified: Mon, 07 Aug 2023 22:15:24 GMT  
		Size: 20.7 MB (20712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4b45e4fbb0e0d80dc55633251556ac971c6a2fdd2f79f1790f0468185a91bf`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f979b5ae9285e493d2b6e84e5ffeac065505e69caf5be55e9baa512436393ffe`  
		Last Modified: Mon, 07 Aug 2023 22:15:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4f9800fae82280c1f3364926c31016bc00e1f7016ab23013ffd259d4d5909d`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1a25b92094ae2cf54f4eb4b6477f62f4f1fd2b98fecf9dd795c4a8a7c23140e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24613316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea821a1c95d40b6d16d8a86614d246303248850411f6a76064fdf680a644d50b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:36:52 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:36:53 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:36:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:36:53 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:36:54 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:36:54 GMT
USER fluent
# Wed, 09 Aug 2023 10:36:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:36:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573645a10251b06427cca69f6934f5778b9e2bbebb05a1e2ce062aeabbcaed6c`  
		Last Modified: Wed, 09 Aug 2023 10:37:16 GMT  
		Size: 21.4 MB (21352813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6def94d3fe0e634f307aedad1ec233f8d5935f5179aae0f45044a0605ef3e11`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7756d7c80fbe1f5d223f7a0272932c0fbf8614cb831377be38e77519709a7b`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be1c945b3a64041a8f970ab711dc39c87fc8649deb1abbafb158ddd892383e`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:39a75b2171984f895bad267615d2a0f22bc36b24f823d8208170a4d29e194ff0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3105df073c5919362ae4ae41dfc99a239bd1a686e61f981c1173e70cd9dfbfb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:25:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:25:52 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:25:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:25:52 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:25:53 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:25:53 GMT
USER fluent
# Mon, 07 Aug 2023 21:25:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:25:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e180d68a6784e287fbd112203e9d4ec2f2d74e0e2d8bc178c61bf9fb8e91ddc`  
		Last Modified: Mon, 07 Aug 2023 21:26:11 GMT  
		Size: 21.0 MB (21003778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f11c2e94ea5541f00dda08086a095742ca1a0d80afc235860d18863cdac5c`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bbf332266ca282817341b04518c3cc87cafaa20c087bc76b44e51e06c199a4`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c068f06a2e3f7536a8bbd8290592b69f4348d82c50e10d45e37dc85620017a`  
		Last Modified: Mon, 07 Aug 2023 21:26:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:e657b8a0462629b862aef1ddd616c3705eb84a12f2572477884fc650da5cdbf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24994027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16729145cd752aa811ffdbb5311976ad8ef6402dca14343d17dd93e1d7d7d15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:06:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:08:31 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:08:36 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:08:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:08:39 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:08:40 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:08:41 GMT
USER fluent
# Mon, 07 Aug 2023 21:08:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:08:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ddfce8ff2f2b7be76fc6d618deefa2282d9d9f7633d981d29d351c5e0bdaea`  
		Last Modified: Mon, 07 Aug 2023 21:09:09 GMT  
		Size: 21.6 MB (21600461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbd13befcd8b8bce1f86cc5544d64cba12edd18a285fb3e19051f8d64fc9b5`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6812f97e8a8535d190c506510893fd75a499f7dad7473591664a510174854e4d`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5366a4f8d0fc4127db1580d845e4a97721553d8b57c161afebe42bcd1fb5fba`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:89ffe3f0d5665ed8fffb7793fecde61036f8d1bdde33976bd4b8e09a19b36909
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24353859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17258134d6b5a069ab70676271ad0cb35ef9a0c6a891ddf2abe2a25ea7dd18`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 20:18:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 20:18:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 20:18:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 20:18:23 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 20:18:24 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 20:18:24 GMT
USER fluent
# Mon, 07 Aug 2023 20:18:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 20:18:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79062a3efcf019be904e5ae4b1fbbe799fefdc6fe332da1cc2200c682770a8b9`  
		Last Modified: Mon, 07 Aug 2023 20:18:53 GMT  
		Size: 21.2 MB (21175672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad859df790fc4746c6b7c74231af5a72c52bce2c893e4aa5586dcb7e7d1b9e1d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff47ba17005f172794ae4f5c7c150a4662a67c98076be03c155c1637c76e3d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c86c53fee1184d9bed9db6a1ca8bea390f1c5851e6763574eeb83a0e609221`  
		Last Modified: Mon, 07 Aug 2023 20:18:51 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:3b5e8bb493f277c0e04a5ff6f48a4a72fd13083a6ff09ac98527bec1c2f9d73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:56c9a79408eb21afe816f7f596cd14c3414bbc1ab216a554194d58ade0318aad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25150972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd0325e67fca65a5c1b19f78bd50b1111fa5725360ebac717b5df77354ef856`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:09:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:09:24 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:09:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:09:24 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:09:25 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:09:25 GMT
USER fluent
# Wed, 09 Aug 2023 10:09:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:09:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e3f26392ec29ada78eeb1c98c2df3f8422b5a581376a4093d8c80c36869b40`  
		Last Modified: Wed, 09 Aug 2023 10:09:41 GMT  
		Size: 21.8 MB (21770144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f2007908d1df8b7db8a7456ff60be7e7b78d2d8f4a8186aaf6ff7d8a2a8fd7`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c1ad76bab10bdb4aef989acd8a09c31f24ebf092418e7c95662a42e7b6c7d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87c4c99fc1a28b6b71ed4b5656764fd53617c4af8a1e7ccc54d90541648b62d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1f96095b93b01bf118f591bf8ddc437903590d141135fe4e8a8170c0fffe6673
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23826878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b69c435230370d631790a81bff0db94ef91908e5d79620ffa8f58cadfcdc1ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 22:15:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 22:15:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 22:15:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 22:15:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 22:15:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 22:15:03 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 22:15:03 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 22:15:03 GMT
USER fluent
# Mon, 07 Aug 2023 22:15:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 22:15:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35333f35db5b3a8277ad49e8df6a413f1d2aa4bc9d4f8f9a1a9e50dc1af890fa`  
		Last Modified: Mon, 07 Aug 2023 22:15:24 GMT  
		Size: 20.7 MB (20712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4b45e4fbb0e0d80dc55633251556ac971c6a2fdd2f79f1790f0468185a91bf`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f979b5ae9285e493d2b6e84e5ffeac065505e69caf5be55e9baa512436393ffe`  
		Last Modified: Mon, 07 Aug 2023 22:15:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4f9800fae82280c1f3364926c31016bc00e1f7016ab23013ffd259d4d5909d`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1a25b92094ae2cf54f4eb4b6477f62f4f1fd2b98fecf9dd795c4a8a7c23140e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24613316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea821a1c95d40b6d16d8a86614d246303248850411f6a76064fdf680a644d50b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:36:52 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:36:53 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:36:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:36:53 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:36:54 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:36:54 GMT
USER fluent
# Wed, 09 Aug 2023 10:36:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:36:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573645a10251b06427cca69f6934f5778b9e2bbebb05a1e2ce062aeabbcaed6c`  
		Last Modified: Wed, 09 Aug 2023 10:37:16 GMT  
		Size: 21.4 MB (21352813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6def94d3fe0e634f307aedad1ec233f8d5935f5179aae0f45044a0605ef3e11`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7756d7c80fbe1f5d223f7a0272932c0fbf8614cb831377be38e77519709a7b`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be1c945b3a64041a8f970ab711dc39c87fc8649deb1abbafb158ddd892383e`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:39a75b2171984f895bad267615d2a0f22bc36b24f823d8208170a4d29e194ff0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3105df073c5919362ae4ae41dfc99a239bd1a686e61f981c1173e70cd9dfbfb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:25:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:25:52 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:25:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:25:52 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:25:53 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:25:53 GMT
USER fluent
# Mon, 07 Aug 2023 21:25:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:25:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e180d68a6784e287fbd112203e9d4ec2f2d74e0e2d8bc178c61bf9fb8e91ddc`  
		Last Modified: Mon, 07 Aug 2023 21:26:11 GMT  
		Size: 21.0 MB (21003778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f11c2e94ea5541f00dda08086a095742ca1a0d80afc235860d18863cdac5c`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bbf332266ca282817341b04518c3cc87cafaa20c087bc76b44e51e06c199a4`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c068f06a2e3f7536a8bbd8290592b69f4348d82c50e10d45e37dc85620017a`  
		Last Modified: Mon, 07 Aug 2023 21:26:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:e657b8a0462629b862aef1ddd616c3705eb84a12f2572477884fc650da5cdbf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24994027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16729145cd752aa811ffdbb5311976ad8ef6402dca14343d17dd93e1d7d7d15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:06:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:08:31 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:08:36 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:08:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:08:39 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:08:40 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:08:41 GMT
USER fluent
# Mon, 07 Aug 2023 21:08:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:08:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ddfce8ff2f2b7be76fc6d618deefa2282d9d9f7633d981d29d351c5e0bdaea`  
		Last Modified: Mon, 07 Aug 2023 21:09:09 GMT  
		Size: 21.6 MB (21600461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbd13befcd8b8bce1f86cc5544d64cba12edd18a285fb3e19051f8d64fc9b5`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6812f97e8a8535d190c506510893fd75a499f7dad7473591664a510174854e4d`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5366a4f8d0fc4127db1580d845e4a97721553d8b57c161afebe42bcd1fb5fba`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:89ffe3f0d5665ed8fffb7793fecde61036f8d1bdde33976bd4b8e09a19b36909
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24353859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17258134d6b5a069ab70676271ad0cb35ef9a0c6a891ddf2abe2a25ea7dd18`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 20:18:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 20:18:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 20:18:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 20:18:23 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 20:18:24 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 20:18:24 GMT
USER fluent
# Mon, 07 Aug 2023 20:18:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 20:18:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79062a3efcf019be904e5ae4b1fbbe799fefdc6fe332da1cc2200c682770a8b9`  
		Last Modified: Mon, 07 Aug 2023 20:18:53 GMT  
		Size: 21.2 MB (21175672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad859df790fc4746c6b7c74231af5a72c52bce2c893e4aa5586dcb7e7d1b9e1d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff47ba17005f172794ae4f5c7c150a4662a67c98076be03c155c1637c76e3d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c86c53fee1184d9bed9db6a1ca8bea390f1c5851e6763574eeb83a0e609221`  
		Last Modified: Mon, 07 Aug 2023 20:18:51 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:cd80e37f01867c7ddabdd587567c3361dba2cdd63ea822eb97a9b4215e785629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:ed8b3432bf803a0766daaa0e4b419cc017f097865baac969b9d59a281d6ddd98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101791082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b913145f835d42ccff0b64bbd97e04f16b76a17852b229359024a16c31c6711`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:26:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 06:26:11 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 06:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 06:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 06:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 06:39:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 06:39:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 06:39:41 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 02:42:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 02:42:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 02:42:00 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 02:44:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 02:44:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 02:44:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 02:44:36 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 02:44:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 02:44:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 02:44:36 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 02:44:36 GMT
USER fluent
# Thu, 17 Aug 2023 02:44:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 02:44:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93848ed1fa68757dba2bfddcb323318666b2d7e550f9919d3ffe23c0bb19e7d0`  
		Last Modified: Wed, 16 Aug 2023 06:45:50 GMT  
		Size: 10.0 MB (10020517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51df3a3763608303de85baddd012d2c7418c1cfe2789c1d5b6a7e5f2e64879d`  
		Last Modified: Wed, 16 Aug 2023 06:45:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb013a82fefc0508910647e9533e736b52d99fdeaff5d028338af710b2bc47bb`  
		Last Modified: Wed, 16 Aug 2023 06:47:14 GMT  
		Size: 32.6 MB (32626101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e292ceba15a41e95f84b77c1514ff9a3f12dd42c9a72a999aa715453be4fc5`  
		Last Modified: Wed, 16 Aug 2023 06:47:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce2e2523b89b0482ffec0505d5201e30b82631f6694b7976327209c6ca4f9d0`  
		Last Modified: Thu, 17 Aug 2023 02:44:50 GMT  
		Size: 27.7 MB (27723703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da78cde44df7ece9e9c60ae0639ee0650d79e037667a9619d1bef2749a954cfd`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c823a8143d7bf1387c41ef28f798d68f8c27f812311035ac54107c79a96f89c`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793e1a36e2e103675c9abb898c07f7ae12086afbc322318166acdeaa4c2295ea`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3136747cc69ee757392c12346ca3703d0b33d371e33125944e6db40ccad0cc46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95273257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3297bed04235239387612537b5bc4c8d042b6689b411716b9c849983fd05f09`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:46 GMT
ADD file:fb0679e6b5c5114176b186c73a97748a7712d856da24ce6f6aad2cd210825755 in / 
# Thu, 07 Sep 2023 00:48:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 12:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 12:24:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 12:24:19 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 12:45:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 12:45:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 12:45:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 12:45:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 12:45:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 12:45:40 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 20:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 20:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 20:38:25 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 20:41:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 20:41:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 20:41:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 20:41:22 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 20:41:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 20:41:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 20:41:22 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 20:41:22 GMT
USER fluent
# Thu, 07 Sep 2023 20:41:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 20:41:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c087ebb90b5f9b89ab4e03487d68bd9805afd41a68507381ba597291c3083d6`  
		Last Modified: Thu, 07 Sep 2023 00:52:19 GMT  
		Size: 28.9 MB (28919010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade30b75c47a14b69887cf5cc38afa1503ae49e1a615fa5662b1100ca8cfee92`  
		Last Modified: Thu, 07 Sep 2023 12:51:35 GMT  
		Size: 8.6 MB (8631321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8d91a80834c51012139f89326abf487a7e4aaa26f17e02aaa168b9235fb85`  
		Last Modified: Thu, 07 Sep 2023 12:51:33 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1face2f9a6568c0fa1abde24fb129766de7e717e01ec24bac0449133d7cd3d4`  
		Last Modified: Thu, 07 Sep 2023 12:53:58 GMT  
		Size: 31.2 MB (31166045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9005c5622f6fd2c57ce5c2924a71d5a86ecc12fdbb83e26654a53bfea0ecaae7`  
		Last Modified: Thu, 07 Sep 2023 12:53:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c832643a2ad8e8c7b078f32392cbdca55f2bfe901fe94161200b51661a41be06`  
		Last Modified: Thu, 07 Sep 2023 20:41:45 GMT  
		Size: 26.6 MB (26553806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd2cd4dd2de9f38ae9175452483d46a17a93fd952f1a65f1991c66216220ad`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520810c24c84d466eb9b7e6e29a526ef49a98b60dd73d3840c00ac6e9be5894a`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304f414b1c1f41131994ca2c471a0a0f323f02a5575538e60696e1d3a81bbd05`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:daa63dee1e42484d5207eac0dd871a7cd3d13ef66ca61c7ceb0a8e2304d3d0cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92142907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabd9ed791ed0f31ecf0ed55976ad9e78bc986001b2efb1fa23fde7e53cf7bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:33 GMT
ADD file:d9383f6a4370dbf4af8e05edac181465a410899022cf1788f9001a976b9beecd in / 
# Wed, 16 Aug 2023 00:17:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:06:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 05:06:14 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 05:17:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 05:17:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 05:17:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 05:17:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 05:17:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 05:17:38 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 00:02:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 00:02:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 00:02:59 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 00:05:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 00:05:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 00:05:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 00:05:40 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 00:05:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 00:05:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 00:05:40 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 00:05:40 GMT
USER fluent
# Thu, 17 Aug 2023 00:05:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 00:05:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:66971a88ba9c0b0ac6503475f1bc4981010269bdba2638318b63c625ee44cd79`  
		Last Modified: Wed, 16 Aug 2023 00:22:09 GMT  
		Size: 26.6 MB (26578637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610e32d81bfedb6dbcbce54a3ede57c03d64596fb5201784582b7f689ba2c57c`  
		Last Modified: Wed, 16 Aug 2023 05:23:28 GMT  
		Size: 8.1 MB (8141708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcee73cf3a4a1347b62919b1786a70e6c830815b81da9254bee72ba3101e7a50`  
		Last Modified: Wed, 16 Aug 2023 05:23:26 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0deda2f1a7382c02c257b72389a0e6bc27865a2cec88c3c8a25dfceff008c5`  
		Last Modified: Wed, 16 Aug 2023 05:24:46 GMT  
		Size: 31.0 MB (31035437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3fcfb01168c310f9a2fe0230b92061fac6e69597cfebfde16054c8970996b6`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ac79b5eae924aec9edba4fecde2ad97233062d93bfc175460ddff258853c6`  
		Last Modified: Thu, 17 Aug 2023 00:06:01 GMT  
		Size: 26.4 MB (26384048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53cbb5efeb6a8f905db0f7e5dbfdf38fa5b85686e65c25b8ac1ac6541dde4d4`  
		Last Modified: Thu, 17 Aug 2023 00:05:58 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddbc2b3a5694d3b580ca51421da56198b71e5b500f9ccab63db3dc183f4233f`  
		Last Modified: Thu, 17 Aug 2023 00:05:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eddc07e07539d0ff8a067eb69a1ebc18f596741bad36a16aacde06efed5b80`  
		Last Modified: Thu, 17 Aug 2023 00:05:57 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a1015cb5d8ba32a962d28556868ace2c425df601c4c84d2c15f0647b55828d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98780629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce393570d7c0891900d8b0cbdc66f0d799bd9e1ff7e771819451fe37e4b7859f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:03:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 02:03:49 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 02:15:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 02:15:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 02:15:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 02:15:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 02:15:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 02:15:13 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 10:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 10:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 10:01:38 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 10:03:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 10:03:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 10:03:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 10:03:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 10:03:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 10:03:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 10:03:53 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 10:03:53 GMT
USER fluent
# Thu, 07 Sep 2023 10:03:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 10:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82e0602f1325d6303aca9fa1455ad8b94302c2415bb8fbc7b499796502a1f91`  
		Last Modified: Thu, 07 Sep 2023 02:20:15 GMT  
		Size: 9.2 MB (9239493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a609a4be0d1f17600b4de42400565b4ad9454b91c3d455edea6fd268649d21`  
		Last Modified: Thu, 07 Sep 2023 02:20:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4acfd8e2987f550ac3247c7e43b7ead8da9025c19f3d9409d8cad8919156cf1`  
		Last Modified: Thu, 07 Sep 2023 02:21:33 GMT  
		Size: 32.0 MB (31987257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1c2c385898cefc52139d5f3c54cc17e7d1256c7b078a043606dc0f3e3c3d82`  
		Last Modified: Thu, 07 Sep 2023 02:21:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e927a6a5fea0d29794cfe37687d7b10555e9eafd66df1c229104fb0ec10b47`  
		Last Modified: Thu, 07 Sep 2023 10:04:12 GMT  
		Size: 27.5 MB (27487896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47f24bcbf93fee3be51a33305b31a547fb53c46d128df820fe6566907d9f0d2`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6901fb6267f673285ed239bfeb571ba8b54ded194cf37bb5586d864e4f605418`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341423fa5bf1e04c09e7e2560a222d1bfd2791555be916f4d03086e6e1949bea`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:4c1b30e91dec61184ee6544abf4ed3b02cfa54ac73b12960d60a8f00964c551d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102180404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a36baf5bc92c445ec07c0689161eb6e418f691c65d725f48eb58a7d619037f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:23 GMT
ADD file:fa0abd37650f364ecdf67d446b3fe2ce58fac1ad53beb5263b4f230fad58931e in / 
# Tue, 15 Aug 2023 23:39:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 08:13:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 08:13:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 08:13:37 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 08:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 08:46:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 08:46:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 08:46:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 08:46:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 08:46:44 GMT
CMD ["irb"]
# Wed, 16 Aug 2023 16:40:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 16 Aug 2023 16:40:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 16 Aug 2023 16:40:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 16 Aug 2023 16:43:57 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 16 Aug 2023 16:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 16 Aug 2023 16:43:58 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 16 Aug 2023 16:43:58 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 16 Aug 2023 16:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 16 Aug 2023 16:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 16 Aug 2023 16:43:58 GMT
EXPOSE 24224 5140
# Wed, 16 Aug 2023 16:43:58 GMT
USER fluent
# Wed, 16 Aug 2023 16:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 16 Aug 2023 16:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f6edc1df8dbb4cb778380e62ce1680ea580c1b213c048642bb7adaafa4cc6d73`  
		Last Modified: Tue, 15 Aug 2023 23:44:11 GMT  
		Size: 32.4 MB (32397200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ba5a1bb68f809f27156c2fa68c74b0cba5057cd17e2d111412c6e4907e959f`  
		Last Modified: Wed, 16 Aug 2023 09:01:55 GMT  
		Size: 12.0 MB (11994796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f40e6f3593eca6361e1b9f9997aa891e4e205f5427f639264a02043274c170`  
		Last Modified: Wed, 16 Aug 2023 09:01:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab0b762c1d6b478a9d61ff98c5768d02ea38f3201694a2fa576e393d19b16f9`  
		Last Modified: Wed, 16 Aug 2023 09:04:24 GMT  
		Size: 31.2 MB (31181636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896c9134c0a11842611c314aa4615444fa2c589c19767d865612a91ca67e9d69`  
		Last Modified: Wed, 16 Aug 2023 09:04:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7489e946352c3fc0dead3a80fa80ff44d9b99bea7195e2eac0b1b3bae111842f`  
		Last Modified: Wed, 16 Aug 2023 16:44:19 GMT  
		Size: 26.6 MB (26603697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb101e392846cf802086e0c5ae2f49ad75e94c29e92965a8f4470a9172204f5e`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f051d0c24bbc48c5e8150145576ded492050282812a0b983a75d924fd1adf6`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cd1a89e65e1a05250776ffe948f98a08d630d2aef7d288a0d430b1e6e85cd1`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7c12f61521cf5242d8be65713eb90a922feddd4761a4c3ca69704aceaf87cd95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106780219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a0b5237f764dc45c219672dcea049f0403c5eab24d708bc0e83ce1d233ba9d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 01:10:12 GMT
ADD file:eeb766a3bb0461f0baa2425cfd43628994c064bd728f51f1b8df659a4bd2f489 in / 
# Wed, 16 Aug 2023 01:10:14 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 08:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 08:50:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Aug 2023 08:50:49 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 09:32:48 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Aug 2023 09:32:55 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 17 Aug 2023 09:33:00 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 17 Aug 2023 09:43:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Aug 2023 09:43:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Aug 2023 09:43:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Aug 2023 09:43:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 09:43:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 17 Aug 2023 09:43:13 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 13:43:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 13:43:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 13:43:54 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 13:49:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 13:49:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 13:49:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 13:49:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 13:49:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 13:49:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 13:49:21 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 13:49:21 GMT
USER fluent
# Thu, 17 Aug 2023 13:49:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 13:49:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dacf4195c8a0403fd11459739bf9dc9be427261bf5e0bedb49e18d1498cf7c2e`  
		Last Modified: Wed, 16 Aug 2023 01:17:04 GMT  
		Size: 35.3 MB (35291067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee07a10913f9f4565e4823be9e12665945297b5440f584e0249f43ece640231`  
		Last Modified: Thu, 17 Aug 2023 10:00:18 GMT  
		Size: 10.5 MB (10478338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458fcdfed2450b7ad6c58dc8e17ea9333d8e97d8bb9682b20dc8dfc5c0fd4cdd`  
		Last Modified: Thu, 17 Aug 2023 10:00:15 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95442ecd417e0450cc05b2b10120858449b97c0debd6ee901910d94dd9c2fe85`  
		Last Modified: Thu, 17 Aug 2023 10:04:21 GMT  
		Size: 32.8 MB (32792156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a56f12fac1274d743a18a0057fa4020fdd8aaa391a5c26b507435afc0f38b1`  
		Last Modified: Thu, 17 Aug 2023 10:04:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41213f17ef44c1db6717d6355085b49d37b45f929fcb584eb160fc41f1176f84`  
		Last Modified: Thu, 17 Aug 2023 13:49:53 GMT  
		Size: 28.2 MB (28215571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0191d2a6c3379ec20b14bab3ecca432244ad85ff957c28acf4afab6269494ba3`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a88eb1dc871e15c2650a3e9c04d4b6309b8dccf00b4f1979540c6cc208dada`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a575a89e63e3a38f025eb7c7d4d1c23daecb8d2b90edb2022dddc563609adc`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:9945278b6d47197a87199045a8868da619bae265940effdb5b1235b4775d157a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98904116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b652d3a139f0e3a872c3b29ead2ad97f1bf37770e7c63e4a96b8beb614565715`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 08:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 08:59:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 08:59:47 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 09:22:32 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 09:22:33 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 09:22:33 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 09:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 09:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 09:28:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 09:28:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:28:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 09:28:05 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 19:40:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 19:40:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 19:40:10 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 19:43:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 19:43:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 19:43:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 19:43:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 19:43:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 19:43:54 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 19:43:54 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 19:43:55 GMT
USER fluent
# Thu, 07 Sep 2023 19:43:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 19:43:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97aae84c7c3cde65a55b4f8feefe271997414dfbfff7a5aad25032356e79191`  
		Last Modified: Thu, 07 Sep 2023 09:37:37 GMT  
		Size: 8.9 MB (8859338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb123504cd97cbeb25a70dece1e77e617e75c3a455f2076e816ada6b23f45ee`  
		Last Modified: Thu, 07 Sep 2023 09:37:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ba862a63270efa26e979f625b9ce37e031380fd1aa6c3b0d244cb36aad758`  
		Last Modified: Thu, 07 Sep 2023 09:39:18 GMT  
		Size: 32.4 MB (32445358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414fc54aa6b3e4a4f56f42714e5a945e24ebe695660c1b66fd7d1a1855ece19c`  
		Last Modified: Thu, 07 Sep 2023 09:39:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3fa0d678fd50319bbced1159da784ca80f910360f48345e00849290518fafe`  
		Last Modified: Thu, 07 Sep 2023 19:44:30 GMT  
		Size: 27.9 MB (27943524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68cf5051cb8e28b53078783ff1e8ba245b8e41d62593e543a7755a61bae59b3`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e803c74a631c2ec1667f46af5e57ca5e8d177f19feababcebb043bf5665ff8f8`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16390a5ef0fc48c41630da1957f223334604b2475e779a62127267cbad1834b`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-1.0`

```console
$ docker pull fluentd@sha256:3b5e8bb493f277c0e04a5ff6f48a4a72fd13083a6ff09ac98527bec1c2f9d73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16.0-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:56c9a79408eb21afe816f7f596cd14c3414bbc1ab216a554194d58ade0318aad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25150972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd0325e67fca65a5c1b19f78bd50b1111fa5725360ebac717b5df77354ef856`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:09:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:09:24 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:09:24 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:09:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:09:24 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:09:25 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:09:25 GMT
USER fluent
# Wed, 09 Aug 2023 10:09:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:09:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e3f26392ec29ada78eeb1c98c2df3f8422b5a581376a4093d8c80c36869b40`  
		Last Modified: Wed, 09 Aug 2023 10:09:41 GMT  
		Size: 21.8 MB (21770144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f2007908d1df8b7db8a7456ff60be7e7b78d2d8f4a8186aaf6ff7d8a2a8fd7`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c1ad76bab10bdb4aef989acd8a09c31f24ebf092418e7c95662a42e7b6c7d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87c4c99fc1a28b6b71ed4b5656764fd53617c4af8a1e7ccc54d90541648b62d`  
		Last Modified: Wed, 09 Aug 2023 10:09:38 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1f96095b93b01bf118f591bf8ddc437903590d141135fe4e8a8170c0fffe6673
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23826878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b69c435230370d631790a81bff0db94ef91908e5d79620ffa8f58cadfcdc1ce`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 22:15:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 22:15:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 22:15:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 22:15:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 22:15:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 22:15:03 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 22:15:03 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 22:15:03 GMT
USER fluent
# Mon, 07 Aug 2023 22:15:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 22:15:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35333f35db5b3a8277ad49e8df6a413f1d2aa4bc9d4f8f9a1a9e50dc1af890fa`  
		Last Modified: Mon, 07 Aug 2023 22:15:24 GMT  
		Size: 20.7 MB (20712211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4b45e4fbb0e0d80dc55633251556ac971c6a2fdd2f79f1790f0468185a91bf`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f979b5ae9285e493d2b6e84e5ffeac065505e69caf5be55e9baa512436393ffe`  
		Last Modified: Mon, 07 Aug 2023 22:15:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4f9800fae82280c1f3364926c31016bc00e1f7016ab23013ffd259d4d5909d`  
		Last Modified: Mon, 07 Aug 2023 22:15:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1a25b92094ae2cf54f4eb4b6477f62f4f1fd2b98fecf9dd795c4a8a7c23140e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24613316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea821a1c95d40b6d16d8a86614d246303248850411f6a76064fdf680a644d50b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 09 Aug 2023 10:36:52 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 09 Aug 2023 10:36:53 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 09 Aug 2023 10:36:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 09 Aug 2023 10:36:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 09 Aug 2023 10:36:53 GMT
ENV LD_PRELOAD=
# Wed, 09 Aug 2023 10:36:54 GMT
EXPOSE 24224 5140
# Wed, 09 Aug 2023 10:36:54 GMT
USER fluent
# Wed, 09 Aug 2023 10:36:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 09 Aug 2023 10:36:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573645a10251b06427cca69f6934f5778b9e2bbebb05a1e2ce062aeabbcaed6c`  
		Last Modified: Wed, 09 Aug 2023 10:37:16 GMT  
		Size: 21.4 MB (21352813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6def94d3fe0e634f307aedad1ec233f8d5935f5179aae0f45044a0605ef3e11`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7756d7c80fbe1f5d223f7a0272932c0fbf8614cb831377be38e77519709a7b`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be1c945b3a64041a8f970ab711dc39c87fc8649deb1abbafb158ddd892383e`  
		Last Modified: Wed, 09 Aug 2023 10:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:39a75b2171984f895bad267615d2a0f22bc36b24f823d8208170a4d29e194ff0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3105df073c5919362ae4ae41dfc99a239bd1a686e61f981c1173e70cd9dfbfb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:25:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:25:52 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:25:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:25:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:25:52 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:25:53 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:25:53 GMT
USER fluent
# Mon, 07 Aug 2023 21:25:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:25:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e180d68a6784e287fbd112203e9d4ec2f2d74e0e2d8bc178c61bf9fb8e91ddc`  
		Last Modified: Mon, 07 Aug 2023 21:26:11 GMT  
		Size: 21.0 MB (21003778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f11c2e94ea5541f00dda08086a095742ca1a0d80afc235860d18863cdac5c`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bbf332266ca282817341b04518c3cc87cafaa20c087bc76b44e51e06c199a4`  
		Last Modified: Mon, 07 Aug 2023 21:26:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c068f06a2e3f7536a8bbd8290592b69f4348d82c50e10d45e37dc85620017a`  
		Last Modified: Mon, 07 Aug 2023 21:26:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:e657b8a0462629b862aef1ddd616c3705eb84a12f2572477884fc650da5cdbf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24994027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16729145cd752aa811ffdbb5311976ad8ef6402dca14343d17dd93e1d7d7d15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 21:06:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 21:08:31 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 21:08:36 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 21:08:38 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 21:08:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 21:08:39 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 21:08:40 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 21:08:41 GMT
USER fluent
# Mon, 07 Aug 2023 21:08:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 21:08:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ddfce8ff2f2b7be76fc6d618deefa2282d9d9f7633d981d29d351c5e0bdaea`  
		Last Modified: Mon, 07 Aug 2023 21:09:09 GMT  
		Size: 21.6 MB (21600461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbd13befcd8b8bce1f86cc5544d64cba12edd18a285fb3e19051f8d64fc9b5`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6812f97e8a8535d190c506510893fd75a499f7dad7473591664a510174854e4d`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5366a4f8d0fc4127db1580d845e4a97721553d8b57c161afebe42bcd1fb5fba`  
		Last Modified: Mon, 07 Aug 2023 21:09:03 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:89ffe3f0d5665ed8fffb7793fecde61036f8d1bdde33976bd4b8e09a19b36909
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24353859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17258134d6b5a069ab70676271ad0cb35ef9a0c6a891ddf2abe2a25ea7dd18`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 07 Aug 2023 20:18:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 07 Aug 2023 20:18:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 07 Aug 2023 20:18:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 07 Aug 2023 20:18:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 07 Aug 2023 20:18:23 GMT
ENV LD_PRELOAD=
# Mon, 07 Aug 2023 20:18:24 GMT
EXPOSE 24224 5140
# Mon, 07 Aug 2023 20:18:24 GMT
USER fluent
# Mon, 07 Aug 2023 20:18:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 07 Aug 2023 20:18:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79062a3efcf019be904e5ae4b1fbbe799fefdc6fe332da1cc2200c682770a8b9`  
		Last Modified: Mon, 07 Aug 2023 20:18:53 GMT  
		Size: 21.2 MB (21175672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad859df790fc4746c6b7c74231af5a72c52bce2c893e4aa5586dcb7e7d1b9e1d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff47ba17005f172794ae4f5c7c150a4662a67c98076be03c155c1637c76e3d`  
		Last Modified: Mon, 07 Aug 2023 20:18:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c86c53fee1184d9bed9db6a1ca8bea390f1c5851e6763574eeb83a0e609221`  
		Last Modified: Mon, 07 Aug 2023 20:18:51 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-debian-1.0`

```console
$ docker pull fluentd@sha256:cd80e37f01867c7ddabdd587567c3361dba2cdd63ea822eb97a9b4215e785629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16.0-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:ed8b3432bf803a0766daaa0e4b419cc017f097865baac969b9d59a281d6ddd98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101791082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b913145f835d42ccff0b64bbd97e04f16b76a17852b229359024a16c31c6711`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:26:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 06:26:11 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 06:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 06:39:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 06:39:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 06:39:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 06:39:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 06:39:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 06:39:41 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 02:42:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 02:42:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 02:42:00 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 02:44:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 02:44:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 02:44:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 02:44:36 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 02:44:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 02:44:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 02:44:36 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 02:44:36 GMT
USER fluent
# Thu, 17 Aug 2023 02:44:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 02:44:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93848ed1fa68757dba2bfddcb323318666b2d7e550f9919d3ffe23c0bb19e7d0`  
		Last Modified: Wed, 16 Aug 2023 06:45:50 GMT  
		Size: 10.0 MB (10020517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51df3a3763608303de85baddd012d2c7418c1cfe2789c1d5b6a7e5f2e64879d`  
		Last Modified: Wed, 16 Aug 2023 06:45:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb013a82fefc0508910647e9533e736b52d99fdeaff5d028338af710b2bc47bb`  
		Last Modified: Wed, 16 Aug 2023 06:47:14 GMT  
		Size: 32.6 MB (32626101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e292ceba15a41e95f84b77c1514ff9a3f12dd42c9a72a999aa715453be4fc5`  
		Last Modified: Wed, 16 Aug 2023 06:47:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce2e2523b89b0482ffec0505d5201e30b82631f6694b7976327209c6ca4f9d0`  
		Last Modified: Thu, 17 Aug 2023 02:44:50 GMT  
		Size: 27.7 MB (27723703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da78cde44df7ece9e9c60ae0639ee0650d79e037667a9619d1bef2749a954cfd`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c823a8143d7bf1387c41ef28f798d68f8c27f812311035ac54107c79a96f89c`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793e1a36e2e103675c9abb898c07f7ae12086afbc322318166acdeaa4c2295ea`  
		Last Modified: Thu, 17 Aug 2023 02:44:46 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3136747cc69ee757392c12346ca3703d0b33d371e33125944e6db40ccad0cc46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95273257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3297bed04235239387612537b5bc4c8d042b6689b411716b9c849983fd05f09`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:46 GMT
ADD file:fb0679e6b5c5114176b186c73a97748a7712d856da24ce6f6aad2cd210825755 in / 
# Thu, 07 Sep 2023 00:48:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 12:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 12:24:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 12:24:19 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 12:43:28 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 12:45:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 12:45:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 12:45:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 12:45:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 12:45:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 12:45:40 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 20:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 20:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 20:38:25 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 20:41:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 20:41:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 20:41:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 20:41:22 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 20:41:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 20:41:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 20:41:22 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 20:41:22 GMT
USER fluent
# Thu, 07 Sep 2023 20:41:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 20:41:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c087ebb90b5f9b89ab4e03487d68bd9805afd41a68507381ba597291c3083d6`  
		Last Modified: Thu, 07 Sep 2023 00:52:19 GMT  
		Size: 28.9 MB (28919010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade30b75c47a14b69887cf5cc38afa1503ae49e1a615fa5662b1100ca8cfee92`  
		Last Modified: Thu, 07 Sep 2023 12:51:35 GMT  
		Size: 8.6 MB (8631321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8d91a80834c51012139f89326abf487a7e4aaa26f17e02aaa168b9235fb85`  
		Last Modified: Thu, 07 Sep 2023 12:51:33 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1face2f9a6568c0fa1abde24fb129766de7e717e01ec24bac0449133d7cd3d4`  
		Last Modified: Thu, 07 Sep 2023 12:53:58 GMT  
		Size: 31.2 MB (31166045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9005c5622f6fd2c57ce5c2924a71d5a86ecc12fdbb83e26654a53bfea0ecaae7`  
		Last Modified: Thu, 07 Sep 2023 12:53:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c832643a2ad8e8c7b078f32392cbdca55f2bfe901fe94161200b51661a41be06`  
		Last Modified: Thu, 07 Sep 2023 20:41:45 GMT  
		Size: 26.6 MB (26553806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd2cd4dd2de9f38ae9175452483d46a17a93fd952f1a65f1991c66216220ad`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520810c24c84d466eb9b7e6e29a526ef49a98b60dd73d3840c00ac6e9be5894a`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304f414b1c1f41131994ca2c471a0a0f323f02a5575538e60696e1d3a81bbd05`  
		Last Modified: Thu, 07 Sep 2023 20:41:39 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:daa63dee1e42484d5207eac0dd871a7cd3d13ef66ca61c7ceb0a8e2304d3d0cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92142907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabd9ed791ed0f31ecf0ed55976ad9e78bc986001b2efb1fa23fde7e53cf7bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:33 GMT
ADD file:d9383f6a4370dbf4af8e05edac181465a410899022cf1788f9001a976b9beecd in / 
# Wed, 16 Aug 2023 00:17:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:06:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 05:06:14 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 05:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 05:17:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 05:17:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 05:17:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 05:17:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 05:17:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 05:17:38 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 00:02:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 00:02:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 00:02:59 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 00:05:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 00:05:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 00:05:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 00:05:40 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 00:05:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 00:05:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 00:05:40 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 00:05:40 GMT
USER fluent
# Thu, 17 Aug 2023 00:05:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 00:05:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:66971a88ba9c0b0ac6503475f1bc4981010269bdba2638318b63c625ee44cd79`  
		Last Modified: Wed, 16 Aug 2023 00:22:09 GMT  
		Size: 26.6 MB (26578637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610e32d81bfedb6dbcbce54a3ede57c03d64596fb5201784582b7f689ba2c57c`  
		Last Modified: Wed, 16 Aug 2023 05:23:28 GMT  
		Size: 8.1 MB (8141708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcee73cf3a4a1347b62919b1786a70e6c830815b81da9254bee72ba3101e7a50`  
		Last Modified: Wed, 16 Aug 2023 05:23:26 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0deda2f1a7382c02c257b72389a0e6bc27865a2cec88c3c8a25dfceff008c5`  
		Last Modified: Wed, 16 Aug 2023 05:24:46 GMT  
		Size: 31.0 MB (31035437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3fcfb01168c310f9a2fe0230b92061fac6e69597cfebfde16054c8970996b6`  
		Last Modified: Wed, 16 Aug 2023 05:24:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ac79b5eae924aec9edba4fecde2ad97233062d93bfc175460ddff258853c6`  
		Last Modified: Thu, 17 Aug 2023 00:06:01 GMT  
		Size: 26.4 MB (26384048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53cbb5efeb6a8f905db0f7e5dbfdf38fa5b85686e65c25b8ac1ac6541dde4d4`  
		Last Modified: Thu, 17 Aug 2023 00:05:58 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddbc2b3a5694d3b580ca51421da56198b71e5b500f9ccab63db3dc183f4233f`  
		Last Modified: Thu, 17 Aug 2023 00:05:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eddc07e07539d0ff8a067eb69a1ebc18f596741bad36a16aacde06efed5b80`  
		Last Modified: Thu, 17 Aug 2023 00:05:57 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a1015cb5d8ba32a962d28556868ace2c425df601c4c84d2c15f0647b55828d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98780629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce393570d7c0891900d8b0cbdc66f0d799bd9e1ff7e771819451fe37e4b7859f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:03:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 02:03:49 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 02:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 02:15:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 02:15:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 02:15:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 02:15:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 02:15:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 02:15:13 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 10:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 10:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 10:01:38 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 10:03:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 10:03:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 10:03:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 10:03:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 10:03:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 10:03:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 10:03:53 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 10:03:53 GMT
USER fluent
# Thu, 07 Sep 2023 10:03:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 10:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82e0602f1325d6303aca9fa1455ad8b94302c2415bb8fbc7b499796502a1f91`  
		Last Modified: Thu, 07 Sep 2023 02:20:15 GMT  
		Size: 9.2 MB (9239493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a609a4be0d1f17600b4de42400565b4ad9454b91c3d455edea6fd268649d21`  
		Last Modified: Thu, 07 Sep 2023 02:20:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4acfd8e2987f550ac3247c7e43b7ead8da9025c19f3d9409d8cad8919156cf1`  
		Last Modified: Thu, 07 Sep 2023 02:21:33 GMT  
		Size: 32.0 MB (31987257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1c2c385898cefc52139d5f3c54cc17e7d1256c7b078a043606dc0f3e3c3d82`  
		Last Modified: Thu, 07 Sep 2023 02:21:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e927a6a5fea0d29794cfe37687d7b10555e9eafd66df1c229104fb0ec10b47`  
		Last Modified: Thu, 07 Sep 2023 10:04:12 GMT  
		Size: 27.5 MB (27487896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47f24bcbf93fee3be51a33305b31a547fb53c46d128df820fe6566907d9f0d2`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6901fb6267f673285ed239bfeb571ba8b54ded194cf37bb5586d864e4f605418`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341423fa5bf1e04c09e7e2560a222d1bfd2791555be916f4d03086e6e1949bea`  
		Last Modified: Thu, 07 Sep 2023 10:04:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:4c1b30e91dec61184ee6544abf4ed3b02cfa54ac73b12960d60a8f00964c551d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102180404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a36baf5bc92c445ec07c0689161eb6e418f691c65d725f48eb58a7d619037f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:23 GMT
ADD file:fa0abd37650f364ecdf67d446b3fe2ce58fac1ad53beb5263b4f230fad58931e in / 
# Tue, 15 Aug 2023 23:39:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 08:13:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 08:13:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 16 Aug 2023 08:13:37 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_MAJOR=3.1
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 16 Aug 2023 08:43:08 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 16 Aug 2023 08:46:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 16 Aug 2023 08:46:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 16 Aug 2023 08:46:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 16 Aug 2023 08:46:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 08:46:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 16 Aug 2023 08:46:44 GMT
CMD ["irb"]
# Wed, 16 Aug 2023 16:40:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 16 Aug 2023 16:40:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 16 Aug 2023 16:40:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 16 Aug 2023 16:43:57 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 16 Aug 2023 16:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 16 Aug 2023 16:43:58 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 16 Aug 2023 16:43:58 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 16 Aug 2023 16:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 16 Aug 2023 16:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 16 Aug 2023 16:43:58 GMT
EXPOSE 24224 5140
# Wed, 16 Aug 2023 16:43:58 GMT
USER fluent
# Wed, 16 Aug 2023 16:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 16 Aug 2023 16:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f6edc1df8dbb4cb778380e62ce1680ea580c1b213c048642bb7adaafa4cc6d73`  
		Last Modified: Tue, 15 Aug 2023 23:44:11 GMT  
		Size: 32.4 MB (32397200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ba5a1bb68f809f27156c2fa68c74b0cba5057cd17e2d111412c6e4907e959f`  
		Last Modified: Wed, 16 Aug 2023 09:01:55 GMT  
		Size: 12.0 MB (11994796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f40e6f3593eca6361e1b9f9997aa891e4e205f5427f639264a02043274c170`  
		Last Modified: Wed, 16 Aug 2023 09:01:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab0b762c1d6b478a9d61ff98c5768d02ea38f3201694a2fa576e393d19b16f9`  
		Last Modified: Wed, 16 Aug 2023 09:04:24 GMT  
		Size: 31.2 MB (31181636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896c9134c0a11842611c314aa4615444fa2c589c19767d865612a91ca67e9d69`  
		Last Modified: Wed, 16 Aug 2023 09:04:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7489e946352c3fc0dead3a80fa80ff44d9b99bea7195e2eac0b1b3bae111842f`  
		Last Modified: Wed, 16 Aug 2023 16:44:19 GMT  
		Size: 26.6 MB (26603697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb101e392846cf802086e0c5ae2f49ad75e94c29e92965a8f4470a9172204f5e`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f051d0c24bbc48c5e8150145576ded492050282812a0b983a75d924fd1adf6`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cd1a89e65e1a05250776ffe948f98a08d630d2aef7d288a0d430b1e6e85cd1`  
		Last Modified: Wed, 16 Aug 2023 16:44:14 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:7c12f61521cf5242d8be65713eb90a922feddd4761a4c3ca69704aceaf87cd95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106780219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a0b5237f764dc45c219672dcea049f0403c5eab24d708bc0e83ce1d233ba9d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 16 Aug 2023 01:10:12 GMT
ADD file:eeb766a3bb0461f0baa2425cfd43628994c064bd728f51f1b8df659a4bd2f489 in / 
# Wed, 16 Aug 2023 01:10:14 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 08:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 08:50:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Aug 2023 08:50:49 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 09:32:48 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Aug 2023 09:32:55 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 17 Aug 2023 09:33:00 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 17 Aug 2023 09:43:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Aug 2023 09:43:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Aug 2023 09:43:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Aug 2023 09:43:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 09:43:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 17 Aug 2023 09:43:13 GMT
CMD ["irb"]
# Thu, 17 Aug 2023 13:43:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 17 Aug 2023 13:43:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 17 Aug 2023 13:43:54 GMT
ENV TINI_VERSION=0.18.0
# Thu, 17 Aug 2023 13:49:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 17 Aug 2023 13:49:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 17 Aug 2023 13:49:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 17 Aug 2023 13:49:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 17 Aug 2023 13:49:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 17 Aug 2023 13:49:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 17 Aug 2023 13:49:21 GMT
EXPOSE 24224 5140
# Thu, 17 Aug 2023 13:49:21 GMT
USER fluent
# Thu, 17 Aug 2023 13:49:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 17 Aug 2023 13:49:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dacf4195c8a0403fd11459739bf9dc9be427261bf5e0bedb49e18d1498cf7c2e`  
		Last Modified: Wed, 16 Aug 2023 01:17:04 GMT  
		Size: 35.3 MB (35291067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee07a10913f9f4565e4823be9e12665945297b5440f584e0249f43ece640231`  
		Last Modified: Thu, 17 Aug 2023 10:00:18 GMT  
		Size: 10.5 MB (10478338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458fcdfed2450b7ad6c58dc8e17ea9333d8e97d8bb9682b20dc8dfc5c0fd4cdd`  
		Last Modified: Thu, 17 Aug 2023 10:00:15 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95442ecd417e0450cc05b2b10120858449b97c0debd6ee901910d94dd9c2fe85`  
		Last Modified: Thu, 17 Aug 2023 10:04:21 GMT  
		Size: 32.8 MB (32792156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a56f12fac1274d743a18a0057fa4020fdd8aaa391a5c26b507435afc0f38b1`  
		Last Modified: Thu, 17 Aug 2023 10:04:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41213f17ef44c1db6717d6355085b49d37b45f929fcb584eb160fc41f1176f84`  
		Last Modified: Thu, 17 Aug 2023 13:49:53 GMT  
		Size: 28.2 MB (28215571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0191d2a6c3379ec20b14bab3ecca432244ad85ff957c28acf4afab6269494ba3`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a88eb1dc871e15c2650a3e9c04d4b6309b8dccf00b4f1979540c6cc208dada`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a575a89e63e3a38f025eb7c7d4d1c23daecb8d2b90edb2022dddc563609adc`  
		Last Modified: Thu, 17 Aug 2023 13:49:47 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:9945278b6d47197a87199045a8868da619bae265940effdb5b1235b4775d157a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98904116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b652d3a139f0e3a872c3b29ead2ad97f1bf37770e7c63e4a96b8beb614565715`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 08:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 08:59:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 07 Sep 2023 08:59:47 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 09:22:32 GMT
ENV RUBY_MAJOR=3.1
# Thu, 07 Sep 2023 09:22:33 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 07 Sep 2023 09:22:33 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 07 Sep 2023 09:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 07 Sep 2023 09:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 07 Sep 2023 09:28:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 07 Sep 2023 09:28:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:28:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 07 Sep 2023 09:28:05 GMT
CMD ["irb"]
# Thu, 07 Sep 2023 19:40:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 07 Sep 2023 19:40:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 07 Sep 2023 19:40:10 GMT
ENV TINI_VERSION=0.18.0
# Thu, 07 Sep 2023 19:43:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 07 Sep 2023 19:43:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 07 Sep 2023 19:43:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 07 Sep 2023 19:43:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 07 Sep 2023 19:43:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 07 Sep 2023 19:43:54 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 07 Sep 2023 19:43:54 GMT
EXPOSE 24224 5140
# Thu, 07 Sep 2023 19:43:55 GMT
USER fluent
# Thu, 07 Sep 2023 19:43:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 07 Sep 2023 19:43:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97aae84c7c3cde65a55b4f8feefe271997414dfbfff7a5aad25032356e79191`  
		Last Modified: Thu, 07 Sep 2023 09:37:37 GMT  
		Size: 8.9 MB (8859338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb123504cd97cbeb25a70dece1e77e617e75c3a455f2076e816ada6b23f45ee`  
		Last Modified: Thu, 07 Sep 2023 09:37:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ba862a63270efa26e979f625b9ce37e031380fd1aa6c3b0d244cb36aad758`  
		Last Modified: Thu, 07 Sep 2023 09:39:18 GMT  
		Size: 32.4 MB (32445358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414fc54aa6b3e4a4f56f42714e5a945e24ebe695660c1b66fd7d1a1855ece19c`  
		Last Modified: Thu, 07 Sep 2023 09:39:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3fa0d678fd50319bbced1159da784ca80f910360f48345e00849290518fafe`  
		Last Modified: Thu, 07 Sep 2023 19:44:30 GMT  
		Size: 27.9 MB (27943524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68cf5051cb8e28b53078783ff1e8ba245b8e41d62593e543a7755a61bae59b3`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e803c74a631c2ec1667f46af5e57ca5e8d177f19feababcebb043bf5665ff8f8`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16390a5ef0fc48c41630da1957f223334604b2475e779a62127267cbad1834b`  
		Last Modified: Thu, 07 Sep 2023 19:44:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
