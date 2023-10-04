<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.2-1.1`](#fluentdv1162-11)
-	[`fluentd:v1.16.2-debian-1.1`](#fluentdv1162-debian-11)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:0e1090ed3901b0f4a5a4faabb10f91c4fa680da2e2a6503c23832ade8212bfc5
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
$ docker pull fluentd@sha256:13ee83b11a86c4e6593b5acb8e647c22cf1b9feef123612b9dd586465ed05254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25155206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e2964bb824f2aacb86d0ca3170997802f000be1eff97299b1188ec8611aa4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:19:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:20:26 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:20:27 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:20:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:20:27 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:20:27 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:20:28 GMT
USER fluent
# Wed, 04 Oct 2023 21:20:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:20:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8827fca176be13b72bd568162360ca80ecd8eef45b5ef68c80b3a000f503183`  
		Last Modified: Wed, 04 Oct 2023 21:24:01 GMT  
		Size: 21.8 MB (21774385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6515ca36e5cdb6a7919ba7b37f2dd0f2d248776d1f9485d6447a039b1ed9452`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3543c7841d7564df2c94d78f0afdedb172e4b82c8677f5b5ad85136ac57a1dd3`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57e8a5d5c2f2b9f7e226a62461f9a68d3c8ffaa5b73c8a92b05fa8bcc8d1d96`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:059df7f5071014b62e8cd4b3d56609cecbf887753011d04bb0a3b0e017a60f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f827678b99b7f0450b51a46ea4bbded99d2af7bc05d42292069f7ac5157f0b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:49:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:50:18 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 20:50:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 20:50:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 20:50:19 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 20:50:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 20:50:19 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 20:50:19 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 20:50:19 GMT
USER fluent
# Wed, 04 Oct 2023 20:50:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 20:50:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553532437e6782bb598563089e5c9712ae1d947bcc0e062ecde36c20a8de5397`  
		Last Modified: Wed, 04 Oct 2023 20:50:32 GMT  
		Size: 20.7 MB (20733532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d15a3c0a2634f3d4b2d360f2e9ef8cf7e467483d959c924d4ce1b9de09ff85`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8122aae986d2ea394888a2a35bdfe989c9aff09557fab2b7a3a40c97ca077`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff8c6799857457a342c810fea84380b9f681c2db904dff6caef780d7e0671d3`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:8197de0448a2f17bf11f791952b47dada2db36420039a914517dd8fdb9576cd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9bbe3c7c4f2dc30c2ce5307d8fe088a8d1b645f876b2f86ab83f0c04d8ec45`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:39:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:40:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:40:19 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:40:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:40:20 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:40:20 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:40:20 GMT
USER fluent
# Wed, 04 Oct 2023 21:40:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:40:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3e3f59536119d5781bb641b631d26d36f17086051a8b4afd4683c39e225bb4`  
		Last Modified: Wed, 04 Oct 2023 21:43:15 GMT  
		Size: 21.4 MB (21368773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf0687a8f3c9c7bc2628fceef6bc75e8642ea202b985274313ddd137d5bde2f`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3742a3460d54456ef66da27bcb397c738c7a99e48ee599835c2d5d935c0ca`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3629019f4be74a2ec436a05f010c0abc28d5060bf37a9e2874366f5210daf2`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:b83b7e92a71b743f967b5288f16a4df4305653819cdb9aaf2d900d46f42909fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24437573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a376d83aefcf980ab1d54ab6eaa54cfe7efd64178c391d35d5dd01828a219566`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:38:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:39:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:39:33 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:39:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:39:33 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:39:33 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:39:33 GMT
USER fluent
# Wed, 04 Oct 2023 21:39:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:39:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82eeb7c7b7c8cf58216ccf047891a51db52037f8d73338c44bda2aade1939af3`  
		Last Modified: Wed, 04 Oct 2023 21:43:33 GMT  
		Size: 21.0 MB (21021575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfff789f4260eb9a35837ba5b55a3132024fc07f657c0a7a36b4c537c93e532`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3634708fd9e50993123edc881d3b612bd7abd118c86c10ae821d153c32627d6c`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecb450aa2b0fc245622f769a3b887b13b78e60ea9541bfea6ff5c6ec88b683f`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:00ec95a9165ad95d580fdd03e9ac2168cbb48c84e783c0d256d2ff2e2c012649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (25008964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2fe004ba2fc07cbd3ae7d50e767842934d907a6ed122619d1e28e110d0efec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:16:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:18:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:18:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:19:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:19:01 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:19:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:19:02 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:19:03 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:19:04 GMT
USER fluent
# Wed, 04 Oct 2023 21:19:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:19:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686c1faa62490a3123a764ff1f9eb8f56b2d2370ca4c57a0df250c27b5f8c567`  
		Last Modified: Wed, 04 Oct 2023 21:27:05 GMT  
		Size: 21.6 MB (21615400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f05d8caa8bd28ac8b74de327805f02bd7541b08a3ff76a90a8edd0ec3be3a8`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74498b595a258f3d58d08ebcd2d0594e2b0954606ac5dce53681b96fa90a9fb6`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e2fa1f46398cb0c1fce47f3a1dbbe71e2ec584d77c560feebc765d18af209`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:4bf9c8b8442eecc11953268bb67197327b4dcd7dfd3c362260c96a431e13fe04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29998860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7f6f610b30aa0140b9f9276b6b90fa1f395f17501f7fcdb7a94c3614ef43a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:41:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:47:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:48:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:48:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:48:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:48:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:48:04 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:48:05 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:48:05 GMT
USER fluent
# Wed, 04 Oct 2023 21:48:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:48:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a7cda602ceb77b991077268ddf9794e50138b46af24af519f72acbdec17298`  
		Last Modified: Wed, 04 Oct 2023 21:54:17 GMT  
		Size: 26.8 MB (26820669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fa9f658a1932ce284e4498f48f661f20e5b5bf01569236217ff0fcc0ea6cc`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a7282d352e8cc5052eaaf24c4c0a054b8e7ed3b58082b373ae53b18b4c2eab`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8e091f38fa0c967d062af79901add256471c87f62cbe5b767a12554086282`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:0e1090ed3901b0f4a5a4faabb10f91c4fa680da2e2a6503c23832ade8212bfc5
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
$ docker pull fluentd@sha256:13ee83b11a86c4e6593b5acb8e647c22cf1b9feef123612b9dd586465ed05254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25155206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e2964bb824f2aacb86d0ca3170997802f000be1eff97299b1188ec8611aa4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:19:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:20:26 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:20:27 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:20:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:20:27 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:20:27 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:20:28 GMT
USER fluent
# Wed, 04 Oct 2023 21:20:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:20:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8827fca176be13b72bd568162360ca80ecd8eef45b5ef68c80b3a000f503183`  
		Last Modified: Wed, 04 Oct 2023 21:24:01 GMT  
		Size: 21.8 MB (21774385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6515ca36e5cdb6a7919ba7b37f2dd0f2d248776d1f9485d6447a039b1ed9452`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3543c7841d7564df2c94d78f0afdedb172e4b82c8677f5b5ad85136ac57a1dd3`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57e8a5d5c2f2b9f7e226a62461f9a68d3c8ffaa5b73c8a92b05fa8bcc8d1d96`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:059df7f5071014b62e8cd4b3d56609cecbf887753011d04bb0a3b0e017a60f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f827678b99b7f0450b51a46ea4bbded99d2af7bc05d42292069f7ac5157f0b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:49:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:50:18 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 20:50:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 20:50:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 20:50:19 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 20:50:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 20:50:19 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 20:50:19 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 20:50:19 GMT
USER fluent
# Wed, 04 Oct 2023 20:50:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 20:50:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553532437e6782bb598563089e5c9712ae1d947bcc0e062ecde36c20a8de5397`  
		Last Modified: Wed, 04 Oct 2023 20:50:32 GMT  
		Size: 20.7 MB (20733532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d15a3c0a2634f3d4b2d360f2e9ef8cf7e467483d959c924d4ce1b9de09ff85`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8122aae986d2ea394888a2a35bdfe989c9aff09557fab2b7a3a40c97ca077`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff8c6799857457a342c810fea84380b9f681c2db904dff6caef780d7e0671d3`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:8197de0448a2f17bf11f791952b47dada2db36420039a914517dd8fdb9576cd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9bbe3c7c4f2dc30c2ce5307d8fe088a8d1b645f876b2f86ab83f0c04d8ec45`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:39:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:40:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:40:19 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:40:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:40:20 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:40:20 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:40:20 GMT
USER fluent
# Wed, 04 Oct 2023 21:40:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:40:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3e3f59536119d5781bb641b631d26d36f17086051a8b4afd4683c39e225bb4`  
		Last Modified: Wed, 04 Oct 2023 21:43:15 GMT  
		Size: 21.4 MB (21368773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf0687a8f3c9c7bc2628fceef6bc75e8642ea202b985274313ddd137d5bde2f`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3742a3460d54456ef66da27bcb397c738c7a99e48ee599835c2d5d935c0ca`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3629019f4be74a2ec436a05f010c0abc28d5060bf37a9e2874366f5210daf2`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:b83b7e92a71b743f967b5288f16a4df4305653819cdb9aaf2d900d46f42909fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24437573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a376d83aefcf980ab1d54ab6eaa54cfe7efd64178c391d35d5dd01828a219566`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:38:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:39:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:39:33 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:39:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:39:33 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:39:33 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:39:33 GMT
USER fluent
# Wed, 04 Oct 2023 21:39:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:39:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82eeb7c7b7c8cf58216ccf047891a51db52037f8d73338c44bda2aade1939af3`  
		Last Modified: Wed, 04 Oct 2023 21:43:33 GMT  
		Size: 21.0 MB (21021575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfff789f4260eb9a35837ba5b55a3132024fc07f657c0a7a36b4c537c93e532`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3634708fd9e50993123edc881d3b612bd7abd118c86c10ae821d153c32627d6c`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecb450aa2b0fc245622f769a3b887b13b78e60ea9541bfea6ff5c6ec88b683f`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:00ec95a9165ad95d580fdd03e9ac2168cbb48c84e783c0d256d2ff2e2c012649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (25008964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2fe004ba2fc07cbd3ae7d50e767842934d907a6ed122619d1e28e110d0efec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:16:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:18:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:18:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:19:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:19:01 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:19:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:19:02 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:19:03 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:19:04 GMT
USER fluent
# Wed, 04 Oct 2023 21:19:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:19:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686c1faa62490a3123a764ff1f9eb8f56b2d2370ca4c57a0df250c27b5f8c567`  
		Last Modified: Wed, 04 Oct 2023 21:27:05 GMT  
		Size: 21.6 MB (21615400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f05d8caa8bd28ac8b74de327805f02bd7541b08a3ff76a90a8edd0ec3be3a8`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74498b595a258f3d58d08ebcd2d0594e2b0954606ac5dce53681b96fa90a9fb6`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e2fa1f46398cb0c1fce47f3a1dbbe71e2ec584d77c560feebc765d18af209`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:4bf9c8b8442eecc11953268bb67197327b4dcd7dfd3c362260c96a431e13fe04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29998860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7f6f610b30aa0140b9f9276b6b90fa1f395f17501f7fcdb7a94c3614ef43a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:41:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:47:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:48:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:48:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:48:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:48:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:48:04 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:48:05 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:48:05 GMT
USER fluent
# Wed, 04 Oct 2023 21:48:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:48:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a7cda602ceb77b991077268ddf9794e50138b46af24af519f72acbdec17298`  
		Last Modified: Wed, 04 Oct 2023 21:54:17 GMT  
		Size: 26.8 MB (26820669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fa9f658a1932ce284e4498f48f661f20e5b5bf01569236217ff0fcc0ea6cc`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a7282d352e8cc5052eaaf24c4c0a054b8e7ed3b58082b373ae53b18b4c2eab`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8e091f38fa0c967d062af79901add256471c87f62cbe5b767a12554086282`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:6837a7996018724262b7a137a0c4c1f384bea795399eb86e0462ee868cb064e0
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
$ docker pull fluentd@sha256:f200e644039dfa3f839fc1c73904dce942ef04ec88b0c9ae05e685caf2a67d74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110795278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d9408d2dad8032d0bd665a5fd63a17effd39370144dc62818b9ed2b9c7d3cc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:27:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 06:27:27 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 06:43:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 06:43:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 06:43:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 06:43:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:43:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 06:43:35 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 21:31:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:20:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:20:42 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:23:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:23:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:23:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:23:36 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:23:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:23:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:23:36 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:23:36 GMT
USER fluent
# Wed, 04 Oct 2023 21:23:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:23:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ca7bee443bcb2df6fefe9dac000084301fc7d16f30007cce46c92524471903`  
		Last Modified: Wed, 20 Sep 2023 06:50:07 GMT  
		Size: 10.0 MB (10018565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d78b16832011f333fa852282b9f3c7b3b7cd3b9ab0f01181f8472d920bfa3e`  
		Last Modified: Wed, 20 Sep 2023 06:50:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b8e6c0d8f9f5a8acca62bcb7a9d7464c9205c295981de5befd83371272f67a`  
		Last Modified: Wed, 20 Sep 2023 06:51:24 GMT  
		Size: 32.6 MB (32626043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab3abb9ee9e3896dce2a66b8eb85f169e73013676286679473487a41d2bea6a`  
		Last Modified: Wed, 20 Sep 2023 06:51:21 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85164087d4bc5eef452f202e56a612be46cfd399b318a3ee58fac055731a06f0`  
		Last Modified: Wed, 04 Oct 2023 21:24:19 GMT  
		Size: 36.7 MB (36729874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5ad63792f74db3749877216b562ebe66d814ef6d51df4a177531feeb03a76`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee99a08dae6683b5d82c25693fb4fb33e34d6bffad7eaf9fd31da9676b4e130c`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc254b21491a471884ee81ba2e1945d2cceeb5cd24d075c25672d5142ce6215b`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d9d60ace3bab736674e8c64d953e632d1778b6c7dcdffe4a0b4f974ea50a7c18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102458094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e7a22aded18cd1e74585559b68e098580569c37eb606e0bcace0fd09c3067`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 00:50:22 GMT
ADD file:3fafe6196c5a5c30a92e0a7cca16de98eecf20e6e40a25a36034e3512e0fceb7 in / 
# Wed, 20 Sep 2023 00:50:23 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:30:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 15:30:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 15:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 15:54:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 15:54:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 15:54:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 15:54:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 15:54:22 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 16:34:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:48:12 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:48:12 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 20:51:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 20:51:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 20:51:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 20:51:11 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 20:51:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 20:51:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 20:51:11 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 20:51:11 GMT
USER fluent
# Wed, 04 Oct 2023 20:51:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 20:51:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:028bb77b977c8effa899ef4c01139f4f5f8d4c94b82f792204b8bca21961fceb`  
		Last Modified: Wed, 20 Sep 2023 00:55:38 GMT  
		Size: 28.9 MB (28919128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9538e3dc01c29ae56a826f9cbba76b6b47353b9d132cb68de0fa524f6cb125d`  
		Last Modified: Wed, 20 Sep 2023 16:01:35 GMT  
		Size: 8.6 MB (8631273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18650dd925389614ca5b08f7a162bd9d218cf719ef9ec8b50064b152c8b34fbe`  
		Last Modified: Wed, 20 Sep 2023 16:01:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b96a26706b2482d7176dbc3a93cdf10d270cc1f4976d5fb7bba7043d2f6e13d`  
		Last Modified: Wed, 20 Sep 2023 16:04:21 GMT  
		Size: 31.2 MB (31165971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a56b30aaf08329d2afbb2b06eedda50e785d3d9c4c92e17900a10d81250889`  
		Last Modified: Wed, 20 Sep 2023 16:04:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ce750eb8b852e31b69f6e97a1d833e90be58ae24eeb24afcf2ee5d2594a68`  
		Last Modified: Wed, 04 Oct 2023 20:51:29 GMT  
		Size: 33.7 MB (33738652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbdcc873c804c68c7f71f1aa190332ae014939ce45813ce8f1b505582b5378`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930676d4cc662adbfad85c7d7bd0752fb75a7cc438b43639c1e6a398b6fa9eca`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7f3a289c84c246b43ba8d7cbb8f6ef4c96e8378a303ba3709401ab1724c47b`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ea45f8c8a9e5eccf441f2718fc1c536b47faaf657cb314ba56901429a4987b9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98853900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2dcd19c9c3de3633a3c82e44dee8d2138a7011109ce1e7afeb39883457dd3e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:35 GMT
ADD file:551a2d9bfca9d524e2144fe06246864ea8480a1567dda26f14d99255ae6a89de in / 
# Wed, 20 Sep 2023 04:57:36 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 14:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 14:54:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 14:54:57 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 15:08:17 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 15:08:17 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 15:08:18 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 15:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 15:10:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 15:10:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 15:10:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 15:10:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 15:10:24 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 01:36:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:57:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:57:22 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:00:09 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:00:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:00:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:00:10 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:00:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:00:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:00:10 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:00:10 GMT
USER fluent
# Wed, 04 Oct 2023 21:00:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:00:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:69e0260f539f90d8f61c40f7822d9c002aa082311842094f6e640751432c0b02`  
		Last Modified: Wed, 20 Sep 2023 05:01:55 GMT  
		Size: 26.6 MB (26578623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c262874c18502eaebc1081376669eb2b2e7fb9f7a9fe6a4634c044e412efa0`  
		Last Modified: Wed, 20 Sep 2023 15:16:42 GMT  
		Size: 8.1 MB (8139904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e37ae340d374a97c0f1eb711de5189c2cc07b01942451baa5bbf13587de3bf3`  
		Last Modified: Wed, 20 Sep 2023 15:16:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c975675033940075215d9bcb1b170567388e0703b2a3d674ca92097754308d4`  
		Last Modified: Wed, 20 Sep 2023 15:18:07 GMT  
		Size: 31.0 MB (31035579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685e94c1f05662f63d3d386b8ee5522f869f117fe856e2d1fec7e384bc40a0`  
		Last Modified: Wed, 20 Sep 2023 15:18:03 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510054dc14b50afd3553abfa2a44de2ab6f08fe00e16933a17cd41107653996c`  
		Last Modified: Wed, 04 Oct 2023 21:00:25 GMT  
		Size: 33.1 MB (33096707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac5e4bed14e34d22e344678721980524e7c564638576a7cc3b60e55bb46bd08`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab33fe2b5f373806de8011c79b608a6f848162504c93ed39b439fba2660629af`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03cfd51cd12e2a97cf36e187173f1eb2c7419fea120e33fd9eb9f0086bd49ca`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a5d2a5aa08d1da833490b164653107f503b30f4970595cf72c1f8e4d2f66b647
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106289025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a68e564693a122e9f46a2343449f5bc548cc3c91553a69b82d8a0d82e9f90c5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:04:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 17:04:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 17:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 17:24:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 17:24:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 17:24:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:24:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 17:24:11 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 03:35:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:40:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:40:27 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:42:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:42:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:42:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:42:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:42:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:42:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:42:53 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:42:53 GMT
USER fluent
# Wed, 04 Oct 2023 21:42:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:42:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b29af6ac0ecb75a158fdf7571ade02faed1a4aa6fc5bd2eefd201a0686a6ce`  
		Last Modified: Wed, 20 Sep 2023 17:32:54 GMT  
		Size: 9.2 MB (9239734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6f9342d6283449d4e6a6eea4286d06b0ae7a6ea0a2bbb2111d3ef48ff50de`  
		Last Modified: Wed, 20 Sep 2023 17:32:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbedbec01f8b12afd8e620c071485bbd918587fbad95da8d6ac048b9c9583817`  
		Last Modified: Wed, 20 Sep 2023 17:35:18 GMT  
		Size: 32.0 MB (31987301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb62b23a503adaec47d8f2cde776b6fca83cf2e9fd45d0631b48dda45c6189`  
		Last Modified: Wed, 20 Sep 2023 17:35:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d38e6a212faa1bc197138d82c6f35cc0097878381369cb71120936a803032b8`  
		Last Modified: Wed, 04 Oct 2023 21:43:29 GMT  
		Size: 35.0 MB (34996039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad995cb0a86d77940ed923ade6ac79a62caab9d8ba226eb9971bab43b1ab2b31`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30e7c3ab5d68afa0386cd1241a1fdec34bbebb383e83aca88584e06fff72b`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4272c33d9eeea733a22b38f8a2e718b7238c16c5f57ae8d6d082ae8e4016789c`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:76948e96d0f641bd0bd9b86561f6faab74ffd1e1cc6c336c98855f07ce4dba39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112611087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58757be068118885ce7fc4db9982326318baa9a5211cd968418da2e328f9ce9a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:18 GMT
ADD file:51db29acb4893b446fcf8a93f7fa809201b49d6ea62a009ab14002cafd3ac4a8 in / 
# Wed, 20 Sep 2023 00:42:18 GMT
CMD ["bash"]
# Thu, 21 Sep 2023 01:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Sep 2023 01:26:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 21 Sep 2023 01:26:59 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_MAJOR=3.1
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 21 Sep 2023 02:04:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 21 Sep 2023 02:04:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 21 Sep 2023 02:04:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 21 Sep 2023 02:04:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 02:04:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 21 Sep 2023 02:04:52 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 08:53:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:39:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:39:43 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:43:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:43:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:43:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:43:12 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:43:12 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:43:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:43:12 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:43:12 GMT
USER fluent
# Wed, 04 Oct 2023 21:43:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:43:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:091eb56f13f4be91ea9416e1b67e2c1f228b5e023f447dda2d3f5c56e57ff871`  
		Last Modified: Wed, 20 Sep 2023 00:47:36 GMT  
		Size: 32.4 MB (32397092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdeb7582a6d800657686c88ebc983eda0b560ea4ef37e0715353e8e80cd8201`  
		Last Modified: Thu, 21 Sep 2023 02:21:15 GMT  
		Size: 12.0 MB (11992494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c219df1668a2db62954869e3a509504299893ee3cf6cebf9d736f5bf594ec227`  
		Last Modified: Thu, 21 Sep 2023 02:21:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b48be9f16d364beb0ec41ab016d537dd64d14a5080f6636c1ad4e3970cbb5ad`  
		Last Modified: Thu, 21 Sep 2023 02:23:45 GMT  
		Size: 31.2 MB (31181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79a12719cdb5761c7591ed09a09f17e59395fb5c60edfb9425da8a48f03852d`  
		Last Modified: Thu, 21 Sep 2023 02:23:41 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16292b28f2a05817a064d0008ba03816f093c3b31532faead557604f291f5c`  
		Last Modified: Wed, 04 Oct 2023 21:43:51 GMT  
		Size: 37.0 MB (37036586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c71a72fc0506420a9ebf1743f4f2144791e5d73f4c0799cb349368bc1c351`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7012f06ec22954ba00ad4cdc7442b37ea20fa88dcd549effdea904600ecafa1`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2909c3a5ff1f87ab312888cc173b0aef2aa071be118de6b39bf8fcca95986c`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f1ecd0f518884d1b4ffcd6ee75f937f713ffe133cde8129e79f47a16d3c0065c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116530469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2552df8c12de59dd353dbd10e35ce278d06b25a055a8022e2889536c5f49d8f5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 07:53:28 GMT
ADD file:906774443118f59963ef3b425ff702af4588c1cf1d7c32f6f72fff8b1af50339 in / 
# Wed, 20 Sep 2023 07:53:30 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:12:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 17:12:59 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:56:46 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 17:56:47 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 17:56:47 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 18:00:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 18:00:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 18:00:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 18:00:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 18:00:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 18:00:53 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 08:59:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:19:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:19:29 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:26:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:26:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:26:41 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:26:42 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:26:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:26:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:26:43 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:26:44 GMT
USER fluent
# Wed, 04 Oct 2023 21:26:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:26:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e64bfb4d4b8bfd61a4dccfc651ce802e40087cdf6029b3cbf1710fa529e70fcb`  
		Last Modified: Wed, 20 Sep 2023 08:50:44 GMT  
		Size: 35.3 MB (35291079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf0ba5b0c31b0e064199e2b7e8413c8d210cd48c2da5f41d1b37d290c24e928`  
		Last Modified: Wed, 20 Sep 2023 18:09:48 GMT  
		Size: 10.5 MB (10478117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4dc88996ed822489c9256ca20f5ae828f925e41ce85b3a4ba30b2cd0eb1a1c`  
		Last Modified: Wed, 20 Sep 2023 18:09:45 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd095dd071295a48de821361e02927c3fcd2e9b2690e208f30072eaa257eb17`  
		Last Modified: Wed, 20 Sep 2023 18:12:38 GMT  
		Size: 32.8 MB (32791662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59320c201ba2e0bd7a58a39625e6dfc078aa38e4f2b560653865411221cf228`  
		Last Modified: Wed, 20 Sep 2023 18:12:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db303ba7a01dd9d17f3989b3bf58aecd153fba49d1488287da9985620d511339`  
		Last Modified: Wed, 04 Oct 2023 21:27:26 GMT  
		Size: 38.0 MB (37966525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c503ce14adedcfc072da9d5c647856d51d472bab6e0d158ac61be0d848a9e5e`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616273d4752f0f9023f55aaa503ac6f355f5c2d6ad9fc5370dbbc6e0f59d616e`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8607fdd16533ef061661234a5d966aa14acc73b85cd12ceaf898efb7363c2c46`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:a12b81aa89a8e6490043003955e96d5a77a9abbe68e935fcaab2fa4cd36c19b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (112004408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f51f524c3671634748bbd0372a83e8b03c280e8531d4e512c45ed7de84f90`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 08:56:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 08:56:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 08:56:43 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 09:10:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 09:10:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:10:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:10:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:10:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 09:10:44 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 16:26:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:48:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:48:24 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:53:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:53:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:53:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:53:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:53:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:53:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:53:53 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:53:53 GMT
USER fluent
# Wed, 04 Oct 2023 21:53:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:53:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47321672005a5546412628ab690cb78399b29b2071581b69a293552bd7afb13`  
		Last Modified: Wed, 20 Sep 2023 09:15:02 GMT  
		Size: 8.9 MB (8859599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90563f0388be4071d58831fa5ec6ce689e243f8b0af47dc8443b79f46f19ab2`  
		Last Modified: Wed, 20 Sep 2023 09:15:00 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459b793e3cb97616aa193779322a4d1a1e153023a57b23a2af4be49a00dc0af4`  
		Last Modified: Wed, 20 Sep 2023 09:16:08 GMT  
		Size: 32.4 MB (32444906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa5c5b25320032ec83fc03c191b7d48f3ba498c5dceaab681159452ebeb016a`  
		Last Modified: Wed, 20 Sep 2023 09:16:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da9111b4ca3bca6b10bf4bcdeefe1f2a9fcdb735fa1b4c2c068828a62f6bee`  
		Last Modified: Wed, 04 Oct 2023 21:54:44 GMT  
		Size: 41.0 MB (41043682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfd5b0e2a4a0d2a91957f07a2c518280fc759eb010520f50bb3e0f47739627b`  
		Last Modified: Wed, 04 Oct 2023 21:54:37 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d2b96f5161ffecb62a9b08a03dd276a89b04136694a684e6a307bbc988d692`  
		Last Modified: Wed, 04 Oct 2023 21:54:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ceb5c4bd4cc8f365608d89a33cbecfecedba80ba76c1fbde759cb224da78123`  
		Last Modified: Wed, 04 Oct 2023 21:54:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.2-1.1`

```console
$ docker pull fluentd@sha256:0e1090ed3901b0f4a5a4faabb10f91c4fa680da2e2a6503c23832ade8212bfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16.2-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:13ee83b11a86c4e6593b5acb8e647c22cf1b9feef123612b9dd586465ed05254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25155206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e2964bb824f2aacb86d0ca3170997802f000be1eff97299b1188ec8611aa4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:08:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:19:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:20:26 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:20:27 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:20:27 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:20:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:20:27 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:20:27 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:20:28 GMT
USER fluent
# Wed, 04 Oct 2023 21:20:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:20:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8827fca176be13b72bd568162360ca80ecd8eef45b5ef68c80b3a000f503183`  
		Last Modified: Wed, 04 Oct 2023 21:24:01 GMT  
		Size: 21.8 MB (21774385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6515ca36e5cdb6a7919ba7b37f2dd0f2d248776d1f9485d6447a039b1ed9452`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3543c7841d7564df2c94d78f0afdedb172e4b82c8677f5b5ad85136ac57a1dd3`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57e8a5d5c2f2b9f7e226a62461f9a68d3c8ffaa5b73c8a92b05fa8bcc8d1d96`  
		Last Modified: Wed, 04 Oct 2023 21:23:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-1.1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:059df7f5071014b62e8cd4b3d56609cecbf887753011d04bb0a3b0e017a60f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f827678b99b7f0450b51a46ea4bbded99d2af7bc05d42292069f7ac5157f0b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:13:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:49:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:50:18 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 20:50:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 20:50:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 20:50:19 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 20:50:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 20:50:19 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 20:50:19 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 20:50:19 GMT
USER fluent
# Wed, 04 Oct 2023 20:50:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 20:50:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553532437e6782bb598563089e5c9712ae1d947bcc0e062ecde36c20a8de5397`  
		Last Modified: Wed, 04 Oct 2023 20:50:32 GMT  
		Size: 20.7 MB (20733532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d15a3c0a2634f3d4b2d360f2e9ef8cf7e467483d959c924d4ce1b9de09ff85`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8122aae986d2ea394888a2a35bdfe989c9aff09557fab2b7a3a40c97ca077`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff8c6799857457a342c810fea84380b9f681c2db904dff6caef780d7e0671d3`  
		Last Modified: Wed, 04 Oct 2023 20:50:29 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:8197de0448a2f17bf11f791952b47dada2db36420039a914517dd8fdb9576cd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9bbe3c7c4f2dc30c2ce5307d8fe088a8d1b645f876b2f86ab83f0c04d8ec45`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 10:36:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:39:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:40:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:40:19 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:40:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:40:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:40:20 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:40:20 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:40:20 GMT
USER fluent
# Wed, 04 Oct 2023 21:40:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:40:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3e3f59536119d5781bb641b631d26d36f17086051a8b4afd4683c39e225bb4`  
		Last Modified: Wed, 04 Oct 2023 21:43:15 GMT  
		Size: 21.4 MB (21368773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf0687a8f3c9c7bc2628fceef6bc75e8642ea202b985274313ddd137d5bde2f`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3742a3460d54456ef66da27bcb397c738c7a99e48ee599835c2d5d935c0ca`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3629019f4be74a2ec436a05f010c0abc28d5060bf37a9e2874366f5210daf2`  
		Last Modified: Wed, 04 Oct 2023 21:43:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:b83b7e92a71b743f967b5288f16a4df4305653819cdb9aaf2d900d46f42909fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24437573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a376d83aefcf980ab1d54ab6eaa54cfe7efd64178c391d35d5dd01828a219566`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:24:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:38:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:39:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:39:33 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:39:33 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:39:33 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:39:33 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:39:33 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:39:33 GMT
USER fluent
# Wed, 04 Oct 2023 21:39:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:39:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82eeb7c7b7c8cf58216ccf047891a51db52037f8d73338c44bda2aade1939af3`  
		Last Modified: Wed, 04 Oct 2023 21:43:33 GMT  
		Size: 21.0 MB (21021575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfff789f4260eb9a35837ba5b55a3132024fc07f657c0a7a36b4c537c93e532`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3634708fd9e50993123edc881d3b612bd7abd118c86c10ae821d153c32627d6c`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecb450aa2b0fc245622f769a3b887b13b78e60ea9541bfea6ff5c6ec88b683f`  
		Last Modified: Wed, 04 Oct 2023 21:43:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:00ec95a9165ad95d580fdd03e9ac2168cbb48c84e783c0d256d2ff2e2c012649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (25008964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2fe004ba2fc07cbd3ae7d50e767842934d907a6ed122619d1e28e110d0efec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:06:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:16:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:18:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:18:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:19:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:19:01 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:19:02 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:19:02 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:19:03 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:19:04 GMT
USER fluent
# Wed, 04 Oct 2023 21:19:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:19:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686c1faa62490a3123a764ff1f9eb8f56b2d2370ca4c57a0df250c27b5f8c567`  
		Last Modified: Wed, 04 Oct 2023 21:27:05 GMT  
		Size: 21.6 MB (21615400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f05d8caa8bd28ac8b74de327805f02bd7541b08a3ff76a90a8edd0ec3be3a8`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74498b595a258f3d58d08ebcd2d0594e2b0954606ac5dce53681b96fa90a9fb6`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3e2fa1f46398cb0c1fce47f3a1dbbe71e2ec584d77c560feebc765d18af209`  
		Last Modified: Wed, 04 Oct 2023 21:26:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:4bf9c8b8442eecc11953268bb67197327b4dcd7dfd3c362260c96a431e13fe04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29998860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7f6f610b30aa0140b9f9276b6b90fa1f395f17501f7fcdb7a94c3614ef43a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:41:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:47:54 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:48:02 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:48:02 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:48:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:48:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:48:04 GMT
ENV LD_PRELOAD=
# Wed, 04 Oct 2023 21:48:05 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:48:05 GMT
USER fluent
# Wed, 04 Oct 2023 21:48:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:48:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a7cda602ceb77b991077268ddf9794e50138b46af24af519f72acbdec17298`  
		Last Modified: Wed, 04 Oct 2023 21:54:17 GMT  
		Size: 26.8 MB (26820669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977fa9f658a1932ce284e4498f48f661f20e5b5bf01569236217ff0fcc0ea6cc`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a7282d352e8cc5052eaaf24c4c0a054b8e7ed3b58082b373ae53b18b4c2eab`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8e091f38fa0c967d062af79901add256471c87f62cbe5b767a12554086282`  
		Last Modified: Wed, 04 Oct 2023 21:54:12 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.2-debian-1.1`

```console
$ docker pull fluentd@sha256:6837a7996018724262b7a137a0c4c1f384bea795399eb86e0462ee868cb064e0
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

### `fluentd:v1.16.2-debian-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:f200e644039dfa3f839fc1c73904dce942ef04ec88b0c9ae05e685caf2a67d74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110795278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d9408d2dad8032d0bd665a5fd63a17effd39370144dc62818b9ed2b9c7d3cc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:27:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 06:27:27 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 06:41:13 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 06:43:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 06:43:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 06:43:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 06:43:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:43:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 06:43:35 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 21:31:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:20:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:20:42 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:23:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:23:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:23:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:23:36 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:23:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:23:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:23:36 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:23:36 GMT
USER fluent
# Wed, 04 Oct 2023 21:23:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:23:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ca7bee443bcb2df6fefe9dac000084301fc7d16f30007cce46c92524471903`  
		Last Modified: Wed, 20 Sep 2023 06:50:07 GMT  
		Size: 10.0 MB (10018565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d78b16832011f333fa852282b9f3c7b3b7cd3b9ab0f01181f8472d920bfa3e`  
		Last Modified: Wed, 20 Sep 2023 06:50:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b8e6c0d8f9f5a8acca62bcb7a9d7464c9205c295981de5befd83371272f67a`  
		Last Modified: Wed, 20 Sep 2023 06:51:24 GMT  
		Size: 32.6 MB (32626043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab3abb9ee9e3896dce2a66b8eb85f169e73013676286679473487a41d2bea6a`  
		Last Modified: Wed, 20 Sep 2023 06:51:21 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85164087d4bc5eef452f202e56a612be46cfd399b318a3ee58fac055731a06f0`  
		Last Modified: Wed, 04 Oct 2023 21:24:19 GMT  
		Size: 36.7 MB (36729874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5ad63792f74db3749877216b562ebe66d814ef6d51df4a177531feeb03a76`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee99a08dae6683b5d82c25693fb4fb33e34d6bffad7eaf9fd31da9676b4e130c`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc254b21491a471884ee81ba2e1945d2cceeb5cd24d075c25672d5142ce6215b`  
		Last Modified: Wed, 04 Oct 2023 21:24:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d9d60ace3bab736674e8c64d953e632d1778b6c7dcdffe4a0b4f974ea50a7c18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102458094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e7a22aded18cd1e74585559b68e098580569c37eb606e0bcace0fd09c3067`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 00:50:22 GMT
ADD file:3fafe6196c5a5c30a92e0a7cca16de98eecf20e6e40a25a36034e3512e0fceb7 in / 
# Wed, 20 Sep 2023 00:50:23 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:30:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 15:30:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 15:51:30 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 15:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 15:54:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 15:54:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 15:54:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 15:54:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 15:54:22 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 16:34:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:48:12 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:48:12 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 20:51:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 20:51:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 20:51:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 20:51:11 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 20:51:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 20:51:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 20:51:11 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 20:51:11 GMT
USER fluent
# Wed, 04 Oct 2023 20:51:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 20:51:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:028bb77b977c8effa899ef4c01139f4f5f8d4c94b82f792204b8bca21961fceb`  
		Last Modified: Wed, 20 Sep 2023 00:55:38 GMT  
		Size: 28.9 MB (28919128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9538e3dc01c29ae56a826f9cbba76b6b47353b9d132cb68de0fa524f6cb125d`  
		Last Modified: Wed, 20 Sep 2023 16:01:35 GMT  
		Size: 8.6 MB (8631273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18650dd925389614ca5b08f7a162bd9d218cf719ef9ec8b50064b152c8b34fbe`  
		Last Modified: Wed, 20 Sep 2023 16:01:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b96a26706b2482d7176dbc3a93cdf10d270cc1f4976d5fb7bba7043d2f6e13d`  
		Last Modified: Wed, 20 Sep 2023 16:04:21 GMT  
		Size: 31.2 MB (31165971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a56b30aaf08329d2afbb2b06eedda50e785d3d9c4c92e17900a10d81250889`  
		Last Modified: Wed, 20 Sep 2023 16:04:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ce750eb8b852e31b69f6e97a1d833e90be58ae24eeb24afcf2ee5d2594a68`  
		Last Modified: Wed, 04 Oct 2023 20:51:29 GMT  
		Size: 33.7 MB (33738652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbdcc873c804c68c7f71f1aa190332ae014939ce45813ce8f1b505582b5378`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930676d4cc662adbfad85c7d7bd0752fb75a7cc438b43639c1e6a398b6fa9eca`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7f3a289c84c246b43ba8d7cbb8f6ef4c96e8378a303ba3709401ab1724c47b`  
		Last Modified: Wed, 04 Oct 2023 20:51:24 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:ea45f8c8a9e5eccf441f2718fc1c536b47faaf657cb314ba56901429a4987b9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98853900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2dcd19c9c3de3633a3c82e44dee8d2138a7011109ce1e7afeb39883457dd3e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:35 GMT
ADD file:551a2d9bfca9d524e2144fe06246864ea8480a1567dda26f14d99255ae6a89de in / 
# Wed, 20 Sep 2023 04:57:36 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 14:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 14:54:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 14:54:57 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 15:08:17 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 15:08:17 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 15:08:18 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 15:10:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 15:10:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 15:10:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 15:10:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 15:10:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 15:10:24 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 01:36:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 20:57:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 20:57:22 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:00:09 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:00:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:00:10 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:00:10 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:00:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:00:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:00:10 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:00:10 GMT
USER fluent
# Wed, 04 Oct 2023 21:00:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:00:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:69e0260f539f90d8f61c40f7822d9c002aa082311842094f6e640751432c0b02`  
		Last Modified: Wed, 20 Sep 2023 05:01:55 GMT  
		Size: 26.6 MB (26578623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c262874c18502eaebc1081376669eb2b2e7fb9f7a9fe6a4634c044e412efa0`  
		Last Modified: Wed, 20 Sep 2023 15:16:42 GMT  
		Size: 8.1 MB (8139904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e37ae340d374a97c0f1eb711de5189c2cc07b01942451baa5bbf13587de3bf3`  
		Last Modified: Wed, 20 Sep 2023 15:16:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c975675033940075215d9bcb1b170567388e0703b2a3d674ca92097754308d4`  
		Last Modified: Wed, 20 Sep 2023 15:18:07 GMT  
		Size: 31.0 MB (31035579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685e94c1f05662f63d3d386b8ee5522f869f117fe856e2d1fec7e384bc40a0`  
		Last Modified: Wed, 20 Sep 2023 15:18:03 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510054dc14b50afd3553abfa2a44de2ab6f08fe00e16933a17cd41107653996c`  
		Last Modified: Wed, 04 Oct 2023 21:00:25 GMT  
		Size: 33.1 MB (33096707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac5e4bed14e34d22e344678721980524e7c564638576a7cc3b60e55bb46bd08`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab33fe2b5f373806de8011c79b608a6f848162504c93ed39b439fba2660629af`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03cfd51cd12e2a97cf36e187173f1eb2c7419fea120e33fd9eb9f0086bd49ca`  
		Last Modified: Wed, 04 Oct 2023 21:00:20 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a5d2a5aa08d1da833490b164653107f503b30f4970595cf72c1f8e4d2f66b647
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106289025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a68e564693a122e9f46a2343449f5bc548cc3c91553a69b82d8a0d82e9f90c5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:04:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 17:04:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 17:22:26 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 17:24:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 17:24:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 17:24:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 17:24:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:24:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 17:24:11 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 03:35:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:40:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:40:27 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:42:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:42:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:42:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:42:52 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:42:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:42:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:42:53 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:42:53 GMT
USER fluent
# Wed, 04 Oct 2023 21:42:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:42:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b29af6ac0ecb75a158fdf7571ade02faed1a4aa6fc5bd2eefd201a0686a6ce`  
		Last Modified: Wed, 20 Sep 2023 17:32:54 GMT  
		Size: 9.2 MB (9239734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6f9342d6283449d4e6a6eea4286d06b0ae7a6ea0a2bbb2111d3ef48ff50de`  
		Last Modified: Wed, 20 Sep 2023 17:32:52 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbedbec01f8b12afd8e620c071485bbd918587fbad95da8d6ac048b9c9583817`  
		Last Modified: Wed, 20 Sep 2023 17:35:18 GMT  
		Size: 32.0 MB (31987301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb62b23a503adaec47d8f2cde776b6fca83cf2e9fd45d0631b48dda45c6189`  
		Last Modified: Wed, 20 Sep 2023 17:35:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d38e6a212faa1bc197138d82c6f35cc0097878381369cb71120936a803032b8`  
		Last Modified: Wed, 04 Oct 2023 21:43:29 GMT  
		Size: 35.0 MB (34996039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad995cb0a86d77940ed923ade6ac79a62caab9d8ba226eb9971bab43b1ab2b31`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30e7c3ab5d68afa0386cd1241a1fdec34bbebb383e83aca88584e06fff72b`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4272c33d9eeea733a22b38f8a2e718b7238c16c5f57ae8d6d082ae8e4016789c`  
		Last Modified: Wed, 04 Oct 2023 21:43:25 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:76948e96d0f641bd0bd9b86561f6faab74ffd1e1cc6c336c98855f07ce4dba39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112611087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58757be068118885ce7fc4db9982326318baa9a5211cd968418da2e328f9ce9a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:18 GMT
ADD file:51db29acb4893b446fcf8a93f7fa809201b49d6ea62a009ab14002cafd3ac4a8 in / 
# Wed, 20 Sep 2023 00:42:18 GMT
CMD ["bash"]
# Thu, 21 Sep 2023 01:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Sep 2023 01:26:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 21 Sep 2023 01:26:59 GMT
ENV LANG=C.UTF-8
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_MAJOR=3.1
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 21 Sep 2023 02:01:01 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 21 Sep 2023 02:04:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 21 Sep 2023 02:04:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 21 Sep 2023 02:04:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 21 Sep 2023 02:04:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 02:04:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 21 Sep 2023 02:04:52 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 08:53:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:39:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:39:43 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:43:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:43:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:43:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:43:12 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:43:12 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:43:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:43:12 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:43:12 GMT
USER fluent
# Wed, 04 Oct 2023 21:43:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:43:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:091eb56f13f4be91ea9416e1b67e2c1f228b5e023f447dda2d3f5c56e57ff871`  
		Last Modified: Wed, 20 Sep 2023 00:47:36 GMT  
		Size: 32.4 MB (32397092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdeb7582a6d800657686c88ebc983eda0b560ea4ef37e0715353e8e80cd8201`  
		Last Modified: Thu, 21 Sep 2023 02:21:15 GMT  
		Size: 12.0 MB (11992494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c219df1668a2db62954869e3a509504299893ee3cf6cebf9d736f5bf594ec227`  
		Last Modified: Thu, 21 Sep 2023 02:21:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b48be9f16d364beb0ec41ab016d537dd64d14a5080f6636c1ad4e3970cbb5ad`  
		Last Modified: Thu, 21 Sep 2023 02:23:45 GMT  
		Size: 31.2 MB (31181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79a12719cdb5761c7591ed09a09f17e59395fb5c60edfb9425da8a48f03852d`  
		Last Modified: Thu, 21 Sep 2023 02:23:41 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16292b28f2a05817a064d0008ba03816f093c3b31532faead557604f291f5c`  
		Last Modified: Wed, 04 Oct 2023 21:43:51 GMT  
		Size: 37.0 MB (37036586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c71a72fc0506420a9ebf1743f4f2144791e5d73f4c0799cb349368bc1c351`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7012f06ec22954ba00ad4cdc7442b37ea20fa88dcd549effdea904600ecafa1`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2909c3a5ff1f87ab312888cc173b0aef2aa071be118de6b39bf8fcca95986c`  
		Last Modified: Wed, 04 Oct 2023 21:43:43 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:f1ecd0f518884d1b4ffcd6ee75f937f713ffe133cde8129e79f47a16d3c0065c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116530469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2552df8c12de59dd353dbd10e35ce278d06b25a055a8022e2889536c5f49d8f5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 07:53:28 GMT
ADD file:906774443118f59963ef3b425ff702af4588c1cf1d7c32f6f72fff8b1af50339 in / 
# Wed, 20 Sep 2023 07:53:30 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:12:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 17:12:59 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:56:46 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 17:56:47 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 17:56:47 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 18:00:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 18:00:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 18:00:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 18:00:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 18:00:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 18:00:53 GMT
CMD ["irb"]
# Thu, 21 Sep 2023 08:59:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:19:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:19:29 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:26:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:26:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:26:41 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:26:42 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:26:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:26:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:26:43 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:26:44 GMT
USER fluent
# Wed, 04 Oct 2023 21:26:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:26:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e64bfb4d4b8bfd61a4dccfc651ce802e40087cdf6029b3cbf1710fa529e70fcb`  
		Last Modified: Wed, 20 Sep 2023 08:50:44 GMT  
		Size: 35.3 MB (35291079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf0ba5b0c31b0e064199e2b7e8413c8d210cd48c2da5f41d1b37d290c24e928`  
		Last Modified: Wed, 20 Sep 2023 18:09:48 GMT  
		Size: 10.5 MB (10478117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4dc88996ed822489c9256ca20f5ae828f925e41ce85b3a4ba30b2cd0eb1a1c`  
		Last Modified: Wed, 20 Sep 2023 18:09:45 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd095dd071295a48de821361e02927c3fcd2e9b2690e208f30072eaa257eb17`  
		Last Modified: Wed, 20 Sep 2023 18:12:38 GMT  
		Size: 32.8 MB (32791662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59320c201ba2e0bd7a58a39625e6dfc078aa38e4f2b560653865411221cf228`  
		Last Modified: Wed, 20 Sep 2023 18:12:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db303ba7a01dd9d17f3989b3bf58aecd153fba49d1488287da9985620d511339`  
		Last Modified: Wed, 04 Oct 2023 21:27:26 GMT  
		Size: 38.0 MB (37966525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c503ce14adedcfc072da9d5c647856d51d472bab6e0d158ac61be0d848a9e5e`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616273d4752f0f9023f55aaa503ac6f355f5c2d6ad9fc5370dbbc6e0f59d616e`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8607fdd16533ef061661234a5d966aa14acc73b85cd12ceaf898efb7363c2c46`  
		Last Modified: Wed, 04 Oct 2023 21:27:17 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.2-debian-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:a12b81aa89a8e6490043003955e96d5a77a9abbe68e935fcaab2fa4cd36c19b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (112004408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f51f524c3671634748bbd0372a83e8b03c280e8531d4e512c45ed7de84f90`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 08:56:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 08:56:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Sep 2023 08:56:43 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 20 Sep 2023 09:08:13 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 20 Sep 2023 09:10:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Sep 2023 09:10:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:10:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:10:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:10:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 20 Sep 2023 09:10:44 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 16:26:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 04 Oct 2023 21:48:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 04 Oct 2023 21:48:24 GMT
ENV TINI_VERSION=0.18.0
# Wed, 04 Oct 2023 21:53:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 04 Oct 2023 21:53:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 04 Oct 2023 21:53:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 04 Oct 2023 21:53:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 04 Oct 2023 21:53:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 04 Oct 2023 21:53:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 04 Oct 2023 21:53:53 GMT
EXPOSE 24224 5140
# Wed, 04 Oct 2023 21:53:53 GMT
USER fluent
# Wed, 04 Oct 2023 21:53:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 04 Oct 2023 21:53:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47321672005a5546412628ab690cb78399b29b2071581b69a293552bd7afb13`  
		Last Modified: Wed, 20 Sep 2023 09:15:02 GMT  
		Size: 8.9 MB (8859599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90563f0388be4071d58831fa5ec6ce689e243f8b0af47dc8443b79f46f19ab2`  
		Last Modified: Wed, 20 Sep 2023 09:15:00 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459b793e3cb97616aa193779322a4d1a1e153023a57b23a2af4be49a00dc0af4`  
		Last Modified: Wed, 20 Sep 2023 09:16:08 GMT  
		Size: 32.4 MB (32444906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa5c5b25320032ec83fc03c191b7d48f3ba498c5dceaab681159452ebeb016a`  
		Last Modified: Wed, 20 Sep 2023 09:16:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da9111b4ca3bca6b10bf4bcdeefe1f2a9fcdb735fa1b4c2c068828a62f6bee`  
		Last Modified: Wed, 04 Oct 2023 21:54:44 GMT  
		Size: 41.0 MB (41043682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfd5b0e2a4a0d2a91957f07a2c518280fc759eb010520f50bb3e0f47739627b`  
		Last Modified: Wed, 04 Oct 2023 21:54:37 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d2b96f5161ffecb62a9b08a03dd276a89b04136694a684e6a307bbc988d692`  
		Last Modified: Wed, 04 Oct 2023 21:54:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ceb5c4bd4cc8f365608d89a33cbecfecedba80ba76c1fbde759cb224da78123`  
		Last Modified: Wed, 04 Oct 2023 21:54:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
