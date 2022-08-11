## `fluentd:latest`

```console
$ docker pull fluentd@sha256:2c544d1dd625eb5a4550b40088478542738f1c6d98f00056a0263c4fb53c80ea
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
$ docker pull fluentd@sha256:67323a2910fb5b4368f54abe047d3f6f77e165fdef4a226909e1826847c9d541
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20354937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0cbc6f7a85d0e3b700a4d0221e538b1679da23ce1a2d1c65435779b5a86e0b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:09:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 09 Aug 2022 19:09:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 09 Aug 2022 19:10:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 09 Aug 2022 19:10:22 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 09 Aug 2022 19:10:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 09 Aug 2022 19:10:22 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 09 Aug 2022 19:10:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 09 Aug 2022 19:10:23 GMT
ENV LD_PRELOAD=
# Tue, 09 Aug 2022 19:10:23 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 09 Aug 2022 19:10:23 GMT
EXPOSE 24224 5140
# Tue, 09 Aug 2022 19:10:23 GMT
USER fluent
# Tue, 09 Aug 2022 19:10:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 09 Aug 2022 19:10:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fdfdb90be4e2976ae1504323c7dfbd8f83e6093ac1f29a7e8c99e3bc113c1e`  
		Last Modified: Tue, 09 Aug 2022 19:10:50 GMT  
		Size: 17.5 MB (17525165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2853ea95f56358be211cebd39cf73e9c22981732f8051e27d2fef8aba70a574`  
		Last Modified: Tue, 09 Aug 2022 19:10:47 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d682038a250a6d16bb9ce04dcc5b29c162489e6e479cc3adf151946eb66c6ad`  
		Last Modified: Tue, 09 Aug 2022 19:10:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96742fcceaa603050c45b5de784a47afb4fc6d7322752289a9b51e3b3183640`  
		Last Modified: Tue, 09 Aug 2022 19:10:47 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:8718335c54e01f691e64a97a58caf6672fdc97b262445b4448df09f4c8abeedb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19562808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c953ec509f7e1b53893dd25d0b2efe0a3bdcc23f2c27c21f8448a3780f5b8520`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:41:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Aug 2022 00:41:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Thu, 11 Aug 2022 00:42:43 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Thu, 11 Aug 2022 00:42:44 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 11 Aug 2022 00:42:44 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 11 Aug 2022 00:42:44 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 11 Aug 2022 00:42:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Aug 2022 00:42:44 GMT
ENV LD_PRELOAD=
# Thu, 11 Aug 2022 00:42:44 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Thu, 11 Aug 2022 00:42:44 GMT
EXPOSE 24224 5140
# Thu, 11 Aug 2022 00:42:45 GMT
USER fluent
# Thu, 11 Aug 2022 00:42:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Aug 2022 00:42:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b664f4ab0a5afb15d2c4fba0f2de5a39846103f0aa33fbe5850c9d7ec2e41d1f`  
		Last Modified: Thu, 11 Aug 2022 00:43:07 GMT  
		Size: 16.9 MB (16927070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe267ba9eebd9a8ba75a89fad74d6309d3d62be94aec9887ab1ad9aa026ecc6f`  
		Last Modified: Thu, 11 Aug 2022 00:43:05 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ac97e6a57fbac79a4e7384df07623f5163311ced2ad16bc01e0d81196b412c`  
		Last Modified: Thu, 11 Aug 2022 00:43:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6305de8830b8f610085574bea7f36f93270e9ed5c76928b07d8ceca85455b0c`  
		Last Modified: Thu, 11 Aug 2022 00:43:05 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ca6062f6262531333a7e811efcb2a57cde2b0a6572e72e2b0a34022e9c46c3f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20172109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf85244dc0a730f24f5f3d1937a97ad841fad259775f15cb53313b96cb565ada`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:40:07 GMT
ADD file:f23c059b4312458fbf0fc018d4695f36157a3eb6e5a83167912a39f9a738f4eb in / 
# Tue, 09 Aug 2022 17:40:07 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:05:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 09 Aug 2022 19:05:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 09 Aug 2022 19:06:27 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 09 Aug 2022 19:06:28 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 09 Aug 2022 19:06:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 09 Aug 2022 19:06:30 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 09 Aug 2022 19:06:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 09 Aug 2022 19:06:31 GMT
ENV LD_PRELOAD=
# Tue, 09 Aug 2022 19:06:32 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 09 Aug 2022 19:06:33 GMT
EXPOSE 24224 5140
# Tue, 09 Aug 2022 19:06:34 GMT
USER fluent
# Tue, 09 Aug 2022 19:06:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 09 Aug 2022 19:06:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:25f523f0e93b2b5fa676c15d91b90f08ee4de7a160874e6c52ea452929d5a7cc`  
		Last Modified: Tue, 09 Aug 2022 17:41:17 GMT  
		Size: 2.7 MB (2722126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5bfb09c1c8e3eba5f4f340fef48a69bc102e247ae251481fd251ab2aa23e92`  
		Last Modified: Tue, 09 Aug 2022 19:07:09 GMT  
		Size: 17.4 MB (17447833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a268e7f70e79853ee6cfdb023b018fbbe6b19d32a9a5ea4e7e454f41cbcd9853`  
		Last Modified: Tue, 09 Aug 2022 19:07:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b7bee12d96226a72274d5e211ea2665830183a410827bf61d7182aa7dd594f`  
		Last Modified: Tue, 09 Aug 2022 19:07:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3345bed44d8e98f7a374999d139df8610817bde4b146ab1ceaf0c56f7c62f6`  
		Last Modified: Tue, 09 Aug 2022 19:07:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:1e89aec0b65ea0b69a04e9c5446ff1243a10249acfa8a5f52e0aa0dc812f8502
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19802444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaae684641a2f6034a3fbfd5e63f3a049e5e6ed4c43ae68ab45700fc122e1de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:01 GMT
ADD file:03626e5c8651aac4c8e12fa9ad40c1ed5c1cf728846275ccb6a154d33f64567e in / 
# Tue, 09 Aug 2022 17:39:01 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:09:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 10 Aug 2022 01:09:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 10 Aug 2022 01:09:56 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 10 Aug 2022 01:09:56 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 10 Aug 2022 01:09:58 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 10 Aug 2022 01:09:59 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 10 Aug 2022 01:09:59 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 10 Aug 2022 01:10:00 GMT
ENV LD_PRELOAD=
# Wed, 10 Aug 2022 01:10:01 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 10 Aug 2022 01:10:02 GMT
EXPOSE 24224 5140
# Wed, 10 Aug 2022 01:10:03 GMT
USER fluent
# Wed, 10 Aug 2022 01:10:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 10 Aug 2022 01:10:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bb0cde90e12d5206d6293dc0d9e482ef617f00aa0d4286810adb0700c188ede4`  
		Last Modified: Tue, 09 Aug 2022 17:40:12 GMT  
		Size: 2.8 MB (2829774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0289063c12e18492172015e820439dff026528aac7210e674a5deb81aeeda0`  
		Last Modified: Wed, 10 Aug 2022 01:10:40 GMT  
		Size: 17.0 MB (16970513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb1d451394dd0b8d59425937088c1fdfa1e98940fc9f8a2d52f5c3e74a9d754`  
		Last Modified: Wed, 10 Aug 2022 01:10:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f51fd0821153758665532d3d715280365f081a21f4388963b39a4fff035dd`  
		Last Modified: Wed, 10 Aug 2022 01:10:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab96ba6380c7427f16a3658c8ab21578a6cb764cdfa4f6e77bac9455677a62b2`  
		Last Modified: Wed, 10 Aug 2022 01:10:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:883f4c01b0bdf7663f8c7e164e4f87605247edc1bdc4c473dc494c3f984eaf67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20392023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c607cb6346e3428e8a59f6fe41bab2b8e76120c1a945e4654a1d5685b5e4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:40 GMT
ADD file:484b4a940601ea0eee86b54ed0bbab522d82063504d5e404297522cec2da2410 in / 
# Tue, 09 Aug 2022 17:17:41 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:08:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 09 Aug 2022 18:08:57 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 09 Aug 2022 18:10:28 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 09 Aug 2022 18:10:30 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 09 Aug 2022 18:10:31 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 09 Aug 2022 18:10:31 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 09 Aug 2022 18:10:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 09 Aug 2022 18:10:32 GMT
ENV LD_PRELOAD=
# Tue, 09 Aug 2022 18:10:32 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 09 Aug 2022 18:10:33 GMT
EXPOSE 24224 5140
# Tue, 09 Aug 2022 18:10:33 GMT
USER fluent
# Tue, 09 Aug 2022 18:10:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 09 Aug 2022 18:10:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:92709067783fb8dba06b304866998cd7cbe11f3ceaaf90c0c74832e1d007c1f7`  
		Last Modified: Tue, 09 Aug 2022 17:19:09 GMT  
		Size: 2.8 MB (2818026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d65297cfa4619fd76539ff0a3ea92b670505b55d214190e4fe0fec8162901`  
		Last Modified: Tue, 09 Aug 2022 18:14:00 GMT  
		Size: 17.6 MB (17571794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36205a093da057b7507ecc826476a80c738ef592242102b8290f5937c94f0bdf`  
		Last Modified: Tue, 09 Aug 2022 18:13:51 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b55613777f231e095a1ccb0e7be0b4b9d1ac04e4c6d64d6d3b819302046ac`  
		Last Modified: Tue, 09 Aug 2022 18:13:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519179f234df848662564d56447ca3dcb0af79940a4e257757822732945e708f`  
		Last Modified: Tue, 09 Aug 2022 18:13:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:960c61bf0422a3a967bc2f7149e24e70f3593792f3ec3574c10b958fa9158a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20079883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2122de3d81cbda66a23dabf6704d4525b476af99daeb4248f930ee6849371bb1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 09 Aug 2022 17:42:10 GMT
ADD file:a30f78876e4c7fee29ec287fe4b4f48621431512b0e81289b1fe23b3d6f7660f in / 
# Tue, 09 Aug 2022 17:42:11 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:43:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 09 Aug 2022 18:43:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 09 Aug 2022 18:44:05 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 09 Aug 2022 18:44:06 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 09 Aug 2022 18:44:06 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 09 Aug 2022 18:44:07 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 09 Aug 2022 18:44:07 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 09 Aug 2022 18:44:07 GMT
ENV LD_PRELOAD=
# Tue, 09 Aug 2022 18:44:07 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 09 Aug 2022 18:44:07 GMT
EXPOSE 24224 5140
# Tue, 09 Aug 2022 18:44:07 GMT
USER fluent
# Tue, 09 Aug 2022 18:44:07 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 09 Aug 2022 18:44:07 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:43943356f3daa5170be0f37f440cbf412003a7271fe424841157976e33a9c418`  
		Last Modified: Tue, 09 Aug 2022 17:43:11 GMT  
		Size: 2.6 MB (2611905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c023e46fdba7afe5ec20f3be1cd360e15d44458f790835c9233d54d006b3a4a`  
		Last Modified: Tue, 09 Aug 2022 18:44:38 GMT  
		Size: 17.5 MB (17465777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f873def13ddb21b3f8546d10b41fe91a83e227aca075ed1191452c07cff172`  
		Last Modified: Tue, 09 Aug 2022 18:44:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef268158caff1dc4c081a45da063c87e2b84fda4946c74bb5f9b3168103d6f2`  
		Last Modified: Tue, 09 Aug 2022 18:44:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f4bf73b7c35f1222224d0936e2d780937bceca43105de08ad0255dd0e9040a`  
		Last Modified: Tue, 09 Aug 2022 18:44:35 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
