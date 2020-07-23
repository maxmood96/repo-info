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
$ docker pull fluentd@sha256:c7352360b43533045e8abeada0dc6638be42797cc08c1ffec9964afaf55091ab
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
$ docker pull fluentd@sha256:13c6b9ccc571d163dbd08022583a3cb83ff5faf755021d4509209f314f008fe5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82353004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e3936a0dfb3405e18f32b48a2a053fb98ffcde0f166e9681f9b96b93862646`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 19:42:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:21:02 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 21:44:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 21:44:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 21:44:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 21:44:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 21:44:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 21:44:37 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:01:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:01:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:01:31 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:03:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:03:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:03:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:03:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:03:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:03:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:03:10 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:03:10 GMT
USER fluent
# Fri, 26 Jun 2020 23:03:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:03:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc90e6cf5818a58b654c668706f45d537bad50a42248d0f237711247c464a1e`  
		Last Modified: Tue, 09 Jun 2020 20:15:23 GMT  
		Size: 12.5 MB (12539281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d55212f71e6943a5df1d5af3c318ba1002ffb5f55e56c922efef942d96523`  
		Last Modified: Tue, 09 Jun 2020 20:15:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129f6bdb9864b324d71243f63b254aab3d41b7c32e20c87d8a69f70f8bf7713c`  
		Last Modified: Fri, 26 Jun 2020 22:32:07 GMT  
		Size: 21.5 MB (21450244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e02c957c3111616ef68e02fc5c99ecea5bc3ee5f6a042c98bed6549bc67a48`  
		Last Modified: Fri, 26 Jun 2020 22:32:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04019cdd490cd35194dbe96de32a175c911fcaa36a5904b40e579253865a2524`  
		Last Modified: Fri, 26 Jun 2020 23:03:23 GMT  
		Size: 21.3 MB (21262215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f67394aa0dfe6aca4c834ec546d0a08fcb83a07961c0529c98dd7fdb6ec204`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f48310cc78f7f891a44c669a3200fd3b118ef507793735b1502d92cf4645fd`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff12dd2c1fc7ace6119b4c2b6192818cd180cf76b41b63fe1949f5097efbfd42`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:25509b0f0a2817283ec51d2b7e859976cd0a961f9a11be98611d0cd3279f2ac9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76292043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5642011048a6817b8a544519e61661be03982fd5a7700450932ce930e16d9fe2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 11:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 11:04:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 11:04:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 11:14:21 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 11:14:23 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 11:14:38 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 11:18:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 11:18:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 11:18:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 11:18:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 11:19:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 11:19:10 GMT
CMD ["irb"]
# Wed, 22 Jul 2020 20:50:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 22 Jul 2020 20:50:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 22 Jul 2020 20:50:46 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 20:54:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 22 Jul 2020 20:54:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 22 Jul 2020 20:54:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 22 Jul 2020 20:54:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 22 Jul 2020 20:54:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 22 Jul 2020 20:54:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 22 Jul 2020 20:54:13 GMT
EXPOSE 24224 5140
# Wed, 22 Jul 2020 20:54:13 GMT
USER fluent
# Wed, 22 Jul 2020 20:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 22 Jul 2020 20:54:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2cef7af0b30099924e137e8a25168454010f4d900fbc56217bfb1404ed6d13`  
		Last Modified: Wed, 22 Jul 2020 11:52:17 GMT  
		Size: 10.3 MB (10327272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4330f5efc5d753f8ed93e50a6513fe00702a413917059506a8c0437561f5b3`  
		Last Modified: Wed, 22 Jul 2020 11:52:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6dfb7de80d34a74664471e8dcf448b475009408b3c86529f427282fb3a8a47`  
		Last Modified: Wed, 22 Jul 2020 11:52:46 GMT  
		Size: 20.7 MB (20713610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c008931a17676fd126dd6ccef91f467d5a06f73d2b355d30e94df33738de2e6`  
		Last Modified: Wed, 22 Jul 2020 11:52:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997735f7e19e5bfcc0de12247a823868cfd779b4b17363e77735abee7e0ffb4`  
		Last Modified: Wed, 22 Jul 2020 20:54:45 GMT  
		Size: 20.4 MB (20410634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ba52db899ada950cc5045f574d06dce638e9ea7adffa22b6abe67755424d6`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea2673dc5d27aac3f3e34462faaeec732fa17e9fecff84eccdc963874c250d3`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f180f51104514b7675a98b7abc54a4b65639012e3b5b954db282caa2b12eb6f`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ddf51974e810f3cc312833affca63ba353c6980640d1010eb33773c270ea2fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73487243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe7a1046bbc746b692715b92d8aacb3f8c1789142b4f42eaee72c28eab85696`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:37:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 20:29:03 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 20:52:18 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 20:52:19 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 20:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 20:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 20:55:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 20:55:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 20:55:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 20:55:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 20:56:00 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:42:16 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:42:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:42:18 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:45:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:45:29 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:45:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:45:30 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:45:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:45:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:45:32 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:45:32 GMT
USER fluent
# Fri, 26 Jun 2020 23:45:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:45:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7868af188cfeba513084a91039368d608c8a42103a20ed66b9d04b121a6c1c0`  
		Last Modified: Tue, 09 Jun 2020 14:25:09 GMT  
		Size: 9.8 MB (9847805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df22981cc3af99b1bfac8bbf09bf01172de3d6220802c7f81c6fadfa88cf0707`  
		Last Modified: Tue, 09 Jun 2020 14:25:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79d7a33efbf5d2e3a2b641584988ad3e2cd46f1618bd8ec1b49ca520d9b4620`  
		Last Modified: Fri, 26 Jun 2020 21:33:40 GMT  
		Size: 20.6 MB (20622548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556dd55a24e7ad4ba86511eb302bb1f491a32e0f6b17f0deef9819f35324c32`  
		Last Modified: Fri, 26 Jun 2020 21:33:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e93be0760887ca18bfdc2b8f0ba6ca11336fa1f593615c569616613063443f`  
		Last Modified: Fri, 26 Jun 2020 23:45:59 GMT  
		Size: 20.3 MB (20307914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac350a5be95f0acf2b2d7dd829509d3356d2aca3d304b496b1c3c68f7d0d9f82`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f013173974eac86836b37d3bfd8505a592994702743067b05b8abcc74ec878`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f53f0f46727e4942eaa2d14413a4510cce34450d6ea03489d01b24b41b8859`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:888e5d0afbb567995983234e7f7a38f562ea5028ca285f2a30b32490de3b8fde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79663675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9dc0117a7017a18830da59f55c9bc9430a8a00a71ae9a35a22174b0ab03e0d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:00:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Jul 2020 05:00:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Jul 2020 05:00:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Jul 2020 05:03:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Jul 2020 05:03:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Jul 2020 05:03:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Jul 2020 05:03:41 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Jul 2020 05:03:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Jul 2020 05:03:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Jul 2020 05:03:47 GMT
EXPOSE 24224 5140
# Thu, 23 Jul 2020 05:03:49 GMT
USER fluent
# Thu, 23 Jul 2020 05:03:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Jul 2020 05:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4e4d9948cacca4ac4cd968097b26c98427d4d4f95f6eeefcb152713ee1b542`  
		Last Modified: Thu, 23 Jul 2020 05:04:18 GMT  
		Size: 21.3 MB (21269586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f2dab6a6f402b3709f1e0bc681ade2859893578b2aa900a85ad1abc593694`  
		Last Modified: Thu, 23 Jul 2020 05:04:13 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76107c20f7cf7b2fe70797e6616aa76223d749c454c6a9bfb1cdfb1b3b6cf48d`  
		Last Modified: Thu, 23 Jul 2020 05:04:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241ff1fdfe960dc924b37bd7d2e56233a314211ea3f3c113216205c1fcdf095d`  
		Last Modified: Thu, 23 Jul 2020 05:04:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:72c84ee98821f6ea97fe69c440d5b7a502acf9541dd7cb19dc2544c7cd27a517
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86305092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbacd4101c6d76b90d460aafbf3b11e11498c68502efe0c1b55aff1f70fdbd7c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 02:09:15 GMT
ADD file:ee51bd8fcf2e02243de32c0f0e7899acebfa23bdceb783f13feb33c484ee98b8 in / 
# Wed, 22 Jul 2020 02:09:15 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 15:44:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 15:44:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 15:44:34 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 15:55:50 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 15:55:51 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 15:55:51 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 16:00:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 16:00:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 16:00:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 16:00:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 16:00:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 16:00:17 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 00:06:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Jul 2020 00:06:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Jul 2020 00:06:15 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Jul 2020 00:08:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Jul 2020 00:08:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Jul 2020 00:08:04 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Jul 2020 00:08:04 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Jul 2020 00:08:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Jul 2020 00:08:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Jul 2020 00:08:05 GMT
EXPOSE 24224 5140
# Thu, 23 Jul 2020 00:08:05 GMT
USER fluent
# Thu, 23 Jul 2020 00:08:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Jul 2020 00:08:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75157e9ef5a857d6b02d235e08a164737ad009bae299277f86131063e6204e0b`  
		Last Modified: Wed, 22 Jul 2020 02:15:45 GMT  
		Size: 27.8 MB (27754899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a8036d73438f05b0681172b526e688d13b318f2333178a38972654137a38dd`  
		Last Modified: Wed, 22 Jul 2020 16:32:55 GMT  
		Size: 17.2 MB (17207484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220cb2c9c5207655428e93a1e71bc60277a23e83e95cb1d84f8293e19a834ead`  
		Last Modified: Wed, 22 Jul 2020 16:32:49 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0cee8ac319d6ca1065063a41167861adcc84bb5737bb61ae479e28ba92327`  
		Last Modified: Wed, 22 Jul 2020 16:33:22 GMT  
		Size: 20.9 MB (20884878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a204af9f4b8f07fdcfab5f059c7cb30d7b7f8adc65779da68f6d7e1e5fd4d72a`  
		Last Modified: Wed, 22 Jul 2020 16:33:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7cf05ac173345ae7c09ca0fee11abb25cb93f88e5001a0c2bec36ee22cb468`  
		Last Modified: Thu, 23 Jul 2020 00:08:23 GMT  
		Size: 20.5 MB (20454830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9ceb814fca33a266495f62a6615a03e02e454b5c8295e7899b7d866a878424`  
		Last Modified: Thu, 23 Jul 2020 00:08:18 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1743f5f71edda2d03a6979b80f0403d0f6add425e64734b369298a9d9eaded05`  
		Last Modified: Thu, 23 Jul 2020 00:08:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e56bb01944b6184a70b424ac2746b7df44bb21eeff6ab2cd4b83c672175b8`  
		Last Modified: Thu, 23 Jul 2020 00:08:19 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:424957c0be136a48dff3eddaf18b6faf1ee9824dd09097f9a68c676ee4b41609
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87015579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a14b045a7ca9e6f605d8576e66089d381c7a668dddd1c1822fd5928cb25b17d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 11:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 11:40:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 20:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:13:50 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:13:53 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:13:56 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 21:19:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 21:19:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 21:19:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 21:19:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 21:19:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 21:20:02 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:27:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:27:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:27:35 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:31:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:31:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:31:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:31:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:31:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:31:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:31:35 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:31:37 GMT
USER fluent
# Fri, 26 Jun 2020 23:31:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:31:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7cc70842ec721d27645e3cedfa00f8a727ffe2e94c35a0e9cef2eed40790a`  
		Last Modified: Tue, 09 Jun 2020 13:01:26 GMT  
		Size: 12.7 MB (12687912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac0516c49e0886398227505c6fe5b41cd409122a9fd57f58a50b86ecbf8d53`  
		Last Modified: Tue, 09 Jun 2020 13:01:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf9fe0b5c4bb6868287fe5392b65203331f0361538a4e1b1fcc823a58e5bf97`  
		Last Modified: Fri, 26 Jun 2020 22:16:38 GMT  
		Size: 22.0 MB (21970055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d7a3ae80a637beb0c001b2c317ad9d5cb46b035deb1ab839e7a4dd87cb7767`  
		Last Modified: Fri, 26 Jun 2020 22:16:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93525e1bc5cad194c762091dab98b0869f8298c72b52aa808e76eef26ed7d6a4`  
		Last Modified: Fri, 26 Jun 2020 23:32:16 GMT  
		Size: 21.8 MB (21830125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444e2d152794c90231f7d0decc8d346b3f477f7692959c2fb7bd5afd9969db4a`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bffb6c0216b306c8fd83e25facd303f7cdc36b0ba3c76887604797818157ec`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5b8f1675d98b7da50ee549b77cf60c0810e346b00aaa0033277e43c5b5f2b2`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:3bd583995c13f706e7006a2e3a0470629cdb3719cdba6856aa7228fd0b9428be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79548765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290fb093755daa1941e06cda4a2e11fdf6d05b3347f6e6cb80af046e7a6cb73`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:41 GMT
ADD file:2864b647009a85c176c3aeb2d75843b9336b02a18412124b8a03710df61dc971 in / 
# Wed, 22 Jul 2020 00:42:43 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:40:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 05:40:18 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 05:50:18 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 05:50:18 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 05:50:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 05:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 05:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 05:51:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 05:51:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 05:51:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 05:51:55 GMT
CMD ["irb"]
# Wed, 22 Jul 2020 11:17:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 22 Jul 2020 11:17:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 22 Jul 2020 11:17:07 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 11:18:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 22 Jul 2020 11:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 22 Jul 2020 11:18:28 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 22 Jul 2020 11:18:28 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 22 Jul 2020 11:18:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 22 Jul 2020 11:18:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 22 Jul 2020 11:18:28 GMT
EXPOSE 24224 5140
# Wed, 22 Jul 2020 11:18:29 GMT
USER fluent
# Wed, 22 Jul 2020 11:18:29 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 22 Jul 2020 11:18:29 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:71104c8b0e24cdcb6152cf3a5afb2944f578c741e6defa1905768c590598a79a`  
		Last Modified: Wed, 22 Jul 2020 00:45:48 GMT  
		Size: 25.7 MB (25712820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d16a3572ceeb5d540897c2409134e2877e5ff4518fd3ce15bd5a7d39383e777`  
		Last Modified: Wed, 22 Jul 2020 05:56:37 GMT  
		Size: 10.8 MB (10796336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470597a2ce72463d5bd8e63f668013916ba4d93ccd055771005d94468b3c6206`  
		Last Modified: Wed, 22 Jul 2020 05:56:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3840a81a8cc728de141c4cd4125ccc0953c2136e3bc825172eb0423dffb0bc`  
		Last Modified: Wed, 22 Jul 2020 05:57:05 GMT  
		Size: 21.6 MB (21597178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8550c4b124cda31d8735a68fa4b261e810dfa6c2665420dfd43fc54bd7bbba6`  
		Last Modified: Wed, 22 Jul 2020 05:57:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc7613d77712348e27399ffd1bc52f6ac5c0e7354c513fc74039678d3bca333`  
		Last Modified: Wed, 22 Jul 2020 11:18:46 GMT  
		Size: 21.4 MB (21439361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea30334acf1cdafa8ebc8b8a6196b6071356454a635dbe640d15e5553070409a`  
		Last Modified: Wed, 22 Jul 2020 11:18:48 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6350700af3cdec6b1ab66dc5085367af1c5ccf4732beff4a031065ec1ca76b`  
		Last Modified: Wed, 22 Jul 2020 11:18:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b16cfa6dcf0e267d4085b5b51847317895031cd5c6d9aeeb71e03e5ba470c4a`  
		Last Modified: Wed, 22 Jul 2020 11:18:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-debian-1`

```console
$ docker pull fluentd@sha256:c7352360b43533045e8abeada0dc6638be42797cc08c1ffec9964afaf55091ab
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
$ docker pull fluentd@sha256:13c6b9ccc571d163dbd08022583a3cb83ff5faf755021d4509209f314f008fe5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82353004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e3936a0dfb3405e18f32b48a2a053fb98ffcde0f166e9681f9b96b93862646`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 19:42:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 21:21:02 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:40:34 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 21:44:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 21:44:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 21:44:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 21:44:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 21:44:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 21:44:37 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:01:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:01:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:01:31 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:03:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:03:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:03:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:03:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:03:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:03:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:03:10 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:03:10 GMT
USER fluent
# Fri, 26 Jun 2020 23:03:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:03:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc90e6cf5818a58b654c668706f45d537bad50a42248d0f237711247c464a1e`  
		Last Modified: Tue, 09 Jun 2020 20:15:23 GMT  
		Size: 12.5 MB (12539281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d55212f71e6943a5df1d5af3c318ba1002ffb5f55e56c922efef942d96523`  
		Last Modified: Tue, 09 Jun 2020 20:15:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129f6bdb9864b324d71243f63b254aab3d41b7c32e20c87d8a69f70f8bf7713c`  
		Last Modified: Fri, 26 Jun 2020 22:32:07 GMT  
		Size: 21.5 MB (21450244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e02c957c3111616ef68e02fc5c99ecea5bc3ee5f6a042c98bed6549bc67a48`  
		Last Modified: Fri, 26 Jun 2020 22:32:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04019cdd490cd35194dbe96de32a175c911fcaa36a5904b40e579253865a2524`  
		Last Modified: Fri, 26 Jun 2020 23:03:23 GMT  
		Size: 21.3 MB (21262215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f67394aa0dfe6aca4c834ec546d0a08fcb83a07961c0529c98dd7fdb6ec204`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f48310cc78f7f891a44c669a3200fd3b118ef507793735b1502d92cf4645fd`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff12dd2c1fc7ace6119b4c2b6192818cd180cf76b41b63fe1949f5097efbfd42`  
		Last Modified: Fri, 26 Jun 2020 23:03:20 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:25509b0f0a2817283ec51d2b7e859976cd0a961f9a11be98611d0cd3279f2ac9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76292043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5642011048a6817b8a544519e61661be03982fd5a7700450932ce930e16d9fe2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 11:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 11:04:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 11:04:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 11:14:21 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 11:14:23 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 11:14:38 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 11:18:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 11:18:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 11:18:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 11:18:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 11:19:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 11:19:10 GMT
CMD ["irb"]
# Wed, 22 Jul 2020 20:50:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 22 Jul 2020 20:50:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 22 Jul 2020 20:50:46 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 20:54:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 22 Jul 2020 20:54:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 22 Jul 2020 20:54:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 22 Jul 2020 20:54:10 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 22 Jul 2020 20:54:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 22 Jul 2020 20:54:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 22 Jul 2020 20:54:13 GMT
EXPOSE 24224 5140
# Wed, 22 Jul 2020 20:54:13 GMT
USER fluent
# Wed, 22 Jul 2020 20:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 22 Jul 2020 20:54:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2cef7af0b30099924e137e8a25168454010f4d900fbc56217bfb1404ed6d13`  
		Last Modified: Wed, 22 Jul 2020 11:52:17 GMT  
		Size: 10.3 MB (10327272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4330f5efc5d753f8ed93e50a6513fe00702a413917059506a8c0437561f5b3`  
		Last Modified: Wed, 22 Jul 2020 11:52:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6dfb7de80d34a74664471e8dcf448b475009408b3c86529f427282fb3a8a47`  
		Last Modified: Wed, 22 Jul 2020 11:52:46 GMT  
		Size: 20.7 MB (20713610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c008931a17676fd126dd6ccef91f467d5a06f73d2b355d30e94df33738de2e6`  
		Last Modified: Wed, 22 Jul 2020 11:52:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997735f7e19e5bfcc0de12247a823868cfd779b4b17363e77735abee7e0ffb4`  
		Last Modified: Wed, 22 Jul 2020 20:54:45 GMT  
		Size: 20.4 MB (20410634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ba52db899ada950cc5045f574d06dce638e9ea7adffa22b6abe67755424d6`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea2673dc5d27aac3f3e34462faaeec732fa17e9fecff84eccdc963874c250d3`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f180f51104514b7675a98b7abc54a4b65639012e3b5b954db282caa2b12eb6f`  
		Last Modified: Wed, 22 Jul 2020 20:54:39 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ddf51974e810f3cc312833affca63ba353c6980640d1010eb33773c270ea2fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73487243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe7a1046bbc746b692715b92d8aacb3f8c1789142b4f42eaee72c28eab85696`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:37:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 20:29:03 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 20:52:18 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 20:52:19 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 20:52:20 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 20:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 20:55:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 20:55:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 20:55:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 20:55:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 20:56:00 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:42:16 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:42:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:42:18 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:45:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:45:29 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:45:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:45:30 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:45:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:45:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:45:32 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:45:32 GMT
USER fluent
# Fri, 26 Jun 2020 23:45:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:45:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7868af188cfeba513084a91039368d608c8a42103a20ed66b9d04b121a6c1c0`  
		Last Modified: Tue, 09 Jun 2020 14:25:09 GMT  
		Size: 9.8 MB (9847805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df22981cc3af99b1bfac8bbf09bf01172de3d6220802c7f81c6fadfa88cf0707`  
		Last Modified: Tue, 09 Jun 2020 14:25:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79d7a33efbf5d2e3a2b641584988ad3e2cd46f1618bd8ec1b49ca520d9b4620`  
		Last Modified: Fri, 26 Jun 2020 21:33:40 GMT  
		Size: 20.6 MB (20622548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556dd55a24e7ad4ba86511eb302bb1f491a32e0f6b17f0deef9819f35324c32`  
		Last Modified: Fri, 26 Jun 2020 21:33:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e93be0760887ca18bfdc2b8f0ba6ca11336fa1f593615c569616613063443f`  
		Last Modified: Fri, 26 Jun 2020 23:45:59 GMT  
		Size: 20.3 MB (20307914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac350a5be95f0acf2b2d7dd829509d3356d2aca3d304b496b1c3c68f7d0d9f82`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f013173974eac86836b37d3bfd8505a592994702743067b05b8abcc74ec878`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f53f0f46727e4942eaa2d14413a4510cce34450d6ea03489d01b24b41b8859`  
		Last Modified: Fri, 26 Jun 2020 23:45:53 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:888e5d0afbb567995983234e7f7a38f562ea5028ca285f2a30b32490de3b8fde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79663675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9dc0117a7017a18830da59f55c9bc9430a8a00a71ae9a35a22174b0ab03e0d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 18:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 18:43:53 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 18:43:55 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 18:43:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 18:48:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 18:48:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 18:48:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 18:48:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 18:48:35 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 05:00:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Jul 2020 05:00:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Jul 2020 05:00:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Jul 2020 05:03:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Jul 2020 05:03:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Jul 2020 05:03:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Jul 2020 05:03:41 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Jul 2020 05:03:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Jul 2020 05:03:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Jul 2020 05:03:47 GMT
EXPOSE 24224 5140
# Thu, 23 Jul 2020 05:03:49 GMT
USER fluent
# Thu, 23 Jul 2020 05:03:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Jul 2020 05:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3f61bb77d63882985d0d92f797b6fcea40c8af8476319dc7a6ea1b884600f5`  
		Last Modified: Wed, 22 Jul 2020 19:14:21 GMT  
		Size: 11.2 MB (11244586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb4a350ec30646772ca5a91d40a13fdf15793a59ce2a023c42cedacfd5bb4f`  
		Last Modified: Wed, 22 Jul 2020 19:14:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd3273d528ccaade6550b7ebd80a412c4969ca8426f2ea9a2a8ac5b4c74b83c`  
		Last Modified: Wed, 22 Jul 2020 19:14:56 GMT  
		Size: 21.3 MB (21288600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3addf443b3b3e2fadf86fefef72575f6a1c3f250e01bc35a69880f40096e7bb6`  
		Last Modified: Wed, 22 Jul 2020 19:14:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4e4d9948cacca4ac4cd968097b26c98427d4d4f95f6eeefcb152713ee1b542`  
		Last Modified: Thu, 23 Jul 2020 05:04:18 GMT  
		Size: 21.3 MB (21269586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f2dab6a6f402b3709f1e0bc681ade2859893578b2aa900a85ad1abc593694`  
		Last Modified: Thu, 23 Jul 2020 05:04:13 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76107c20f7cf7b2fe70797e6616aa76223d749c454c6a9bfb1cdfb1b3b6cf48d`  
		Last Modified: Thu, 23 Jul 2020 05:04:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241ff1fdfe960dc924b37bd7d2e56233a314211ea3f3c113216205c1fcdf095d`  
		Last Modified: Thu, 23 Jul 2020 05:04:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:72c84ee98821f6ea97fe69c440d5b7a502acf9541dd7cb19dc2544c7cd27a517
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86305092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbacd4101c6d76b90d460aafbf3b11e11498c68502efe0c1b55aff1f70fdbd7c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 02:09:15 GMT
ADD file:ee51bd8fcf2e02243de32c0f0e7899acebfa23bdceb783f13feb33c484ee98b8 in / 
# Wed, 22 Jul 2020 02:09:15 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 15:44:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 15:44:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 15:44:34 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 15:55:50 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 15:55:51 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 15:55:51 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 16:00:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 16:00:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 16:00:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 16:00:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 16:00:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 16:00:17 GMT
CMD ["irb"]
# Thu, 23 Jul 2020 00:06:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 23 Jul 2020 00:06:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 23 Jul 2020 00:06:15 GMT
ENV TINI_VERSION=0.18.0
# Thu, 23 Jul 2020 00:08:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 23 Jul 2020 00:08:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 23 Jul 2020 00:08:04 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 23 Jul 2020 00:08:04 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 23 Jul 2020 00:08:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 23 Jul 2020 00:08:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 23 Jul 2020 00:08:05 GMT
EXPOSE 24224 5140
# Thu, 23 Jul 2020 00:08:05 GMT
USER fluent
# Thu, 23 Jul 2020 00:08:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 23 Jul 2020 00:08:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75157e9ef5a857d6b02d235e08a164737ad009bae299277f86131063e6204e0b`  
		Last Modified: Wed, 22 Jul 2020 02:15:45 GMT  
		Size: 27.8 MB (27754899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a8036d73438f05b0681172b526e688d13b318f2333178a38972654137a38dd`  
		Last Modified: Wed, 22 Jul 2020 16:32:55 GMT  
		Size: 17.2 MB (17207484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220cb2c9c5207655428e93a1e71bc60277a23e83e95cb1d84f8293e19a834ead`  
		Last Modified: Wed, 22 Jul 2020 16:32:49 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0cee8ac319d6ca1065063a41167861adcc84bb5737bb61ae479e28ba92327`  
		Last Modified: Wed, 22 Jul 2020 16:33:22 GMT  
		Size: 20.9 MB (20884878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a204af9f4b8f07fdcfab5f059c7cb30d7b7f8adc65779da68f6d7e1e5fd4d72a`  
		Last Modified: Wed, 22 Jul 2020 16:33:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7cf05ac173345ae7c09ca0fee11abb25cb93f88e5001a0c2bec36ee22cb468`  
		Last Modified: Thu, 23 Jul 2020 00:08:23 GMT  
		Size: 20.5 MB (20454830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9ceb814fca33a266495f62a6615a03e02e454b5c8295e7899b7d866a878424`  
		Last Modified: Thu, 23 Jul 2020 00:08:18 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1743f5f71edda2d03a6979b80f0403d0f6add425e64734b369298a9d9eaded05`  
		Last Modified: Thu, 23 Jul 2020 00:08:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e56bb01944b6184a70b424ac2746b7df44bb21eeff6ab2cd4b83c672175b8`  
		Last Modified: Thu, 23 Jul 2020 00:08:19 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:424957c0be136a48dff3eddaf18b6faf1ee9824dd09097f9a68c676ee4b41609
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87015579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a14b045a7ca9e6f605d8576e66089d381c7a668dddd1c1822fd5928cb25b17d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 11:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 11:40:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 26 Jun 2020 20:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2020 21:13:50 GMT
ENV RUBY_MAJOR=2.6
# Fri, 26 Jun 2020 21:13:53 GMT
ENV RUBY_VERSION=2.6.6
# Fri, 26 Jun 2020 21:13:56 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Fri, 26 Jun 2020 21:19:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 26 Jun 2020 21:19:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 26 Jun 2020 21:19:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 26 Jun 2020 21:19:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2020 21:19:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 26 Jun 2020 21:20:02 GMT
CMD ["irb"]
# Fri, 26 Jun 2020 23:27:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 26 Jun 2020 23:27:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 26 Jun 2020 23:27:35 GMT
ENV TINI_VERSION=0.18.0
# Fri, 26 Jun 2020 23:31:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 26 Jun 2020 23:31:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 26 Jun 2020 23:31:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 26 Jun 2020 23:31:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 26 Jun 2020 23:31:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 26 Jun 2020 23:31:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 26 Jun 2020 23:31:35 GMT
EXPOSE 24224 5140
# Fri, 26 Jun 2020 23:31:37 GMT
USER fluent
# Fri, 26 Jun 2020 23:31:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 26 Jun 2020 23:31:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7cc70842ec721d27645e3cedfa00f8a727ffe2e94c35a0e9cef2eed40790a`  
		Last Modified: Tue, 09 Jun 2020 13:01:26 GMT  
		Size: 12.7 MB (12687912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac0516c49e0886398227505c6fe5b41cd409122a9fd57f58a50b86ecbf8d53`  
		Last Modified: Tue, 09 Jun 2020 13:01:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf9fe0b5c4bb6868287fe5392b65203331f0361538a4e1b1fcc823a58e5bf97`  
		Last Modified: Fri, 26 Jun 2020 22:16:38 GMT  
		Size: 22.0 MB (21970055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d7a3ae80a637beb0c001b2c317ad9d5cb46b035deb1ab839e7a4dd87cb7767`  
		Last Modified: Fri, 26 Jun 2020 22:16:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93525e1bc5cad194c762091dab98b0869f8298c72b52aa808e76eef26ed7d6a4`  
		Last Modified: Fri, 26 Jun 2020 23:32:16 GMT  
		Size: 21.8 MB (21830125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444e2d152794c90231f7d0decc8d346b3f477f7692959c2fb7bd5afd9969db4a`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bffb6c0216b306c8fd83e25facd303f7cdc36b0ba3c76887604797818157ec`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5b8f1675d98b7da50ee549b77cf60c0810e346b00aaa0033277e43c5b5f2b2`  
		Last Modified: Fri, 26 Jun 2020 23:32:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:3bd583995c13f706e7006a2e3a0470629cdb3719cdba6856aa7228fd0b9428be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79548765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290fb093755daa1941e06cda4a2e11fdf6d05b3347f6e6cb80af046e7a6cb73`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:41 GMT
ADD file:2864b647009a85c176c3aeb2d75843b9336b02a18412124b8a03710df61dc971 in / 
# Wed, 22 Jul 2020 00:42:43 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:40:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 22 Jul 2020 05:40:18 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 05:50:18 GMT
ENV RUBY_MAJOR=2.6
# Wed, 22 Jul 2020 05:50:18 GMT
ENV RUBY_VERSION=2.6.6
# Wed, 22 Jul 2020 05:50:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Wed, 22 Jul 2020 05:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 22 Jul 2020 05:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Jul 2020 05:51:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Jul 2020 05:51:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 05:51:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 22 Jul 2020 05:51:55 GMT
CMD ["irb"]
# Wed, 22 Jul 2020 11:17:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 22 Jul 2020 11:17:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 22 Jul 2020 11:17:07 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 11:18:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 22 Jul 2020 11:18:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 22 Jul 2020 11:18:28 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 22 Jul 2020 11:18:28 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 22 Jul 2020 11:18:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 22 Jul 2020 11:18:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 22 Jul 2020 11:18:28 GMT
EXPOSE 24224 5140
# Wed, 22 Jul 2020 11:18:29 GMT
USER fluent
# Wed, 22 Jul 2020 11:18:29 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 22 Jul 2020 11:18:29 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:71104c8b0e24cdcb6152cf3a5afb2944f578c741e6defa1905768c590598a79a`  
		Last Modified: Wed, 22 Jul 2020 00:45:48 GMT  
		Size: 25.7 MB (25712820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d16a3572ceeb5d540897c2409134e2877e5ff4518fd3ce15bd5a7d39383e777`  
		Last Modified: Wed, 22 Jul 2020 05:56:37 GMT  
		Size: 10.8 MB (10796336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470597a2ce72463d5bd8e63f668013916ba4d93ccd055771005d94468b3c6206`  
		Last Modified: Wed, 22 Jul 2020 05:56:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3840a81a8cc728de141c4cd4125ccc0953c2136e3bc825172eb0423dffb0bc`  
		Last Modified: Wed, 22 Jul 2020 05:57:05 GMT  
		Size: 21.6 MB (21597178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8550c4b124cda31d8735a68fa4b261e810dfa6c2665420dfd43fc54bd7bbba6`  
		Last Modified: Wed, 22 Jul 2020 05:57:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc7613d77712348e27399ffd1bc52f6ac5c0e7354c513fc74039678d3bca333`  
		Last Modified: Wed, 22 Jul 2020 11:18:46 GMT  
		Size: 21.4 MB (21439361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea30334acf1cdafa8ebc8b8a6196b6071356454a635dbe640d15e5553070409a`  
		Last Modified: Wed, 22 Jul 2020 11:18:48 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6350700af3cdec6b1ab66dc5085367af1c5ccf4732beff4a031065ec1ca76b`  
		Last Modified: Wed, 22 Jul 2020 11:18:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b16cfa6dcf0e267d4085b5b51847317895031cd5c6d9aeeb71e03e5ba470c4a`  
		Last Modified: Wed, 22 Jul 2020 11:18:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
