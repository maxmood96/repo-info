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
$ docker pull fluentd@sha256:af43b6601b5ff21da92174fc832076be8cf69ca4a6163ea4f7e84c13e67bdb98
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
$ docker pull fluentd@sha256:6243dfe38a630f07433d37dd9ab4b0851934b36a3ac5901bdd39064dd0275d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101439280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2df5cfe4104eeb86da8d11a5d1e61ab54277fff17703b167f74e09625e8d37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283409bbcf6725e16a30f8733ec96183462ec2025ccd7c452c4c97d5317aa51`  
		Last Modified: Tue, 12 Mar 2024 01:59:14 GMT  
		Size: 10.0 MB (10019195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eff8149490762ab409469e8b418ac5390daa8def5a1e844c1d51a7def34cd7`  
		Last Modified: Tue, 12 Mar 2024 01:59:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94469a0c0a728e08e58994d23c616c9538f5a20f555f3d0dada7740d5152964d`  
		Last Modified: Tue, 12 Mar 2024 01:59:15 GMT  
		Size: 32.4 MB (32417118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9be53a2c5d07688baf64ea55c6b79f8c12537dd0f0a3b509dbc0346dde3c9`  
		Last Modified: Tue, 12 Mar 2024 01:59:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1f8e0e59973865379b9601dec0f260920d28e15b123d24cadb79bf79e0cc41`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 27.6 MB (27577550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4e051c6e6efd4f3f13d2be64c51899060e6a01689de76c6b63bdae5bedfbef`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d47630df3482a763aa8706dbb777be3445d960bca96f9628157f3a0c6a8f85a`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f970ed2995181f355cb504e02a7de681c588edfce27189a02967498d869f720d`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:44c132669e4273274dd1a2df63550387fd3ce6463c5fda84c46269e392bf1a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1fa5d9ae4b98b1f8402f12bed6eed349405a133737dea45f7b683b92c61f11`

```dockerfile
```

-	Layers:
	-	`sha256:35f915c1263fe623a15615f680b68f9c3991ff24dcb57fb83a3a537bc67fdde6`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 4.2 MB (4158432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688e1d8879f6f0ee352d55b14cb607f6f64ef290865a0fe00ee85c8a4d267db9`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 21.7 KB (21730 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:9aea8617c3c47542a31a3607d0d8a8be1949b3f2658876244d75185aa3bfee73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faed22dfaad0b6bc3744e9ffab3ead39f59ef1643ec30fc8b451fa180a092804`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
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
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59405f0ccf0ddc1d620dcbdabd2bbbb178484dfb04c92e6198fc202d247bf98e`  
		Last Modified: Tue, 12 Mar 2024 21:31:15 GMT  
		Size: 8.6 MB (8632512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf1c262c568728790a89c33a8c3d708fe45353a868e257057131a565c556c9`  
		Last Modified: Tue, 12 Mar 2024 21:31:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0df823455becb66992d03163420a47fb396428c584186f57e3c1ff95462ef8`  
		Last Modified: Tue, 12 Mar 2024 22:10:09 GMT  
		Size: 31.0 MB (30954072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a10f0a8fb7c76ccba08cec5465801f41f01fb6e8136a721ce4891d22dfafaa`  
		Last Modified: Tue, 12 Mar 2024 22:10:07 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71514ad91988ecd8f291ad31be7863eb9ed79a4dd8a879d26dc32ee80d516a4`  
		Last Modified: Tue, 12 Mar 2024 22:58:32 GMT  
		Size: 26.4 MB (26432656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ba03071c9a7e5d3b8759109ca7db7f4e71e189843e2f7c8282c0163a3d6db`  
		Last Modified: Tue, 12 Mar 2024 22:58:30 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05447736b97188f52bcb5328d794db679e5fae462713c8c046280f7d36449f`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2aa0ba8feeb21c860460ed2782a79fc1a9ed9eae25b7475273067acdc41c9`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c780bd4769235eb952fdc91dda855cfad0efeb5df8a7b85ecaa94ad4f63fefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9671bfa83ee40ff6d41fc32133199112d5f405cac6d7aff4052cfc5a66be7159`

```dockerfile
```

-	Layers:
	-	`sha256:f1dd2bb11c9c45e8b500c9108370d12b3a7e93eaedef7e455c339f671c542d05`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 4.1 MB (4129648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f4cbfc024609956cb26330f1ca44f2bef3afd4d044ec41a175e01e1324e647`  
		Last Modified: Tue, 12 Mar 2024 22:58:30 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:bdb430f06229a092c6d68de0de97aa32ff79d56266e9d7e41f21dd40c95ae985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91823664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbf4af9cad21f8c3a7da82da5ec7e5781d4786cb22b6b95fbe150004f4688f8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
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
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d41f3a8e88176da522ecdcfb27243ff8242f2891b24c865c113974b1f6c78c6`  
		Last Modified: Wed, 13 Mar 2024 08:36:55 GMT  
		Size: 8.1 MB (8140786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51854233f8e6b65efa5673d4cc3a32ed96110ad9f485ef0f4ed4d77b56e4e99b`  
		Last Modified: Wed, 13 Mar 2024 08:36:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5ff38d96a5bac0bbf5c2ed176ffe7ae528d6d451f8faed09983bddbf945fe3`  
		Last Modified: Wed, 13 Mar 2024 08:58:14 GMT  
		Size: 30.8 MB (30827243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3b623cc416339cafffa4b77ec8c231d49552d7b0085283057951c28740250a`  
		Last Modified: Wed, 13 Mar 2024 08:58:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f04e02713e5e7e4c47028f0a9fc2d52670cf01621002fba72a6772e64c5857`  
		Last Modified: Wed, 13 Mar 2024 10:47:27 GMT  
		Size: 26.3 MB (26269996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41751edda5876c0769e9466532d153dc004e86d67cab18452dbb8508ca14407`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271f663ce1af5fa046ad19412f0152feab5bec4e34fc046d59e6eca78b583762`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b4b91c0168a1ff1da509857dd0b586df09fbaf8ef759cbe8d2faeed4291456`  
		Last Modified: Wed, 13 Mar 2024 10:47:27 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f528f74f74a46ba124bc3e273ee1116ce5070d44ab9a57f6b07b040738b94a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6972f9b685262ccdbbba13d1a05e72401f7cb3019a6f34b473cb4875d4ada46`

```dockerfile
```

-	Layers:
	-	`sha256:04e3ee64b961993d1260087a38bb3482398a03e18e3d04c3416038dbdc13c9d5`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 4.1 MB (4132416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f30629f1c53cb0f876338a4ec7940c4dd5253242727f3165da2448acd5ff0f`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1111a7dd8eb347697a9ee48db8f6448115200a68742a131dd0e3e8836c3be268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98458051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93957bb0f0e3c4825eb7884629589a24fe343bbe38e5c3b0b8b4a0936a83da91`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb512b419861d39e27ddea7236798af420a58b2c85345c1a9fabd4b5ce2dfa3`  
		Last Modified: Wed, 13 Mar 2024 04:39:54 GMT  
		Size: 9.2 MB (9240668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0c0ad46bd96e85894a6ae1c392a3c301436efcdb83b7302f8b6a3bceec2a5`  
		Last Modified: Wed, 13 Mar 2024 04:39:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c0de5a9d784f8cccd4c319a0eac1b7910a04b48fe5613814a558a64bec950f`  
		Last Modified: Wed, 13 Mar 2024 05:08:28 GMT  
		Size: 31.8 MB (31780775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645dcc0d6737795e745d76565e4425492ec3f1662bacd3385818a9fd0aa2cb00`  
		Last Modified: Wed, 13 Mar 2024 05:08:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0546eff6f8c859779fc60c550beafb9d6c00378a7edbca27a7969d397831989`  
		Last Modified: Wed, 13 Mar 2024 08:41:56 GMT  
		Size: 27.4 MB (27362545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b276ad50b662f2b574a523e7bf0044c9b4d14efbca9d24b6161663cf000816`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930034ddc7a340b48eb0fa6dc7b78f4f76960a9b8e2736b11eff74c2ea16b710`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba184da4cf8af41e5dfcbef86a8d41455d0b83160ac07fa769510fa96748132`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:65e8fc17577ff0311fab5dd4a93fd71ea01af2ee3d0608300a068bbb0030b97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0cabb3c627cff4998ba475820ceef81b5681084a18ff3e4fa9ed144c99cdc8`

```dockerfile
```

-	Layers:
	-	`sha256:b4167d3e3e54b7f7311bf36bee92d70372819e34e713e2749df6b341fc635ff2`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 4.1 MB (4132771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c325a6ea37a5e3f0ea02918db62441621d49e00ad55273e184ea9d4d80016e2`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:38e5dab2e37407748c0b4e1061850ee938ce3b2e5b27141b634d51b42e8f65c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101830807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb1dd12f35822c5eb1327206a81559d82d545274c4e4f557ff85210a7d4f559`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
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
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4449a78d85c35d005e14c02051f922c15ce85515f23a3b02f5d95fcdb83c65c9`  
		Last Modified: Tue, 12 Mar 2024 01:59:27 GMT  
		Size: 12.0 MB (11994381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68c7a471344332bd6c9ff70ff66428398bae6e17f2bd73e69f6ca4fd7a4ee`  
		Last Modified: Tue, 12 Mar 2024 01:59:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e1ca595a45956ba439220dba755b97ac59b4a300cd274ffba16e9ba70b8fc0`  
		Last Modified: Tue, 12 Mar 2024 01:59:28 GMT  
		Size: 31.0 MB (30969914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb226cc3333683c1f4fb82d4cba752052da4513dd11c7db0148c4d569dc33ae`  
		Last Modified: Tue, 12 Mar 2024 01:59:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b211b5f1c062969b142ab7ebd513564730a3b1cba3ede002895525109d0618`  
		Last Modified: Tue, 12 Mar 2024 02:57:44 GMT  
		Size: 26.5 MB (26456000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f28f1772a6b4fe98a7b6791b1966fc6f916da70b5820f8bdca91043729ddad`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5b10f7ab211e77e47be0ebb7f7ce1b09902bb9c060e087f9b9f9fa5a6b6ba5`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7578e1c859c2b7babf557d12c25595dd5e36d3e7be41122910f2f546441cc7`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e4be70697c515d4f2bf73218d2098261be34152e08ae6f97efd7ac6c1c24a683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc61a421991bf79c413395152aa88bb377d95b91b8aad505e6275f9aeb8facf9`

```dockerfile
```

-	Layers:
	-	`sha256:a8e410ed81162e3040268653c59266c97d4d215fc4e50c11cf30debc2c370e47`  
		Last Modified: Tue, 12 Mar 2024 02:57:43 GMT  
		Size: 4.2 MB (4162641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed93898a94398f417116f43a0d97235adccc12fa07c4bf47ee4a8f0da6d32578`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 21.7 KB (21705 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:91a10199b3756f2e8313fa4dc9280543733efe24f5b7c3135ee960f6d45a396c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106451571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869ff3c5bcde70730b3654f539380fa4165d3e6d55d2f76be1d71afdccd02a42`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc02f8761ff460024c63b11ed867400af92083b7e0e95eac24d1761bf0288ab4`  
		Last Modified: Wed, 13 Mar 2024 07:18:35 GMT  
		Size: 10.5 MB (10479553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36a5e0859a09a8c472ea1fe096ec442ea6cb20f3a0b72b66f928b7a87bcce6`  
		Last Modified: Wed, 13 Mar 2024 07:18:34 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9ff491e12ca5f1ac7128f947d5ffffccbd95fb32fd6e73f134781adc3410b`  
		Last Modified: Wed, 13 Mar 2024 07:51:04 GMT  
		Size: 32.6 MB (32584181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37ee379dffdfd40d1d83484310d597c92ab39a100c6fa206ef45ef48e6e93ef`  
		Last Modified: Wed, 13 Mar 2024 07:51:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6fdad0e22a4f58bd761bcff8ea9949fc39a4905dc241a716aea3edb01aefd`  
		Last Modified: Wed, 13 Mar 2024 10:00:40 GMT  
		Size: 28.1 MB (28086897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85579f4098e1936dfbf5f1c7fc8ab1af9f54adab502c43e4dee8b251775704fb`  
		Last Modified: Wed, 13 Mar 2024 10:00:38 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657afe7e91f48836970bd63d64ad7b403d9aa00c8158e3ee612b7a7c37104bc`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca5de28251db9fec1e62be7e221e41b5cd2c276285dd4d30809248e56bc924`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0359a7cf809cbc92e7958ef32c7fe3291bedc3f91f8c0d3b56a140da97c154ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6decededdce1d8378400615ca0f8e3b2a251db04d9b94173494ebecbc23f30dd`

```dockerfile
```

-	Layers:
	-	`sha256:840b34bb813d8f0b3ee828e363b4b01dde43deea55a377d835d02655700cbe5d`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 4.1 MB (4147326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8d7612b49a8b3803cd55f743f15a079fe8aba953342d10b06d109e450bddb2`  
		Last Modified: Wed, 13 Mar 2024 10:00:38 GMT  
		Size: 21.8 KB (21800 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:3ef38f43fcf36476b169606002a8ba6b601d9edd335431f219a95c1349e9a9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98578970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fded1edbc15785afa11cbfc74614a8547f9493aba946e097e442588b95462af4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
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
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f258da6cceecf5c0f7ccc2c92bc9661c5707ddc2d08dc3b54f9644f30df2dc`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 8.9 MB (8860667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bbe743c4c86dfe8406ae6e1ae48dd2188e11d67401106b7cdd68fc0d88ca94`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4f9ad750deefa633b927d79494fca8126ec9feee7557abe69da0c731e77926`  
		Last Modified: Thu, 15 Feb 2024 19:20:28 GMT  
		Size: 32.2 MB (32227693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c809275b504b3c323cc3a5b0f5125431ccdf548112269484cf00af9c234cc5c`  
		Last Modified: Thu, 15 Feb 2024 19:20:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd5abbb0faaadd016adddbb28b13446230346b2f274284e77b5f4d64729d76`  
		Last Modified: Fri, 16 Feb 2024 19:23:29 GMT  
		Size: 27.8 MB (27827507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f324329d1588c45d45f27be169dd3e2f13b6554f693c76a0b6646c0d26eca5ad`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e16f61bcf7782d452f4598eafbcb5cbd20f145f774c59697b3a154801c195`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27f1070d557515436e56911252f0c4a7d86e2dcc569a876de23de6aae1c9db`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8075112bdbd3f0be0ba8b36dee0115182da7a57b95143c456641cc801044219d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368ac10cd589370362faca8e7867487464e9c0df3bf40c3cee61a2e10e013e91`

```dockerfile
```

-	Layers:
	-	`sha256:fd26bf3c8a9b60d791d7b718b3c6b5880df1ead6d5d6ec5f21cdc531cf716379`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 3.6 MB (3618884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095d4659105db18254bc89694fba696765936a3f3011db64dfa17365c3746281`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
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
$ docker pull fluentd@sha256:af43b6601b5ff21da92174fc832076be8cf69ca4a6163ea4f7e84c13e67bdb98
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
$ docker pull fluentd@sha256:6243dfe38a630f07433d37dd9ab4b0851934b36a3ac5901bdd39064dd0275d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101439280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2df5cfe4104eeb86da8d11a5d1e61ab54277fff17703b167f74e09625e8d37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
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
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283409bbcf6725e16a30f8733ec96183462ec2025ccd7c452c4c97d5317aa51`  
		Last Modified: Tue, 12 Mar 2024 01:59:14 GMT  
		Size: 10.0 MB (10019195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eff8149490762ab409469e8b418ac5390daa8def5a1e844c1d51a7def34cd7`  
		Last Modified: Tue, 12 Mar 2024 01:59:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94469a0c0a728e08e58994d23c616c9538f5a20f555f3d0dada7740d5152964d`  
		Last Modified: Tue, 12 Mar 2024 01:59:15 GMT  
		Size: 32.4 MB (32417118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9be53a2c5d07688baf64ea55c6b79f8c12537dd0f0a3b509dbc0346dde3c9`  
		Last Modified: Tue, 12 Mar 2024 01:59:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1f8e0e59973865379b9601dec0f260920d28e15b123d24cadb79bf79e0cc41`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 27.6 MB (27577550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4e051c6e6efd4f3f13d2be64c51899060e6a01689de76c6b63bdae5bedfbef`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d47630df3482a763aa8706dbb777be3445d960bca96f9628157f3a0c6a8f85a`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f970ed2995181f355cb504e02a7de681c588edfce27189a02967498d869f720d`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:44c132669e4273274dd1a2df63550387fd3ce6463c5fda84c46269e392bf1a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1fa5d9ae4b98b1f8402f12bed6eed349405a133737dea45f7b683b92c61f11`

```dockerfile
```

-	Layers:
	-	`sha256:35f915c1263fe623a15615f680b68f9c3991ff24dcb57fb83a3a537bc67fdde6`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 4.2 MB (4158432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688e1d8879f6f0ee352d55b14cb607f6f64ef290865a0fe00ee85c8a4d267db9`  
		Last Modified: Tue, 12 Mar 2024 02:57:30 GMT  
		Size: 21.7 KB (21730 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:9aea8617c3c47542a31a3607d0d8a8be1949b3f2658876244d75185aa3bfee73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94946720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faed22dfaad0b6bc3744e9ffab3ead39f59ef1643ec30fc8b451fa180a092804`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
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
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59405f0ccf0ddc1d620dcbdabd2bbbb178484dfb04c92e6198fc202d247bf98e`  
		Last Modified: Tue, 12 Mar 2024 21:31:15 GMT  
		Size: 8.6 MB (8632512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf1c262c568728790a89c33a8c3d708fe45353a868e257057131a565c556c9`  
		Last Modified: Tue, 12 Mar 2024 21:31:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0df823455becb66992d03163420a47fb396428c584186f57e3c1ff95462ef8`  
		Last Modified: Tue, 12 Mar 2024 22:10:09 GMT  
		Size: 31.0 MB (30954072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a10f0a8fb7c76ccba08cec5465801f41f01fb6e8136a721ce4891d22dfafaa`  
		Last Modified: Tue, 12 Mar 2024 22:10:07 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71514ad91988ecd8f291ad31be7863eb9ed79a4dd8a879d26dc32ee80d516a4`  
		Last Modified: Tue, 12 Mar 2024 22:58:32 GMT  
		Size: 26.4 MB (26432656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ba03071c9a7e5d3b8759109ca7db7f4e71e189843e2f7c8282c0163a3d6db`  
		Last Modified: Tue, 12 Mar 2024 22:58:30 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05447736b97188f52bcb5328d794db679e5fae462713c8c046280f7d36449f`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2aa0ba8feeb21c860460ed2782a79fc1a9ed9eae25b7475273067acdc41c9`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c780bd4769235eb952fdc91dda855cfad0efeb5df8a7b85ecaa94ad4f63fefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9671bfa83ee40ff6d41fc32133199112d5f405cac6d7aff4052cfc5a66be7159`

```dockerfile
```

-	Layers:
	-	`sha256:f1dd2bb11c9c45e8b500c9108370d12b3a7e93eaedef7e455c339f671c542d05`  
		Last Modified: Tue, 12 Mar 2024 22:58:31 GMT  
		Size: 4.1 MB (4129648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f4cbfc024609956cb26330f1ca44f2bef3afd4d044ec41a175e01e1324e647`  
		Last Modified: Tue, 12 Mar 2024 22:58:30 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:bdb430f06229a092c6d68de0de97aa32ff79d56266e9d7e41f21dd40c95ae985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91823664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbf4af9cad21f8c3a7da82da5ec7e5781d4786cb22b6b95fbe150004f4688f8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
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
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d41f3a8e88176da522ecdcfb27243ff8242f2891b24c865c113974b1f6c78c6`  
		Last Modified: Wed, 13 Mar 2024 08:36:55 GMT  
		Size: 8.1 MB (8140786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51854233f8e6b65efa5673d4cc3a32ed96110ad9f485ef0f4ed4d77b56e4e99b`  
		Last Modified: Wed, 13 Mar 2024 08:36:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5ff38d96a5bac0bbf5c2ed176ffe7ae528d6d451f8faed09983bddbf945fe3`  
		Last Modified: Wed, 13 Mar 2024 08:58:14 GMT  
		Size: 30.8 MB (30827243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3b623cc416339cafffa4b77ec8c231d49552d7b0085283057951c28740250a`  
		Last Modified: Wed, 13 Mar 2024 08:58:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f04e02713e5e7e4c47028f0a9fc2d52670cf01621002fba72a6772e64c5857`  
		Last Modified: Wed, 13 Mar 2024 10:47:27 GMT  
		Size: 26.3 MB (26269996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41751edda5876c0769e9466532d153dc004e86d67cab18452dbb8508ca14407`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271f663ce1af5fa046ad19412f0152feab5bec4e34fc046d59e6eca78b583762`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b4b91c0168a1ff1da509857dd0b586df09fbaf8ef759cbe8d2faeed4291456`  
		Last Modified: Wed, 13 Mar 2024 10:47:27 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f528f74f74a46ba124bc3e273ee1116ce5070d44ab9a57f6b07b040738b94a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6972f9b685262ccdbbba13d1a05e72401f7cb3019a6f34b473cb4875d4ada46`

```dockerfile
```

-	Layers:
	-	`sha256:04e3ee64b961993d1260087a38bb3482398a03e18e3d04c3416038dbdc13c9d5`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 4.1 MB (4132416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f30629f1c53cb0f876338a4ec7940c4dd5253242727f3165da2448acd5ff0f`  
		Last Modified: Wed, 13 Mar 2024 10:47:26 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1111a7dd8eb347697a9ee48db8f6448115200a68742a131dd0e3e8836c3be268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98458051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93957bb0f0e3c4825eb7884629589a24fe343bbe38e5c3b0b8b4a0936a83da91`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb512b419861d39e27ddea7236798af420a58b2c85345c1a9fabd4b5ce2dfa3`  
		Last Modified: Wed, 13 Mar 2024 04:39:54 GMT  
		Size: 9.2 MB (9240668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0c0ad46bd96e85894a6ae1c392a3c301436efcdb83b7302f8b6a3bceec2a5`  
		Last Modified: Wed, 13 Mar 2024 04:39:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c0de5a9d784f8cccd4c319a0eac1b7910a04b48fe5613814a558a64bec950f`  
		Last Modified: Wed, 13 Mar 2024 05:08:28 GMT  
		Size: 31.8 MB (31780775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645dcc0d6737795e745d76565e4425492ec3f1662bacd3385818a9fd0aa2cb00`  
		Last Modified: Wed, 13 Mar 2024 05:08:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0546eff6f8c859779fc60c550beafb9d6c00378a7edbca27a7969d397831989`  
		Last Modified: Wed, 13 Mar 2024 08:41:56 GMT  
		Size: 27.4 MB (27362545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b276ad50b662f2b574a523e7bf0044c9b4d14efbca9d24b6161663cf000816`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930034ddc7a340b48eb0fa6dc7b78f4f76960a9b8e2736b11eff74c2ea16b710`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba184da4cf8af41e5dfcbef86a8d41455d0b83160ac07fa769510fa96748132`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:65e8fc17577ff0311fab5dd4a93fd71ea01af2ee3d0608300a068bbb0030b97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0cabb3c627cff4998ba475820ceef81b5681084a18ff3e4fa9ed144c99cdc8`

```dockerfile
```

-	Layers:
	-	`sha256:b4167d3e3e54b7f7311bf36bee92d70372819e34e713e2749df6b341fc635ff2`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 4.1 MB (4132771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c325a6ea37a5e3f0ea02918db62441621d49e00ad55273e184ea9d4d80016e2`  
		Last Modified: Wed, 13 Mar 2024 08:41:54 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:38e5dab2e37407748c0b4e1061850ee938ce3b2e5b27141b634d51b42e8f65c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101830807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb1dd12f35822c5eb1327206a81559d82d545274c4e4f557ff85210a7d4f559`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
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
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4449a78d85c35d005e14c02051f922c15ce85515f23a3b02f5d95fcdb83c65c9`  
		Last Modified: Tue, 12 Mar 2024 01:59:27 GMT  
		Size: 12.0 MB (11994381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68c7a471344332bd6c9ff70ff66428398bae6e17f2bd73e69f6ca4fd7a4ee`  
		Last Modified: Tue, 12 Mar 2024 01:59:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e1ca595a45956ba439220dba755b97ac59b4a300cd274ffba16e9ba70b8fc0`  
		Last Modified: Tue, 12 Mar 2024 01:59:28 GMT  
		Size: 31.0 MB (30969914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb226cc3333683c1f4fb82d4cba752052da4513dd11c7db0148c4d569dc33ae`  
		Last Modified: Tue, 12 Mar 2024 01:59:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b211b5f1c062969b142ab7ebd513564730a3b1cba3ede002895525109d0618`  
		Last Modified: Tue, 12 Mar 2024 02:57:44 GMT  
		Size: 26.5 MB (26456000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f28f1772a6b4fe98a7b6791b1966fc6f916da70b5820f8bdca91043729ddad`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5b10f7ab211e77e47be0ebb7f7ce1b09902bb9c060e087f9b9f9fa5a6b6ba5`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7578e1c859c2b7babf557d12c25595dd5e36d3e7be41122910f2f546441cc7`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e4be70697c515d4f2bf73218d2098261be34152e08ae6f97efd7ac6c1c24a683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc61a421991bf79c413395152aa88bb377d95b91b8aad505e6275f9aeb8facf9`

```dockerfile
```

-	Layers:
	-	`sha256:a8e410ed81162e3040268653c59266c97d4d215fc4e50c11cf30debc2c370e47`  
		Last Modified: Tue, 12 Mar 2024 02:57:43 GMT  
		Size: 4.2 MB (4162641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed93898a94398f417116f43a0d97235adccc12fa07c4bf47ee4a8f0da6d32578`  
		Last Modified: Tue, 12 Mar 2024 02:57:42 GMT  
		Size: 21.7 KB (21705 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:91a10199b3756f2e8313fa4dc9280543733efe24f5b7c3135ee960f6d45a396c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106451571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869ff3c5bcde70730b3654f539380fa4165d3e6d55d2f76be1d71afdccd02a42`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc02f8761ff460024c63b11ed867400af92083b7e0e95eac24d1761bf0288ab4`  
		Last Modified: Wed, 13 Mar 2024 07:18:35 GMT  
		Size: 10.5 MB (10479553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36a5e0859a09a8c472ea1fe096ec442ea6cb20f3a0b72b66f928b7a87bcce6`  
		Last Modified: Wed, 13 Mar 2024 07:18:34 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9ff491e12ca5f1ac7128f947d5ffffccbd95fb32fd6e73f134781adc3410b`  
		Last Modified: Wed, 13 Mar 2024 07:51:04 GMT  
		Size: 32.6 MB (32584181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37ee379dffdfd40d1d83484310d597c92ab39a100c6fa206ef45ef48e6e93ef`  
		Last Modified: Wed, 13 Mar 2024 07:51:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6fdad0e22a4f58bd761bcff8ea9949fc39a4905dc241a716aea3edb01aefd`  
		Last Modified: Wed, 13 Mar 2024 10:00:40 GMT  
		Size: 28.1 MB (28086897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85579f4098e1936dfbf5f1c7fc8ab1af9f54adab502c43e4dee8b251775704fb`  
		Last Modified: Wed, 13 Mar 2024 10:00:38 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657afe7e91f48836970bd63d64ad7b403d9aa00c8158e3ee612b7a7c37104bc`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca5de28251db9fec1e62be7e221e41b5cd2c276285dd4d30809248e56bc924`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0359a7cf809cbc92e7958ef32c7fe3291bedc3f91f8c0d3b56a140da97c154ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6decededdce1d8378400615ca0f8e3b2a251db04d9b94173494ebecbc23f30dd`

```dockerfile
```

-	Layers:
	-	`sha256:840b34bb813d8f0b3ee828e363b4b01dde43deea55a377d835d02655700cbe5d`  
		Last Modified: Wed, 13 Mar 2024 10:00:39 GMT  
		Size: 4.1 MB (4147326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8d7612b49a8b3803cd55f743f15a079fe8aba953342d10b06d109e450bddb2`  
		Last Modified: Wed, 13 Mar 2024 10:00:38 GMT  
		Size: 21.8 KB (21800 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:3ef38f43fcf36476b169606002a8ba6b601d9edd335431f219a95c1349e9a9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98578970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fded1edbc15785afa11cbfc74614a8547f9493aba946e097e442588b95462af4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 18:08:16 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
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
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f258da6cceecf5c0f7ccc2c92bc9661c5707ddc2d08dc3b54f9644f30df2dc`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 8.9 MB (8860667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bbe743c4c86dfe8406ae6e1ae48dd2188e11d67401106b7cdd68fc0d88ca94`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4f9ad750deefa633b927d79494fca8126ec9feee7557abe69da0c731e77926`  
		Last Modified: Thu, 15 Feb 2024 19:20:28 GMT  
		Size: 32.2 MB (32227693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c809275b504b3c323cc3a5b0f5125431ccdf548112269484cf00af9c234cc5c`  
		Last Modified: Thu, 15 Feb 2024 19:20:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd5abbb0faaadd016adddbb28b13446230346b2f274284e77b5f4d64729d76`  
		Last Modified: Fri, 16 Feb 2024 19:23:29 GMT  
		Size: 27.8 MB (27827507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f324329d1588c45d45f27be169dd3e2f13b6554f693c76a0b6646c0d26eca5ad`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e16f61bcf7782d452f4598eafbcb5cbd20f145f774c59697b3a154801c195`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27f1070d557515436e56911252f0c4a7d86e2dcc569a876de23de6aae1c9db`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8075112bdbd3f0be0ba8b36dee0115182da7a57b95143c456641cc801044219d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368ac10cd589370362faca8e7867487464e9c0df3bf40c3cee61a2e10e013e91`

```dockerfile
```

-	Layers:
	-	`sha256:fd26bf3c8a9b60d791d7b718b3c6b5880df1ead6d5d6ec5f21cdc531cf716379`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 3.6 MB (3618884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095d4659105db18254bc89694fba696765936a3f3011db64dfa17365c3746281`  
		Last Modified: Fri, 16 Feb 2024 19:23:28 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json
