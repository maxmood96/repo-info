## `fluentd:latest`

```console
$ docker pull fluentd@sha256:5244218ec2029380bb4d6eb4c6eb9fc0317805fba43770c85adc0e5249ab8e32
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
$ docker pull fluentd@sha256:0041aa53f7ec368a40a5b01b3019dc3f975d7f07c7381d0dca0f2de0c7078db6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19202602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f846a973029c4ac357617a3758c1d486a2527a927092f1b97c0fc59126eefe`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:38:02 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 19 Jul 2022 23:38:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 19 Jul 2022 23:38:48 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 19 Jul 2022 23:38:49 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 19 Jul 2022 23:38:49 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 19 Jul 2022 23:38:49 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 19 Jul 2022 23:38:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 19 Jul 2022 23:38:49 GMT
ENV LD_PRELOAD=
# Tue, 19 Jul 2022 23:38:49 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 19 Jul 2022 23:38:49 GMT
EXPOSE 24224 5140
# Tue, 19 Jul 2022 23:38:49 GMT
USER fluent
# Tue, 19 Jul 2022 23:38:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 19 Jul 2022 23:38:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75866a6b2770e8b31f85ea24c051a5c03d492660bcdb35e8cd785471039c07c`  
		Last Modified: Tue, 19 Jul 2022 23:39:12 GMT  
		Size: 16.4 MB (16381070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e9367632bfedf4ac4a7c9a5e1219c31d859c25618f859c28fdf7d15ad0550`  
		Last Modified: Tue, 19 Jul 2022 23:39:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20ed5123a37894d4bd3971dfccd5afb27c7d400bf5f9ab2dc070cf6690e0bf2`  
		Last Modified: Tue, 19 Jul 2022 23:39:10 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1766e2df13a984406f9fe6f1b6e46c8f5b370f1a384f62ead15699704ef0c2d`  
		Last Modified: Tue, 19 Jul 2022 23:39:10 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:8d1bc7233876f084b3fdaf9201d9f06ceccbd66a2d7a82bc6baed0714ece6211
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18485307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5cfd1c9dd951c0b4875712b55c43357d7453f69119e2b2ee598a2f120d07ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:15 GMT
ADD file:19dc757ba128952e4f765f774da40913195379a34f272ac71f3b3a651adf2740 in / 
# Tue, 19 Jul 2022 22:50:16 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:14:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Jul 2022 00:14:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 20 Jul 2022 00:16:19 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 20 Jul 2022 00:16:22 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 20 Jul 2022 00:16:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 20 Jul 2022 00:16:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 20 Jul 2022 00:16:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Jul 2022 00:16:24 GMT
ENV LD_PRELOAD=
# Wed, 20 Jul 2022 00:16:24 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 20 Jul 2022 00:16:24 GMT
EXPOSE 24224 5140
# Wed, 20 Jul 2022 00:16:25 GMT
USER fluent
# Wed, 20 Jul 2022 00:16:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Jul 2022 00:16:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ecfe29996dc654c28c0e2c4726e34d251c79330ce39875ae8fbb5462d2695d5a`  
		Last Modified: Tue, 19 Jul 2022 22:51:54 GMT  
		Size: 2.6 MB (2625483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83880417b8e1d93315351d4b1a05d72cec112bed25505e935120cd05965aea0e`  
		Last Modified: Wed, 20 Jul 2022 00:17:11 GMT  
		Size: 15.9 MB (15857618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b61f765100eafdfeabf46aaa6f0c3958a8eb4f61ab185af21b09a8287060b01`  
		Last Modified: Wed, 20 Jul 2022 00:17:01 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3153b2297daa54746fb1890441136b7352362f4dc6dd8193e6b16432be2099`  
		Last Modified: Wed, 20 Jul 2022 00:17:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0938d4a485e16ef7c787e2c5feb6fe3c0c812e4f2d5db7665b3c98f2f7c59859`  
		Last Modified: Wed, 20 Jul 2022 00:17:00 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:3fe7b8a7ba111e45de8ef57528ab6fb5018105b689da8261044e8c7ef9dd58e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19036688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a44a62ea9d3376c5b5802ff70866dc70c9b7c8cae9cc2448833a43873c5fe3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 05:57:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Jul 2022 05:57:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 20 Jul 2022 05:58:45 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 20 Jul 2022 05:58:45 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 20 Jul 2022 05:58:47 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 20 Jul 2022 05:58:48 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 20 Jul 2022 05:58:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Jul 2022 05:58:49 GMT
ENV LD_PRELOAD=
# Wed, 20 Jul 2022 05:58:50 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 20 Jul 2022 05:58:51 GMT
EXPOSE 24224 5140
# Wed, 20 Jul 2022 05:58:52 GMT
USER fluent
# Wed, 20 Jul 2022 05:58:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Jul 2022 05:58:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2fe96531fd9472ea920d41f865bee575d1bb8ba5de9fbf5712668679b0ff86`  
		Last Modified: Wed, 20 Jul 2022 05:59:43 GMT  
		Size: 16.3 MB (16313345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3395f244805a2857d3354abdb90d6940628c712e435386591f834c49e9fe173`  
		Last Modified: Wed, 20 Jul 2022 05:59:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcd7d20da5629691c1e3908ae30fe3a8abc0d66992633d4b1eca7430fb29955`  
		Last Modified: Wed, 20 Jul 2022 05:59:40 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda13b6e8606215d56328a71a283b93f8dc343d5b32056aad847192c2b5ec4b`  
		Last Modified: Wed, 20 Jul 2022 05:59:40 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:ea6570baac3902be3f0d11f7bc91717f6b35e23c490f1b27f67196c602e0fa32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18724290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5185eff52fac4e4d36c219fa50f80f199feee2507740f040c0b3c77b171e4267`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:48 GMT
ADD file:216b59d90f7e2b47e8e2db0e1ab68a5709b4ed1fc33a98d40089570dedd3b4cb in / 
# Tue, 19 Jul 2022 22:38:48 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:33:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 19 Jul 2022 23:33:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Tue, 19 Jul 2022 23:34:40 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Tue, 19 Jul 2022 23:34:41 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Tue, 19 Jul 2022 23:34:43 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Tue, 19 Jul 2022 23:34:44 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Tue, 19 Jul 2022 23:34:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 19 Jul 2022 23:34:45 GMT
ENV LD_PRELOAD=
# Tue, 19 Jul 2022 23:34:46 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Tue, 19 Jul 2022 23:34:47 GMT
EXPOSE 24224 5140
# Tue, 19 Jul 2022 23:34:48 GMT
USER fluent
# Tue, 19 Jul 2022 23:34:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 19 Jul 2022 23:34:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:77bace7fb30573dc3142aca393994871a56867f2e249e3e412697ed19e0735e4`  
		Last Modified: Tue, 19 Jul 2022 22:39:46 GMT  
		Size: 2.8 MB (2820956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b357e0b415e234114b15893ce1038cfdb1347def87a55def3905f39378262c`  
		Last Modified: Tue, 19 Jul 2022 23:35:24 GMT  
		Size: 15.9 MB (15901180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397a2bae804d74cd2a434298c071ebb98aa8cb7928ca9a3d19eb2273f6b7ccdf`  
		Last Modified: Tue, 19 Jul 2022 23:35:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62531317ae2607c2e1c7dc2f1adeefb0cc27de45a7101dfe043a872c11a4aee4`  
		Last Modified: Tue, 19 Jul 2022 23:35:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9047ac928347340994e4fe508ab8ecdbc4fd3219e1e9b86ee3811a92277c587`  
		Last Modified: Tue, 19 Jul 2022 23:35:22 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3a154fbfef8018f51daadffba4b022f094dfc4e34c6b00441cff33cd671ef29c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19274125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1074abf6eee060be9e7b9d340db6948f39df1da4630124b771ec5efadedc64bf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:27:03 GMT
ADD file:eb7e6ef6aa9d85f173cbf5d2b4398bdfdcc69912dacc8023920100cbdf033327 in / 
# Tue, 19 Jul 2022 22:27:06 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:40:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Jul 2022 06:40:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 20 Jul 2022 06:42:40 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 20 Jul 2022 06:43:15 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 20 Jul 2022 06:43:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 20 Jul 2022 06:43:28 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 20 Jul 2022 06:43:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Jul 2022 06:43:52 GMT
ENV LD_PRELOAD=
# Wed, 20 Jul 2022 06:44:10 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 20 Jul 2022 06:44:18 GMT
EXPOSE 24224 5140
# Wed, 20 Jul 2022 06:44:29 GMT
USER fluent
# Wed, 20 Jul 2022 06:44:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Jul 2022 06:44:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6193977833871e9bbffe277f6d183f69eb24184f8ebf196455d2bb21c9152cd2`  
		Last Modified: Tue, 19 Jul 2022 22:28:20 GMT  
		Size: 2.8 MB (2815156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850f96c71d4a1b188dae2ac6ef937b82490e37cbb2c2cadd465056156a8756a`  
		Last Modified: Wed, 20 Jul 2022 06:45:26 GMT  
		Size: 16.5 MB (16456756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6ff473718228e860ba24ea0b328690d59bbc7bee24869065555e7815527f9`  
		Last Modified: Wed, 20 Jul 2022 06:45:23 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d311207e4b980a9f44087b9cefb76fa36e7be471e56a07e31542a90699c9bd9`  
		Last Modified: Wed, 20 Jul 2022 06:45:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c1326a3921f11942b1c3c525680bfa54ea0e6ef8a1f2dceb5450ffeeaa3082`  
		Last Modified: Wed, 20 Jul 2022 06:45:23 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:caa3883002bf0d220e56c8cae03ae4b9cb59fa27129329996cc45833ed21c37f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f5a43a323377aab44ea7885fad96d88c7b43b505a6f88ab68aba8f10532c40`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 19 Jul 2022 22:42:24 GMT
ADD file:5fe2b0e3ef35cc888c633b75e54dc7eb4ff746a5ce6f9ba5aedc3ea2928d077e in / 
# Tue, 19 Jul 2022 22:42:25 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 01:45:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Jul 2022 01:45:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.14.0
# Wed, 20 Jul 2022 01:46:22 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.10.18  && gem install json -v 2.4.1  && gem install async-http -v 0.54.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.14.0  && gem install bigdecimal -v 1.4.4  && gem install resolv -v 0.2.1  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test
# Wed, 20 Jul 2022 01:46:25 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 20 Jul 2022 01:46:25 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 20 Jul 2022 01:46:25 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 20 Jul 2022 01:46:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Jul 2022 01:46:26 GMT
ENV LD_PRELOAD=
# Wed, 20 Jul 2022 01:46:26 GMT
ENV RUBYLIB=/usr/lib/ruby/gems/2.7.0/gems/resolv-0.2.1/lib
# Wed, 20 Jul 2022 01:46:26 GMT
EXPOSE 24224 5140
# Wed, 20 Jul 2022 01:46:26 GMT
USER fluent
# Wed, 20 Jul 2022 01:46:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Jul 2022 01:46:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1a99e19db362ebd2927fb2a1efc264ef3789cda1f093cb68f927252d173c4019`  
		Last Modified: Tue, 19 Jul 2022 22:43:32 GMT  
		Size: 2.6 MB (2605443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb04dd1faa9b4e1813c995c49fb2356a19e51c69d379b5b3e3df84c8c5aea01b`  
		Last Modified: Wed, 20 Jul 2022 01:46:56 GMT  
		Size: 16.3 MB (16318380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de21ff08c4ac6d89bc258c0c033ca7e0ed550175cfbd1ee4d9dfb9fd3d81581`  
		Last Modified: Wed, 20 Jul 2022 01:46:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b74497672e75002022bb6fb4d50d48443c8a4d28d029b0ab1d01591970e1b0`  
		Last Modified: Wed, 20 Jul 2022 01:46:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b8baa8644e3a87686e6c20d4f48f664f9cf3f72d2abaf4c552163f869fdc58`  
		Last Modified: Wed, 20 Jul 2022 01:46:53 GMT  
		Size: 457.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
