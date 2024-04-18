<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.20`](#kibana71720)
-	[`kibana:8.13.0`](#kibana8130)

## `kibana:7.17.20`

```console
$ docker pull kibana@sha256:81d3c458373bc8aaba1805714c304d89f992aed7df9781eab27a347926457ed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.20` - linux; amd64

```console
$ docker pull kibana@sha256:ce6da794d6308a4fd3e243c009eb908a1e9d5fa0f1333cfd3a1c24c4f2dd1872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360565069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991143f55922404e284474926c59a0b3164c5dbe641b7c101bcc052ee53e29df`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ca70d9a06f149f64aa7897bdfb51e9459dea15a8c1b007f85e558195e0647f`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 11.6 MB (11580838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c1b6650f92cc71b6eacb401802a10759fdfb51471d788458b3255125dc786`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2a1ad44b2c94a2fc92f075f9d2901821664e5f98cf6b7721477d6397b4858c`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6951d00fb782b3dbd8a896caf9d3822c05fa2c6ed3fc98f72a5bba23b40d2acd`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9420d44314b322e4dc9798f36daea84cb7b01a22468408bcbdd18055748a6`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045e0c38010acd3ca9fb388f3408aa7a57dfb6036cb418d297fa7fdd6a76f594`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 304.8 MB (304800212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0db2b355eaabce0bcf181af1a27054504fd335df45abdb01abe8a288279d5`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2687ff44196c3f3e7717b4787718af27d687a53d2de50c60fd98c4eaec5e0330`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdadaf31762092ca5161250a7e50aebe1cce7f4fc81c1a87aa64bcfa07d9b18`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4867cbfe45bd25e5076bc5e0040c61b8ebd031cb158290292e0114e26a0264`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258a9654aca7392d8e8b72889f1bed3a448f2e08b13e21ecda4f545aaac323d6`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2eeb64cf73caaeee19af103e3de695247431e21907679193866df17f084924`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:e76421cc82b3ae539b5cbc28b93bfc72ec4f23d6a8127e978e7a5fdfa4a9f349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac5b495e87b47c51e19ba7c404aaa407049304062b5a52b435822f145efbdd9`

```dockerfile
```

-	Layers:
	-	`sha256:672c66cc280f0e9d99ae0219311fbb34a432114698fd812399051980ca70aa72`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 3.3 MB (3289902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce4a9c6de2de008dc5e43c5fdbfaf7fcb3426f722c1fbc5bbdadba7c83fede8`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 44.4 KB (44363 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.20` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d6ef6ad700485132d9cce8a99e864532ed59d08c414578b17939b717192c1fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370942071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d66f86dcc5860531f705a2ada1128b7cf6b1241ff0ff7758ba6177d52172e4`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be3e0ca1f245b261a2e3ea462fa017e4ba5744fa43b3dd7dbf74648f0b2f141`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 11.4 MB (11393565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4deff12b3b413b54ea9a29b3fdb7796582180f23355031acc0b3a730511eb`  
		Last Modified: Tue, 16 Apr 2024 10:44:02 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4b2239e5048626b442615222224cc765a569d0e5c8fbcdef06ec04c0eba249`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6107a2a242f6aba97de63bd5df85b42a25287786ea2624a1774c82f62e406841`  
		Last Modified: Tue, 16 Apr 2024 10:44:04 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e2a8daee61fbe438bbc741bc23ffa1f9386fcb0e26111b32240efa82065c`  
		Last Modified: Tue, 16 Apr 2024 10:44:04 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2ea1873796f635ef8537e0a0eb55e1e87d622105f4b81b7f086d23623b6729`  
		Last Modified: Tue, 16 Apr 2024 11:19:34 GMT  
		Size: 316.9 MB (316907884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ba1cbd5eba2adf93a5d6f3ccc170bc47f1c5af73ccc1e5b28cebbd92bc3457`  
		Last Modified: Tue, 16 Apr 2024 11:19:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8960a7702ac6c91e876580d3e3e9f932790bda3d0e2e23c478ccadbafab8d9`  
		Last Modified: Tue, 16 Apr 2024 11:19:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a460c4a1cd80a962412c1f0714bee5325e1d8008b731a9a2eba5fa8f24dd8d21`  
		Last Modified: Tue, 16 Apr 2024 11:19:28 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59c7d8f819e7898da73db9a0c06863ef44af4ea23b979a140be022b8b831459`  
		Last Modified: Tue, 16 Apr 2024 11:19:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e51951dd089f284d6ae432bd4b744249295a4444c61afa54b1a29ebb464d20`  
		Last Modified: Tue, 16 Apr 2024 10:44:07 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ed4d52b32017c0c3a907226c9f458119af3a2e2807d0fbe94c020ee7ca0526`  
		Last Modified: Tue, 16 Apr 2024 11:19:29 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:f1254a47511258e5db8ffe1cb4b7024ff56bf3fbb99705cb03b0f76f9f38d84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee2624ac4d2b4ba30607c8fe915db873ba13a76599f32b4e9f8fff670fc7fb9`

```dockerfile
```

-	Layers:
	-	`sha256:685c16ff311988e34514e1d14d074d554be5356ce66f78069e96d35957daac1c`  
		Last Modified: Tue, 16 Apr 2024 11:19:28 GMT  
		Size: 3.3 MB (3290137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34a17d800175a5ff570f9b083ac6d274e29f1ec6fa8fce1c30f315b1d2dd1ed`  
		Last Modified: Tue, 16 Apr 2024 11:19:27 GMT  
		Size: 44.2 KB (44205 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.13.0`

```console
$ docker pull kibana@sha256:60f9dea65872b59a245e32783f5497b6215a0c88a6a38b82e85a77e946208292
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.0` - linux; amd64

```console
$ docker pull kibana@sha256:d49bb88a231b7bb7acf9dc92b915325480a428ddaeeb7f355f76b126dc2acde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.9 MB (375929068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eea0db0a4b07327315fda2b327125aa5f9a9252c437602de5650a59420a921d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5a3edb2abd7826997997d1309ee9753ef1a565c28ee79291dba4eede9b78c5`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 11.6 MB (11580885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58960dff290233a2836d157ff6f1b983101305e6d7982bff6e12b5834f9a56f7`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95e25456d28a79011c942ce50b2ccb944e03e3d69bf243ae1badbae95bdb2b8`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d883d1421fe9ceebaf897a17aa2b603e5c58d5ead4cb8f0ce05d9b7770f7c`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a479d4ff521ad53ada831352f253a819d92165aa0351a0fbc6c5f62f0de83`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 5.3 KB (5292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874e163cf879e2403037506626abf5a7822d917459bf6cb1b24868899b8ee51`  
		Last Modified: Tue, 16 Apr 2024 04:28:20 GMT  
		Size: 320.2 MB (320164088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818464c02fe5350ac16cb2d8361cdd2dfc899c6f5bab6b1f9d86dda99642581d`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a218d9d98aecfe34699161be1d56ca6f7a4e777e7443a06ae656822a79aaeba`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ffa6ce416ba36cc665d6ffde3b7d46b4e81d1035446fa2b7f76c57d7f566aa`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 4.6 KB (4563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d1e5de15cdaad966db7af0071e0256721cfdbf8c00cda0bf9ade3be26ef94e`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876b6997c43ab71b120aebbf60609d7fc5c285d9fee48def60bddd31837759f0`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 189.4 KB (189429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec46a661a3e774666f0c4e9ace78e8be9e6c85e655de883f0a1dc96767223f6`  
		Last Modified: Tue, 16 Apr 2024 04:28:18 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:8e9cd8741f34357b945237a0c5268814fa133fe2b3b6e83475c8e5ea7fb5e80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3793944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5291d7fcbfe5147b9f701fb62fc0ae6293074456b4a90ab68c6316914d40930`

```dockerfile
```

-	Layers:
	-	`sha256:4186065a74691cd194a93a16cda7067c0fe1626ca1126baa5aaa0f8aface2190`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 3.7 MB (3749593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7811e12a23aeeb3118cbd8137c8c273251ba69d8598938f00382830f11748d91`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 44.4 KB (44351 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a148ba2b2473d4736bcb80c1d914562cf5d9d4dbc898bda1f668d3c57b926c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386328638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e7daf5ebb67e1ce6298cdc509ec16a847ece065aaf8df5539abb73691efef1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be3e0ca1f245b261a2e3ea462fa017e4ba5744fa43b3dd7dbf74648f0b2f141`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 11.4 MB (11393565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4deff12b3b413b54ea9a29b3fdb7796582180f23355031acc0b3a730511eb`  
		Last Modified: Tue, 16 Apr 2024 10:44:02 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4b2239e5048626b442615222224cc765a569d0e5c8fbcdef06ec04c0eba249`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6107a2a242f6aba97de63bd5df85b42a25287786ea2624a1774c82f62e406841`  
		Last Modified: Tue, 16 Apr 2024 10:44:04 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e2a8daee61fbe438bbc741bc23ffa1f9386fcb0e26111b32240efa82065c`  
		Last Modified: Tue, 16 Apr 2024 10:44:04 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622451d9d361140d776fd73b2cd1f2652561e9c748d0e6f79148356c69f2f03`  
		Last Modified: Tue, 16 Apr 2024 10:44:10 GMT  
		Size: 332.3 MB (332294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0cddc021a6ba59c65190bdefc0b59862925ae5a8bc0af4eeb04cd24296cd4`  
		Last Modified: Tue, 16 Apr 2024 10:44:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d66a014da205161c0a0810a1a03cb89bbf96c16446660807f1201f97869597`  
		Last Modified: Tue, 16 Apr 2024 10:44:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32c642c764e53bf8d4f02cf7ce6c4f13bb789e9a79794e404da26ff26a00b63`  
		Last Modified: Tue, 16 Apr 2024 10:44:06 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d32034051fd5c9a0800e3904a644457b7b4d5b160d32af372114786805e318`  
		Last Modified: Tue, 16 Apr 2024 10:44:06 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e51951dd089f284d6ae432bd4b744249295a4444c61afa54b1a29ebb464d20`  
		Last Modified: Tue, 16 Apr 2024 10:44:07 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae2bcada80e248d1ca351617677467bfc8375ae7b7ff0b37fe6b0189612368`  
		Last Modified: Tue, 16 Apr 2024 10:44:07 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:2be7a2bfb7f48bc647ffec69f70c8d98108db143e8bedba821e62aa681f24a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf18d691694b8483bc6382a1d554f4b8d7415428245851d753563c2619c03ec`

```dockerfile
```

-	Layers:
	-	`sha256:f7f285f8df33d279ff9246c89f66dd5f2fba4bf2b1aa97f2111873e7d3fb1a4d`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 3.7 MB (3749828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff791d5c076f32e5df697091e2288b37c11d623ca61ce5a15503c41d8e629d6`  
		Last Modified: Tue, 16 Apr 2024 10:44:03 GMT  
		Size: 44.2 KB (44195 bytes)  
		MIME: application/vnd.in-toto+json
