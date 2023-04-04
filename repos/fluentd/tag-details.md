<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.0-1.0`](#fluentdv1160-10)
-	[`fluentd:v1.16.0-debian-1.0`](#fluentdv1160-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:7025883ec528c64536f5a566c6780b15b63d23ed51ac40a40e646fe84edf3ff2
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
$ docker pull fluentd@sha256:0df9599d013815bc02c8046b1df6e8137bef905fd5d4d15612ef4c7506528af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20382342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bb541bfc9908f21cb0dd96aaaacb54d846895aecd4b03c4a16707d4f4f13e4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 21:15:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 06 Oct 2022 21:15:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Thu, 06 Oct 2022 21:15:59 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Thu, 06 Oct 2022 21:16:00 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 06 Oct 2022 21:16:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 06 Oct 2022 21:16:00 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 06 Oct 2022 21:16:01 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 06 Oct 2022 21:16:01 GMT
ENV LD_PRELOAD=
# Thu, 06 Oct 2022 21:16:01 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Thu, 06 Oct 2022 21:16:01 GMT
EXPOSE 24224 5140
# Thu, 06 Oct 2022 21:16:01 GMT
USER fluent
# Thu, 06 Oct 2022 21:16:01 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 06 Oct 2022 21:16:01 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9fa3e4dcfc088d46409de9b0d40c5fc4940e4c7a6975ef269dd6a7e8a6a6a`  
		Last Modified: Thu, 06 Oct 2022 21:16:26 GMT  
		Size: 17.6 MB (17552569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7bec4ded6c3da9e4647897ca5b68a1c7d8e70bcfd0442325778e2753addd2`  
		Last Modified: Thu, 06 Oct 2022 21:16:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7caecdf56fe6b18386ddd1f5b3f445e694b76d8c72ffea129afc0f645c4692`  
		Last Modified: Thu, 06 Oct 2022 21:16:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cecf5130357297a55cad85eb73b9c571a0d6d42377e70e805ff8fd7e29adb7`  
		Last Modified: Thu, 06 Oct 2022 21:16:23 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65d2a7a2677137edd41e9d5c64ff89acfc281743d7ef32412c813534067daa2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23810626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3c8433a0c3f42b76c1509792a291d63f86697031c4f1d8a3b5f7559d859cf7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Tue, 04 Apr 2023 00:07:39 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Tue, 04 Apr 2023 00:07:40 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 04 Apr 2023 00:07:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Apr 2023 00:07:40 GMT
ENV LD_PRELOAD=
# Tue, 04 Apr 2023 00:07:40 GMT
EXPOSE 24224 5140
# Tue, 04 Apr 2023 00:07:40 GMT
USER fluent
# Tue, 04 Apr 2023 00:07:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Apr 2023 00:07:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba6d6f8ecfc29753c59b0ba643012ce6907ab381fb451d451a93c0c17012e6`  
		Last Modified: Tue, 04 Apr 2023 00:07:57 GMT  
		Size: 20.7 MB (20697612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf6c016ad72c78a88d7b7b26a7cf1d74fd021da7b18ad6459839400bb684668`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63640f7ce6faef8e9f6a1c2363709bccc7380527b37269499ed9c29c0bba312`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1774ae06f6540f8048b494472e2863501a9defbb42df777d641b26195c23f1`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f0a2b35718ed6aeb5dfa63f71fe1bb4c9536ff0716723c1381ed15a43397ae1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20183367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb924fbdb3d9747d5621b71908001ddf98333f879af3ebbfeef93d699f2677`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:56 GMT
ADD file:f23c059b4312458fbf0fc018d4695f36157a3eb6e5a83167912a39f9a738f4eb in / 
# Thu, 10 Nov 2022 20:39:56 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:41:33 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 10 Nov 2022 21:41:33 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Thu, 10 Nov 2022 21:42:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Thu, 10 Nov 2022 21:42:12 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 10 Nov 2022 21:42:12 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 10 Nov 2022 21:42:12 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 10 Nov 2022 21:42:12 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 10 Nov 2022 21:42:12 GMT
ENV LD_PRELOAD=
# Thu, 10 Nov 2022 21:42:12 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Thu, 10 Nov 2022 21:42:12 GMT
EXPOSE 24224 5140
# Thu, 10 Nov 2022 21:42:12 GMT
USER fluent
# Thu, 10 Nov 2022 21:42:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 10 Nov 2022 21:42:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:25f523f0e93b2b5fa676c15d91b90f08ee4de7a160874e6c52ea452929d5a7cc`  
		Last Modified: Tue, 09 Aug 2022 17:41:17 GMT  
		Size: 2.7 MB (2722126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943400719ecc8dd281506bcfbeacdfe71001445486b5dca2cee2337f5b22d0c2`  
		Last Modified: Thu, 10 Nov 2022 21:44:00 GMT  
		Size: 17.5 MB (17459038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a24bdbe56f1da427c4e69fc430a098c16ab68b5ea63a248877090fc9e89984`  
		Last Modified: Thu, 10 Nov 2022 21:43:57 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74291d8e80b8d1091254b1ac1e9106904ba335d7be86b101ae92b1941ad30f20`  
		Last Modified: Thu, 10 Nov 2022 21:43:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b5bf292ba846aa42a8ba9878c9fb4012c5c220de02c9ee04dff2046f263046`  
		Last Modified: Thu, 10 Nov 2022 21:43:57 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:b66541795230b2fdc7bf6cb992e970dc4748d1661b2247e7b6336fccb63a135c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19823898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658931d6dd91998c443e0aa2fe274c9d981066e7068552e304584def612377f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:01 GMT
ADD file:03626e5c8651aac4c8e12fa9ad40c1ed5c1cf728846275ccb6a154d33f64567e in / 
# Tue, 09 Aug 2022 17:39:01 GMT
CMD ["/bin/sh"]
# Thu, 02 Mar 2023 05:43:09 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 02 Mar 2023 05:43:09 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Thu, 02 Mar 2023 05:44:00 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Thu, 02 Mar 2023 05:44:00 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 02 Mar 2023 05:44:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 02 Mar 2023 05:44:00 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 02 Mar 2023 05:44:01 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 02 Mar 2023 05:44:01 GMT
ENV LD_PRELOAD=
# Thu, 02 Mar 2023 05:44:01 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Thu, 02 Mar 2023 05:44:01 GMT
EXPOSE 24224 5140
# Thu, 02 Mar 2023 05:44:01 GMT
USER fluent
# Thu, 02 Mar 2023 05:44:01 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 02 Mar 2023 05:44:01 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bb0cde90e12d5206d6293dc0d9e482ef617f00aa0d4286810adb0700c188ede4`  
		Last Modified: Tue, 09 Aug 2022 17:40:12 GMT  
		Size: 2.8 MB (2829774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007dd554939fa7dcd490b5dcf4cb724dc0e7a94b3aec395ff53821a844ed1d5c`  
		Last Modified: Thu, 02 Mar 2023 05:46:07 GMT  
		Size: 17.0 MB (16991923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0774b0475fe341424d65c4beed39e326aca33161d958eaebbff1efa8838aaf`  
		Last Modified: Thu, 02 Mar 2023 05:46:04 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d293a1001afabcbde858181c772ab38cdc84d75657c9401bb556d8649f4fb70`  
		Last Modified: Thu, 02 Mar 2023 05:46:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b20eb660dfe6dbf24e1962849d1fc76e32ca9b5004fe2aa2e17b55f647a8d3`  
		Last Modified: Thu, 02 Mar 2023 05:46:04 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:fa629c265dbdb5d8807f13fdc5f66cc0c192ae6daff666447a9192c2f50b30f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20423388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d62a279499a9175102ccbbd930054f6269d0f5f7cb95cd0222eb1178cc42ba`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:40 GMT
ADD file:484b4a940601ea0eee86b54ed0bbab522d82063504d5e404297522cec2da2410 in / 
# Tue, 09 Aug 2022 17:17:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:23:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 06 Oct 2022 20:23:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Thu, 06 Oct 2022 20:24:50 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Thu, 06 Oct 2022 20:24:53 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 06 Oct 2022 20:24:53 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 06 Oct 2022 20:24:53 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 06 Oct 2022 20:24:54 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 06 Oct 2022 20:24:54 GMT
ENV LD_PRELOAD=
# Thu, 06 Oct 2022 20:24:54 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Thu, 06 Oct 2022 20:24:54 GMT
EXPOSE 24224 5140
# Thu, 06 Oct 2022 20:24:55 GMT
USER fluent
# Thu, 06 Oct 2022 20:24:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 06 Oct 2022 20:24:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:92709067783fb8dba06b304866998cd7cbe11f3ceaaf90c0c74832e1d007c1f7`  
		Last Modified: Tue, 09 Aug 2022 17:19:09 GMT  
		Size: 2.8 MB (2818026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c076900adce70b7c3d31c631d52677dfc674e6d136423ed13e365bfea0d9bb45`  
		Last Modified: Thu, 06 Oct 2022 20:25:26 GMT  
		Size: 17.6 MB (17603156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffd94570f6e1867831f4ad21939b2b03a9ce2c5dfa4df81afbe8e50358dbc5f`  
		Last Modified: Thu, 06 Oct 2022 20:25:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7042d0234b589dfe0b2277327f7196d75b99509a3bfce6ca685e1f389b1f213`  
		Last Modified: Thu, 06 Oct 2022 20:25:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec0f74ee2d2468c4ae957e6e2e4380bfcda95647dbc0371c3a5674b8f1c4a4`  
		Last Modified: Thu, 06 Oct 2022 20:25:22 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:001d2a51a850037c96ed3ac4fa78cbcbd1221839de5da38b6634c6e9eba86a51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b3c4874df382cf8694342ff89e648274603b841bd70352f48306bedbbc493`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 23:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:27:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:28:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:28:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:28:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:28:50 GMT
ENV LD_PRELOAD=
# Mon, 03 Apr 2023 23:28:51 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:28:51 GMT
USER fluent
# Mon, 03 Apr 2023 23:28:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:28:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac5bd72fbffa874e5d0fe209c6a1b307198f205b8e4d5ec8f020526670649`  
		Last Modified: Mon, 03 Apr 2023 23:31:22 GMT  
		Size: 21.2 MB (21172560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a476a1392375893899c9adccc09d5de446342c3b3679c6b7d59b94001ec262d4`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cd03bd7b304700dfc5d69e003ba9fe11e67c6277731736c718afd73aa4fa54`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4921fcfe9790dd687de7cfeeb8e67b1cc300da3276d37aa99171ecfbc47b6e`  
		Last Modified: Mon, 03 Apr 2023 23:31:19 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:c8f958696ef2e17d14a51489e2f13e1716faac727f26d6fb5ed619d0738c5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; s390x

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65d2a7a2677137edd41e9d5c64ff89acfc281743d7ef32412c813534067daa2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23810626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3c8433a0c3f42b76c1509792a291d63f86697031c4f1d8a3b5f7559d859cf7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Tue, 04 Apr 2023 00:07:39 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Tue, 04 Apr 2023 00:07:40 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 04 Apr 2023 00:07:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Apr 2023 00:07:40 GMT
ENV LD_PRELOAD=
# Tue, 04 Apr 2023 00:07:40 GMT
EXPOSE 24224 5140
# Tue, 04 Apr 2023 00:07:40 GMT
USER fluent
# Tue, 04 Apr 2023 00:07:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Apr 2023 00:07:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba6d6f8ecfc29753c59b0ba643012ce6907ab381fb451d451a93c0c17012e6`  
		Last Modified: Tue, 04 Apr 2023 00:07:57 GMT  
		Size: 20.7 MB (20697612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf6c016ad72c78a88d7b7b26a7cf1d74fd021da7b18ad6459839400bb684668`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63640f7ce6faef8e9f6a1c2363709bccc7380527b37269499ed9c29c0bba312`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1774ae06f6540f8048b494472e2863501a9defbb42df777d641b26195c23f1`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:001d2a51a850037c96ed3ac4fa78cbcbd1221839de5da38b6634c6e9eba86a51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b3c4874df382cf8694342ff89e648274603b841bd70352f48306bedbbc493`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 23:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:27:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:28:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:28:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:28:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:28:50 GMT
ENV LD_PRELOAD=
# Mon, 03 Apr 2023 23:28:51 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:28:51 GMT
USER fluent
# Mon, 03 Apr 2023 23:28:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:28:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac5bd72fbffa874e5d0fe209c6a1b307198f205b8e4d5ec8f020526670649`  
		Last Modified: Mon, 03 Apr 2023 23:31:22 GMT  
		Size: 21.2 MB (21172560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a476a1392375893899c9adccc09d5de446342c3b3679c6b7d59b94001ec262d4`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cd03bd7b304700dfc5d69e003ba9fe11e67c6277731736c718afd73aa4fa54`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4921fcfe9790dd687de7cfeeb8e67b1cc300da3276d37aa99171ecfbc47b6e`  
		Last Modified: Mon, 03 Apr 2023 23:31:19 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:a8bcf812632906afdfd185837691e78ae42059d0125a27c8c7e10bbacfd6fba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	linux; s390x

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:942fbb6ef96523333a78f5ab305c24efb3486c972067774ccb43b2deae8485af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95261905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8ddc2c445ca2b4020d5202e9eeae14120c9c4007817d7c656d4a1e01ae85c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:44 GMT
ADD file:7595c7bfa6b3741f57a3ec7790e3108bb526244e52bb4a54548b8b5541e66616 in / 
# Thu, 23 Mar 2023 00:48:44 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:42:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 06:42:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 06:47:41 GMT
ENV RUBY_MAJOR=3.1
# Thu, 30 Mar 2023 19:00:30 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 30 Mar 2023 19:00:30 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 30 Mar 2023 19:02:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 19:02:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 19:02:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 19:02:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 19:02:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 19:02:39 GMT
CMD ["irb"]
# Mon, 03 Apr 2023 23:12:15 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:12:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:12:15 GMT
ENV TINI_VERSION=0.18.0
# Mon, 03 Apr 2023 23:15:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:15:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:15:06 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:15:07 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:15:07 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:15:07 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 03 Apr 2023 23:15:07 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:15:07 GMT
USER fluent
# Mon, 03 Apr 2023 23:15:07 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:15:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b83d345710cdef1626d1940689dd3160e5ce3e4f63b3154cf612c52b704baa66`  
		Last Modified: Thu, 23 Mar 2023 02:22:00 GMT  
		Size: 28.9 MB (28915852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01823b006e73c4ea0cff9c35ae3dce62fc987febd01d0a092b8ac2815d5246b1`  
		Last Modified: Fri, 24 Mar 2023 23:27:15 GMT  
		Size: 8.6 MB (8635898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dbe6acaf6962399719d4c660823c56b892af485f4e2596b748c9cd0724b9c1`  
		Last Modified: Fri, 24 Mar 2023 23:27:12 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e78b20864ab83fc7e0329e406a79ade96d4f76e5b7d02518a761d09109c878a`  
		Last Modified: Thu, 30 Mar 2023 20:49:57 GMT  
		Size: 31.2 MB (31165835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6bd7652282f7fef67562600ec96645d6f69afd7148bd96fcf2338f14fda129`  
		Last Modified: Thu, 30 Mar 2023 20:49:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa72e0fb53c78f2bb5e28287e2564cc778a9cc3f108f60194d953d88cca93cf`  
		Last Modified: Tue, 04 Apr 2023 00:19:44 GMT  
		Size: 26.5 MB (26541244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a040e51f0d0904dc704461487f6d32a29eec953099246b328f21677ca24a4ee1`  
		Last Modified: Tue, 04 Apr 2023 00:19:40 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f970057ef53b3683906d0d7b950d6f5dd92fea0d834c0f7cdac37bea6d07606a`  
		Last Modified: Tue, 04 Apr 2023 00:19:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f608622e1770272b304b55a84eb3224200c9e19a6a80dff37b166e0eb61433b4`  
		Last Modified: Tue, 04 Apr 2023 00:19:39 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:61575f83c479d25cf7821001a2cfa66038bf1cd8709eb94ba4dfbdcac71ecec2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98884414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db35df468c33fe5092a52e4899849c285514a2a80b0759f64e3dc3e0e336e1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:04:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:04:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 11:04:28 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 11:08:50 GMT
ENV RUBY_MAJOR=3.1
# Thu, 30 Mar 2023 18:53:15 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 30 Mar 2023 18:53:15 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 30 Mar 2023 18:55:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 18:55:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 18:55:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 18:55:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 18:55:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 18:55:13 GMT
CMD ["irb"]
# Mon, 03 Apr 2023 23:28:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:28:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:28:56 GMT
ENV TINI_VERSION=0.18.0
# Mon, 03 Apr 2023 23:31:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:31:03 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:31:03 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:31:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:31:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:31:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 03 Apr 2023 23:31:03 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:31:03 GMT
USER fluent
# Mon, 03 Apr 2023 23:31:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:31:03 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b9af96d3e722e82f7629031b0987250947fbdb2a8206dccca92c1619fb8929`  
		Last Modified: Thu, 23 Mar 2023 11:19:23 GMT  
		Size: 8.9 MB (8863610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59a5c6470be792bccee1395851606bf8f724f17e1ff5739ef9263875df729f`  
		Last Modified: Thu, 23 Mar 2023 11:19:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59dd1de97cd6a2c8d0f9521202d9e34c41b19728220deed1369b77dd87be66`  
		Last Modified: Thu, 30 Mar 2023 19:12:10 GMT  
		Size: 32.4 MB (32445106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f01f7bb1614c319af053459a9cd260edc96aac21be2d49e0651aca0727dcc`  
		Last Modified: Thu, 30 Mar 2023 19:12:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4947e4d6ca83043a92e5549f2fee48c32fd03d7b0448c52203b178ee1df59e`  
		Last Modified: Mon, 03 Apr 2023 23:31:31 GMT  
		Size: 27.9 MB (27925787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350890baf78ab1d5caeac50183b0564d3eb0220e574f9a8a9dd8aeced4513d31`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8decf9537301401dc59e52fd3ad9523f9315b2659c57225acf452b1d4643c8`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bf28f08285199ee9856ee7b66725de48925a0e36411555f33fb3f5f9de3a0`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-1.0`

```console
$ docker pull fluentd@sha256:c8f958696ef2e17d14a51489e2f13e1716faac727f26d6fb5ed619d0738c5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; s390x

### `fluentd:v1.16.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:65d2a7a2677137edd41e9d5c64ff89acfc281743d7ef32412c813534067daa2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23810626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3c8433a0c3f42b76c1509792a291d63f86697031c4f1d8a3b5f7559d859cf7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 04 Apr 2023 00:06:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Tue, 04 Apr 2023 00:07:39 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Tue, 04 Apr 2023 00:07:40 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 04 Apr 2023 00:07:40 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 04 Apr 2023 00:07:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 04 Apr 2023 00:07:40 GMT
ENV LD_PRELOAD=
# Tue, 04 Apr 2023 00:07:40 GMT
EXPOSE 24224 5140
# Tue, 04 Apr 2023 00:07:40 GMT
USER fluent
# Tue, 04 Apr 2023 00:07:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 04 Apr 2023 00:07:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba6d6f8ecfc29753c59b0ba643012ce6907ab381fb451d451a93c0c17012e6`  
		Last Modified: Tue, 04 Apr 2023 00:07:57 GMT  
		Size: 20.7 MB (20697612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf6c016ad72c78a88d7b7b26a7cf1d74fd021da7b18ad6459839400bb684668`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63640f7ce6faef8e9f6a1c2363709bccc7380527b37269499ed9c29c0bba312`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1774ae06f6540f8048b494472e2863501a9defbb42df777d641b26195c23f1`  
		Last Modified: Tue, 04 Apr 2023 00:07:53 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:001d2a51a850037c96ed3ac4fa78cbcbd1221839de5da38b6634c6e9eba86a51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880b3c4874df382cf8694342ff89e648274603b841bd70352f48306bedbbc493`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 23:27:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:27:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:28:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:28:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:28:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:28:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:28:50 GMT
ENV LD_PRELOAD=
# Mon, 03 Apr 2023 23:28:51 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:28:51 GMT
USER fluent
# Mon, 03 Apr 2023 23:28:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:28:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac5bd72fbffa874e5d0fe209c6a1b307198f205b8e4d5ec8f020526670649`  
		Last Modified: Mon, 03 Apr 2023 23:31:22 GMT  
		Size: 21.2 MB (21172560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a476a1392375893899c9adccc09d5de446342c3b3679c6b7d59b94001ec262d4`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cd03bd7b304700dfc5d69e003ba9fe11e67c6277731736c718afd73aa4fa54`  
		Last Modified: Mon, 03 Apr 2023 23:31:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4921fcfe9790dd687de7cfeeb8e67b1cc300da3276d37aa99171ecfbc47b6e`  
		Last Modified: Mon, 03 Apr 2023 23:31:19 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-debian-1.0`

```console
$ docker pull fluentd@sha256:a8bcf812632906afdfd185837691e78ae42059d0125a27c8c7e10bbacfd6fba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	linux; s390x

### `fluentd:v1.16.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:942fbb6ef96523333a78f5ab305c24efb3486c972067774ccb43b2deae8485af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95261905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8ddc2c445ca2b4020d5202e9eeae14120c9c4007817d7c656d4a1e01ae85c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:44 GMT
ADD file:7595c7bfa6b3741f57a3ec7790e3108bb526244e52bb4a54548b8b5541e66616 in / 
# Thu, 23 Mar 2023 00:48:44 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:42:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 06:42:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 06:47:41 GMT
ENV RUBY_MAJOR=3.1
# Thu, 30 Mar 2023 19:00:30 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 30 Mar 2023 19:00:30 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 30 Mar 2023 19:02:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 19:02:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 19:02:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 19:02:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 19:02:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 19:02:39 GMT
CMD ["irb"]
# Mon, 03 Apr 2023 23:12:15 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:12:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:12:15 GMT
ENV TINI_VERSION=0.18.0
# Mon, 03 Apr 2023 23:15:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:15:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:15:06 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:15:07 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:15:07 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:15:07 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 03 Apr 2023 23:15:07 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:15:07 GMT
USER fluent
# Mon, 03 Apr 2023 23:15:07 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:15:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b83d345710cdef1626d1940689dd3160e5ce3e4f63b3154cf612c52b704baa66`  
		Last Modified: Thu, 23 Mar 2023 02:22:00 GMT  
		Size: 28.9 MB (28915852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01823b006e73c4ea0cff9c35ae3dce62fc987febd01d0a092b8ac2815d5246b1`  
		Last Modified: Fri, 24 Mar 2023 23:27:15 GMT  
		Size: 8.6 MB (8635898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dbe6acaf6962399719d4c660823c56b892af485f4e2596b748c9cd0724b9c1`  
		Last Modified: Fri, 24 Mar 2023 23:27:12 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e78b20864ab83fc7e0329e406a79ade96d4f76e5b7d02518a761d09109c878a`  
		Last Modified: Thu, 30 Mar 2023 20:49:57 GMT  
		Size: 31.2 MB (31165835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6bd7652282f7fef67562600ec96645d6f69afd7148bd96fcf2338f14fda129`  
		Last Modified: Thu, 30 Mar 2023 20:49:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa72e0fb53c78f2bb5e28287e2564cc778a9cc3f108f60194d953d88cca93cf`  
		Last Modified: Tue, 04 Apr 2023 00:19:44 GMT  
		Size: 26.5 MB (26541244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a040e51f0d0904dc704461487f6d32a29eec953099246b328f21677ca24a4ee1`  
		Last Modified: Tue, 04 Apr 2023 00:19:40 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f970057ef53b3683906d0d7b950d6f5dd92fea0d834c0f7cdac37bea6d07606a`  
		Last Modified: Tue, 04 Apr 2023 00:19:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f608622e1770272b304b55a84eb3224200c9e19a6a80dff37b166e0eb61433b4`  
		Last Modified: Tue, 04 Apr 2023 00:19:39 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:61575f83c479d25cf7821001a2cfa66038bf1cd8709eb94ba4dfbdcac71ecec2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98884414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db35df468c33fe5092a52e4899849c285514a2a80b0759f64e3dc3e0e336e1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:04:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:04:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 11:04:28 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 11:08:50 GMT
ENV RUBY_MAJOR=3.1
# Thu, 30 Mar 2023 18:53:15 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 30 Mar 2023 18:53:15 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 30 Mar 2023 18:55:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 18:55:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 18:55:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 18:55:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 18:55:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 18:55:13 GMT
CMD ["irb"]
# Mon, 03 Apr 2023 23:28:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 03 Apr 2023 23:28:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Mon, 03 Apr 2023 23:28:56 GMT
ENV TINI_VERSION=0.18.0
# Mon, 03 Apr 2023 23:31:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Mon, 03 Apr 2023 23:31:03 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Mon, 03 Apr 2023 23:31:03 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Mon, 03 Apr 2023 23:31:03 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Mon, 03 Apr 2023 23:31:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 03 Apr 2023 23:31:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Mon, 03 Apr 2023 23:31:03 GMT
EXPOSE 24224 5140
# Mon, 03 Apr 2023 23:31:03 GMT
USER fluent
# Mon, 03 Apr 2023 23:31:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 03 Apr 2023 23:31:03 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b9af96d3e722e82f7629031b0987250947fbdb2a8206dccca92c1619fb8929`  
		Last Modified: Thu, 23 Mar 2023 11:19:23 GMT  
		Size: 8.9 MB (8863610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59a5c6470be792bccee1395851606bf8f724f17e1ff5739ef9263875df729f`  
		Last Modified: Thu, 23 Mar 2023 11:19:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59dd1de97cd6a2c8d0f9521202d9e34c41b19728220deed1369b77dd87be66`  
		Last Modified: Thu, 30 Mar 2023 19:12:10 GMT  
		Size: 32.4 MB (32445106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f01f7bb1614c319af053459a9cd260edc96aac21be2d49e0651aca0727dcc`  
		Last Modified: Thu, 30 Mar 2023 19:12:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4947e4d6ca83043a92e5549f2fee48c32fd03d7b0448c52203b178ee1df59e`  
		Last Modified: Mon, 03 Apr 2023 23:31:31 GMT  
		Size: 27.9 MB (27925787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350890baf78ab1d5caeac50183b0564d3eb0220e574f9a8a9dd8aeced4513d31`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8decf9537301401dc59e52fd3ad9523f9315b2659c57225acf452b1d4643c8`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bf28f08285199ee9856ee7b66725de48925a0e36411555f33fb3f5f9de3a0`  
		Last Modified: Mon, 03 Apr 2023 23:31:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
