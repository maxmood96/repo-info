<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.9-1`](#fluentdv19-1)
-	[`fluentd:v1.9.1-1.0`](#fluentdv191-10)
-	[`fluentd:v1.9.1-debian-1.0`](#fluentdv191-debian-10)
-	[`fluentd:v1.9-debian-1`](#fluentdv19-debian-1)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:af335887b3a1c7f23b2d54aba84a7c4e0cddd50e70d18ee5a4feb281133bf608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:b0136e1ac811a9bc03d2af9049acc8dccc5b891fe3d4bd08798ae3511ec81103
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16531173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77776ad237484ae2ba463aa4246f529828e3a7dae22f59328fb310ca0d3591`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:23:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 13:23:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 13:23:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 13:23:53 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 13:23:54 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 13:23:54 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 13:23:54 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 13:23:55 GMT
USER fluent
# Fri, 24 Apr 2020 13:23:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 13:23:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58109e9b1ba0d634974981e1f60a467213412df52e63c2e0810a0e12bfd92a15`  
		Last Modified: Fri, 24 Apr 2020 13:25:56 GMT  
		Size: 13.8 MB (13755597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678a9500d8f0582867bfbfeeca06fafa14fc99c60d195dc4ff8982194a5a2b7b`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93abfddd6b877c4887a4bc98b9858a2224d45b266db8698704bdffd3e505844c`  
		Last Modified: Fri, 24 Apr 2020 13:25:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eca423c53486a28c557132cc9f38051b64967ceac115bdc32dc2cf670599150`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
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
$ docker pull fluentd@sha256:9a3af653771a6a04c358f7c2a60b8bb57c64d3de5dd298c0d4657ceb35ea0f66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16449859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62a0ca09e6cfbf89d9db9d526962faa229e3de5ec48e9ef934e8566431b4c9d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:05:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 09:05:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 09:06:41 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 09:06:45 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 09:06:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 09:06:48 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 09:06:48 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 09:06:49 GMT
USER fluent
# Fri, 24 Apr 2020 09:06:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 09:06:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7c433500fac88cd265a112da6bb53517cca36634a766db54f966da1f64e6ae`  
		Last Modified: Fri, 24 Apr 2020 09:07:26 GMT  
		Size: 13.8 MB (13753176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcba662d9a25425bd9d1fd78c25999719742ab37190f21b0228c999766407978`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a458dc4b98ef9ffa86fcd837c55416fd16fee3a6154a3e1f38011c7dad2a51`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0293d533db263a29c969b1f2ca4ef1c0df2bbfe728041795f264b905641d6009`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:c0c904864ac5d726fc15c7cdb7b8d67a1f22886deaebd1866846350eb8790b7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16431173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53efeb733ffb3b78b1ef4a7016222c61969cd70e411e9d45dd1c5491f69dd816`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 04:29:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 04:29:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 04:29:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 04:29:53 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 04:29:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 04:29:53 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 04:29:53 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 04:29:53 GMT
USER fluent
# Fri, 24 Apr 2020 04:29:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 04:29:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7374d1118539f8cf16f7ad0d1ecc12433d5e0ac9d266240c79fe9a0cef6a6e53`  
		Last Modified: Fri, 24 Apr 2020 04:30:15 GMT  
		Size: 13.7 MB (13659274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d96f8829ce290acf10dbe54f9301927a2550a63c9cc65b71d637bf23ececafb`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f44bc85b96f853ae9bba560eb64dfb9cdbf63f9b3ae81c8cd4fcc231643c792`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9aa3a6d42037036e91d7173f9964bb6ff7f5dc820e9244d9a1d8be06697e3c`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:624655b564b9a0d8aff2adb11bc4e4ab152cc6cddbb0f80dbec0ccc280a6c7e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16969348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996e3889db7f499cb26285f39e7577a3572c8c83eefb66472ac0e3d67d6c9f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:52:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 02:52:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 02:53:15 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 02:53:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 02:53:21 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 02:53:22 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 02:53:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 02:53:26 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 02:53:27 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 02:53:29 GMT
USER fluent
# Fri, 24 Apr 2020 02:53:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 02:53:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27df74a3decbbc71f688e8319c7055315cbba6b350b28324d4ad9c021ca50135`  
		Last Modified: Fri, 24 Apr 2020 02:54:03 GMT  
		Size: 14.2 MB (14179267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465abcf9b778cb4d299d4fec3ccbd1b1284867a62dc8b6d6d59a7a195cc0203`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b323e14271e2cf6ac4ee482e207353aa39585d4e58bf75475fe54e2a7f1fdb65`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a13af9e734338dbe7adf7de4ab71210d13beaeed6a6fec5d7b9a7b4dff17131`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:12f970948d5704cc42194be7cbfd8fe038e802f8fc2fb8f2169bf7c4c2c5eb5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6e3f25bb06297f8b35538b6b7a44d6c0ce04bfa379393397e3eef1c4c16e9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 20:00:12 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 20:00:14 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 20:00:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 20:00:14 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 20:00:15 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 20:00:15 GMT
USER fluent
# Thu, 23 Apr 2020 20:00:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 20:00:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84a8d1f46d684e96854f17f7222edf696d71cf5cd842954e92f378e005dab17`  
		Last Modified: Thu, 23 Apr 2020 20:00:33 GMT  
		Size: 13.9 MB (13889338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52edf66127670c83c7f5a2aed5e38db5dca87e51eb8966174df5900dc2e0c9`  
		Last Modified: Thu, 23 Apr 2020 20:00:30 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec06b392ce74e92be850c3ddc84f05a6f54ed80e3920a6da6d4327a8d62b5137`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d063c86f8d64af1ad29498f54a054870ec143617b700e0f374dd7a023214ef43`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-1`

```console
$ docker pull fluentd@sha256:af335887b3a1c7f23b2d54aba84a7c4e0cddd50e70d18ee5a4feb281133bf608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9-1` - linux; amd64

```console
$ docker pull fluentd@sha256:b0136e1ac811a9bc03d2af9049acc8dccc5b891fe3d4bd08798ae3511ec81103
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16531173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77776ad237484ae2ba463aa4246f529828e3a7dae22f59328fb310ca0d3591`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:23:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 13:23:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 13:23:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 13:23:53 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 13:23:54 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 13:23:54 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 13:23:54 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 13:23:55 GMT
USER fluent
# Fri, 24 Apr 2020 13:23:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 13:23:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58109e9b1ba0d634974981e1f60a467213412df52e63c2e0810a0e12bfd92a15`  
		Last Modified: Fri, 24 Apr 2020 13:25:56 GMT  
		Size: 13.8 MB (13755597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678a9500d8f0582867bfbfeeca06fafa14fc99c60d195dc4ff8982194a5a2b7b`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93abfddd6b877c4887a4bc98b9858a2224d45b266db8698704bdffd3e505844c`  
		Last Modified: Fri, 24 Apr 2020 13:25:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eca423c53486a28c557132cc9f38051b64967ceac115bdc32dc2cf670599150`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
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
$ docker pull fluentd@sha256:9a3af653771a6a04c358f7c2a60b8bb57c64d3de5dd298c0d4657ceb35ea0f66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16449859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62a0ca09e6cfbf89d9db9d526962faa229e3de5ec48e9ef934e8566431b4c9d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:05:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 09:05:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 09:06:41 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 09:06:45 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 09:06:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 09:06:48 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 09:06:48 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 09:06:49 GMT
USER fluent
# Fri, 24 Apr 2020 09:06:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 09:06:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7c433500fac88cd265a112da6bb53517cca36634a766db54f966da1f64e6ae`  
		Last Modified: Fri, 24 Apr 2020 09:07:26 GMT  
		Size: 13.8 MB (13753176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcba662d9a25425bd9d1fd78c25999719742ab37190f21b0228c999766407978`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a458dc4b98ef9ffa86fcd837c55416fd16fee3a6154a3e1f38011c7dad2a51`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0293d533db263a29c969b1f2ca4ef1c0df2bbfe728041795f264b905641d6009`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; 386

```console
$ docker pull fluentd@sha256:c0c904864ac5d726fc15c7cdb7b8d67a1f22886deaebd1866846350eb8790b7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16431173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53efeb733ffb3b78b1ef4a7016222c61969cd70e411e9d45dd1c5491f69dd816`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 04:29:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 04:29:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 04:29:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 04:29:53 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 04:29:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 04:29:53 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 04:29:53 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 04:29:53 GMT
USER fluent
# Fri, 24 Apr 2020 04:29:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 04:29:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7374d1118539f8cf16f7ad0d1ecc12433d5e0ac9d266240c79fe9a0cef6a6e53`  
		Last Modified: Fri, 24 Apr 2020 04:30:15 GMT  
		Size: 13.7 MB (13659274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d96f8829ce290acf10dbe54f9301927a2550a63c9cc65b71d637bf23ececafb`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f44bc85b96f853ae9bba560eb64dfb9cdbf63f9b3ae81c8cd4fcc231643c792`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9aa3a6d42037036e91d7173f9964bb6ff7f5dc820e9244d9a1d8be06697e3c`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:624655b564b9a0d8aff2adb11bc4e4ab152cc6cddbb0f80dbec0ccc280a6c7e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16969348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996e3889db7f499cb26285f39e7577a3572c8c83eefb66472ac0e3d67d6c9f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:52:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 02:52:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 02:53:15 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 02:53:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 02:53:21 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 02:53:22 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 02:53:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 02:53:26 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 02:53:27 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 02:53:29 GMT
USER fluent
# Fri, 24 Apr 2020 02:53:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 02:53:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27df74a3decbbc71f688e8319c7055315cbba6b350b28324d4ad9c021ca50135`  
		Last Modified: Fri, 24 Apr 2020 02:54:03 GMT  
		Size: 14.2 MB (14179267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465abcf9b778cb4d299d4fec3ccbd1b1284867a62dc8b6d6d59a7a195cc0203`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b323e14271e2cf6ac4ee482e207353aa39585d4e58bf75475fe54e2a7f1fdb65`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a13af9e734338dbe7adf7de4ab71210d13beaeed6a6fec5d7b9a7b4dff17131`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; s390x

```console
$ docker pull fluentd@sha256:12f970948d5704cc42194be7cbfd8fe038e802f8fc2fb8f2169bf7c4c2c5eb5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6e3f25bb06297f8b35538b6b7a44d6c0ce04bfa379393397e3eef1c4c16e9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 20:00:12 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 20:00:14 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 20:00:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 20:00:14 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 20:00:15 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 20:00:15 GMT
USER fluent
# Thu, 23 Apr 2020 20:00:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 20:00:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84a8d1f46d684e96854f17f7222edf696d71cf5cd842954e92f378e005dab17`  
		Last Modified: Thu, 23 Apr 2020 20:00:33 GMT  
		Size: 13.9 MB (13889338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52edf66127670c83c7f5a2aed5e38db5dca87e51eb8966174df5900dc2e0c9`  
		Last Modified: Thu, 23 Apr 2020 20:00:30 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec06b392ce74e92be850c3ddc84f05a6f54ed80e3920a6da6d4327a8d62b5137`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d063c86f8d64af1ad29498f54a054870ec143617b700e0f374dd7a023214ef43`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-1.0`

```console
$ docker pull fluentd@sha256:af335887b3a1c7f23b2d54aba84a7c4e0cddd50e70d18ee5a4feb281133bf608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9.1-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:b0136e1ac811a9bc03d2af9049acc8dccc5b891fe3d4bd08798ae3511ec81103
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16531173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec77776ad237484ae2ba463aa4246f529828e3a7dae22f59328fb310ca0d3591`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:23:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 13:23:18 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 13:23:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 13:23:53 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 13:23:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 13:23:54 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 13:23:54 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 13:23:54 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 13:23:55 GMT
USER fluent
# Fri, 24 Apr 2020 13:23:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 13:23:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58109e9b1ba0d634974981e1f60a467213412df52e63c2e0810a0e12bfd92a15`  
		Last Modified: Fri, 24 Apr 2020 13:25:56 GMT  
		Size: 13.8 MB (13755597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678a9500d8f0582867bfbfeeca06fafa14fc99c60d195dc4ff8982194a5a2b7b`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93abfddd6b877c4887a4bc98b9858a2224d45b266db8698704bdffd3e505844c`  
		Last Modified: Fri, 24 Apr 2020 13:25:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eca423c53486a28c557132cc9f38051b64967ceac115bdc32dc2cf670599150`  
		Last Modified: Fri, 24 Apr 2020 13:25:53 GMT  
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
$ docker pull fluentd@sha256:9a3af653771a6a04c358f7c2a60b8bb57c64d3de5dd298c0d4657ceb35ea0f66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16449859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62a0ca09e6cfbf89d9db9d526962faa229e3de5ec48e9ef934e8566431b4c9d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 24 Apr 2020 00:15:12 GMT
ADD file:da3ddeca2212f561c1f428b662a1f1f1200e2d18a42bffb28a0322c235f06582 in / 
# Fri, 24 Apr 2020 00:15:15 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:05:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 09:05:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 09:06:41 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 09:06:45 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 09:06:46 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 09:06:47 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 09:06:48 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 09:06:48 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 09:06:49 GMT
USER fluent
# Fri, 24 Apr 2020 09:06:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 09:06:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:941f399634ec37b35e6764d0e6cf350593652f06f76586d45ddfc0d77de7a701`  
		Last Modified: Fri, 24 Apr 2020 00:16:02 GMT  
		Size: 2.7 MB (2694467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7c433500fac88cd265a112da6bb53517cca36634a766db54f966da1f64e6ae`  
		Last Modified: Fri, 24 Apr 2020 09:07:26 GMT  
		Size: 13.8 MB (13753176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcba662d9a25425bd9d1fd78c25999719742ab37190f21b0228c999766407978`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a458dc4b98ef9ffa86fcd837c55416fd16fee3a6154a3e1f38011c7dad2a51`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0293d533db263a29c969b1f2ca4ef1c0df2bbfe728041795f264b905641d6009`  
		Last Modified: Fri, 24 Apr 2020 09:07:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c0c904864ac5d726fc15c7cdb7b8d67a1f22886deaebd1866846350eb8790b7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16431173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53efeb733ffb3b78b1ef4a7016222c61969cd70e411e9d45dd1c5491f69dd816`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:18 GMT
ADD file:68d5786259963a2b97cf808d79de83cbd0281dfea284e1a401bc851a3585e1bd in / 
# Thu, 23 Apr 2020 21:16:19 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 04:29:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 04:29:51 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 04:29:52 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 04:29:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 04:29:53 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 04:29:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 04:29:53 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 04:29:53 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 04:29:53 GMT
USER fluent
# Fri, 24 Apr 2020 04:29:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 04:29:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2f4fdbe0599cb5bbd0664b1cdad4997f428ce2495ae3eabf942129dc197d991c`  
		Last Modified: Thu, 23 Apr 2020 21:16:41 GMT  
		Size: 2.8 MB (2769736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7374d1118539f8cf16f7ad0d1ecc12433d5e0ac9d266240c79fe9a0cef6a6e53`  
		Last Modified: Fri, 24 Apr 2020 04:30:15 GMT  
		Size: 13.7 MB (13659274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d96f8829ce290acf10dbe54f9301927a2550a63c9cc65b71d637bf23ececafb`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f44bc85b96f853ae9bba560eb64dfb9cdbf63f9b3ae81c8cd4fcc231643c792`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9aa3a6d42037036e91d7173f9964bb6ff7f5dc820e9244d9a1d8be06697e3c`  
		Last Modified: Fri, 24 Apr 2020 04:30:11 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:624655b564b9a0d8aff2adb11bc4e4ab152cc6cddbb0f80dbec0ccc280a6c7e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16969348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996e3889db7f499cb26285f39e7577a3572c8c83eefb66472ac0e3d67d6c9f7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 20:41:14 GMT
ADD file:2eaa074d9379f98d31cc4112997e1c1bb55b3871574af6aee576cf1c5ed99645 in / 
# Thu, 23 Apr 2020 20:41:16 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:52:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 02:52:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 02:53:15 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 02:53:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 02:53:21 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 02:53:22 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 02:53:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 02:53:26 GMT
ENV LD_PRELOAD=
# Fri, 24 Apr 2020 02:53:27 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 02:53:29 GMT
USER fluent
# Fri, 24 Apr 2020 02:53:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 02:53:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16f2eaeeecc1446c304d41ae21441f168e376dc76733ec3a9f8f2d17119638a1`  
		Last Modified: Thu, 23 Apr 2020 20:41:57 GMT  
		Size: 2.8 MB (2787865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27df74a3decbbc71f688e8319c7055315cbba6b350b28324d4ad9c021ca50135`  
		Last Modified: Fri, 24 Apr 2020 02:54:03 GMT  
		Size: 14.2 MB (14179267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465abcf9b778cb4d299d4fec3ccbd1b1284867a62dc8b6d6d59a7a195cc0203`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b323e14271e2cf6ac4ee482e207353aa39585d4e58bf75475fe54e2a7f1fdb65`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a13af9e734338dbe7adf7de4ab71210d13beaeed6a6fec5d7b9a7b4dff17131`  
		Last Modified: Fri, 24 Apr 2020 02:53:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:12f970948d5704cc42194be7cbfd8fe038e802f8fc2fb8f2169bf7c4c2c5eb5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6e3f25bb06297f8b35538b6b7a44d6c0ce04bfa379393397e3eef1c4c16e9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:19 GMT
ADD file:87357838aa76ab358b68ac6734871df2dacb0b5918d89a091836f0d33264f803 in / 
# Thu, 23 Apr 2020 17:51:20 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 19:59:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 20:00:12 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 20:00:14 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 20:00:14 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 20:00:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 20:00:14 GMT
ENV LD_PRELOAD=
# Thu, 23 Apr 2020 20:00:15 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 20:00:15 GMT
USER fluent
# Thu, 23 Apr 2020 20:00:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 20:00:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aff3887737eb15ee1a53e92e8c87162b9caac2281ecb01242da00d1a32f5a04`  
		Last Modified: Thu, 23 Apr 2020 17:51:52 GMT  
		Size: 2.6 MB (2550329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84a8d1f46d684e96854f17f7222edf696d71cf5cd842954e92f378e005dab17`  
		Last Modified: Thu, 23 Apr 2020 20:00:33 GMT  
		Size: 13.9 MB (13889338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52edf66127670c83c7f5a2aed5e38db5dca87e51eb8966174df5900dc2e0c9`  
		Last Modified: Thu, 23 Apr 2020 20:00:30 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec06b392ce74e92be850c3ddc84f05a6f54ed80e3920a6da6d4327a8d62b5137`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d063c86f8d64af1ad29498f54a054870ec143617b700e0f374dd7a023214ef43`  
		Last Modified: Thu, 23 Apr 2020 20:00:35 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-debian-1.0`

```console
$ docker pull fluentd@sha256:98563baa01b0ab31317b62dcc52847a51e889a36c9013f4255ed0e00dd1a358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9.1-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:c187a97a025889572d8e2793ba44cadf5c15f3d7fdcaf8f5f8b3a743be3f2f06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85950478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5b4fe1e6ac82410ddb476206dfcd4a5159691cb042f1c3ac1f0cbfd48a2585`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 19:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:14:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 19:25:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 19:25:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 19:25:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 19:25:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 19:25:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 19:25:42 GMT
CMD ["irb"]
# Fri, 24 Apr 2020 13:24:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 13:24:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 13:24:04 GMT
ENV TINI_VERSION=0.18.0
# Fri, 24 Apr 2020 13:25:31 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 13:25:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 13:25:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 13:25:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 13:25:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 13:25:33 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 24 Apr 2020 13:25:33 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 13:25:33 GMT
USER fluent
# Fri, 24 Apr 2020 13:25:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 13:25:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfc531926e1cdd90cf7f3117ef03a4809cae01e5595149a0c28e39871cc3fba`  
		Last Modified: Thu, 23 Apr 2020 19:47:04 GMT  
		Size: 12.5 MB (12539631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500c509d215c9eeedb6e1ec9144f4bbec0e77e8b82304ded5afbc3811549b02`  
		Last Modified: Thu, 23 Apr 2020 19:47:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983d76fd37e5eefdb9d5971e7d00aa6c4a34dc383e5f2ac3340611fd01a06a56`  
		Last Modified: Thu, 23 Apr 2020 19:47:25 GMT  
		Size: 21.4 MB (21449495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2425985c16174ce55e0d520b5781ca858cb5841b757840be06692d92b5515fc2`  
		Last Modified: Thu, 23 Apr 2020 19:47:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37d114ce46c7d4bf065ae1f71f7e05e4e50efcca9a9380e74d0f965307fdd7`  
		Last Modified: Fri, 24 Apr 2020 13:26:05 GMT  
		Size: 24.9 MB (24860094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e144fde6d9a9f9d237f2c064968170265c05e12511598d455135f7a2d8d1c2`  
		Last Modified: Fri, 24 Apr 2020 13:26:00 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6492ccbc22be0686fd3dad842da669814e4b54aed3ff32aa94afada30049bb14`  
		Last Modified: Fri, 24 Apr 2020 13:26:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6d67b1cdfaff1b8a8e7a657bded6f2e68beddb8858d810c826ac7bc65ce24`  
		Last Modified: Fri, 24 Apr 2020 13:26:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:11c9c3e1ddd5138aa3c265fb4dfbfd02240623df10ee75a37afd64a66fa65075
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79891155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedb001e45f62baae16e21e971ee4582030d0a2a4dcfd40416d0e88bdbd02292`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:56:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 04:56:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 15 May 2020 05:03:53 GMT
ENV RUBY_MAJOR=2.6
# Fri, 15 May 2020 05:03:54 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 15 May 2020 05:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 15 May 2020 05:07:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 15 May 2020 05:07:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 May 2020 05:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 May 2020 05:07:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 05:07:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 15 May 2020 05:07:41 GMT
CMD ["irb"]
# Fri, 15 May 2020 12:10:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 15 May 2020 12:10:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 15 May 2020 12:10:44 GMT
ENV TINI_VERSION=0.18.0
# Fri, 15 May 2020 12:14:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 15 May 2020 12:14:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 15 May 2020 12:14:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 15 May 2020 12:14:20 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 15 May 2020 12:14:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 15 May 2020 12:14:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 15 May 2020 12:14:23 GMT
EXPOSE 24224 5140
# Fri, 15 May 2020 12:14:24 GMT
USER fluent
# Fri, 15 May 2020 12:14:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 15 May 2020 12:14:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ebdbe89249843e1a499d37e59553757fb9bd2840d51c8a299a7d1602132ff`  
		Last Modified: Fri, 15 May 2020 05:31:58 GMT  
		Size: 10.3 MB (10326232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3925cbe165b7c17f2269be849efe8b1fa39f9870ed90f2934a887ddba9555a`  
		Last Modified: Fri, 15 May 2020 05:31:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0c768150fe51028569c7ba42e6eb621eb64a0f35da91c05752e80abaf98596`  
		Last Modified: Fri, 15 May 2020 05:32:30 GMT  
		Size: 20.7 MB (20713769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90c87e332d6034c71da4087c099e0a99ba19a13b87795a3080d127336022ff`  
		Last Modified: Fri, 15 May 2020 05:32:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0574b74c12b7b89882a7022454d702e7d5f4d3bfa9aa78d7f7802ebfe66e7`  
		Last Modified: Fri, 15 May 2020 12:14:44 GMT  
		Size: 24.0 MB (24009617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf22c5f9a0926a8066bdd25e4db185b23432b9f27860424ea013a36a254b2b3`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced567849405cc55e1f0117b7e1b12fbb8752e6dafafad78d45ee696dfc5bb5`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd141455a434717ed302b9299a7c17f4cd6e84ef7bb00c77112519d8252e2fa`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:84c33aa6b17ed808689b652c5164046723b123bd059b3c0b07b978b610749544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77079069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbad1c2b5d43ba8a9bfe6d5c43555903e6a41b3b033820a9ab0acee5bfa5849e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:26 GMT
ADD file:db6122b36f3e70c5f490b50afba99d49fa345f11d0f5c77bb3c6749f8e2a4f81 in / 
# Thu, 23 Apr 2020 01:03:28 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 21:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 21:14:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 21:31:06 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 21:31:07 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 21:31:08 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 21:34:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 21:34:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 21:34:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 21:34:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 21:34:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 21:34:20 GMT
CMD ["irb"]
# Fri, 24 Apr 2020 01:14:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 01:14:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 01:14:08 GMT
ENV TINI_VERSION=0.18.0
# Fri, 24 Apr 2020 01:17:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 01:17:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 01:17:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 01:17:24 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 01:17:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 01:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 24 Apr 2020 01:17:29 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 01:17:32 GMT
USER fluent
# Fri, 24 Apr 2020 01:17:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 01:17:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:50fb0052086928803f00724ca465c89c45dde5b082b1e59dadb8101286dd5ab6`  
		Last Modified: Thu, 23 Apr 2020 01:11:08 GMT  
		Size: 22.7 MB (22705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5662967f494fc27c62dd6d3f1e2a0e45154e8f30e30b8026f15958dd64a7da9`  
		Last Modified: Thu, 23 Apr 2020 21:56:49 GMT  
		Size: 9.8 MB (9847330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648dccab79aa71cee391d4fc16f7ce1b241c56e0ad1e8db2b63904009360c2d9`  
		Last Modified: Thu, 23 Apr 2020 21:56:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9d71d44ace789e2c166638227981d84ef9f7bb65347931be25016dc132ee84`  
		Last Modified: Thu, 23 Apr 2020 21:57:25 GMT  
		Size: 20.6 MB (20622426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ada9d090f0add93c3f59b997104a1582116952e6c577aa20a86fee1c6e4430`  
		Last Modified: Thu, 23 Apr 2020 21:57:20 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5713d02a93f949c35e6e10576e07b517f3badb99d770e6188b284589320dcfdc`  
		Last Modified: Fri, 24 Apr 2020 01:18:08 GMT  
		Size: 23.9 MB (23900872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fea65fe9e0cc6bd58540fc7bf117427b5154a9b75bc87f106a92e15e3ef1e7`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5302b90868403bb0c23309be18d0600a25ec4ebd6b63d1c36e36433792c7c65`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c041d8b59cd6d7844aea941f9ffc57f75487af4b18f0c4d0760de2cd8301d4`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f181d38475d37084e2b5cc8a5ff8b420e3c8bec7f494e37e038c99fc1ca08aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83254248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98496c1be084705e2416b08a0fd9b6ae9cebe477bc567e02174a7ac5ffaed20`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 10:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:42:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 10:49:19 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 10:49:20 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 10:49:21 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 10:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 10:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 10:52:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 10:52:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 10:52:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 10:52:57 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:07:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 22:07:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 22:07:03 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 22:09:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 22:09:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 22:09:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 22:09:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 22:09:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 22:09:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 22:09:56 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 22:09:56 GMT
USER fluent
# Thu, 23 Apr 2020 22:09:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 22:09:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d379aa1fbe75be722a3f77b30cd7f9f9442a56d8666dc54ad35e6e95d488876f`  
		Last Modified: Thu, 23 Apr 2020 11:15:55 GMT  
		Size: 11.2 MB (11244783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8c92cbc8dba1f71530cf605b640b97dac9babecb718980b2adc09e59dbf267`  
		Last Modified: Thu, 23 Apr 2020 11:15:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8991757f10a395830efb735835ce381056f2e6f69f911203bd23d3854f1c9dad`  
		Last Modified: Thu, 23 Apr 2020 11:16:42 GMT  
		Size: 21.3 MB (21287907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbffffad20983c342a0aed076202c7ff1596a03be3b64f8a1f9490f083994c0`  
		Last Modified: Thu, 23 Apr 2020 11:16:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8494fdea4f2cc1b45b7de2adf9c6a33cc316a58c5e5ee89819280e493b245021`  
		Last Modified: Thu, 23 Apr 2020 22:10:18 GMT  
		Size: 24.9 MB (24860680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b5514725152e78c1573e36094d2e4925b35d729ce6c19f69fc3c47d8f5731`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72058a1e7c2ccb1d262b1e8e415681bb88c6e4635cdd1029be33854f0c5a475`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b98ca8109625b5169165879b22ca5549a7b1bf2bafadeabc941fe5895c6641`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:b9bc108261e2759174f4cd32001c0fa8e8f067ecd1d30efacc2fe13c5cdcdc90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89899361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05ee364fa8a9351bc4de3926cb93c2266ce0a4b21933126a865df36198ee2f3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 14:33:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 14:45:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 14:45:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 14:45:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 14:45:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 14:45:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 14:45:54 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 21:05:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 21:05:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 21:05:10 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 21:06:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 21:06:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 21:06:58 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 21:06:59 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 21:06:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 21:07:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 21:07:00 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 21:07:01 GMT
USER fluent
# Thu, 23 Apr 2020 21:07:01 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 21:07:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2efbbee96c0806febf1671a3e99a0bc815043cd437b9528ee3d2c0717a9e745`  
		Last Modified: Thu, 23 Apr 2020 15:11:05 GMT  
		Size: 17.2 MB (17205909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28e617ff318449d3d1a87125415d39df597ef4a0a60bdaae33e3dcbc97c79fb`  
		Last Modified: Thu, 23 Apr 2020 15:10:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51e1e68c255b5f4be8eb7642a5ffaa65412b8b902e6bcdbd0f3e60108dc6f37`  
		Last Modified: Thu, 23 Apr 2020 15:11:28 GMT  
		Size: 20.9 MB (20884621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78d10ea00d0708b0069a1aba497f96cec6e29f43b4181f86d878227e4982c12`  
		Last Modified: Thu, 23 Apr 2020 15:11:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2680843a50b32ec4041400b5c25d9f3cd3b3fde5c44ab89a0b488b2b74ebde0`  
		Last Modified: Thu, 23 Apr 2020 21:07:20 GMT  
		Size: 24.1 MB (24051854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbccdc9af5cefdeb2b58da6b66d6abfcd17e3c436cba21c345601ed25fcf0cd`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc82663507da5a18fc1d883d2f32412f778c3dcd2b101a9a6194ab18be4ba12`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed380f0b820b93502bdeb13b50a7edc2b7ded7229dafb591f85dceff6f264d`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:888b2a900b890f251c4e60db79e1eac67b95ccd3a5e713481484348544a546df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90609476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5e05885cefe81264a684b1ff90f3f9b303f7cc016f7ca788265c49b4f280`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:36:00 GMT
ADD file:5b3c3d2945800e1743dc02a4f68bd830fe2f67ca437223692eb460147c158c2b in / 
# Thu, 23 Apr 2020 00:36:04 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 10:43:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:43:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 10:56:22 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 10:56:24 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 10:56:27 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 11:02:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 11:02:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 11:02:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 11:02:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 11:02:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 11:02:34 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 19:14:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 19:14:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 19:14:46 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 19:18:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 19:18:54 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 19:18:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 19:18:56 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 19:18:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 19:19:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 19:19:06 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 19:19:11 GMT
USER fluent
# Thu, 23 Apr 2020 19:19:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 19:19:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:012c6cdbd1af202bbfbea5945fafbb9aca9097f1fa3cb493a29155fdc02cc43c`  
		Last Modified: Thu, 23 Apr 2020 00:50:14 GMT  
		Size: 30.5 MB (30524638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fa45a3e00b0104c63430762cb13611c3218b82a1740c840723690d6e88c4c1`  
		Last Modified: Thu, 23 Apr 2020 11:36:51 GMT  
		Size: 12.7 MB (12688890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f38baf28458b1fdc1cd3870908bfc1f3b7c6fe4f3db2b68001e1a8d2c85b762`  
		Last Modified: Thu, 23 Apr 2020 11:36:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8166b72629ee6af5fd3fde7e635fbdc0e4a09b4afb2cbc9256710251128be85`  
		Last Modified: Thu, 23 Apr 2020 11:37:54 GMT  
		Size: 22.0 MB (21969854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3985ded020681007314feaa564cf6968fdc05843a07cfb0b0db42d31695e2d`  
		Last Modified: Thu, 23 Apr 2020 11:37:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d808f072c64fc8991f0e7d6fd3fe0388d7b7bbdbfd3d05f02c75a4968c7a2f84`  
		Last Modified: Thu, 23 Apr 2020 19:19:31 GMT  
		Size: 25.4 MB (25423018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f514db3f22f6fd655bbe2fe73c11d9e2d79e5b444971b5f8ed59c4a98638b`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040985fd33d4a5939640cf27bb87f9a4391710485d4f3293a6090c0c811ad45`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4c35147a7b8e8caf5e09ba5253761e7f9a17fdab1ef78fa6882a8659e283e`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:336f7bdacf0e0df40c8a9c980500aeee236302cb74ddef8cad8a125f4bb346b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c08b2a2ec48e3f82880a0988852dfc5da05bc1b3217fa4b0f99aea75242df4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 07:52:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 07:52:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_MAJOR=2.6
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 15 May 2020 08:04:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 15 May 2020 08:04:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 May 2020 08:04:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 May 2020 08:04:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 08:04:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 15 May 2020 08:04:13 GMT
CMD ["irb"]
# Fri, 15 May 2020 15:01:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 15 May 2020 15:01:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 15 May 2020 15:01:26 GMT
ENV TINI_VERSION=0.18.0
# Fri, 15 May 2020 15:02:57 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 15 May 2020 15:03:01 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 15 May 2020 15:03:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 15 May 2020 15:03:02 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 15 May 2020 15:03:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 15 May 2020 15:03:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 15 May 2020 15:03:04 GMT
EXPOSE 24224 5140
# Fri, 15 May 2020 15:03:04 GMT
USER fluent
# Fri, 15 May 2020 15:03:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 15 May 2020 15:03:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf580d99c5da349d4ff059737fde7704c61728e7ed92ef175c78b3f88617ee2f`  
		Last Modified: Fri, 15 May 2020 08:16:02 GMT  
		Size: 10.8 MB (10796062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2245207f05eb67bc8e0b08218b93b76f15462c426018cecbd6bbe4ae72cbe`  
		Last Modified: Fri, 15 May 2020 08:16:02 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6949fa818ccb6f405f00cb89bda209eb637c583fcf6821fe7d9bcb494a0d842a`  
		Last Modified: Fri, 15 May 2020 08:16:30 GMT  
		Size: 21.6 MB (21597395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d029bfdba2e88f02f7567c2fecfa268e3e65584970184af90248cd60b1fe2`  
		Last Modified: Fri, 15 May 2020 08:16:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3531fd6ba0a472043342f160f2df1a596372dd111be9297263e512d4cac777c1`  
		Last Modified: Fri, 15 May 2020 15:03:32 GMT  
		Size: 25.0 MB (25036865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efac4bdb820e1bc28105e28673f89ad14aa701742b12eab86e60dc07b8418c38`  
		Last Modified: Fri, 15 May 2020 15:03:16 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8de30e709a0c1a9455706dd0f99f7dd599115ef835580b641eb23e496c015f`  
		Last Modified: Fri, 15 May 2020 15:03:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d272ad5202998c2eda4b302cdbd87f766d3c6a91dbb698626a3058859ccb1`  
		Last Modified: Fri, 15 May 2020 15:03:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-debian-1`

```console
$ docker pull fluentd@sha256:98563baa01b0ab31317b62dcc52847a51e889a36c9013f4255ed0e00dd1a358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:c187a97a025889572d8e2793ba44cadf5c15f3d7fdcaf8f5f8b3a743be3f2f06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85950478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5b4fe1e6ac82410ddb476206dfcd4a5159691cb042f1c3ac1f0cbfd48a2585`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 19:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:14:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 19:22:16 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 19:25:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 19:25:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 19:25:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 19:25:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 19:25:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 19:25:42 GMT
CMD ["irb"]
# Fri, 24 Apr 2020 13:24:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 13:24:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 13:24:04 GMT
ENV TINI_VERSION=0.18.0
# Fri, 24 Apr 2020 13:25:31 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 13:25:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 13:25:32 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 13:25:32 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 13:25:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 13:25:33 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 24 Apr 2020 13:25:33 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 13:25:33 GMT
USER fluent
# Fri, 24 Apr 2020 13:25:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 13:25:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfc531926e1cdd90cf7f3117ef03a4809cae01e5595149a0c28e39871cc3fba`  
		Last Modified: Thu, 23 Apr 2020 19:47:04 GMT  
		Size: 12.5 MB (12539631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500c509d215c9eeedb6e1ec9144f4bbec0e77e8b82304ded5afbc3811549b02`  
		Last Modified: Thu, 23 Apr 2020 19:47:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983d76fd37e5eefdb9d5971e7d00aa6c4a34dc383e5f2ac3340611fd01a06a56`  
		Last Modified: Thu, 23 Apr 2020 19:47:25 GMT  
		Size: 21.4 MB (21449495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2425985c16174ce55e0d520b5781ca858cb5841b757840be06692d92b5515fc2`  
		Last Modified: Thu, 23 Apr 2020 19:47:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37d114ce46c7d4bf065ae1f71f7e05e4e50efcca9a9380e74d0f965307fdd7`  
		Last Modified: Fri, 24 Apr 2020 13:26:05 GMT  
		Size: 24.9 MB (24860094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e144fde6d9a9f9d237f2c064968170265c05e12511598d455135f7a2d8d1c2`  
		Last Modified: Fri, 24 Apr 2020 13:26:00 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6492ccbc22be0686fd3dad842da669814e4b54aed3ff32aa94afada30049bb14`  
		Last Modified: Fri, 24 Apr 2020 13:26:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6d67b1cdfaff1b8a8e7a657bded6f2e68beddb8858d810c826ac7bc65ce24`  
		Last Modified: Fri, 24 Apr 2020 13:26:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:11c9c3e1ddd5138aa3c265fb4dfbfd02240623df10ee75a37afd64a66fa65075
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79891155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedb001e45f62baae16e21e971ee4582030d0a2a4dcfd40416d0e88bdbd02292`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:56:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 04:56:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 15 May 2020 05:03:53 GMT
ENV RUBY_MAJOR=2.6
# Fri, 15 May 2020 05:03:54 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 15 May 2020 05:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 15 May 2020 05:07:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 15 May 2020 05:07:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 May 2020 05:07:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 May 2020 05:07:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 05:07:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 15 May 2020 05:07:41 GMT
CMD ["irb"]
# Fri, 15 May 2020 12:10:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 15 May 2020 12:10:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 15 May 2020 12:10:44 GMT
ENV TINI_VERSION=0.18.0
# Fri, 15 May 2020 12:14:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 15 May 2020 12:14:18 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 15 May 2020 12:14:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 15 May 2020 12:14:20 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 15 May 2020 12:14:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 15 May 2020 12:14:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 15 May 2020 12:14:23 GMT
EXPOSE 24224 5140
# Fri, 15 May 2020 12:14:24 GMT
USER fluent
# Fri, 15 May 2020 12:14:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 15 May 2020 12:14:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ebdbe89249843e1a499d37e59553757fb9bd2840d51c8a299a7d1602132ff`  
		Last Modified: Fri, 15 May 2020 05:31:58 GMT  
		Size: 10.3 MB (10326232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3925cbe165b7c17f2269be849efe8b1fa39f9870ed90f2934a887ddba9555a`  
		Last Modified: Fri, 15 May 2020 05:31:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0c768150fe51028569c7ba42e6eb621eb64a0f35da91c05752e80abaf98596`  
		Last Modified: Fri, 15 May 2020 05:32:30 GMT  
		Size: 20.7 MB (20713769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90c87e332d6034c71da4087c099e0a99ba19a13b87795a3080d127336022ff`  
		Last Modified: Fri, 15 May 2020 05:32:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0574b74c12b7b89882a7022454d702e7d5f4d3bfa9aa78d7f7802ebfe66e7`  
		Last Modified: Fri, 15 May 2020 12:14:44 GMT  
		Size: 24.0 MB (24009617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf22c5f9a0926a8066bdd25e4db185b23432b9f27860424ea013a36a254b2b3`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced567849405cc55e1f0117b7e1b12fbb8752e6dafafad78d45ee696dfc5bb5`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd141455a434717ed302b9299a7c17f4cd6e84ef7bb00c77112519d8252e2fa`  
		Last Modified: Fri, 15 May 2020 12:14:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:84c33aa6b17ed808689b652c5164046723b123bd059b3c0b07b978b610749544
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77079069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbad1c2b5d43ba8a9bfe6d5c43555903e6a41b3b033820a9ab0acee5bfa5849e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:26 GMT
ADD file:db6122b36f3e70c5f490b50afba99d49fa345f11d0f5c77bb3c6749f8e2a4f81 in / 
# Thu, 23 Apr 2020 01:03:28 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 21:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 21:14:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 21:31:06 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 21:31:07 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 21:31:08 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 21:34:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 21:34:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 21:34:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 21:34:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 21:34:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 21:34:20 GMT
CMD ["irb"]
# Fri, 24 Apr 2020 01:14:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 24 Apr 2020 01:14:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 24 Apr 2020 01:14:08 GMT
ENV TINI_VERSION=0.18.0
# Fri, 24 Apr 2020 01:17:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 24 Apr 2020 01:17:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 24 Apr 2020 01:17:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 24 Apr 2020 01:17:24 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 24 Apr 2020 01:17:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 24 Apr 2020 01:17:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 24 Apr 2020 01:17:29 GMT
EXPOSE 24224 5140
# Fri, 24 Apr 2020 01:17:32 GMT
USER fluent
# Fri, 24 Apr 2020 01:17:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 24 Apr 2020 01:17:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:50fb0052086928803f00724ca465c89c45dde5b082b1e59dadb8101286dd5ab6`  
		Last Modified: Thu, 23 Apr 2020 01:11:08 GMT  
		Size: 22.7 MB (22705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5662967f494fc27c62dd6d3f1e2a0e45154e8f30e30b8026f15958dd64a7da9`  
		Last Modified: Thu, 23 Apr 2020 21:56:49 GMT  
		Size: 9.8 MB (9847330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648dccab79aa71cee391d4fc16f7ce1b241c56e0ad1e8db2b63904009360c2d9`  
		Last Modified: Thu, 23 Apr 2020 21:56:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9d71d44ace789e2c166638227981d84ef9f7bb65347931be25016dc132ee84`  
		Last Modified: Thu, 23 Apr 2020 21:57:25 GMT  
		Size: 20.6 MB (20622426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ada9d090f0add93c3f59b997104a1582116952e6c577aa20a86fee1c6e4430`  
		Last Modified: Thu, 23 Apr 2020 21:57:20 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5713d02a93f949c35e6e10576e07b517f3badb99d770e6188b284589320dcfdc`  
		Last Modified: Fri, 24 Apr 2020 01:18:08 GMT  
		Size: 23.9 MB (23900872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fea65fe9e0cc6bd58540fc7bf117427b5154a9b75bc87f106a92e15e3ef1e7`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5302b90868403bb0c23309be18d0600a25ec4ebd6b63d1c36e36433792c7c65`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c041d8b59cd6d7844aea941f9ffc57f75487af4b18f0c4d0760de2cd8301d4`  
		Last Modified: Fri, 24 Apr 2020 01:17:59 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f181d38475d37084e2b5cc8a5ff8b420e3c8bec7f494e37e038c99fc1ca08aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83254248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98496c1be084705e2416b08a0fd9b6ae9cebe477bc567e02174a7ac5ffaed20`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 10:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:42:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 10:49:19 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 10:49:20 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 10:49:21 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 10:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 10:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 10:52:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 10:52:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 10:52:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 10:52:57 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:07:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 22:07:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 22:07:03 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 22:09:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 22:09:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 22:09:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 22:09:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 22:09:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 22:09:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 22:09:56 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 22:09:56 GMT
USER fluent
# Thu, 23 Apr 2020 22:09:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 22:09:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d379aa1fbe75be722a3f77b30cd7f9f9442a56d8666dc54ad35e6e95d488876f`  
		Last Modified: Thu, 23 Apr 2020 11:15:55 GMT  
		Size: 11.2 MB (11244783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8c92cbc8dba1f71530cf605b640b97dac9babecb718980b2adc09e59dbf267`  
		Last Modified: Thu, 23 Apr 2020 11:15:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8991757f10a395830efb735835ce381056f2e6f69f911203bd23d3854f1c9dad`  
		Last Modified: Thu, 23 Apr 2020 11:16:42 GMT  
		Size: 21.3 MB (21287907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbffffad20983c342a0aed076202c7ff1596a03be3b64f8a1f9490f083994c0`  
		Last Modified: Thu, 23 Apr 2020 11:16:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8494fdea4f2cc1b45b7de2adf9c6a33cc316a58c5e5ee89819280e493b245021`  
		Last Modified: Thu, 23 Apr 2020 22:10:18 GMT  
		Size: 24.9 MB (24860680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b5514725152e78c1573e36094d2e4925b35d729ce6c19f69fc3c47d8f5731`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72058a1e7c2ccb1d262b1e8e415681bb88c6e4635cdd1029be33854f0c5a475`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b98ca8109625b5169165879b22ca5549a7b1bf2bafadeabc941fe5895c6641`  
		Last Modified: Thu, 23 Apr 2020 22:10:10 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:b9bc108261e2759174f4cd32001c0fa8e8f067ecd1d30efacc2fe13c5cdcdc90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89899361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05ee364fa8a9351bc4de3926cb93c2266ce0a4b21933126a865df36198ee2f3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 14:33:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 14:41:46 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 14:45:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 14:45:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 14:45:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 14:45:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 14:45:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 14:45:54 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 21:05:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 21:05:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 21:05:10 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 21:06:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 21:06:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 21:06:58 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 21:06:59 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 21:06:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 21:07:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 21:07:00 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 21:07:01 GMT
USER fluent
# Thu, 23 Apr 2020 21:07:01 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 21:07:02 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2efbbee96c0806febf1671a3e99a0bc815043cd437b9528ee3d2c0717a9e745`  
		Last Modified: Thu, 23 Apr 2020 15:11:05 GMT  
		Size: 17.2 MB (17205909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28e617ff318449d3d1a87125415d39df597ef4a0a60bdaae33e3dcbc97c79fb`  
		Last Modified: Thu, 23 Apr 2020 15:10:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51e1e68c255b5f4be8eb7642a5ffaa65412b8b902e6bcdbd0f3e60108dc6f37`  
		Last Modified: Thu, 23 Apr 2020 15:11:28 GMT  
		Size: 20.9 MB (20884621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78d10ea00d0708b0069a1aba497f96cec6e29f43b4181f86d878227e4982c12`  
		Last Modified: Thu, 23 Apr 2020 15:11:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2680843a50b32ec4041400b5c25d9f3cd3b3fde5c44ab89a0b488b2b74ebde0`  
		Last Modified: Thu, 23 Apr 2020 21:07:20 GMT  
		Size: 24.1 MB (24051854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbccdc9af5cefdeb2b58da6b66d6abfcd17e3c436cba21c345601ed25fcf0cd`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc82663507da5a18fc1d883d2f32412f778c3dcd2b101a9a6194ab18be4ba12`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed380f0b820b93502bdeb13b50a7edc2b7ded7229dafb591f85dceff6f264d`  
		Last Modified: Thu, 23 Apr 2020 21:07:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:888b2a900b890f251c4e60db79e1eac67b95ccd3a5e713481484348544a546df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90609476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5e05885cefe81264a684b1ff90f3f9b303f7cc016f7ca788265c49b4f280`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Apr 2020 00:36:00 GMT
ADD file:5b3c3d2945800e1743dc02a4f68bd830fe2f67ca437223692eb460147c158c2b in / 
# Thu, 23 Apr 2020 00:36:04 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 10:43:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 10:43:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Apr 2020 10:56:22 GMT
ENV RUBY_MAJOR=2.6
# Thu, 23 Apr 2020 10:56:24 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 23 Apr 2020 10:56:27 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 23 Apr 2020 11:02:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 23 Apr 2020 11:02:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 11:02:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 11:02:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 11:02:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 23 Apr 2020 11:02:34 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 19:14:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Apr 2020 19:14:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Apr 2020 19:14:46 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Apr 2020 19:18:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Apr 2020 19:18:54 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Apr 2020 19:18:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Apr 2020 19:18:56 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Apr 2020 19:18:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Apr 2020 19:19:02 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Apr 2020 19:19:06 GMT
EXPOSE 24224 5140
# Thu, 23 Apr 2020 19:19:11 GMT
USER fluent
# Thu, 23 Apr 2020 19:19:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Apr 2020 19:19:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:012c6cdbd1af202bbfbea5945fafbb9aca9097f1fa3cb493a29155fdc02cc43c`  
		Last Modified: Thu, 23 Apr 2020 00:50:14 GMT  
		Size: 30.5 MB (30524638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fa45a3e00b0104c63430762cb13611c3218b82a1740c840723690d6e88c4c1`  
		Last Modified: Thu, 23 Apr 2020 11:36:51 GMT  
		Size: 12.7 MB (12688890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f38baf28458b1fdc1cd3870908bfc1f3b7c6fe4f3db2b68001e1a8d2c85b762`  
		Last Modified: Thu, 23 Apr 2020 11:36:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8166b72629ee6af5fd3fde7e635fbdc0e4a09b4afb2cbc9256710251128be85`  
		Last Modified: Thu, 23 Apr 2020 11:37:54 GMT  
		Size: 22.0 MB (21969854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3985ded020681007314feaa564cf6968fdc05843a07cfb0b0db42d31695e2d`  
		Last Modified: Thu, 23 Apr 2020 11:37:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d808f072c64fc8991f0e7d6fd3fe0388d7b7bbdbfd3d05f02c75a4968c7a2f84`  
		Last Modified: Thu, 23 Apr 2020 19:19:31 GMT  
		Size: 25.4 MB (25423018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f514db3f22f6fd655bbe2fe73c11d9e2d79e5b444971b5f8ed59c4a98638b`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040985fd33d4a5939640cf27bb87f9a4391710485d4f3293a6090c0c811ad45`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d4c35147a7b8e8caf5e09ba5253761e7f9a17fdab1ef78fa6882a8659e283e`  
		Last Modified: Thu, 23 Apr 2020 19:19:26 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:336f7bdacf0e0df40c8a9c980500aeee236302cb74ddef8cad8a125f4bb346b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c08b2a2ec48e3f82880a0988852dfc5da05bc1b3217fa4b0f99aea75242df4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 07:52:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 07:52:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_MAJOR=2.6
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 15 May 2020 08:02:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 15 May 2020 08:04:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 15 May 2020 08:04:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 May 2020 08:04:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 May 2020 08:04:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 08:04:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 15 May 2020 08:04:13 GMT
CMD ["irb"]
# Fri, 15 May 2020 15:01:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 15 May 2020 15:01:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 15 May 2020 15:01:26 GMT
ENV TINI_VERSION=0.18.0
# Fri, 15 May 2020 15:02:57 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 15 May 2020 15:03:01 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 15 May 2020 15:03:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 15 May 2020 15:03:02 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 15 May 2020 15:03:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 15 May 2020 15:03:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 15 May 2020 15:03:04 GMT
EXPOSE 24224 5140
# Fri, 15 May 2020 15:03:04 GMT
USER fluent
# Fri, 15 May 2020 15:03:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 15 May 2020 15:03:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf580d99c5da349d4ff059737fde7704c61728e7ed92ef175c78b3f88617ee2f`  
		Last Modified: Fri, 15 May 2020 08:16:02 GMT  
		Size: 10.8 MB (10796062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2245207f05eb67bc8e0b08218b93b76f15462c426018cecbd6bbe4ae72cbe`  
		Last Modified: Fri, 15 May 2020 08:16:02 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6949fa818ccb6f405f00cb89bda209eb637c583fcf6821fe7d9bcb494a0d842a`  
		Last Modified: Fri, 15 May 2020 08:16:30 GMT  
		Size: 21.6 MB (21597395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d029bfdba2e88f02f7567c2fecfa268e3e65584970184af90248cd60b1fe2`  
		Last Modified: Fri, 15 May 2020 08:16:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3531fd6ba0a472043342f160f2df1a596372dd111be9297263e512d4cac777c1`  
		Last Modified: Fri, 15 May 2020 15:03:32 GMT  
		Size: 25.0 MB (25036865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efac4bdb820e1bc28105e28673f89ad14aa701742b12eab86e60dc07b8418c38`  
		Last Modified: Fri, 15 May 2020 15:03:16 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8de30e709a0c1a9455706dd0f99f7dd599115ef835580b641eb23e496c015f`  
		Last Modified: Fri, 15 May 2020 15:03:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d272ad5202998c2eda4b302cdbd87f766d3c6a91dbb698626a3058859ccb1`  
		Last Modified: Fri, 15 May 2020 15:03:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
