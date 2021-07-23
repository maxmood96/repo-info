<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.9-1`](#fluentdv19-1)
-	[`fluentd:v1.9-debian-1`](#fluentdv19-debian-1)
-	[`fluentd:v1.9.1-1.0`](#fluentdv191-10)
-	[`fluentd:v1.9.1-debian-1.0`](#fluentdv191-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:6c30754e8ed25a6326bbeb80b5293efba00992e23fdfe8ca6232ee914bb866a9
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
$ docker pull fluentd@sha256:3536d047aa7a961d8c826617282e8afa2075990c7e4be122a6501605ec5f3a8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15174420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84547e9c6cfe8be39cc6870d9b942554d48005ecf5cd2ba4156a3a380fa53a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 11:39:29 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 11:39:30 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 11:39:30 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 11:39:31 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 11:39:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 11:39:31 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 11:39:31 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 11:39:31 GMT
USER fluent
# Sat, 13 Mar 2021 11:39:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 11:39:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9651430fd06f066ea7cd1dde55009fe606a5c9357f60d2c418363f4c8d3e29d6`  
		Last Modified: Sat, 13 Mar 2021 11:41:13 GMT  
		Size: 12.4 MB (12398794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1eccd3574cb406400b237809e45a86e63983263d1f67e8887c6e89d31ef835`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cd5db2e3e2d262b39a393666a8efc9edb577b63c8f3934f23e7f16425cd4cd`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d18dcc36773b2d18dbe989da843efc8bee18a990bfd603d2a340174c3246af`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:44f31c1936eb1fb832ffab84cf23b98d016b2646cae11aaec96aef5939cd17e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15976216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021add57c37363fa0e7aa9dd21f7a3fe33da8e7e72cb09d25d866ddb6f3fd259`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:39:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 17:39:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 17:41:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 17:41:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 17:41:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 17:41:34 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 17:41:34 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 17:41:35 GMT
USER fluent
# Thu, 23 Apr 2020 17:41:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 17:41:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d522b01371d30767392094a66b629aa2f6a1cfeeb82ae15eeb64f931a1fa4b`  
		Last Modified: Thu, 23 Apr 2020 17:42:00 GMT  
		Size: 13.4 MB (13425275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad32a34e355514cb68abd5ee8454fa9b8f13c30395d005fccaa99434a30406e`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f703ee04ff8bd4f967972c80763171663ea5f1670044ebf18ff8273097c5c5`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24c5529dab1e5be1e7eec9c51d402281e9e72a5e13f9244a461073bca7241c`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:3ef9814c782a7e7cdc0268b47e590403c0321c4b9d1d66a0e7cacf59543f7754
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15099662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b88625287f0b6428b2072ca256feab07af6b5b01b58b6cd60fb45e108c12a4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 28 May 2021 15:35:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 28 May 2021 15:35:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 28 May 2021 15:36:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 28 May 2021 15:36:20 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 28 May 2021 15:36:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 28 May 2021 15:36:21 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 28 May 2021 15:36:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 28 May 2021 15:36:21 GMT
ENV LD_PRELOAD=
# Fri, 28 May 2021 15:36:21 GMT
EXPOSE 24224 5140
# Fri, 28 May 2021 15:36:21 GMT
USER fluent
# Fri, 28 May 2021 15:36:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 28 May 2021 15:36:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0858af0b4a7c5b26260974b4f76b1d3ff9dbdc88b08c57202e6575ac6928e562`  
		Last Modified: Fri, 28 May 2021 15:38:26 GMT  
		Size: 12.4 MB (12402980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850351b0271c72d09de3b8139370ed2b4e7f4611774d2f4896bbb22d45fd786`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c60c84ed38e3f0bf31854beaaa00b34eb733bbe0c94ffcb6ed4ad4531df6d87`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a053bf6b9a880e418f54c9dbd940e3e35398b7a02eddf8f09378fdab0b6d7500`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:2674458e5ee30b6811a635b030e7a5c02f09a60ac2b526e9233ae520b9e52d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6050199bd42bf9ce01c19ba5ea4ae473745e01fa2692be5d9603f3ab09958dc7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 04:53:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 04:53:03 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 04:53:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 04:53:05 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 04:53:05 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 04:53:06 GMT
USER fluent
# Sat, 13 Mar 2021 04:53:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 04:53:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86c3883d026d251c0b98f179473179adc48ddd9931c34671ec927485c2b30`  
		Last Modified: Sat, 13 Mar 2021 04:56:41 GMT  
		Size: 12.3 MB (12295016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdff586ec846debe504cab0d5418aed7a757990f1c2e5535febd3c2434383f9`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec361a5d42c106aff6fc935ed2b65a028307e9e2fee0160ec1d41376855b6969`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1fe75d1dda1ff8c1442a52d915e50e76400a2c2499c166340a71e5c9953409`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:925ec7b3db656179a9af649ecd7d460c382f83d67304675afedb1159e81c1980
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15626197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755cd8e04c80f0a9347682c54255141e4f127e51183e38a2242f2d11c8edcf2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 18:48:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 18:48:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 18:50:24 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 18:50:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 18:50:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 18:50:55 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 18:51:06 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 18:51:13 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 18:51:18 GMT
USER fluent
# Sun, 27 Jun 2021 18:51:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 18:51:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae0a9e68c3f4c3d3eef8c7882717f269e9eb77f3e51bd1a2592d777e5a4427`  
		Last Modified: Sun, 27 Jun 2021 19:00:34 GMT  
		Size: 12.8 MB (12836111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7920a62d83d64590cfc92eac07bfb198c34a84a7487d89d088dde583eb69738c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860be6886a328eed1f65ab57baf55366b67c34da0d78aba679ce67410fee056c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b79692d180ddfa6088bf602fee8e46e7e8843dd63d9783ff8e3aed0d9ff62`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:aea0285407ba5f065d490ed4425d92314b6f670d4db7bb1bbf78ae93fbbf8d66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15093638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227db6dba721583273f8ca5ae46885447b9b718b10050e2aa0607b5a4479872b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 11:58:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 11:58:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 11:58:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 11:58:32 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 11:58:33 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 11:58:33 GMT
USER fluent
# Sun, 27 Jun 2021 11:58:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 11:58:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4e4e2a782de008a6aae9ac5068ef04e51be2e395241f079c96708720aeaab`  
		Last Modified: Sun, 27 Jun 2021 12:00:54 GMT  
		Size: 12.5 MB (12541087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c87bf341b6629aa3298cb16a2134db8713c139b8e9fc51fe6ca115cf471ee`  
		Last Modified: Sun, 27 Jun 2021 12:00:53 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeceecc1ac6b27f1bce5dfbe45250c4fe5737e4411fb8c302dde72f38391645`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32a790b0e4bfd66ad1e75830473d2345e198aac4ca2bcc6b9a59f963f1a392e`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-1`

```console
$ docker pull fluentd@sha256:6c30754e8ed25a6326bbeb80b5293efba00992e23fdfe8ca6232ee914bb866a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9-1` - linux; amd64

```console
$ docker pull fluentd@sha256:3536d047aa7a961d8c826617282e8afa2075990c7e4be122a6501605ec5f3a8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15174420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84547e9c6cfe8be39cc6870d9b942554d48005ecf5cd2ba4156a3a380fa53a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 11:39:29 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 11:39:30 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 11:39:30 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 11:39:31 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 11:39:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 11:39:31 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 11:39:31 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 11:39:31 GMT
USER fluent
# Sat, 13 Mar 2021 11:39:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 11:39:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9651430fd06f066ea7cd1dde55009fe606a5c9357f60d2c418363f4c8d3e29d6`  
		Last Modified: Sat, 13 Mar 2021 11:41:13 GMT  
		Size: 12.4 MB (12398794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1eccd3574cb406400b237809e45a86e63983263d1f67e8887c6e89d31ef835`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cd5db2e3e2d262b39a393666a8efc9edb577b63c8f3934f23e7f16425cd4cd`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d18dcc36773b2d18dbe989da843efc8bee18a990bfd603d2a340174c3246af`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:44f31c1936eb1fb832ffab84cf23b98d016b2646cae11aaec96aef5939cd17e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15976216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021add57c37363fa0e7aa9dd21f7a3fe33da8e7e72cb09d25d866ddb6f3fd259`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:39:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 17:39:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 17:41:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 17:41:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 17:41:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 17:41:34 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 17:41:34 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 17:41:35 GMT
USER fluent
# Thu, 23 Apr 2020 17:41:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 17:41:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d522b01371d30767392094a66b629aa2f6a1cfeeb82ae15eeb64f931a1fa4b`  
		Last Modified: Thu, 23 Apr 2020 17:42:00 GMT  
		Size: 13.4 MB (13425275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad32a34e355514cb68abd5ee8454fa9b8f13c30395d005fccaa99434a30406e`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f703ee04ff8bd4f967972c80763171663ea5f1670044ebf18ff8273097c5c5`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24c5529dab1e5be1e7eec9c51d402281e9e72a5e13f9244a461073bca7241c`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:3ef9814c782a7e7cdc0268b47e590403c0321c4b9d1d66a0e7cacf59543f7754
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15099662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b88625287f0b6428b2072ca256feab07af6b5b01b58b6cd60fb45e108c12a4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 28 May 2021 15:35:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 28 May 2021 15:35:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 28 May 2021 15:36:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 28 May 2021 15:36:20 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 28 May 2021 15:36:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 28 May 2021 15:36:21 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 28 May 2021 15:36:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 28 May 2021 15:36:21 GMT
ENV LD_PRELOAD=
# Fri, 28 May 2021 15:36:21 GMT
EXPOSE 24224 5140
# Fri, 28 May 2021 15:36:21 GMT
USER fluent
# Fri, 28 May 2021 15:36:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 28 May 2021 15:36:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0858af0b4a7c5b26260974b4f76b1d3ff9dbdc88b08c57202e6575ac6928e562`  
		Last Modified: Fri, 28 May 2021 15:38:26 GMT  
		Size: 12.4 MB (12402980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850351b0271c72d09de3b8139370ed2b4e7f4611774d2f4896bbb22d45fd786`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c60c84ed38e3f0bf31854beaaa00b34eb733bbe0c94ffcb6ed4ad4531df6d87`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a053bf6b9a880e418f54c9dbd940e3e35398b7a02eddf8f09378fdab0b6d7500`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; 386

```console
$ docker pull fluentd@sha256:2674458e5ee30b6811a635b030e7a5c02f09a60ac2b526e9233ae520b9e52d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6050199bd42bf9ce01c19ba5ea4ae473745e01fa2692be5d9603f3ab09958dc7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 04:53:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 04:53:03 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 04:53:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 04:53:05 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 04:53:05 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 04:53:06 GMT
USER fluent
# Sat, 13 Mar 2021 04:53:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 04:53:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86c3883d026d251c0b98f179473179adc48ddd9931c34671ec927485c2b30`  
		Last Modified: Sat, 13 Mar 2021 04:56:41 GMT  
		Size: 12.3 MB (12295016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdff586ec846debe504cab0d5418aed7a757990f1c2e5535febd3c2434383f9`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec361a5d42c106aff6fc935ed2b65a028307e9e2fee0160ec1d41376855b6969`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1fe75d1dda1ff8c1442a52d915e50e76400a2c2499c166340a71e5c9953409`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:925ec7b3db656179a9af649ecd7d460c382f83d67304675afedb1159e81c1980
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15626197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755cd8e04c80f0a9347682c54255141e4f127e51183e38a2242f2d11c8edcf2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 18:48:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 18:48:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 18:50:24 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 18:50:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 18:50:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 18:50:55 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 18:51:06 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 18:51:13 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 18:51:18 GMT
USER fluent
# Sun, 27 Jun 2021 18:51:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 18:51:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae0a9e68c3f4c3d3eef8c7882717f269e9eb77f3e51bd1a2592d777e5a4427`  
		Last Modified: Sun, 27 Jun 2021 19:00:34 GMT  
		Size: 12.8 MB (12836111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7920a62d83d64590cfc92eac07bfb198c34a84a7487d89d088dde583eb69738c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860be6886a328eed1f65ab57baf55366b67c34da0d78aba679ce67410fee056c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b79692d180ddfa6088bf602fee8e46e7e8843dd63d9783ff8e3aed0d9ff62`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; s390x

```console
$ docker pull fluentd@sha256:aea0285407ba5f065d490ed4425d92314b6f670d4db7bb1bbf78ae93fbbf8d66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15093638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227db6dba721583273f8ca5ae46885447b9b718b10050e2aa0607b5a4479872b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 11:58:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 11:58:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 11:58:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 11:58:32 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 11:58:33 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 11:58:33 GMT
USER fluent
# Sun, 27 Jun 2021 11:58:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 11:58:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4e4e2a782de008a6aae9ac5068ef04e51be2e395241f079c96708720aeaab`  
		Last Modified: Sun, 27 Jun 2021 12:00:54 GMT  
		Size: 12.5 MB (12541087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c87bf341b6629aa3298cb16a2134db8713c139b8e9fc51fe6ca115cf471ee`  
		Last Modified: Sun, 27 Jun 2021 12:00:53 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeceecc1ac6b27f1bce5dfbe45250c4fe5737e4411fb8c302dde72f38391645`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32a790b0e4bfd66ad1e75830473d2345e198aac4ca2bcc6b9a59f963f1a392e`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-debian-1`

```console
$ docker pull fluentd@sha256:0d418c094397227445f3ff2e015ce8ba1dab5e611873d1705075be22b8487a89
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

### `fluentd:v1.9-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:50e8af57813bdaf1fcb2f640ec297ea801e8c6216045e0b9c7be7a9ab636a782
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82498240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4b0adc59a25fd1a60aa569969a7676e91046938ebff618d42d76c3a142a87b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 17:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 17:07:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 17:07:37 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 17:20:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 07 Jul 2021 19:55:24 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 07 Jul 2021 19:55:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 07 Jul 2021 19:59:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:59:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:59:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:59:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:59:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:59:30 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:37:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 07 Jul 2021 20:37:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 07 Jul 2021 20:37:20 GMT
ENV TINI_VERSION=0.18.0
# Wed, 07 Jul 2021 20:38:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 07 Jul 2021 20:38:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 07 Jul 2021 20:38:44 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 07 Jul 2021 20:38:44 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 07 Jul 2021 20:38:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 07 Jul 2021 20:38:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 07 Jul 2021 20:38:45 GMT
EXPOSE 24224 5140
# Wed, 07 Jul 2021 20:38:45 GMT
USER fluent
# Wed, 07 Jul 2021 20:38:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 07 Jul 2021 20:38:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8edb0654f16a0b0dfa9167e58fdc2d00d20e61f18f10d3e848418baf5bef4ab`  
		Last Modified: Wed, 23 Jun 2021 17:42:38 GMT  
		Size: 12.6 MB (12562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ba211d3249c13e0f844045a38f32ef8cce47229548262f3503816661e9af`  
		Last Modified: Wed, 23 Jun 2021 17:42:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bd4dd650c8621dab8128db8ca0e3f89acd9839366648234c17d3016f1bc8da`  
		Last Modified: Wed, 07 Jul 2021 20:20:53 GMT  
		Size: 21.5 MB (21467547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ad4efca5cc78409013778f13741b076a4217a9a2ff39f594ab9ac6bbe2a8`  
		Last Modified: Wed, 07 Jul 2021 20:20:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5c63f0d0b48895c2d8a041ffaff393965ef65b2c57b4afaeb31bc31943332a`  
		Last Modified: Wed, 07 Jul 2021 20:39:19 GMT  
		Size: 21.3 MB (21319081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ceda07a7783210fa4d3c002fd6c721fb0b2f2ffb7b93402974dd361b5d70e`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b23094e57bf985ee0dd9b82978d7046ed0dbeb4bbacbf9a1ad8466e1133f85c`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f95c7d868707b4ea38ebb508124a26a5ea4ff7a8593daadeb658ef149ccee3`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3cf174b45751bba25e64e246b1347f6ee7463ee7276504b1ac48f7a4f7b9efed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76441363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e217a5cbb4be6a6f01b26da78aad75dbb89631c1acfeadf7243d615e48324`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:09 GMT
ADD file:78d4ced31112d85490c684f350aceeebfc72a804262c7ad3e033257e3894f5c4 in / 
# Tue, 22 Jun 2021 23:50:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 13:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 13:06:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 13:06:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 13:26:59 GMT
ENV RUBY_MAJOR=2.6
# Wed, 07 Jul 2021 19:16:44 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 07 Jul 2021 19:16:45 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 20:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 20:29:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 20:29:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 20:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 20:29:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 20:29:03 GMT
CMD ["irb"]
# Thu, 08 Jul 2021 22:27:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 08 Jul 2021 22:27:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 08 Jul 2021 22:27:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 08 Jul 2021 22:31:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 08 Jul 2021 22:31:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 08 Jul 2021 22:31:17 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 08 Jul 2021 22:31:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 08 Jul 2021 22:31:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 08 Jul 2021 22:31:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 08 Jul 2021 22:31:19 GMT
EXPOSE 24224 5140
# Thu, 08 Jul 2021 22:31:19 GMT
USER fluent
# Thu, 08 Jul 2021 22:31:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 08 Jul 2021 22:31:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:532d6df30af5174ac6e1b379c32b8f464d44651ac060376a560c4a76a87704a7`  
		Last Modified: Wed, 23 Jun 2021 00:01:46 GMT  
		Size: 24.9 MB (24878945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b3ba0f03212caacd2191837bdac2f1a9abf399938b4020b315e4c6ea7ba0c7`  
		Last Modified: Wed, 23 Jun 2021 14:05:28 GMT  
		Size: 10.3 MB (10345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfab7796870f80c9db896239384ac194808f4ce5fab9f16ba155559772cc1e`  
		Last Modified: Wed, 23 Jun 2021 14:05:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7534381e53bd89c246e0ccb2c35dac17bf88c731c8d0526c63e59be51e884c`  
		Last Modified: Thu, 08 Jul 2021 20:44:48 GMT  
		Size: 20.7 MB (20733354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f2a9ffe5b789dd841f07056ea0122491118e78120d0f014d80085c602ab19c`  
		Last Modified: Thu, 08 Jul 2021 20:44:37 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53375448933745d1437697aa94de4f65ad7dd85cf0d12a5764f5f4039cc1f2ae`  
		Last Modified: Thu, 08 Jul 2021 22:32:03 GMT  
		Size: 20.5 MB (20480186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd2ce1c758b4f0514fc36ebc44892a9845629fc9f0ebc67a2df9bb310980a8`  
		Last Modified: Thu, 08 Jul 2021 22:31:49 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cdc90d57b4b04f88f5dfa42f67ee15e28e3137cfeb1c9ccc99010d684df1c0`  
		Last Modified: Thu, 08 Jul 2021 22:31:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ead428bd4ded189b1f5b87e09eee478183b5bd88394f2023b50204dd8e8b3`  
		Last Modified: Thu, 08 Jul 2021 22:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9235c6e70e486cac0a150cb183d629517bc4a810c17f3c2531dfcef8990b0b9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73647779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2223849c2403143d4b6910186c8ed64b9f4c2b3aaaed4c1a4a1a39716aeed88`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:31 GMT
ADD file:8d200a3bbe985ff355343675c5555852f27550a9e367969df6bc98034efb8fd4 in / 
# Wed, 23 Jun 2021 00:20:31 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 23:18:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 23:18:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 23:18:54 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 23:58:55 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 00:04:37 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 00:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:55:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:56:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:56:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:56:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:56:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:56:03 GMT
CMD ["irb"]
# Fri, 09 Jul 2021 04:01:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 09 Jul 2021 04:01:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 09 Jul 2021 04:01:41 GMT
ENV TINI_VERSION=0.18.0
# Fri, 09 Jul 2021 04:05:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 09 Jul 2021 04:05:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 09 Jul 2021 04:05:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 09 Jul 2021 04:05:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 09 Jul 2021 04:05:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 09 Jul 2021 04:05:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 09 Jul 2021 04:05:12 GMT
EXPOSE 24224 5140
# Fri, 09 Jul 2021 04:05:12 GMT
USER fluent
# Fri, 09 Jul 2021 04:05:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 09 Jul 2021 04:05:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8452be1adf00f91570fe21a8e61aaf4c12e014daf67d7de65d984f4e8ecca2f1`  
		Last Modified: Wed, 23 Jun 2021 00:31:49 GMT  
		Size: 22.7 MB (22746055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08b763290fb30bc16e505b4aa06ba1c3041182ac9bd8be48df5e94cbbe8545d`  
		Last Modified: Thu, 24 Jun 2021 00:49:52 GMT  
		Size: 9.9 MB (9872206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f611d0cebec7d01271526d00ff39f508174641d4e952ac4954fb89f368bf331`  
		Last Modified: Thu, 24 Jun 2021 00:49:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae3ab28fbce4cee595eb301139ed362bf539fc80d87e1203e0c2d53b9f30bd5`  
		Last Modified: Thu, 08 Jul 2021 23:21:22 GMT  
		Size: 20.6 MB (20643638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7253813058a0314e3fee8530b64e5f281a4697fd64c8d4f59d4d3c1e02f8b2`  
		Last Modified: Thu, 08 Jul 2021 23:21:13 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc18a211a0cca6c11802cffd13fdad743c24bfd4c334a8ccaad98172d9ec2896`  
		Last Modified: Fri, 09 Jul 2021 04:05:53 GMT  
		Size: 20.4 MB (20382811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34137f1b37968908d40479e6d67a978a416f2291f68e38100e1dfcae4ef788b`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d43ec4b79d73197faa62650842a01c6fa9b0a2346361a32ebb81223c6dfa29`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53744178b2807edafb8f5fb45cb8696552a6dff22eecff9e0f2ee5183f8a8ed0`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:c83b3bfbf8fec8f4208ba7f706c31652bbabba57e3ac3aa835f06c0e8c579eb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79827396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574d3523410b97677aa128cb6c513f1b754e5873fa77d2e739e53bb01979f0ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:36:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 12:36:23 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 12:45:29 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 12:45:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 12:45:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 12:47:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 12:47:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 12:47:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 12:47:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 12:47:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 12:47:36 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:08:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 Jul 2021 01:08:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 23 Jul 2021 01:08:35 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 Jul 2021 01:10:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 23 Jul 2021 01:10:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 23 Jul 2021 01:10:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 23 Jul 2021 01:10:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 23 Jul 2021 01:10:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 Jul 2021 01:10:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 Jul 2021 01:10:19 GMT
EXPOSE 24224 5140
# Fri, 23 Jul 2021 01:10:19 GMT
USER fluent
# Fri, 23 Jul 2021 01:10:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 Jul 2021 01:10:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a77364b6ec6cfc9422903e0f9d3f5cab5ee0ac4b62cfac6fc7c3d544ad7f57`  
		Last Modified: Thu, 22 Jul 2021 12:55:11 GMT  
		Size: 11.3 MB (11263053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68321ef048d82e4480bc2de1681a811f18b2e1d04b5aa9dec38030570eaa40`  
		Last Modified: Thu, 22 Jul 2021 12:55:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6319f6f39ac757356a2f054631df2eaa6a111934c0e9128d04df9f2296eef143`  
		Last Modified: Thu, 22 Jul 2021 12:57:16 GMT  
		Size: 21.3 MB (21308954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3246f58f273186efdfacba513b296257ca20afe8e09b07635bf20c90f80cc2eb`  
		Last Modified: Thu, 22 Jul 2021 12:57:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab3282f0fb48112a0effdd553644cac9a62479e329c809f90d29eb8edb1e86e`  
		Last Modified: Fri, 23 Jul 2021 01:10:51 GMT  
		Size: 21.3 MB (21337526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e667546acdbc1c28b869dd2490d127a9688c1563714695080163fd222b375033`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23323ada676d2a58b1324a6d2053a00334f5b9a6ab9e40d94d52cda23d655ca6`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca484b49fcadaf6b61eb57eeb8d4539ec27ae15c2dec2fc46c72c6ba021f91`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5d9286d609eb3c569e19819b553a38f5d7c56dfaa3c86d77c770acf17dd73030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86464108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676ac46428ece24c2bbfcc40027c5c2a9917cc1825fba756c6910f9f6e0fe9ed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:25:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 Jul 2021 00:25:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 23 Jul 2021 00:25:49 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 Jul 2021 00:28:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 23 Jul 2021 00:28:24 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 23 Jul 2021 00:28:25 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 23 Jul 2021 00:28:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 23 Jul 2021 00:28:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 Jul 2021 00:28:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 Jul 2021 00:28:27 GMT
EXPOSE 24224 5140
# Fri, 23 Jul 2021 00:28:27 GMT
USER fluent
# Fri, 23 Jul 2021 00:28:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 Jul 2021 00:28:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee986006d0a1514dc50f94c03a18a978cbb6f23f08f1b8dee2ae8d565754b639`  
		Last Modified: Fri, 23 Jul 2021 00:29:19 GMT  
		Size: 20.5 MB (20526184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7920af8104c552585562b5ac1c6c038ab50755907ff0961092d014530f3b3d37`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1912669ba82bd80883884327a2fbb14c9838155677dcd70bb817923817a564`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a730038d783f586952462aa6a745e03eeea75dd5505757af50c67922c40bc8`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4e3ff6b868060678c3c9b338c66ea64831177c561b3b45fb75a5183871400c2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87141526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24937a3b7450b29f4b23590f0453d62bf14526ad1d6d84375a87678f0557d63a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 09 Jul 2021 15:58:12 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Fri, 09 Jul 2021 15:58:14 GMT
CMD ["bash"]
# Sat, 10 Jul 2021 17:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Jul 2021 17:22:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Jul 2021 17:22:32 GMT
ENV LANG=C.UTF-8
# Sat, 10 Jul 2021 18:06:39 GMT
ENV RUBY_MAJOR=2.6
# Sat, 10 Jul 2021 18:06:44 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 10 Jul 2021 18:06:50 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 10 Jul 2021 18:17:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Jul 2021 18:17:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Jul 2021 18:17:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Jul 2021 18:17:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Jul 2021 18:17:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Jul 2021 18:17:54 GMT
CMD ["irb"]
# Sun, 11 Jul 2021 07:07:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 11 Jul 2021 07:07:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 11 Jul 2021 07:08:04 GMT
ENV TINI_VERSION=0.18.0
# Sun, 11 Jul 2021 07:17:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 11 Jul 2021 07:17:33 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 11 Jul 2021 07:17:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 11 Jul 2021 07:17:43 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 11 Jul 2021 07:17:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 11 Jul 2021 07:18:01 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 11 Jul 2021 07:18:10 GMT
EXPOSE 24224 5140
# Sun, 11 Jul 2021 07:18:13 GMT
USER fluent
# Sun, 11 Jul 2021 07:18:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 11 Jul 2021 07:18:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceba063dbcdd8aa55ec2183194edae6ea424d440c8c3c4ab57e29bdc8d30739f`  
		Last Modified: Sat, 10 Jul 2021 18:24:25 GMT  
		Size: 12.7 MB (12704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bed40ec71d6898df63835eb0d9463b4672fcb74c6d77594621b1a9d96089b`  
		Last Modified: Sat, 10 Jul 2021 18:24:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae8fcb5d02ee6d84244d4abd42aa33daa130c38c85615ab4a4d0874e18a3233`  
		Last Modified: Sat, 10 Jul 2021 18:26:36 GMT  
		Size: 22.0 MB (21985630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0cda1836341e17f7519b587492ca37a7b447a8d6bfd60379f598076d411808`  
		Last Modified: Sat, 10 Jul 2021 18:26:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33260f68026a2621389506634cd9b3e9ef5cff70cd022cfa160fc9adbde88154`  
		Last Modified: Sun, 11 Jul 2021 07:19:03 GMT  
		Size: 21.9 MB (21894810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f797f4c906fbc966a0327c26710cf166903c7e55b87a7ef9f35743f14e4fd9`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e7ff3624577bccc08b53882d95dfde9b26e7422b508039b0b2369c5d305914`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2208dd9bf4657a470d24c85597db3ad09cced8d0b1d59d2354113117437890eb`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8b8189d3268179136fbe534b8257594ef98c0d59f852f7c1321b7f69305be372
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79685762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6b271f25bbf2780c254b71b002ad0a5c11662ebf24ff08246ab8c6d0043d35`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 09 Jul 2021 02:50:32 GMT
ADD file:a53e5772eefa4592eeff989f279dcc870986db7207b419dc3ae61cae85fce41f in / 
# Fri, 09 Jul 2021 02:50:33 GMT
CMD ["bash"]
# Fri, 09 Jul 2021 03:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 03:56:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 09 Jul 2021 03:56:46 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jul 2021 04:25:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 09 Jul 2021 04:25:02 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 09 Jul 2021 04:25:02 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 09 Jul 2021 04:28:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 09 Jul 2021 04:28:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 09 Jul 2021 04:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 09 Jul 2021 04:28:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 04:28:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 09 Jul 2021 04:28:27 GMT
CMD ["irb"]
# Sat, 10 Jul 2021 03:55:02 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 10 Jul 2021 03:55:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 10 Jul 2021 03:55:03 GMT
ENV TINI_VERSION=0.18.0
# Sat, 10 Jul 2021 03:57:12 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 10 Jul 2021 03:57:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 10 Jul 2021 03:57:17 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 10 Jul 2021 03:57:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 10 Jul 2021 03:57:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 10 Jul 2021 03:57:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sat, 10 Jul 2021 03:57:19 GMT
EXPOSE 24224 5140
# Sat, 10 Jul 2021 03:57:20 GMT
USER fluent
# Sat, 10 Jul 2021 03:57:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 10 Jul 2021 03:57:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d08eb187b3111e87e1b138f7b93df64c5470da613a64d0adc804e17e12aed4dc`  
		Last Modified: Tue, 22 Jun 2021 23:45:45 GMT  
		Size: 25.8 MB (25760716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb0861b7843d74cdcb468db372740a5fbb65d1a7a489cd207e57603e23b308`  
		Last Modified: Fri, 09 Jul 2021 04:33:35 GMT  
		Size: 10.8 MB (10814494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5b9cde22299f5aa53f8d9540f770e1b6ab0e6223d1d106df86a5a071f8f3ec`  
		Last Modified: Fri, 09 Jul 2021 04:33:33 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c567400e82e0da61d3cd0628acf038b1f660df828736d747c5f078bf89f66f`  
		Last Modified: Fri, 09 Jul 2021 04:34:45 GMT  
		Size: 21.6 MB (21620064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267c98f7b0020a56c2dea2572a1386e898081dfbd1aa8e5c5c7b637234b6106c`  
		Last Modified: Fri, 09 Jul 2021 04:34:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309d252d6604d37ac2bf8689d1fc22693c5d2b2190f265fda5df0851de6a4fb3`  
		Last Modified: Sat, 10 Jul 2021 03:57:58 GMT  
		Size: 21.5 MB (21487405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125ac0abd2b02b029a1a7996a8a6e23dee7735ca79369f80bed132e63ad0e4c`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36804af8612a2f4b5e2d7a5c2d796eba46bab55d58a5cf47d2ce693cc0fc8de5`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c9f58ff02b3ce299a5749e2fed7e649930b05d8b337ba5c941f0569c876e3a`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-1.0`

```console
$ docker pull fluentd@sha256:6c30754e8ed25a6326bbeb80b5293efba00992e23fdfe8ca6232ee914bb866a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9.1-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:3536d047aa7a961d8c826617282e8afa2075990c7e4be122a6501605ec5f3a8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15174420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84547e9c6cfe8be39cc6870d9b942554d48005ecf5cd2ba4156a3a380fa53a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 11:38:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 11:39:29 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 11:39:30 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 11:39:30 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 11:39:31 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 11:39:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 11:39:31 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 11:39:31 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 11:39:31 GMT
USER fluent
# Sat, 13 Mar 2021 11:39:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 11:39:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9651430fd06f066ea7cd1dde55009fe606a5c9357f60d2c418363f4c8d3e29d6`  
		Last Modified: Sat, 13 Mar 2021 11:41:13 GMT  
		Size: 12.4 MB (12398794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1eccd3574cb406400b237809e45a86e63983263d1f67e8887c6e89d31ef835`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cd5db2e3e2d262b39a393666a8efc9edb577b63c8f3934f23e7f16425cd4cd`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d18dcc36773b2d18dbe989da843efc8bee18a990bfd603d2a340174c3246af`  
		Last Modified: Sat, 13 Mar 2021 11:41:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:44f31c1936eb1fb832ffab84cf23b98d016b2646cae11aaec96aef5939cd17e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15976216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021add57c37363fa0e7aa9dd21f7a3fe33da8e7e72cb09d25d866ddb6f3fd259`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:39:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 17:39:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 17:41:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 17:41:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 17:41:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 17:41:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 17:41:34 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 17:41:34 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 17:41:35 GMT
USER fluent
# Thu, 23 Apr 2020 17:41:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 17:41:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d522b01371d30767392094a66b629aa2f6a1cfeeb82ae15eeb64f931a1fa4b`  
		Last Modified: Thu, 23 Apr 2020 17:42:00 GMT  
		Size: 13.4 MB (13425275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad32a34e355514cb68abd5ee8454fa9b8f13c30395d005fccaa99434a30406e`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f703ee04ff8bd4f967972c80763171663ea5f1670044ebf18ff8273097c5c5`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24c5529dab1e5be1e7eec9c51d402281e9e72a5e13f9244a461073bca7241c`  
		Last Modified: Thu, 23 Apr 2020 17:41:55 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:3ef9814c782a7e7cdc0268b47e590403c0321c4b9d1d66a0e7cacf59543f7754
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15099662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b88625287f0b6428b2072ca256feab07af6b5b01b58b6cd60fb45e108c12a4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 28 May 2021 15:35:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 28 May 2021 15:35:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 28 May 2021 15:36:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 28 May 2021 15:36:20 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 28 May 2021 15:36:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 28 May 2021 15:36:21 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 28 May 2021 15:36:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 28 May 2021 15:36:21 GMT
ENV LD_PRELOAD=
# Fri, 28 May 2021 15:36:21 GMT
EXPOSE 24224 5140
# Fri, 28 May 2021 15:36:21 GMT
USER fluent
# Fri, 28 May 2021 15:36:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 28 May 2021 15:36:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0858af0b4a7c5b26260974b4f76b1d3ff9dbdc88b08c57202e6575ac6928e562`  
		Last Modified: Fri, 28 May 2021 15:38:26 GMT  
		Size: 12.4 MB (12402980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850351b0271c72d09de3b8139370ed2b4e7f4611774d2f4896bbb22d45fd786`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c60c84ed38e3f0bf31854beaaa00b34eb733bbe0c94ffcb6ed4ad4531df6d87`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a053bf6b9a880e418f54c9dbd940e3e35398b7a02eddf8f09378fdab0b6d7500`  
		Last Modified: Fri, 28 May 2021 15:38:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:2674458e5ee30b6811a635b030e7a5c02f09a60ac2b526e9233ae520b9e52d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6050199bd42bf9ce01c19ba5ea4ae473745e01fa2692be5d9603f3ab09958dc7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 13 Mar 2021 04:51:47 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 13 Mar 2021 04:53:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 13 Mar 2021 04:53:03 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 13 Mar 2021 04:53:04 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 13 Mar 2021 04:53:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 13 Mar 2021 04:53:05 GMT
ENV LD_PRELOAD=
# Sat, 13 Mar 2021 04:53:05 GMT
EXPOSE 24224 5140
# Sat, 13 Mar 2021 04:53:06 GMT
USER fluent
# Sat, 13 Mar 2021 04:53:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 13 Mar 2021 04:53:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a86c3883d026d251c0b98f179473179adc48ddd9931c34671ec927485c2b30`  
		Last Modified: Sat, 13 Mar 2021 04:56:41 GMT  
		Size: 12.3 MB (12295016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdff586ec846debe504cab0d5418aed7a757990f1c2e5535febd3c2434383f9`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec361a5d42c106aff6fc935ed2b65a028307e9e2fee0160ec1d41376855b6969`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1fe75d1dda1ff8c1442a52d915e50e76400a2c2499c166340a71e5c9953409`  
		Last Modified: Sat, 13 Mar 2021 04:56:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:925ec7b3db656179a9af649ecd7d460c382f83d67304675afedb1159e81c1980
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15626197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755cd8e04c80f0a9347682c54255141e4f127e51183e38a2242f2d11c8edcf2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 18:48:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 18:48:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 18:50:24 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 18:50:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 18:50:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 18:50:55 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 18:51:06 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 18:51:13 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 18:51:18 GMT
USER fluent
# Sun, 27 Jun 2021 18:51:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 18:51:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeae0a9e68c3f4c3d3eef8c7882717f269e9eb77f3e51bd1a2592d777e5a4427`  
		Last Modified: Sun, 27 Jun 2021 19:00:34 GMT  
		Size: 12.8 MB (12836111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7920a62d83d64590cfc92eac07bfb198c34a84a7487d89d088dde583eb69738c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860be6886a328eed1f65ab57baf55366b67c34da0d78aba679ce67410fee056c`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b79692d180ddfa6088bf602fee8e46e7e8843dd63d9783ff8e3aed0d9ff62`  
		Last Modified: Sun, 27 Jun 2021 19:00:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:aea0285407ba5f065d490ed4425d92314b6f670d4db7bb1bbf78ae93fbbf8d66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15093638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227db6dba721583273f8ca5ae46885447b9b718b10050e2aa0607b5a4479872b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 27 Jun 2021 11:57:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 27 Jun 2021 11:58:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 27 Jun 2021 11:58:31 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 27 Jun 2021 11:58:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 27 Jun 2021 11:58:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 27 Jun 2021 11:58:32 GMT
ENV LD_PRELOAD=
# Sun, 27 Jun 2021 11:58:33 GMT
EXPOSE 24224 5140
# Sun, 27 Jun 2021 11:58:33 GMT
USER fluent
# Sun, 27 Jun 2021 11:58:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 27 Jun 2021 11:58:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd4e4e2a782de008a6aae9ac5068ef04e51be2e395241f079c96708720aeaab`  
		Last Modified: Sun, 27 Jun 2021 12:00:54 GMT  
		Size: 12.5 MB (12541087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c87bf341b6629aa3298cb16a2134db8713c139b8e9fc51fe6ca115cf471ee`  
		Last Modified: Sun, 27 Jun 2021 12:00:53 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeceecc1ac6b27f1bce5dfbe45250c4fe5737e4411fb8c302dde72f38391645`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32a790b0e4bfd66ad1e75830473d2345e198aac4ca2bcc6b9a59f963f1a392e`  
		Last Modified: Sun, 27 Jun 2021 12:00:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-debian-1.0`

```console
$ docker pull fluentd@sha256:0d418c094397227445f3ff2e015ce8ba1dab5e611873d1705075be22b8487a89
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

### `fluentd:v1.9.1-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:50e8af57813bdaf1fcb2f640ec297ea801e8c6216045e0b9c7be7a9ab636a782
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82498240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4b0adc59a25fd1a60aa569969a7676e91046938ebff618d42d76c3a142a87b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 17:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 17:07:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 17:07:37 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 17:20:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 07 Jul 2021 19:55:24 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 07 Jul 2021 19:55:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 07 Jul 2021 19:59:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:59:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:59:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:59:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:59:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:59:30 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:37:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 07 Jul 2021 20:37:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 07 Jul 2021 20:37:20 GMT
ENV TINI_VERSION=0.18.0
# Wed, 07 Jul 2021 20:38:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 07 Jul 2021 20:38:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 07 Jul 2021 20:38:44 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 07 Jul 2021 20:38:44 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 07 Jul 2021 20:38:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 07 Jul 2021 20:38:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 07 Jul 2021 20:38:45 GMT
EXPOSE 24224 5140
# Wed, 07 Jul 2021 20:38:45 GMT
USER fluent
# Wed, 07 Jul 2021 20:38:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 07 Jul 2021 20:38:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8edb0654f16a0b0dfa9167e58fdc2d00d20e61f18f10d3e848418baf5bef4ab`  
		Last Modified: Wed, 23 Jun 2021 17:42:38 GMT  
		Size: 12.6 MB (12562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ba211d3249c13e0f844045a38f32ef8cce47229548262f3503816661e9af`  
		Last Modified: Wed, 23 Jun 2021 17:42:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bd4dd650c8621dab8128db8ca0e3f89acd9839366648234c17d3016f1bc8da`  
		Last Modified: Wed, 07 Jul 2021 20:20:53 GMT  
		Size: 21.5 MB (21467547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ad4efca5cc78409013778f13741b076a4217a9a2ff39f594ab9ac6bbe2a8`  
		Last Modified: Wed, 07 Jul 2021 20:20:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5c63f0d0b48895c2d8a041ffaff393965ef65b2c57b4afaeb31bc31943332a`  
		Last Modified: Wed, 07 Jul 2021 20:39:19 GMT  
		Size: 21.3 MB (21319081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ceda07a7783210fa4d3c002fd6c721fb0b2f2ffb7b93402974dd361b5d70e`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b23094e57bf985ee0dd9b82978d7046ed0dbeb4bbacbf9a1ad8466e1133f85c`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f95c7d868707b4ea38ebb508124a26a5ea4ff7a8593daadeb658ef149ccee3`  
		Last Modified: Wed, 07 Jul 2021 20:39:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3cf174b45751bba25e64e246b1347f6ee7463ee7276504b1ac48f7a4f7b9efed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76441363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e217a5cbb4be6a6f01b26da78aad75dbb89631c1acfeadf7243d615e48324`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:09 GMT
ADD file:78d4ced31112d85490c684f350aceeebfc72a804262c7ad3e033257e3894f5c4 in / 
# Tue, 22 Jun 2021 23:50:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 13:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 13:06:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 13:06:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 13:26:59 GMT
ENV RUBY_MAJOR=2.6
# Wed, 07 Jul 2021 19:16:44 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 07 Jul 2021 19:16:45 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 20:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 20:29:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 20:29:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 20:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 20:29:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 20:29:03 GMT
CMD ["irb"]
# Thu, 08 Jul 2021 22:27:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 08 Jul 2021 22:27:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 08 Jul 2021 22:27:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 08 Jul 2021 22:31:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 08 Jul 2021 22:31:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 08 Jul 2021 22:31:17 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 08 Jul 2021 22:31:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 08 Jul 2021 22:31:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 08 Jul 2021 22:31:18 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 08 Jul 2021 22:31:19 GMT
EXPOSE 24224 5140
# Thu, 08 Jul 2021 22:31:19 GMT
USER fluent
# Thu, 08 Jul 2021 22:31:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 08 Jul 2021 22:31:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:532d6df30af5174ac6e1b379c32b8f464d44651ac060376a560c4a76a87704a7`  
		Last Modified: Wed, 23 Jun 2021 00:01:46 GMT  
		Size: 24.9 MB (24878945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b3ba0f03212caacd2191837bdac2f1a9abf399938b4020b315e4c6ea7ba0c7`  
		Last Modified: Wed, 23 Jun 2021 14:05:28 GMT  
		Size: 10.3 MB (10345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfab7796870f80c9db896239384ac194808f4ce5fab9f16ba155559772cc1e`  
		Last Modified: Wed, 23 Jun 2021 14:05:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7534381e53bd89c246e0ccb2c35dac17bf88c731c8d0526c63e59be51e884c`  
		Last Modified: Thu, 08 Jul 2021 20:44:48 GMT  
		Size: 20.7 MB (20733354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f2a9ffe5b789dd841f07056ea0122491118e78120d0f014d80085c602ab19c`  
		Last Modified: Thu, 08 Jul 2021 20:44:37 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53375448933745d1437697aa94de4f65ad7dd85cf0d12a5764f5f4039cc1f2ae`  
		Last Modified: Thu, 08 Jul 2021 22:32:03 GMT  
		Size: 20.5 MB (20480186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd2ce1c758b4f0514fc36ebc44892a9845629fc9f0ebc67a2df9bb310980a8`  
		Last Modified: Thu, 08 Jul 2021 22:31:49 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cdc90d57b4b04f88f5dfa42f67ee15e28e3137cfeb1c9ccc99010d684df1c0`  
		Last Modified: Thu, 08 Jul 2021 22:31:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ead428bd4ded189b1f5b87e09eee478183b5bd88394f2023b50204dd8e8b3`  
		Last Modified: Thu, 08 Jul 2021 22:31:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:9235c6e70e486cac0a150cb183d629517bc4a810c17f3c2531dfcef8990b0b9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73647779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2223849c2403143d4b6910186c8ed64b9f4c2b3aaaed4c1a4a1a39716aeed88`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:31 GMT
ADD file:8d200a3bbe985ff355343675c5555852f27550a9e367969df6bc98034efb8fd4 in / 
# Wed, 23 Jun 2021 00:20:31 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 23:18:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 23:18:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 23:18:54 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 23:58:55 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 00:04:37 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 00:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:55:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:56:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:56:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:56:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:56:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:56:03 GMT
CMD ["irb"]
# Fri, 09 Jul 2021 04:01:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 09 Jul 2021 04:01:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 09 Jul 2021 04:01:41 GMT
ENV TINI_VERSION=0.18.0
# Fri, 09 Jul 2021 04:05:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 09 Jul 2021 04:05:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 09 Jul 2021 04:05:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 09 Jul 2021 04:05:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 09 Jul 2021 04:05:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 09 Jul 2021 04:05:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 09 Jul 2021 04:05:12 GMT
EXPOSE 24224 5140
# Fri, 09 Jul 2021 04:05:12 GMT
USER fluent
# Fri, 09 Jul 2021 04:05:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 09 Jul 2021 04:05:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8452be1adf00f91570fe21a8e61aaf4c12e014daf67d7de65d984f4e8ecca2f1`  
		Last Modified: Wed, 23 Jun 2021 00:31:49 GMT  
		Size: 22.7 MB (22746055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08b763290fb30bc16e505b4aa06ba1c3041182ac9bd8be48df5e94cbbe8545d`  
		Last Modified: Thu, 24 Jun 2021 00:49:52 GMT  
		Size: 9.9 MB (9872206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f611d0cebec7d01271526d00ff39f508174641d4e952ac4954fb89f368bf331`  
		Last Modified: Thu, 24 Jun 2021 00:49:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae3ab28fbce4cee595eb301139ed362bf539fc80d87e1203e0c2d53b9f30bd5`  
		Last Modified: Thu, 08 Jul 2021 23:21:22 GMT  
		Size: 20.6 MB (20643638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7253813058a0314e3fee8530b64e5f281a4697fd64c8d4f59d4d3c1e02f8b2`  
		Last Modified: Thu, 08 Jul 2021 23:21:13 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc18a211a0cca6c11802cffd13fdad743c24bfd4c334a8ccaad98172d9ec2896`  
		Last Modified: Fri, 09 Jul 2021 04:05:53 GMT  
		Size: 20.4 MB (20382811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34137f1b37968908d40479e6d67a978a416f2291f68e38100e1dfcae4ef788b`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d43ec4b79d73197faa62650842a01c6fa9b0a2346361a32ebb81223c6dfa29`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53744178b2807edafb8f5fb45cb8696552a6dff22eecff9e0f2ee5183f8a8ed0`  
		Last Modified: Fri, 09 Jul 2021 04:05:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:c83b3bfbf8fec8f4208ba7f706c31652bbabba57e3ac3aa835f06c0e8c579eb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79827396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574d3523410b97677aa128cb6c513f1b754e5873fa77d2e739e53bb01979f0ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:36:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 12:36:23 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 12:45:29 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 12:45:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 12:45:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 12:47:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 12:47:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 12:47:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 12:47:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 12:47:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 12:47:36 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:08:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 Jul 2021 01:08:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 23 Jul 2021 01:08:35 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 Jul 2021 01:10:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 23 Jul 2021 01:10:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 23 Jul 2021 01:10:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 23 Jul 2021 01:10:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 23 Jul 2021 01:10:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 Jul 2021 01:10:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 Jul 2021 01:10:19 GMT
EXPOSE 24224 5140
# Fri, 23 Jul 2021 01:10:19 GMT
USER fluent
# Fri, 23 Jul 2021 01:10:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 Jul 2021 01:10:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a77364b6ec6cfc9422903e0f9d3f5cab5ee0ac4b62cfac6fc7c3d544ad7f57`  
		Last Modified: Thu, 22 Jul 2021 12:55:11 GMT  
		Size: 11.3 MB (11263053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68321ef048d82e4480bc2de1681a811f18b2e1d04b5aa9dec38030570eaa40`  
		Last Modified: Thu, 22 Jul 2021 12:55:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6319f6f39ac757356a2f054631df2eaa6a111934c0e9128d04df9f2296eef143`  
		Last Modified: Thu, 22 Jul 2021 12:57:16 GMT  
		Size: 21.3 MB (21308954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3246f58f273186efdfacba513b296257ca20afe8e09b07635bf20c90f80cc2eb`  
		Last Modified: Thu, 22 Jul 2021 12:57:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab3282f0fb48112a0effdd553644cac9a62479e329c809f90d29eb8edb1e86e`  
		Last Modified: Fri, 23 Jul 2021 01:10:51 GMT  
		Size: 21.3 MB (21337526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e667546acdbc1c28b869dd2490d127a9688c1563714695080163fd222b375033`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23323ada676d2a58b1324a6d2053a00334f5b9a6ab9e40d94d52cda23d655ca6`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca484b49fcadaf6b61eb57eeb8d4539ec27ae15c2dec2fc46c72c6ba021f91`  
		Last Modified: Fri, 23 Jul 2021 01:10:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5d9286d609eb3c569e19819b553a38f5d7c56dfaa3c86d77c770acf17dd73030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86464108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676ac46428ece24c2bbfcc40027c5c2a9917cc1825fba756c6910f9f6e0fe9ed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:25:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 Jul 2021 00:25:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 23 Jul 2021 00:25:49 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 Jul 2021 00:28:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 23 Jul 2021 00:28:24 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 23 Jul 2021 00:28:25 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 23 Jul 2021 00:28:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 23 Jul 2021 00:28:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 Jul 2021 00:28:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 Jul 2021 00:28:27 GMT
EXPOSE 24224 5140
# Fri, 23 Jul 2021 00:28:27 GMT
USER fluent
# Fri, 23 Jul 2021 00:28:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 Jul 2021 00:28:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee986006d0a1514dc50f94c03a18a978cbb6f23f08f1b8dee2ae8d565754b639`  
		Last Modified: Fri, 23 Jul 2021 00:29:19 GMT  
		Size: 20.5 MB (20526184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7920af8104c552585562b5ac1c6c038ab50755907ff0961092d014530f3b3d37`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1912669ba82bd80883884327a2fbb14c9838155677dcd70bb817923817a564`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a730038d783f586952462aa6a745e03eeea75dd5505757af50c67922c40bc8`  
		Last Modified: Fri, 23 Jul 2021 00:29:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4e3ff6b868060678c3c9b338c66ea64831177c561b3b45fb75a5183871400c2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87141526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24937a3b7450b29f4b23590f0453d62bf14526ad1d6d84375a87678f0557d63a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 09 Jul 2021 15:58:12 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Fri, 09 Jul 2021 15:58:14 GMT
CMD ["bash"]
# Sat, 10 Jul 2021 17:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Jul 2021 17:22:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 10 Jul 2021 17:22:32 GMT
ENV LANG=C.UTF-8
# Sat, 10 Jul 2021 18:06:39 GMT
ENV RUBY_MAJOR=2.6
# Sat, 10 Jul 2021 18:06:44 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 10 Jul 2021 18:06:50 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 10 Jul 2021 18:17:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 10 Jul 2021 18:17:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 10 Jul 2021 18:17:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 10 Jul 2021 18:17:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Jul 2021 18:17:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 10 Jul 2021 18:17:54 GMT
CMD ["irb"]
# Sun, 11 Jul 2021 07:07:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 11 Jul 2021 07:07:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sun, 11 Jul 2021 07:08:04 GMT
ENV TINI_VERSION=0.18.0
# Sun, 11 Jul 2021 07:17:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sun, 11 Jul 2021 07:17:33 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sun, 11 Jul 2021 07:17:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sun, 11 Jul 2021 07:17:43 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sun, 11 Jul 2021 07:17:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 11 Jul 2021 07:18:01 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 11 Jul 2021 07:18:10 GMT
EXPOSE 24224 5140
# Sun, 11 Jul 2021 07:18:13 GMT
USER fluent
# Sun, 11 Jul 2021 07:18:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 11 Jul 2021 07:18:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceba063dbcdd8aa55ec2183194edae6ea424d440c8c3c4ab57e29bdc8d30739f`  
		Last Modified: Sat, 10 Jul 2021 18:24:25 GMT  
		Size: 12.7 MB (12704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bed40ec71d6898df63835eb0d9463b4672fcb74c6d77594621b1a9d96089b`  
		Last Modified: Sat, 10 Jul 2021 18:24:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae8fcb5d02ee6d84244d4abd42aa33daa130c38c85615ab4a4d0874e18a3233`  
		Last Modified: Sat, 10 Jul 2021 18:26:36 GMT  
		Size: 22.0 MB (21985630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0cda1836341e17f7519b587492ca37a7b447a8d6bfd60379f598076d411808`  
		Last Modified: Sat, 10 Jul 2021 18:26:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33260f68026a2621389506634cd9b3e9ef5cff70cd022cfa160fc9adbde88154`  
		Last Modified: Sun, 11 Jul 2021 07:19:03 GMT  
		Size: 21.9 MB (21894810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f797f4c906fbc966a0327c26710cf166903c7e55b87a7ef9f35743f14e4fd9`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e7ff3624577bccc08b53882d95dfde9b26e7422b508039b0b2369c5d305914`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2208dd9bf4657a470d24c85597db3ad09cced8d0b1d59d2354113117437890eb`  
		Last Modified: Sun, 11 Jul 2021 07:18:58 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8b8189d3268179136fbe534b8257594ef98c0d59f852f7c1321b7f69305be372
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79685762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6b271f25bbf2780c254b71b002ad0a5c11662ebf24ff08246ab8c6d0043d35`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 09 Jul 2021 02:50:32 GMT
ADD file:a53e5772eefa4592eeff989f279dcc870986db7207b419dc3ae61cae85fce41f in / 
# Fri, 09 Jul 2021 02:50:33 GMT
CMD ["bash"]
# Fri, 09 Jul 2021 03:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 03:56:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 09 Jul 2021 03:56:46 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jul 2021 04:25:01 GMT
ENV RUBY_MAJOR=2.6
# Fri, 09 Jul 2021 04:25:02 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 09 Jul 2021 04:25:02 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 09 Jul 2021 04:28:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 09 Jul 2021 04:28:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 09 Jul 2021 04:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 09 Jul 2021 04:28:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 04:28:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 09 Jul 2021 04:28:27 GMT
CMD ["irb"]
# Sat, 10 Jul 2021 03:55:02 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sat, 10 Jul 2021 03:55:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Sat, 10 Jul 2021 03:55:03 GMT
ENV TINI_VERSION=0.18.0
# Sat, 10 Jul 2021 03:57:12 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Sat, 10 Jul 2021 03:57:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Sat, 10 Jul 2021 03:57:17 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Sat, 10 Jul 2021 03:57:18 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Sat, 10 Jul 2021 03:57:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Sat, 10 Jul 2021 03:57:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sat, 10 Jul 2021 03:57:19 GMT
EXPOSE 24224 5140
# Sat, 10 Jul 2021 03:57:20 GMT
USER fluent
# Sat, 10 Jul 2021 03:57:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sat, 10 Jul 2021 03:57:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d08eb187b3111e87e1b138f7b93df64c5470da613a64d0adc804e17e12aed4dc`  
		Last Modified: Tue, 22 Jun 2021 23:45:45 GMT  
		Size: 25.8 MB (25760716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb0861b7843d74cdcb468db372740a5fbb65d1a7a489cd207e57603e23b308`  
		Last Modified: Fri, 09 Jul 2021 04:33:35 GMT  
		Size: 10.8 MB (10814494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5b9cde22299f5aa53f8d9540f770e1b6ab0e6223d1d106df86a5a071f8f3ec`  
		Last Modified: Fri, 09 Jul 2021 04:33:33 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c567400e82e0da61d3cd0628acf038b1f660df828736d747c5f078bf89f66f`  
		Last Modified: Fri, 09 Jul 2021 04:34:45 GMT  
		Size: 21.6 MB (21620064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267c98f7b0020a56c2dea2572a1386e898081dfbd1aa8e5c5c7b637234b6106c`  
		Last Modified: Fri, 09 Jul 2021 04:34:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309d252d6604d37ac2bf8689d1fc22693c5d2b2190f265fda5df0851de6a4fb3`  
		Last Modified: Sat, 10 Jul 2021 03:57:58 GMT  
		Size: 21.5 MB (21487405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125ac0abd2b02b029a1a7996a8a6e23dee7735ca79369f80bed132e63ad0e4c`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36804af8612a2f4b5e2d7a5c2d796eba46bab55d58a5cf47d2ce693cc0fc8de5`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c9f58ff02b3ce299a5749e2fed7e649930b05d8b337ba5c941f0569c876e3a`  
		Last Modified: Sat, 10 Jul 2021 03:57:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
