## `fluentd:latest`

```console
$ docker pull fluentd@sha256:714ee9e3b38bcfbd9468035e0a772c7bb21bc069eb9c25f08a32c466bd61d640
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
$ docker pull fluentd@sha256:21303421f4f8e3cf8b3398e4522a5756ed3967dac22c59e4a86596fc55086bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19079844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3134b06b92a81f10483c2a8787351fd5f29558f2f102b9d10cac903c05fabb42`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 20:20:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Sep 2021 20:20:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 07 Sep 2021 20:21:40 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 07 Sep 2021 20:21:41 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 07 Sep 2021 20:21:41 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 07 Sep 2021 20:21:42 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 07 Sep 2021 20:21:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Sep 2021 20:21:42 GMT
ENV LD_PRELOAD=
# Tue, 07 Sep 2021 20:21:42 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 07 Sep 2021 20:21:42 GMT
EXPOSE 24224 5140
# Tue, 07 Sep 2021 20:21:42 GMT
USER fluent
# Tue, 07 Sep 2021 20:21:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Sep 2021 20:21:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d74db1dcb580089442caaa14445aae91594a0d03f053028dbd9f4296834bd3`  
		Last Modified: Tue, 07 Sep 2021 20:23:38 GMT  
		Size: 16.3 MB (16263561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e54056b9038af025f41617e6d10336bf82aa74cd2a95c91388cb8b86c8cbd2`  
		Last Modified: Tue, 07 Sep 2021 20:23:36 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3929dea8cde2a8c168df44bab12475fece2ff2ad7a3a18ba505a9e9e1e84705`  
		Last Modified: Tue, 07 Sep 2021 20:23:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f55539abe84d550d6beb0b7616282c8a6a80bb37c98fa52f2ccd0cf38f8e35`  
		Last Modified: Tue, 07 Sep 2021 20:23:36 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65a6a197f958f1377eeb170c66127ad81e6658eb4afb37e34dd1ea29adc00969
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18399672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8230937f87367b64bce083b46594408cc94f1bc9eb3a30fe45a55c288e8c0a45`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:10:18 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 12 Nov 2021 17:10:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Fri, 12 Nov 2021 17:12:25 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Fri, 12 Nov 2021 17:12:27 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 12 Nov 2021 17:12:28 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 12 Nov 2021 17:12:28 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 12 Nov 2021 17:12:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 12 Nov 2021 17:12:29 GMT
ENV LD_PRELOAD=
# Fri, 12 Nov 2021 17:12:30 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Fri, 12 Nov 2021 17:12:30 GMT
EXPOSE 24224 5140
# Fri, 12 Nov 2021 17:12:30 GMT
USER fluent
# Fri, 12 Nov 2021 17:12:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 12 Nov 2021 17:12:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff475b9767d8c8b660254919cdacfb07d41726bcf6ae57bd82df1ab92964973`  
		Last Modified: Fri, 12 Nov 2021 17:13:19 GMT  
		Size: 15.8 MB (15764124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688a0000f32840ee0b24105fa7e0a8961a424e9cc972883a857a725d352294e0`  
		Last Modified: Fri, 12 Nov 2021 17:13:07 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bca9fcdd7bd010eb56f1658123023630d8a2feff9eb6e7dc663d84b97c1cac`  
		Last Modified: Fri, 12 Nov 2021 17:13:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cfca946685484b3ea43c9624c073dd8ae63bf180f0cbdba40ed2ed0a6d594c`  
		Last Modified: Fri, 12 Nov 2021 17:13:07 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:0feb9834b2a5fa548e44ef3df0d1660ae087593d5efbaa23bfcb105c499e7f17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18917798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d72b77133450207e1fe2573c8efd6843da74f6f2e9548548323f9473304edf6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 13 Oct 2021 18:02:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 13 Oct 2021 18:02:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 13 Oct 2021 18:03:26 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 13 Oct 2021 18:03:27 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 13 Oct 2021 18:03:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 13 Oct 2021 18:03:30 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 13 Oct 2021 18:03:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 13 Oct 2021 18:03:31 GMT
ENV LD_PRELOAD=
# Wed, 13 Oct 2021 18:03:32 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 13 Oct 2021 18:03:33 GMT
EXPOSE 24224 5140
# Wed, 13 Oct 2021 18:03:34 GMT
USER fluent
# Wed, 13 Oct 2021 18:03:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 13 Oct 2021 18:03:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031e4ef6f37192217ef5ea14313e0dcde48c78f017f299d23eea24bdb091e97f`  
		Last Modified: Wed, 13 Oct 2021 18:05:46 GMT  
		Size: 16.2 MB (16202633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5a8f29bddf5b67aacb989bc759ae4098ef74d6c11e8af2faca5551af655a98`  
		Last Modified: Wed, 13 Oct 2021 18:05:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26e5195aff116c7617d4339f7e3e98efc5ba17a7755ed3cbb583fe5ec1265fc`  
		Last Modified: Wed, 13 Oct 2021 18:05:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0334573a05aef20987ce376db4b6dfef8d6aa179f297062afc2d2e25a81d9be`  
		Last Modified: Wed, 13 Oct 2021 18:05:44 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:507bfb76f1e7f4cf106e82a22b8feca0ddeabec72d54018185c38b71d6cc2efd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18610135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4e08554bde9771b13000042d41d7ab6b4ba302562df1f2c438d82d54c905a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 20:38:57 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Sep 2021 20:38:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 07 Sep 2021 20:39:50 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 07 Sep 2021 20:39:51 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 07 Sep 2021 20:39:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 07 Sep 2021 20:39:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 07 Sep 2021 20:39:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Sep 2021 20:39:52 GMT
ENV LD_PRELOAD=
# Tue, 07 Sep 2021 20:39:52 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 07 Sep 2021 20:39:53 GMT
EXPOSE 24224 5140
# Tue, 07 Sep 2021 20:39:53 GMT
USER fluent
# Tue, 07 Sep 2021 20:39:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Sep 2021 20:39:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839ea22df0bc2e8d07e4813e30c7ca185a40ee3d13fa58743a31fa30a15af5bf`  
		Last Modified: Tue, 07 Sep 2021 20:42:12 GMT  
		Size: 15.8 MB (15786839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35a8cc0c8001d1c49febce49c713b8e5f6f003cece0be7bdaf0419e2770b57`  
		Last Modified: Tue, 07 Sep 2021 20:42:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848011ed348ffb82fd1282d2320030b9be8f3b2c6709a036772bff944b81c4b1`  
		Last Modified: Tue, 07 Sep 2021 20:42:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0b8201a679c29d06d372d77acf1764115098c283bb63a06cf78d792a96d81c`  
		Last Modified: Tue, 07 Sep 2021 20:42:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:aab9d909252af4256baec64f9fda57ce36dd0a75df59be1bb7a002f9c7219700
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19145994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cc52353d6416fa4e1d7d9d7427f578e3770d0b32fde1b259bd27d78e0ac544`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 01 Sep 2021 02:42:40 GMT
ADD file:07a51f1a2f818bd1c1651832ce63cb1e0046a57994724cda6a20ff1a2a685295 in / 
# Wed, 01 Sep 2021 02:42:41 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 20:16:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Sep 2021 20:16:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 07 Sep 2021 20:18:18 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 07 Sep 2021 20:18:33 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 07 Sep 2021 20:18:37 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 07 Sep 2021 20:18:42 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 07 Sep 2021 20:18:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Sep 2021 20:18:52 GMT
ENV LD_PRELOAD=
# Tue, 07 Sep 2021 20:18:56 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 07 Sep 2021 20:19:01 GMT
EXPOSE 24224 5140
# Tue, 07 Sep 2021 20:19:09 GMT
USER fluent
# Tue, 07 Sep 2021 20:19:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Sep 2021 20:19:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:39d9bf63205258fe1d085fd596101e6fc46ff796cda8d3ba2983e166a25b74db`  
		Last Modified: Wed, 01 Sep 2021 02:43:53 GMT  
		Size: 2.8 MB (2814813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214731170d95d46d51466ca736dcae549ca4cb2cd89ff7bb8834f08371cc830`  
		Last Modified: Tue, 07 Sep 2021 20:27:04 GMT  
		Size: 16.3 MB (16328974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b953a57f1c8b1d34fbdba7c739fc68549f8a4f848d0caff4cfe6489d90b94`  
		Last Modified: Tue, 07 Sep 2021 20:27:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cb3ad67c383333d29832f2970b813793e4aa74b50669b481cd80b19408ba78`  
		Last Modified: Tue, 07 Sep 2021 20:27:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb74a463295355bce6d358068c04bc86fbd2211f74a78be02e2f77300696707`  
		Last Modified: Tue, 07 Sep 2021 20:27:01 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:ead3e7fe4bae3c87994a3d55e2c4340d13b4807e6ab3ffd221bd7ecb8566b90d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18787715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5c8c592bac991df94d8370c013eec31e3d447a5a886f6b0d0516b3b92b1b79`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 01 Sep 2021 01:15:21 GMT
ADD file:def74c9e73d87d3c8b94cc0200f2723aea3a7462f8d2e0852db9da25c19855ac in / 
# Wed, 01 Sep 2021 01:15:22 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 20:41:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Sep 2021 20:41:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 07 Sep 2021 20:42:25 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 07 Sep 2021 20:42:28 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 07 Sep 2021 20:42:28 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 07 Sep 2021 20:42:29 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 07 Sep 2021 20:42:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Sep 2021 20:42:29 GMT
ENV LD_PRELOAD=
# Tue, 07 Sep 2021 20:42:30 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 07 Sep 2021 20:42:30 GMT
EXPOSE 24224 5140
# Tue, 07 Sep 2021 20:42:30 GMT
USER fluent
# Tue, 07 Sep 2021 20:42:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Sep 2021 20:42:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c1d78e8a87395f597d24b8eb78423ccdcfd404846906154e15aea8be9541c3ae`  
		Last Modified: Wed, 01 Sep 2021 01:16:19 GMT  
		Size: 2.6 MB (2604390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb52069d70b8339548c913c62816a1041e2b58492eed2ecafd0ebe8dfbd291`  
		Last Modified: Tue, 07 Sep 2021 20:45:06 GMT  
		Size: 16.2 MB (16181126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf205afdde7410ba47394a3fad5fed8e4973131a11c9363aa6b4b7ba3bc930a`  
		Last Modified: Tue, 07 Sep 2021 20:45:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3628a5e9b4e88cb3095f8b1042bfbde9c592dc862d157982d7e9130151466d5`  
		Last Modified: Tue, 07 Sep 2021 20:45:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf74414db9a2e48243f98b424ada7c935664a9bb7b25e633adb1738b50d6cd0`  
		Last Modified: Tue, 07 Sep 2021 20:45:03 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
