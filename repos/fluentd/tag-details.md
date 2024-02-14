<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.2-1.1`](#fluentdv1162-11)
-	[`fluentd:v1.16.2-debian-1.1`](#fluentdv1162-debian-11)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:17971d152bb45b141229e30540cce2a60cc8161b0808cec59559b2f9f1ccd880
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
$ docker pull fluentd@sha256:452a80b204895bf4b4eea054b86b325c998d66dfb68efef1e4353155255cb656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25124717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657945478f75c86fb21bb10fe0d2cda0514d1238a50e3ec3b1d8a44427dd8f71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea4e9e4a232b968fa2c133e4b6c26306fce69db3a49e1adbe237c2756b837a`  
		Last Modified: Sat, 27 Jan 2024 00:55:01 GMT  
		Size: 21.7 MB (21743147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b793d0bb733b6c0501e4945f24a5216ad8adac79ff91b1e506103d9abe57891`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3666c0e762dbe8030ba636377f2f01016a0acded9549ca96d9e392653b87eae`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258e80c06270b6b9e41aa95e3deb27f6633e786f6da2d015bcc0997a1aacbb80`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9866a651eb47a333ee0b3d05b3fd33e038f86ebb8706080fb16eaa0d95c4d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.2 KB (797186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a4137a5b2b92b9d78cee1801b3b4f6bd15d2b657d8210aafe2fbcbc2a2be0`

```dockerfile
```

-	Layers:
	-	`sha256:39343fced00865c47b9ec3182866d3c37cf9bb08df09bbd2e30167d83eeb2251`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 783.3 KB (783258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904dbac96399ec5b51e90742ef716afde64a50d72de946a3944442c474de25e2`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1bc94a5c10d8c323faee2eb93e074d8820fba676f2ca827279c5ccfc03ed96bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23807441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f7dcacdbc6ea950f81747fa737f926c055202571e91c5148fb9e14d9baf36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
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
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2352fa41ac154f4e2e5367461993fada2899f2bfc547dbc0578c53a4b7cf23`  
		Last Modified: Tue, 30 Jan 2024 23:05:11 GMT  
		Size: 20.7 MB (20692158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b886caf0093c3e985b44ee4fe118cc5576df44157615afdf850699a2cb81dd`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bca9b4eac5a5009ca4f98a07e60d59c69a14dfda07e25cfa495fffc2d08023f`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e97aad89cf553919c43addbe6ca528c635496ddf00cd853d14f01185541e75`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:03fe08ed5c3f48a3524c3439d8842bee7b4d972fefb57f76f438f0d3e4479fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130111a706a16711523274cae9cc6fee7dfa99a8d9dbb1e1a9d93e6fd7df86c6`

```dockerfile
```

-	Layers:
	-	`sha256:1951357f9f6485a60fe8b27a9b1f03b5c192051955170f3b04604df6d9553ecb`  
		Last Modified: Tue, 30 Jan 2024 23:05:09 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f3b9319ebf791466f71195b66df8f1f25b49acadf325405b8cfebed75dd5c402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24594006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb271860983aeade86cbff5238b75ce5b238f8e12a5bbdb2ad7cb0504af9133`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01a23a2374d171c93b47bb26da2db576f451d45e0a27a667e37bd6cbb7e87b3`  
		Last Modified: Sun, 28 Jan 2024 00:24:36 GMT  
		Size: 21.3 MB (21333562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb368f87cba216705ce5a1331fb697a9629476403fa09f52f8d795c7eac2a0f0`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5955ef227ad76005af8d8aac2aac0fd0aa0cefbae5e1a62e3706fcdc8820a2c`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10d28c7a2db55c1b35d08d3ffef4b595e14954b6fb67e11417584a4af70b0bb`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:d03f120c24c0724b8b4f490ff9d22ac3440efbbb5c2943628f1215619651febe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.1 KB (797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df82fc3dfc87e368c73025f95bc0c481f23f9789b75e47cecef8b8841992f768`

```dockerfile
```

-	Layers:
	-	`sha256:8df571d423c02398e866de0225369606734ae0fabbb2c3a1295e614c1b705019`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 783.4 KB (783364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9ef17d7b14bfeda650020e0cca056efac85dfe5f0bdc1197a850af6d6a30c6`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:799c7569cd97e023ec2aaffbf926581afd93267c431735f1a00a1f0e6311fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24393632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81131e85bc077170a30424fb24c9a52e4a26f790dd5d3dfc9a0cc76fc8ed34f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
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
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df30d7d2f7b03c651d6cd536b7762833a63f793c9d140f59451eda04da81708`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 21.0 MB (20976292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec772bd6f3724ee81dd51ce8a8e326ab53bbba5c1f8d3485bd71e9108e707e2d`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b531889e4df9c460dd0641755a0cb8d817cc302e1ba39a7ead5972d4e8f15d48`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c973ed5e9ddf074f5d4d60a90a427d5ddb499e561218c22f3706cede95f2de`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:17cf841adbacedff8ee12522211672ee0cabc2a2bbc1b363e122f4acdd87c635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.9 KB (796946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d0ac82f23f0cc11c4b282edd3dd8a2c9d6766a1f6fc20348580c81551be5cd`

```dockerfile
```

-	Layers:
	-	`sha256:370c6020e183e6c33ba2997dcf4794975b5f6c4acca9bb32b22c0fd83eee378c`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 783.0 KB (783044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e86405cc79800f51fa7306a0be3378fecaf499bd7e1f515e00730748c811319`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 13.9 KB (13902 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9d1f51d62b0766c7f307d0f71dea4e4c584860f597975ed1111447c165994e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24982485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0548fee0d47e59d4c75dbabcce17ce175288a09f8918317c5402d53b906c2f8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94a6899c2def4c88392adce414ff838ba4d7981bbae29ca91a55dd5715b7b22`  
		Last Modified: Sat, 27 Jan 2024 11:37:55 GMT  
		Size: 21.6 MB (21588206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108fcff8ea7131dc2b08602727f72e98f9e375d6c513d31b77c437747be692d6`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b768671a5aafa1da69c21f008b76c96a8ea5c3e6d68fa2ed12edbef69ef713c`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf48df70f2bb2716bd9d9c43bde8d731bbb35fe6abe17baeb46a1282ae7ff30`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:9fcf2c79918734ae1561f5a9276bf6c8edfc2559d9514862d010f960e144f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.9 KB (795930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6734e6e41693a3ced230b9772cc97b4461e49555391703eaadfbfbb4c0976e6`

```dockerfile
```

-	Layers:
	-	`sha256:f7738f5e157f300fad15469848d06950b27ff8ef89e3142bacb794d49bdf21ac`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 782.1 KB (782135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d92909243fa607abd5b7dbbaf7bc7966f7e679d9a79a1ffbb023f201b72d7f3`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 13.8 KB (13795 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:25b64b8dfb564439d5b9d8b707991674d28c52a36bce3056a50213d536e66579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24346804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0aeb83a8a6ede2efef41019622d1fb5d27339963670fb42462db50f1ade75c7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
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
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93d5dc93ac82bd628be17a0099b3f938cd87353c260161347383112c62a0be`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 21.2 MB (21168114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a3cd5047901169f44a32cf5c9b1d016ea08fe9d7186bb5e08fb22f825c031`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f60e893142480493ed865854c0775913b4f08549b13281a21e303f0a91ae97d`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88530a7eb1af88b4d3e7b71a9933e6a2b0f58083886b2b3f88b732d57eed524a`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:bf00a1f1f40bfa28b432b19e88641284b09919bcaa2306da07b1cad78ffe2762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 KB (795286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041aa04f1a808235e7b591e5a79054b059752361bdc4298287674ee6a589a24e`

```dockerfile
```

-	Layers:
	-	`sha256:5853a8045217c8cb3f1067b6b94a23e20271259e53a89ac6bae192b368f18648`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 781.5 KB (781525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be5bc1784b74172b94ddbe1ee0c8174e50895a2bfb1c570062f50bfea9cbf0e`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 13.8 KB (13761 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:17971d152bb45b141229e30540cce2a60cc8161b0808cec59559b2f9f1ccd880
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

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:452a80b204895bf4b4eea054b86b325c998d66dfb68efef1e4353155255cb656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25124717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657945478f75c86fb21bb10fe0d2cda0514d1238a50e3ec3b1d8a44427dd8f71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea4e9e4a232b968fa2c133e4b6c26306fce69db3a49e1adbe237c2756b837a`  
		Last Modified: Sat, 27 Jan 2024 00:55:01 GMT  
		Size: 21.7 MB (21743147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b793d0bb733b6c0501e4945f24a5216ad8adac79ff91b1e506103d9abe57891`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3666c0e762dbe8030ba636377f2f01016a0acded9549ca96d9e392653b87eae`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258e80c06270b6b9e41aa95e3deb27f6633e786f6da2d015bcc0997a1aacbb80`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9866a651eb47a333ee0b3d05b3fd33e038f86ebb8706080fb16eaa0d95c4d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.2 KB (797186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a4137a5b2b92b9d78cee1801b3b4f6bd15d2b657d8210aafe2fbcbc2a2be0`

```dockerfile
```

-	Layers:
	-	`sha256:39343fced00865c47b9ec3182866d3c37cf9bb08df09bbd2e30167d83eeb2251`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 783.3 KB (783258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904dbac96399ec5b51e90742ef716afde64a50d72de946a3944442c474de25e2`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1bc94a5c10d8c323faee2eb93e074d8820fba676f2ca827279c5ccfc03ed96bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23807441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f7dcacdbc6ea950f81747fa737f926c055202571e91c5148fb9e14d9baf36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
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
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2352fa41ac154f4e2e5367461993fada2899f2bfc547dbc0578c53a4b7cf23`  
		Last Modified: Tue, 30 Jan 2024 23:05:11 GMT  
		Size: 20.7 MB (20692158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b886caf0093c3e985b44ee4fe118cc5576df44157615afdf850699a2cb81dd`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bca9b4eac5a5009ca4f98a07e60d59c69a14dfda07e25cfa495fffc2d08023f`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e97aad89cf553919c43addbe6ca528c635496ddf00cd853d14f01185541e75`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:03fe08ed5c3f48a3524c3439d8842bee7b4d972fefb57f76f438f0d3e4479fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130111a706a16711523274cae9cc6fee7dfa99a8d9dbb1e1a9d93e6fd7df86c6`

```dockerfile
```

-	Layers:
	-	`sha256:1951357f9f6485a60fe8b27a9b1f03b5c192051955170f3b04604df6d9553ecb`  
		Last Modified: Tue, 30 Jan 2024 23:05:09 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f3b9319ebf791466f71195b66df8f1f25b49acadf325405b8cfebed75dd5c402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24594006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb271860983aeade86cbff5238b75ce5b238f8e12a5bbdb2ad7cb0504af9133`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01a23a2374d171c93b47bb26da2db576f451d45e0a27a667e37bd6cbb7e87b3`  
		Last Modified: Sun, 28 Jan 2024 00:24:36 GMT  
		Size: 21.3 MB (21333562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb368f87cba216705ce5a1331fb697a9629476403fa09f52f8d795c7eac2a0f0`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5955ef227ad76005af8d8aac2aac0fd0aa0cefbae5e1a62e3706fcdc8820a2c`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10d28c7a2db55c1b35d08d3ffef4b595e14954b6fb67e11417584a4af70b0bb`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d03f120c24c0724b8b4f490ff9d22ac3440efbbb5c2943628f1215619651febe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.1 KB (797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df82fc3dfc87e368c73025f95bc0c481f23f9789b75e47cecef8b8841992f768`

```dockerfile
```

-	Layers:
	-	`sha256:8df571d423c02398e866de0225369606734ae0fabbb2c3a1295e614c1b705019`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 783.4 KB (783364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9ef17d7b14bfeda650020e0cca056efac85dfe5f0bdc1197a850af6d6a30c6`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:799c7569cd97e023ec2aaffbf926581afd93267c431735f1a00a1f0e6311fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24393632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81131e85bc077170a30424fb24c9a52e4a26f790dd5d3dfc9a0cc76fc8ed34f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
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
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df30d7d2f7b03c651d6cd536b7762833a63f793c9d140f59451eda04da81708`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 21.0 MB (20976292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec772bd6f3724ee81dd51ce8a8e326ab53bbba5c1f8d3485bd71e9108e707e2d`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b531889e4df9c460dd0641755a0cb8d817cc302e1ba39a7ead5972d4e8f15d48`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c973ed5e9ddf074f5d4d60a90a427d5ddb499e561218c22f3706cede95f2de`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:17cf841adbacedff8ee12522211672ee0cabc2a2bbc1b363e122f4acdd87c635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.9 KB (796946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d0ac82f23f0cc11c4b282edd3dd8a2c9d6766a1f6fc20348580c81551be5cd`

```dockerfile
```

-	Layers:
	-	`sha256:370c6020e183e6c33ba2997dcf4794975b5f6c4acca9bb32b22c0fd83eee378c`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 783.0 KB (783044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e86405cc79800f51fa7306a0be3378fecaf499bd7e1f515e00730748c811319`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 13.9 KB (13902 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9d1f51d62b0766c7f307d0f71dea4e4c584860f597975ed1111447c165994e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24982485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0548fee0d47e59d4c75dbabcce17ce175288a09f8918317c5402d53b906c2f8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94a6899c2def4c88392adce414ff838ba4d7981bbae29ca91a55dd5715b7b22`  
		Last Modified: Sat, 27 Jan 2024 11:37:55 GMT  
		Size: 21.6 MB (21588206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108fcff8ea7131dc2b08602727f72e98f9e375d6c513d31b77c437747be692d6`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b768671a5aafa1da69c21f008b76c96a8ea5c3e6d68fa2ed12edbef69ef713c`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf48df70f2bb2716bd9d9c43bde8d731bbb35fe6abe17baeb46a1282ae7ff30`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9fcf2c79918734ae1561f5a9276bf6c8edfc2559d9514862d010f960e144f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.9 KB (795930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6734e6e41693a3ced230b9772cc97b4461e49555391703eaadfbfbb4c0976e6`

```dockerfile
```

-	Layers:
	-	`sha256:f7738f5e157f300fad15469848d06950b27ff8ef89e3142bacb794d49bdf21ac`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 782.1 KB (782135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d92909243fa607abd5b7dbbaf7bc7966f7e679d9a79a1ffbb023f201b72d7f3`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 13.8 KB (13795 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:25b64b8dfb564439d5b9d8b707991674d28c52a36bce3056a50213d536e66579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24346804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0aeb83a8a6ede2efef41019622d1fb5d27339963670fb42462db50f1ade75c7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
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
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93d5dc93ac82bd628be17a0099b3f938cd87353c260161347383112c62a0be`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 21.2 MB (21168114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a3cd5047901169f44a32cf5c9b1d016ea08fe9d7186bb5e08fb22f825c031`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f60e893142480493ed865854c0775913b4f08549b13281a21e303f0a91ae97d`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88530a7eb1af88b4d3e7b71a9933e6a2b0f58083886b2b3f88b732d57eed524a`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bf00a1f1f40bfa28b432b19e88641284b09919bcaa2306da07b1cad78ffe2762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 KB (795286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041aa04f1a808235e7b591e5a79054b059752361bdc4298287674ee6a589a24e`

```dockerfile
```

-	Layers:
	-	`sha256:5853a8045217c8cb3f1067b6b94a23e20271259e53a89ac6bae192b368f18648`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 781.5 KB (781525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be5bc1784b74172b94ddbe1ee0c8174e50895a2bfb1c570062f50bfea9cbf0e`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 13.8 KB (13761 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:c5bcd66bca336b44f6f94273fe51d8e32a957571206bad023545c4fb8269c819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:c9a98f428cba1dc697ee8a86494d00a07fb93be9de01b986290d0ac2446ba19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101440601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f34768308894aaa647a9690d80ed28a24d3907233cb06f98d610ae7f633b6e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d1c7fb8f3d1b4044bd6d6d05c3d5221ab0b0d23b861034221a0729f3f5e05e`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 10.0 MB (10019247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3594d5f3eee1edd44e5d35581227c806baa7ff2d6e69c2dfedca42f3c57e6b3e`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037ad1326f63794876e13aa67f3385cc191f60fd7faecdd8b91203b9432bcef3`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 32.4 MB (32416622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0e740bbfc9d1f650471f1d467a1fdcdac4c78602c4a05e25ffe7e6e3365646`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcfcf2370d9f2d20a6e895856965b7af114f5be2815932a070bbd98c705bfe7`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 27.6 MB (27579386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614706cb9ca01928f60a27be7b8b12d82aaf6343af4cd68b30524ee9151e8d3c`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c860968a36a14d0ff0532b93c0d3a1a84aab89c6a78351d20a876b255fc2a17c`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5fa22ea2fdebbdce849aaec0ea2b55cec89a9e6313e22ec2ed57465c2a3f16`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c95129282c46b9a45162c1904c0a43bdfcf77ddb650a57f0e90d1273026083f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3650557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed8b2978f98dfede3d55bdd153fd3a14fdad2c3bd52aa4df342c5e557a4f63`

```dockerfile
```

-	Layers:
	-	`sha256:b480baa59ea6843baf5a07886e08e6e47491e3a7834127014ae5cd79fbc96060`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 3.6 MB (3628827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406dd3b1cce2eb10e57fc90c6bb36a346f32afc26ed9d233d7a80721726d6910`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 21.7 KB (21730 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:9a9b8a87a08242bcedded60ed2eff9a49ff8bb34177a2980ca052252c4168374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94720119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a7dacaeb38c9734bbe50b6ce4aaf118ee96025cba00d79b18725a477eef65`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:1b6dd4809e22729ef9f0432014187762756f1518e85ecf13db6c505bfff65308 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:dfbf1dc0873e0cde30013d8526571f69d5c53be2b8d637a6235c623cc1f66192`  
		Last Modified: Wed, 31 Jan 2024 22:48:48 GMT  
		Size: 28.9 MB (28921333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81908d3ec659c323c38d371d856a58ca7fcda6f482a503f10fc1bab9a3f702be`  
		Last Modified: Thu, 01 Feb 2024 18:27:34 GMT  
		Size: 8.4 MB (8427867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be5ce4a7bd65ddd6cfb5023fdf9a50f9c386d849c3d83a16765840b0f4ac55`  
		Last Modified: Thu, 01 Feb 2024 18:27:33 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6422acad76c511f1e918d400342d06adf32c4679793810baea969418bd902efa`  
		Last Modified: Thu, 01 Feb 2024 18:49:16 GMT  
		Size: 31.0 MB (30950562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2465a4385b4991a12e1e50fd86cd011ebb75be08e07bf74f94ac2c75b981ef3`  
		Last Modified: Thu, 01 Feb 2024 18:49:15 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e65076511a6451fe0e5268b6c929574ed4455c9a08c650aec8fb68a576ae1`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 26.4 MB (26417436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac14d2bb479fa870ec2a21faba398dcd965a7d365067e23f1a1fa3890f3b1a9`  
		Last Modified: Thu, 01 Feb 2024 19:45:03 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1446abb4f341e8b522498d4662cb1f43b6a8ea7a7fca544cf8d7f015e72945`  
		Last Modified: Thu, 01 Feb 2024 19:45:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec2c83135c7b9dee81942bd497008c17fc383307ce4718361a83b36245228e`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:024f41b462cdbccfb759d44b7a8e70740e5eafab683e85ad7927ad24ee86a32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a551864b65e888287cc57bc3ce889d8599738ad776d9243f9230c6cd29d92832`

```dockerfile
```

-	Layers:
	-	`sha256:deae7fb60de53d39c554ba57ef795ef840c48d50bceac10d00cff06f98059019`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 3.5 MB (3450744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1147e25cb6d9c6b641cb34d5190ec08627309fec3d028fb402edc0ed29fe3632`  
		Last Modified: Thu, 01 Feb 2024 19:45:02 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5ec7506c0df076fbea27f2509e7fce3e9a0af9ce3b33fa1f49b1a9440a529bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91599061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4a807266ceba1ee2eea3fe6df4c20e5ec2fa8e0981f89cf8cc29b1836210d4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb8b1e53340c66d7f8666bead8dc92493a496ffab6753fd5a1d5a71200fc19f`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 7.9 MB (7936144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7fea31b19e61a014b3c03b4f0d1a107468f693b69e4c8002ddc2971cc18850`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a452870d4441e01bdef6b77e570312aa3e22210d586f49fce423ef3b55ff1`  
		Last Modified: Fri, 02 Feb 2024 11:53:27 GMT  
		Size: 30.8 MB (30818994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1232ee13c4f5e96179fa04533aa6ab4289edfe5ca3f95501a0b0258d8a74b759`  
		Last Modified: Fri, 02 Feb 2024 11:53:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f337b287832e067041ea001799e24175cf99c3b25e3e5cc64e38e77c26e83fa`  
		Last Modified: Sat, 03 Feb 2024 21:47:02 GMT  
		Size: 26.3 MB (26261789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0db77e8c897e91af883a4c30afd4882e1b0fe80d280d8b06ffd321a41bddb4`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70553432f8b9bd44338c9c577ee4aa04e2ff7e787e814aaa038b1d9e5b40342a`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded50679e09e21d174fcff59ac7bc9b7d099ff547fe5365d3d7bd6c1013e6a77`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:345037db62e3e2d5150613ecf266d4cb8230b4e7099f8c6ad490946ff72ac89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91754f1bd38b1c1f2819f6fff340edc42a75d4c14d4d63b9635c106812483c`

```dockerfile
```

-	Layers:
	-	`sha256:a996bb1c3596890d806fffa27f7ca4be5588af63440853e904d5f793c8257b72`  
		Last Modified: Sat, 03 Feb 2024 21:47:01 GMT  
		Size: 3.5 MB (3515073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32e3353bd0b0c493f893e610d2e7b094afab5517078467bb7080dbde2c1669c`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:62d26e710026d84ea00144f171a9f476153094acd0d89633ecec869e54c2a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98456126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aeffe8997b3c1c5cdba9bc0133eacb5582954eafa0932a1f36212af7b6efa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e97c022709be1e17b17f402896b1bb1848ac5a221f138773e28f7d47d1e4e86`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 9.2 MB (9240742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe340a408654e6223a3620962945372c82dbf2fb43915bea5ae05c27263e47f0`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2255c28da2246780a7a6d22a7a04342f59f038140671b66c2295d6adf77b5f3`  
		Last Modified: Wed, 14 Feb 2024 09:03:21 GMT  
		Size: 31.8 MB (31780990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513661499fc869838327302165f569ed64dd4d123bd457b7706621bd0f9a6e04`  
		Last Modified: Wed, 14 Feb 2024 09:03:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b2c21c5109b50b865b7308e46e66d8fee224cbc1f32768c06ee39beb4f8d8d`  
		Last Modified: Wed, 14 Feb 2024 11:32:37 GMT  
		Size: 27.4 MB (27360385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff21369b8425b69e83fc9d056fb1b6a449da5cec1b57fe2201859c69dc15d7b`  
		Last Modified: Wed, 14 Feb 2024 11:32:35 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48155b30620469fd4cf42c56926bba69bdaedb455f15fdbaa35de30365c8bf`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af0d9a2fbe2027692421b63c23e48fc2f2e6aa4e1e3a2a6707ba8703547a0e`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cd30ccfa00fc536f5a2af7f67068fd1c5622054e89b90fd2cfb3878a3acbad80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c949f73d0853162e3c61e42edce2805b5f8b1512056071a115c83fa4ae9e363`

```dockerfile
```

-	Layers:
	-	`sha256:b3960d83f97703cce0f4ea9df7820755f29b6515ac72c38427594f2c75ddafa1`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 3.6 MB (3606770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c3d1d9b5cef4f0ee688eb21859c8b8dcac3683dbc35a1ee08f0ba8d7e0773`  
		Last Modified: Wed, 14 Feb 2024 11:32:35 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:b455f8bed8535e5b91cd42a11819fefe8b5e05052e596056eb19bd82cd72752a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101819623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeefa074392b3129f51a973d2d5311d17b248f62d556231e0624f848a8c17ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ba90c9da04555eba7a7a6f7159ba742aaf8eac7c3f47335f89aa25dc7cc2a`  
		Last Modified: Tue, 13 Feb 2024 01:57:36 GMT  
		Size: 12.0 MB (11994474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6201af0e25827efd1725b5e15f61f30b5b0ed7c2d886db9fc847e9ca95a44ae`  
		Last Modified: Tue, 13 Feb 2024 01:57:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87b28c4009b753cb2d497e8bfa6c7f4ee64b956035f9e4da359783c31eaea99`  
		Last Modified: Tue, 13 Feb 2024 01:57:36 GMT  
		Size: 31.0 MB (30970141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46040005c56f00ed36ef6763152bee927ed34189c0f51b57dfdb51eb9cabbf53`  
		Last Modified: Tue, 13 Feb 2024 01:57:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276aa887afb73c9cc94c8e6f3e3078530ebdc577f0787b56c9d782980e48818`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 26.4 MB (26444648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c340b9824aede5bdf530d6bbe7f23d488f8d44051ee0a429d11a66d38d3e834`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d026c3763d5a13e442d50a5073d520b07695ea6b6e582c02a880d5f4a9ffc`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd632d44d5e5a191d7ea431db930a2a9e074f770e16ab048d5dab9443c420455`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:adea36b1739001b81f20707fe7b494f56853698dc938a81e159a17d25886f985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3653788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877192d2e4dbc82a34d730b2b20f8a0c5c17d152253227d3b1e6f8aa0d3534e6`

```dockerfile
```

-	Layers:
	-	`sha256:fdf5cbb69bbdc31e9c7a9d668a965f3ba495f899badc47c6d35750eccb62eb4d`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 3.6 MB (3632082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89030bf03d48c70688d83069ba3fb8453212aec17b6b7e7c5855db65949c8b18`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 21.7 KB (21706 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:1878b37955e2ceeeb56b8131e02a1a94e46a0c533eabb30dc704afd236fb45c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106445165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ac5f7f7a3c55c323e50656c1ca0273a50a7f652208261786a53a92588f563f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2643e4e06fe71f452e4298b49d63c37ea9b10701eb01ccf9775c017a8d73831`  
		Last Modified: Wed, 14 Feb 2024 04:42:48 GMT  
		Size: 10.5 MB (10479507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa588bcd76b4962e69ab665cf8bb4e6d06fc6aa058863b16292a7c1c9942e66d`  
		Last Modified: Wed, 14 Feb 2024 04:42:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53336422c877eb458cd32cc08df748e5a5c4d65d8e6ae234d55a68a5e947250`  
		Last Modified: Wed, 14 Feb 2024 05:09:58 GMT  
		Size: 32.6 MB (32583959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3fe277251403d28b0567a5dc2cbec22e7f5d8a01422c9f86e70f6170ca2fa9`  
		Last Modified: Wed, 14 Feb 2024 05:09:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224b51bc717a449b6997e7d57bfaf9b25aa2192fd3eafc6efc2fd9821298cd7`  
		Last Modified: Wed, 14 Feb 2024 06:40:05 GMT  
		Size: 28.1 MB (28080965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce6c1a48128e8322c6832b86b67c8133f1bd045c4e8808fe67f0551bb65778e`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a909935a56c34311a8d2262cceafeb28afa6265f306b53094e046b6d92686c76`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2b26f60ebab4bca36c02b001e79ff9dabfe2f0bf31651b6a3df1d0453653d`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc54c29cd80c55ceda4ae31ceb1cff15de2e39942769604c642d387470c7896a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4c4599761310d0f47736b6b152b3d3f2bc7f282f28fa58962d3c144d489ce0`

```dockerfile
```

-	Layers:
	-	`sha256:661bdcaa04cce0b96b66f31b44548d4ecc059e2f2ee6c463a7871924055c106c`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 3.6 MB (3620159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f980298ba876f1a28bd2c1efbb46aef3d74b37ae7695f43a11b72820a42a5cc9`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:bd964dd8fe87974d5468caec8f195861b8f2b77e8a8cda6328e51d9007187065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98366238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7937da7b0d5d498fbab40b65f1e719bc611a50bebe4bc2100c8b44d18e4216f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a93f5c178c7826ecdaefb1b339a399d44aa16824b3b280809923e34007ddf`  
		Last Modified: Wed, 07 Feb 2024 14:20:36 GMT  
		Size: 8.7 MB (8655944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355b16a2a6aa0edc49141250a7763934521bea4b41c49fcb9bbfb7ea925991a`  
		Last Modified: Wed, 07 Feb 2024 14:20:35 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af44823ae10856a360dd6288e76ec224890d4dcf60c1390adbc910358fb5b899`  
		Last Modified: Wed, 07 Feb 2024 16:59:27 GMT  
		Size: 32.2 MB (32229779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0243d565e852c67b6dbf959b888834f7170a339a8b5402470e3ec8afe596f2`  
		Last Modified: Wed, 07 Feb 2024 16:59:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476de961336036cfe1c92239e1b51ace6a0e3c287e11047356c2dd2c65d0e8b2`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 27.8 MB (27820443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1993b9fd86a27d3c0f178274f5e6ab4fb0bf5bf63b20818008f37d6dcbf7db`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5100321e108d7b7dcb53cf4cdb55d2f129823f1df8847503b06c7af2930e340`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b9651cd0104556ddb52d972bf1e1280d6b0aa91dc921c98be707564192a3ef`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:acea03d91592f55598af2afeaa0c428d63ac154d2a001d4179e6b990cce66caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839a7c6fa201139095fd885ab42cd3cde9a0248b1aaec08c0e3a3df4ec8cc21`

```dockerfile
```

-	Layers:
	-	`sha256:d2a472c792388425ce9ce68e6bd379571821d678fe33aa8d5b9b657a33f52d96`  
		Last Modified: Fri, 09 Feb 2024 01:15:12 GMT  
		Size: 3.5 MB (3527118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b46d62fc4f33cef25401ab7e36d50519f9f9ffe04788ead3791ef2de1044aa9`  
		Last Modified: Fri, 09 Feb 2024 01:15:10 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.2-1.1`

```console
$ docker pull fluentd@sha256:17971d152bb45b141229e30540cce2a60cc8161b0808cec59559b2f9f1ccd880
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

### `fluentd:v1.16.2-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:452a80b204895bf4b4eea054b86b325c998d66dfb68efef1e4353155255cb656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25124717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657945478f75c86fb21bb10fe0d2cda0514d1238a50e3ec3b1d8a44427dd8f71`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea4e9e4a232b968fa2c133e4b6c26306fce69db3a49e1adbe237c2756b837a`  
		Last Modified: Sat, 27 Jan 2024 00:55:01 GMT  
		Size: 21.7 MB (21743147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b793d0bb733b6c0501e4945f24a5216ad8adac79ff91b1e506103d9abe57891`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3666c0e762dbe8030ba636377f2f01016a0acded9549ca96d9e392653b87eae`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258e80c06270b6b9e41aa95e3deb27f6633e786f6da2d015bcc0997a1aacbb80`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9866a651eb47a333ee0b3d05b3fd33e038f86ebb8706080fb16eaa0d95c4d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.2 KB (797186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6a4137a5b2b92b9d78cee1801b3b4f6bd15d2b657d8210aafe2fbcbc2a2be0`

```dockerfile
```

-	Layers:
	-	`sha256:39343fced00865c47b9ec3182866d3c37cf9bb08df09bbd2e30167d83eeb2251`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 783.3 KB (783258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904dbac96399ec5b51e90742ef716afde64a50d72de946a3944442c474de25e2`  
		Last Modified: Sat, 27 Jan 2024 00:55:00 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:1bc94a5c10d8c323faee2eb93e074d8820fba676f2ca827279c5ccfc03ed96bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23807441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f7dcacdbc6ea950f81747fa737f926c055202571e91c5148fb9e14d9baf36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
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
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2352fa41ac154f4e2e5367461993fada2899f2bfc547dbc0578c53a4b7cf23`  
		Last Modified: Tue, 30 Jan 2024 23:05:11 GMT  
		Size: 20.7 MB (20692158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b886caf0093c3e985b44ee4fe118cc5576df44157615afdf850699a2cb81dd`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bca9b4eac5a5009ca4f98a07e60d59c69a14dfda07e25cfa495fffc2d08023f`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e97aad89cf553919c43addbe6ca528c635496ddf00cd853d14f01185541e75`  
		Last Modified: Tue, 30 Jan 2024 23:05:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:03fe08ed5c3f48a3524c3439d8842bee7b4d972fefb57f76f438f0d3e4479fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130111a706a16711523274cae9cc6fee7dfa99a8d9dbb1e1a9d93e6fd7df86c6`

```dockerfile
```

-	Layers:
	-	`sha256:1951357f9f6485a60fe8b27a9b1f03b5c192051955170f3b04604df6d9553ecb`  
		Last Modified: Tue, 30 Jan 2024 23:05:09 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f3b9319ebf791466f71195b66df8f1f25b49acadf325405b8cfebed75dd5c402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24594006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb271860983aeade86cbff5238b75ce5b238f8e12a5bbdb2ad7cb0504af9133`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01a23a2374d171c93b47bb26da2db576f451d45e0a27a667e37bd6cbb7e87b3`  
		Last Modified: Sun, 28 Jan 2024 00:24:36 GMT  
		Size: 21.3 MB (21333562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb368f87cba216705ce5a1331fb697a9629476403fa09f52f8d795c7eac2a0f0`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5955ef227ad76005af8d8aac2aac0fd0aa0cefbae5e1a62e3706fcdc8820a2c`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10d28c7a2db55c1b35d08d3ffef4b595e14954b6fb67e11417584a4af70b0bb`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d03f120c24c0724b8b4f490ff9d22ac3440efbbb5c2943628f1215619651febe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.1 KB (797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df82fc3dfc87e368c73025f95bc0c481f23f9789b75e47cecef8b8841992f768`

```dockerfile
```

-	Layers:
	-	`sha256:8df571d423c02398e866de0225369606734ae0fabbb2c3a1295e614c1b705019`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 783.4 KB (783364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9ef17d7b14bfeda650020e0cca056efac85dfe5f0bdc1197a850af6d6a30c6`  
		Last Modified: Sun, 28 Jan 2024 00:24:35 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:799c7569cd97e023ec2aaffbf926581afd93267c431735f1a00a1f0e6311fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24393632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81131e85bc077170a30424fb24c9a52e4a26f790dd5d3dfc9a0cc76fc8ed34f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
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
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df30d7d2f7b03c651d6cd536b7762833a63f793c9d140f59451eda04da81708`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 21.0 MB (20976292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec772bd6f3724ee81dd51ce8a8e326ab53bbba5c1f8d3485bd71e9108e707e2d`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b531889e4df9c460dd0641755a0cb8d817cc302e1ba39a7ead5972d4e8f15d48`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c973ed5e9ddf074f5d4d60a90a427d5ddb499e561218c22f3706cede95f2de`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:17cf841adbacedff8ee12522211672ee0cabc2a2bbc1b363e122f4acdd87c635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.9 KB (796946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d0ac82f23f0cc11c4b282edd3dd8a2c9d6766a1f6fc20348580c81551be5cd`

```dockerfile
```

-	Layers:
	-	`sha256:370c6020e183e6c33ba2997dcf4794975b5f6c4acca9bb32b22c0fd83eee378c`  
		Last Modified: Sat, 27 Jan 2024 01:55:57 GMT  
		Size: 783.0 KB (783044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e86405cc79800f51fa7306a0be3378fecaf499bd7e1f515e00730748c811319`  
		Last Modified: Sat, 27 Jan 2024 01:55:56 GMT  
		Size: 13.9 KB (13902 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9d1f51d62b0766c7f307d0f71dea4e4c584860f597975ed1111447c165994e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24982485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0548fee0d47e59d4c75dbabcce17ce175288a09f8918317c5402d53b906c2f8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94a6899c2def4c88392adce414ff838ba4d7981bbae29ca91a55dd5715b7b22`  
		Last Modified: Sat, 27 Jan 2024 11:37:55 GMT  
		Size: 21.6 MB (21588206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108fcff8ea7131dc2b08602727f72e98f9e375d6c513d31b77c437747be692d6`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b768671a5aafa1da69c21f008b76c96a8ea5c3e6d68fa2ed12edbef69ef713c`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf48df70f2bb2716bd9d9c43bde8d731bbb35fe6abe17baeb46a1282ae7ff30`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9fcf2c79918734ae1561f5a9276bf6c8edfc2559d9514862d010f960e144f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.9 KB (795930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6734e6e41693a3ced230b9772cc97b4461e49555391703eaadfbfbb4c0976e6`

```dockerfile
```

-	Layers:
	-	`sha256:f7738f5e157f300fad15469848d06950b27ff8ef89e3142bacb794d49bdf21ac`  
		Last Modified: Sat, 27 Jan 2024 11:37:54 GMT  
		Size: 782.1 KB (782135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d92909243fa607abd5b7dbbaf7bc7966f7e679d9a79a1ffbb023f201b72d7f3`  
		Last Modified: Sat, 27 Jan 2024 11:37:53 GMT  
		Size: 13.8 KB (13795 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:25b64b8dfb564439d5b9d8b707991674d28c52a36bce3056a50213d536e66579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24346804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0aeb83a8a6ede2efef41019622d1fb5d27339963670fb42462db50f1ade75c7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
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
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93d5dc93ac82bd628be17a0099b3f938cd87353c260161347383112c62a0be`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 21.2 MB (21168114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a3cd5047901169f44a32cf5c9b1d016ea08fe9d7186bb5e08fb22f825c031`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f60e893142480493ed865854c0775913b4f08549b13281a21e303f0a91ae97d`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88530a7eb1af88b4d3e7b71a9933e6a2b0f58083886b2b3f88b732d57eed524a`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bf00a1f1f40bfa28b432b19e88641284b09919bcaa2306da07b1cad78ffe2762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 KB (795286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041aa04f1a808235e7b591e5a79054b059752361bdc4298287674ee6a589a24e`

```dockerfile
```

-	Layers:
	-	`sha256:5853a8045217c8cb3f1067b6b94a23e20271259e53a89ac6bae192b368f18648`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 781.5 KB (781525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be5bc1784b74172b94ddbe1ee0c8174e50895a2bfb1c570062f50bfea9cbf0e`  
		Last Modified: Sun, 28 Jan 2024 22:28:47 GMT  
		Size: 13.8 KB (13761 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.2-debian-1.1`

```console
$ docker pull fluentd@sha256:c5bcd66bca336b44f6f94273fe51d8e32a957571206bad023545c4fb8269c819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.2-debian-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:c9a98f428cba1dc697ee8a86494d00a07fb93be9de01b986290d0ac2446ba19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101440601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f34768308894aaa647a9690d80ed28a24d3907233cb06f98d610ae7f633b6e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d1c7fb8f3d1b4044bd6d6d05c3d5221ab0b0d23b861034221a0729f3f5e05e`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 10.0 MB (10019247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3594d5f3eee1edd44e5d35581227c806baa7ff2d6e69c2dfedca42f3c57e6b3e`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037ad1326f63794876e13aa67f3385cc191f60fd7faecdd8b91203b9432bcef3`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 32.4 MB (32416622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0e740bbfc9d1f650471f1d467a1fdcdac4c78602c4a05e25ffe7e6e3365646`  
		Last Modified: Tue, 13 Feb 2024 01:57:17 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcfcf2370d9f2d20a6e895856965b7af114f5be2815932a070bbd98c705bfe7`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 27.6 MB (27579386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614706cb9ca01928f60a27be7b8b12d82aaf6343af4cd68b30524ee9151e8d3c`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c860968a36a14d0ff0532b93c0d3a1a84aab89c6a78351d20a876b255fc2a17c`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5fa22ea2fdebbdce849aaec0ea2b55cec89a9e6313e22ec2ed57465c2a3f16`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c95129282c46b9a45162c1904c0a43bdfcf77ddb650a57f0e90d1273026083f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3650557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed8b2978f98dfede3d55bdd153fd3a14fdad2c3bd52aa4df342c5e557a4f63`

```dockerfile
```

-	Layers:
	-	`sha256:b480baa59ea6843baf5a07886e08e6e47491e3a7834127014ae5cd79fbc96060`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 3.6 MB (3628827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406dd3b1cce2eb10e57fc90c6bb36a346f32afc26ed9d233d7a80721726d6910`  
		Last Modified: Tue, 13 Feb 2024 03:05:59 GMT  
		Size: 21.7 KB (21730 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:9a9b8a87a08242bcedded60ed2eff9a49ff8bb34177a2980ca052252c4168374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94720119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a7dacaeb38c9734bbe50b6ce4aaf118ee96025cba00d79b18725a477eef65`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:1b6dd4809e22729ef9f0432014187762756f1518e85ecf13db6c505bfff65308 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:dfbf1dc0873e0cde30013d8526571f69d5c53be2b8d637a6235c623cc1f66192`  
		Last Modified: Wed, 31 Jan 2024 22:48:48 GMT  
		Size: 28.9 MB (28921333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81908d3ec659c323c38d371d856a58ca7fcda6f482a503f10fc1bab9a3f702be`  
		Last Modified: Thu, 01 Feb 2024 18:27:34 GMT  
		Size: 8.4 MB (8427867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be5ce4a7bd65ddd6cfb5023fdf9a50f9c386d849c3d83a16765840b0f4ac55`  
		Last Modified: Thu, 01 Feb 2024 18:27:33 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6422acad76c511f1e918d400342d06adf32c4679793810baea969418bd902efa`  
		Last Modified: Thu, 01 Feb 2024 18:49:16 GMT  
		Size: 31.0 MB (30950562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2465a4385b4991a12e1e50fd86cd011ebb75be08e07bf74f94ac2c75b981ef3`  
		Last Modified: Thu, 01 Feb 2024 18:49:15 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e65076511a6451fe0e5268b6c929574ed4455c9a08c650aec8fb68a576ae1`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 26.4 MB (26417436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac14d2bb479fa870ec2a21faba398dcd965a7d365067e23f1a1fa3890f3b1a9`  
		Last Modified: Thu, 01 Feb 2024 19:45:03 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1446abb4f341e8b522498d4662cb1f43b6a8ea7a7fca544cf8d7f015e72945`  
		Last Modified: Thu, 01 Feb 2024 19:45:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec2c83135c7b9dee81942bd497008c17fc383307ce4718361a83b36245228e`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:024f41b462cdbccfb759d44b7a8e70740e5eafab683e85ad7927ad24ee86a32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a551864b65e888287cc57bc3ce889d8599738ad776d9243f9230c6cd29d92832`

```dockerfile
```

-	Layers:
	-	`sha256:deae7fb60de53d39c554ba57ef795ef840c48d50bceac10d00cff06f98059019`  
		Last Modified: Thu, 01 Feb 2024 19:45:04 GMT  
		Size: 3.5 MB (3450744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1147e25cb6d9c6b641cb34d5190ec08627309fec3d028fb402edc0ed29fe3632`  
		Last Modified: Thu, 01 Feb 2024 19:45:02 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:5ec7506c0df076fbea27f2509e7fce3e9a0af9ce3b33fa1f49b1a9440a529bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91599061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4a807266ceba1ee2eea3fe6df4c20e5ec2fa8e0981f89cf8cc29b1836210d4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb8b1e53340c66d7f8666bead8dc92493a496ffab6753fd5a1d5a71200fc19f`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 7.9 MB (7936144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7fea31b19e61a014b3c03b4f0d1a107468f693b69e4c8002ddc2971cc18850`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a452870d4441e01bdef6b77e570312aa3e22210d586f49fce423ef3b55ff1`  
		Last Modified: Fri, 02 Feb 2024 11:53:27 GMT  
		Size: 30.8 MB (30818994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1232ee13c4f5e96179fa04533aa6ab4289edfe5ca3f95501a0b0258d8a74b759`  
		Last Modified: Fri, 02 Feb 2024 11:53:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f337b287832e067041ea001799e24175cf99c3b25e3e5cc64e38e77c26e83fa`  
		Last Modified: Sat, 03 Feb 2024 21:47:02 GMT  
		Size: 26.3 MB (26261789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0db77e8c897e91af883a4c30afd4882e1b0fe80d280d8b06ffd321a41bddb4`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70553432f8b9bd44338c9c577ee4aa04e2ff7e787e814aaa038b1d9e5b40342a`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded50679e09e21d174fcff59ac7bc9b7d099ff547fe5365d3d7bd6c1013e6a77`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:345037db62e3e2d5150613ecf266d4cb8230b4e7099f8c6ad490946ff72ac89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d91754f1bd38b1c1f2819f6fff340edc42a75d4c14d4d63b9635c106812483c`

```dockerfile
```

-	Layers:
	-	`sha256:a996bb1c3596890d806fffa27f7ca4be5588af63440853e904d5f793c8257b72`  
		Last Modified: Sat, 03 Feb 2024 21:47:01 GMT  
		Size: 3.5 MB (3515073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32e3353bd0b0c493f893e610d2e7b094afab5517078467bb7080dbde2c1669c`  
		Last Modified: Sat, 03 Feb 2024 21:47:00 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:62d26e710026d84ea00144f171a9f476153094acd0d89633ecec869e54c2a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98456126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aeffe8997b3c1c5cdba9bc0133eacb5582954eafa0932a1f36212af7b6efa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e97c022709be1e17b17f402896b1bb1848ac5a221f138773e28f7d47d1e4e86`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 9.2 MB (9240742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe340a408654e6223a3620962945372c82dbf2fb43915bea5ae05c27263e47f0`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2255c28da2246780a7a6d22a7a04342f59f038140671b66c2295d6adf77b5f3`  
		Last Modified: Wed, 14 Feb 2024 09:03:21 GMT  
		Size: 31.8 MB (31780990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513661499fc869838327302165f569ed64dd4d123bd457b7706621bd0f9a6e04`  
		Last Modified: Wed, 14 Feb 2024 09:03:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b2c21c5109b50b865b7308e46e66d8fee224cbc1f32768c06ee39beb4f8d8d`  
		Last Modified: Wed, 14 Feb 2024 11:32:37 GMT  
		Size: 27.4 MB (27360385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff21369b8425b69e83fc9d056fb1b6a449da5cec1b57fe2201859c69dc15d7b`  
		Last Modified: Wed, 14 Feb 2024 11:32:35 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48155b30620469fd4cf42c56926bba69bdaedb455f15fdbaa35de30365c8bf`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af0d9a2fbe2027692421b63c23e48fc2f2e6aa4e1e3a2a6707ba8703547a0e`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cd30ccfa00fc536f5a2af7f67068fd1c5622054e89b90fd2cfb3878a3acbad80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c949f73d0853162e3c61e42edce2805b5f8b1512056071a115c83fa4ae9e363`

```dockerfile
```

-	Layers:
	-	`sha256:b3960d83f97703cce0f4ea9df7820755f29b6515ac72c38427594f2c75ddafa1`  
		Last Modified: Wed, 14 Feb 2024 11:32:36 GMT  
		Size: 3.6 MB (3606770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c3d1d9b5cef4f0ee688eb21859c8b8dcac3683dbc35a1ee08f0ba8d7e0773`  
		Last Modified: Wed, 14 Feb 2024 11:32:35 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:b455f8bed8535e5b91cd42a11819fefe8b5e05052e596056eb19bd82cd72752a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101819623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adeefa074392b3129f51a973d2d5311d17b248f62d556231e0624f848a8c17ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ba90c9da04555eba7a7a6f7159ba742aaf8eac7c3f47335f89aa25dc7cc2a`  
		Last Modified: Tue, 13 Feb 2024 01:57:36 GMT  
		Size: 12.0 MB (11994474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6201af0e25827efd1725b5e15f61f30b5b0ed7c2d886db9fc847e9ca95a44ae`  
		Last Modified: Tue, 13 Feb 2024 01:57:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87b28c4009b753cb2d497e8bfa6c7f4ee64b956035f9e4da359783c31eaea99`  
		Last Modified: Tue, 13 Feb 2024 01:57:36 GMT  
		Size: 31.0 MB (30970141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46040005c56f00ed36ef6763152bee927ed34189c0f51b57dfdb51eb9cabbf53`  
		Last Modified: Tue, 13 Feb 2024 01:57:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276aa887afb73c9cc94c8e6f3e3078530ebdc577f0787b56c9d782980e48818`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 26.4 MB (26444648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c340b9824aede5bdf530d6bbe7f23d488f8d44051ee0a429d11a66d38d3e834`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d026c3763d5a13e442d50a5073d520b07695ea6b6e582c02a880d5f4a9ffc`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd632d44d5e5a191d7ea431db930a2a9e074f770e16ab048d5dab9443c420455`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:adea36b1739001b81f20707fe7b494f56853698dc938a81e159a17d25886f985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3653788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877192d2e4dbc82a34d730b2b20f8a0c5c17d152253227d3b1e6f8aa0d3534e6`

```dockerfile
```

-	Layers:
	-	`sha256:fdf5cbb69bbdc31e9c7a9d668a965f3ba495f899badc47c6d35750eccb62eb4d`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 3.6 MB (3632082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89030bf03d48c70688d83069ba3fb8453212aec17b6b7e7c5855db65949c8b18`  
		Last Modified: Tue, 13 Feb 2024 03:04:26 GMT  
		Size: 21.7 KB (21706 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:1878b37955e2ceeeb56b8131e02a1a94e46a0c533eabb30dc704afd236fb45c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106445165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ac5f7f7a3c55c323e50656c1ca0273a50a7f652208261786a53a92588f563f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2643e4e06fe71f452e4298b49d63c37ea9b10701eb01ccf9775c017a8d73831`  
		Last Modified: Wed, 14 Feb 2024 04:42:48 GMT  
		Size: 10.5 MB (10479507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa588bcd76b4962e69ab665cf8bb4e6d06fc6aa058863b16292a7c1c9942e66d`  
		Last Modified: Wed, 14 Feb 2024 04:42:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53336422c877eb458cd32cc08df748e5a5c4d65d8e6ae234d55a68a5e947250`  
		Last Modified: Wed, 14 Feb 2024 05:09:58 GMT  
		Size: 32.6 MB (32583959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3fe277251403d28b0567a5dc2cbec22e7f5d8a01422c9f86e70f6170ca2fa9`  
		Last Modified: Wed, 14 Feb 2024 05:09:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224b51bc717a449b6997e7d57bfaf9b25aa2192fd3eafc6efc2fd9821298cd7`  
		Last Modified: Wed, 14 Feb 2024 06:40:05 GMT  
		Size: 28.1 MB (28080965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce6c1a48128e8322c6832b86b67c8133f1bd045c4e8808fe67f0551bb65778e`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a909935a56c34311a8d2262cceafeb28afa6265f306b53094e046b6d92686c76`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2b26f60ebab4bca36c02b001e79ff9dabfe2f0bf31651b6a3df1d0453653d`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bc54c29cd80c55ceda4ae31ceb1cff15de2e39942769604c642d387470c7896a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4c4599761310d0f47736b6b152b3d3f2bc7f282f28fa58962d3c144d489ce0`

```dockerfile
```

-	Layers:
	-	`sha256:661bdcaa04cce0b96b66f31b44548d4ecc059e2f2ee6c463a7871924055c106c`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 3.6 MB (3620159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f980298ba876f1a28bd2c1efbb46aef3d74b37ae7695f43a11b72820a42a5cc9`  
		Last Modified: Wed, 14 Feb 2024 06:40:03 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:bd964dd8fe87974d5468caec8f195861b8f2b77e8a8cda6328e51d9007187065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98366238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7937da7b0d5d498fbab40b65f1e719bc611a50bebe4bc2100c8b44d18e4216f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:08:16 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 13 Jun 2023 18:08:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jun 2023 18:08:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 18:08:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jun 2023 18:08:16 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a93f5c178c7826ecdaefb1b339a399d44aa16824b3b280809923e34007ddf`  
		Last Modified: Wed, 07 Feb 2024 14:20:36 GMT  
		Size: 8.7 MB (8655944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355b16a2a6aa0edc49141250a7763934521bea4b41c49fcb9bbfb7ea925991a`  
		Last Modified: Wed, 07 Feb 2024 14:20:35 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af44823ae10856a360dd6288e76ec224890d4dcf60c1390adbc910358fb5b899`  
		Last Modified: Wed, 07 Feb 2024 16:59:27 GMT  
		Size: 32.2 MB (32229779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0243d565e852c67b6dbf959b888834f7170a339a8b5402470e3ec8afe596f2`  
		Last Modified: Wed, 07 Feb 2024 16:59:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476de961336036cfe1c92239e1b51ace6a0e3c287e11047356c2dd2c65d0e8b2`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 27.8 MB (27820443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1993b9fd86a27d3c0f178274f5e6ab4fb0bf5bf63b20818008f37d6dcbf7db`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5100321e108d7b7dcb53cf4cdb55d2f129823f1df8847503b06c7af2930e340`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b9651cd0104556ddb52d972bf1e1280d6b0aa91dc921c98be707564192a3ef`  
		Last Modified: Fri, 09 Feb 2024 01:15:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:acea03d91592f55598af2afeaa0c428d63ac154d2a001d4179e6b990cce66caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839a7c6fa201139095fd885ab42cd3cde9a0248b1aaec08c0e3a3df4ec8cc21`

```dockerfile
```

-	Layers:
	-	`sha256:d2a472c792388425ce9ce68e6bd379571821d678fe33aa8d5b9b657a33f52d96`  
		Last Modified: Fri, 09 Feb 2024 01:15:12 GMT  
		Size: 3.5 MB (3527118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b46d62fc4f33cef25401ab7e36d50519f9f9ffe04788ead3791ef2de1044aa9`  
		Last Modified: Fri, 09 Feb 2024 01:15:10 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json
