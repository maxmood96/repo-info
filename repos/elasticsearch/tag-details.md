<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.16`](#elasticsearch71716)
-	[`elasticsearch:8.11.2`](#elasticsearch8112)
-	[`elasticsearch:8.11.3`](#elasticsearch8113)

## `elasticsearch:7.17.16`

```console
$ docker pull elasticsearch@sha256:fa2d4b8b61463150d12533712cd7e656423ec9d1fb1ea81dc6bade7816ad528d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.16` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2701b3b14cede7427a1b1c431329d116c148b046e0fd51e1692ff4fc7b85609d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359794117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697bd265a575670964f47521902556d61d9c2f7f171415cd9b64ebd9532b7d24`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T10:06:54.672540567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b23fa076334f8d4651aeebe458a955a2ae23218 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T10:06:54.672540567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b23fa076334f8d4651aeebe458a955a2ae23218 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0392900c090e0874026902fcf47570efe46a3ad865442d3405133fd9d5d1f2`  
		Last Modified: Sat, 16 Dec 2023 10:49:40 GMT  
		Size: 7.5 MB (7507967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e1fb8f2e7018d4149fa020b7d8a86ebf994b3bfda9c7082ad280bec5bd497`  
		Last Modified: Sat, 16 Dec 2023 10:49:39 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07542030d0683cfb3c2e788a23ba0f6d3e68a570b52c6c5ca9189f63f60998`  
		Last Modified: Sat, 16 Dec 2023 10:49:45 GMT  
		Size: 324.5 MB (324455734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4ccccfb1b809375ba9cee7a276f6f8dbe3fa587c07c724cb95405027b7ff05`  
		Last Modified: Sat, 16 Dec 2023 10:49:40 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e174847d32055c4f97fc38e1daaf8a0bd99bbc714d73a81c37d4f92cc1dd0570`  
		Last Modified: Sat, 16 Dec 2023 10:49:41 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f8c3340002597eda9bbe5dde18ac80b13821d4584862dd0a44dbf270ca872`  
		Last Modified: Sat, 16 Dec 2023 10:49:41 GMT  
		Size: 192.1 KB (192139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a5da86cfd8a041da96c5ef53efaae037ef64f0c1591386ef3660ae95c17daf`  
		Last Modified: Sat, 16 Dec 2023 10:49:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f9700eab1ef95eaab31593030f82816b1ce3234f472ae3ac8664da930aa3c`  
		Last Modified: Sat, 16 Dec 2023 10:49:42 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:73c70f673d17ac6df8e8403ef165b737e40d8bcc15b5d5a9bea2c314d95bdd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a956f437c186cf5a8e522464fc3f8da1d78c95870b6a288e89d05d399b25b2`

```dockerfile
```

-	Layers:
	-	`sha256:14b741a0405c8c20b72a53d0ce8a6944da335bf2d76a17c2f9c4d0819b23ef6b`  
		Last Modified: Sat, 16 Dec 2023 10:49:39 GMT  
		Size: 2.1 MB (2069775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b83c7b1dc543de472b4aeda9f41214bf0c4d7b104b259272be0a5cd3531ee5d`  
		Last Modified: Sat, 16 Dec 2023 10:49:39 GMT  
		Size: 37.7 KB (37742 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.16` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ef9473a9d447bd09e8f278ca55bce993f6718e320b59c67ff9c8cebabda09dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356008387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e945c491a342c588b989cf2ebfaca64bd897ef41079ec02ae95f4c760a09e1e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T10:06:54.672540567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b23fa076334f8d4651aeebe458a955a2ae23218 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T10:06:54.672540567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b23fa076334f8d4651aeebe458a955a2ae23218 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267a6aaeba7c0ad2ae15343e114cb50dfdb25bde0232df9a69f6578cc0ec2a1`  
		Last Modified: Mon, 18 Dec 2023 19:53:16 GMT  
		Size: 7.3 MB (7327973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314340ae71fad54fe2bde96fe4b9ddf0ba484ab3aeb8d6c94a874a1074305cc4`  
		Last Modified: Mon, 18 Dec 2023 19:53:15 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ffe7d055edc8c8aecd186efaabd33c1a1de4f2e60ad0b12fda4ecf1edf57e`  
		Last Modified: Mon, 18 Dec 2023 19:53:23 GMT  
		Size: 322.4 MB (322394402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b9b4eb3bfda9c2f1cc9dabbd9d7e0f91779f92d3575beba61da73b5122874`  
		Last Modified: Mon, 18 Dec 2023 19:53:16 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a47eac053fe6de44b779c90cab9ed1967786ec9d733bd3d05a8a23b4268d53`  
		Last Modified: Mon, 18 Dec 2023 19:53:17 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32253d29a7016b9341dfb8f267cc3e8b55624be86b5f41760d2a3f958003d74c`  
		Last Modified: Mon, 18 Dec 2023 19:53:17 GMT  
		Size: 186.2 KB (186162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d1c1588278519d61bc3da145e39363eddc7bfb76e2266264bfd3167437a2b5`  
		Last Modified: Mon, 18 Dec 2023 19:53:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c32842f215710335facb043938e7f09eaeb69fbee3d96fa1af0e94f07eda26e`  
		Last Modified: Mon, 18 Dec 2023 19:53:18 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:7416b02feedde4e4ea2b5f04f17cd5edd5672d488eb1a838d024196411d37588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba70acc211c3547cb0fb45472f805c1213298adf922a014e1c9e3032016780a`

```dockerfile
```

-	Layers:
	-	`sha256:faacf40107f65d452f08a427e1ac748fa500513e527115e2377a596ef4e27449`  
		Last Modified: Mon, 18 Dec 2023 19:53:16 GMT  
		Size: 2.1 MB (2070098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d1e103986790d94259790ffb58e96497a4d02a9326a3cf58e470ce37d50b3d`  
		Last Modified: Mon, 18 Dec 2023 19:53:15 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.11.2`

```console
$ docker pull elasticsearch@sha256:56257a116f4b5de1ace0fe40ced4a8495efd6cadae8889b14c49afb62c3eef25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.11.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7ec8e6e6eb32522e42346288ddf87eb7a63ffb2afea47bb3d807b43213bb164c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.3 MB (673279297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd23e0d92af843760d60bddce650814844ed657923ddf401b49b8301befd0723`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Dec 2023 12:34:16 GMT
ARG RELEASE
# Thu, 07 Dec 2023 12:34:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 07 Dec 2023 12:34:16 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T10:03:47.729926671Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=76013fa76dcbf144c886990c6290715f5dc2ae20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T10:03:47.729926671Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=76013fa76dcbf144c886990c6290715f5dc2ae20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["eswrapper"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1b2d3060242e81915ea135bc9bcbd11f8a981ee26f1453db7dd8e2e8d1693`  
		Last Modified: Sat, 16 Dec 2023 10:50:29 GMT  
		Size: 7.5 MB (7507938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581503f8352f112b3935bd3fe47e04b75d9996fb6f16fd1afb8f4f800665179d`  
		Last Modified: Sat, 16 Dec 2023 10:50:29 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29ac748c000264a4b5cc14719be283c76d670b22c4a84ea972c415f552a5fbc`  
		Last Modified: Sat, 16 Dec 2023 10:50:43 GMT  
		Size: 637.9 MB (637941465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf24b99a884370c20573059ddcd56e4d713f08594189374a8a4f739ae0e5f94`  
		Last Modified: Sat, 16 Dec 2023 10:50:29 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021f7a48ece6b33dad9927fb9665a38b788bf9742d268de0ca1b9097a66434e1`  
		Last Modified: Sat, 16 Dec 2023 10:50:30 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b2302c3a0b5a91ee54d72cf186bdc43046defc240efb50086d48d8b8a66ae`  
		Last Modified: Sat, 16 Dec 2023 10:50:30 GMT  
		Size: 191.9 KB (191875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e93798e494890a0971c68571672f6eab64313bc352b38d311b2f8d30fbe511f`  
		Last Modified: Sat, 16 Dec 2023 10:50:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8cb414bcdb6faf94408bf9af63bede825babb42317d1b0e11849f3ebec2a2c`  
		Last Modified: Sat, 16 Dec 2023 10:50:31 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:790df170b272ecbb8671a9faf48efb7b95cfb7cdc4f8a541db03d3c58bd77b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd4f47bb3ff90d649537597f66cad1cab62d75507d06633a02b497f82cce140`

```dockerfile
```

-	Layers:
	-	`sha256:1b2ea3c736caad1cf8d2827789f890bc553a7a93edad37cf8d346bacbb0071ad`  
		Last Modified: Sat, 16 Dec 2023 10:50:29 GMT  
		Size: 2.3 MB (2339082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad4463453006c62811eb4121ad73918fbcd3980b183d43ad957634f9314c487`  
		Last Modified: Sat, 16 Dec 2023 10:50:29 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.11.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9e4c19d83455009ae97cf43bfbb6a4c73fee3338cec4848ab452b868a0402c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450760898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd6ceb923afa2ce9d1507a6a3f88b5b71ac4d92e615fe5f5d7f6bff92f24cc5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Dec 2023 12:34:16 GMT
ARG RELEASE
# Thu, 07 Dec 2023 12:34:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 07 Dec 2023 12:34:16 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T10:03:47.729926671Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=76013fa76dcbf144c886990c6290715f5dc2ae20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T10:03:47.729926671Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=76013fa76dcbf144c886990c6290715f5dc2ae20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["eswrapper"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be98b1d6e32cc22228ec68b71e2945257970e71f3a550061a4abecd4492d29`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 7.3 MB (7328019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7cc25a9ed6ca506a18bf041b668a08ef9a82e1c729ffb8271bba1b89a972e0`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c65f57748854dc99277f9c58a2b86e30667a25b2f519be6fd96665741f36e`  
		Last Modified: Mon, 18 Dec 2023 19:52:55 GMT  
		Size: 417.1 MB (417147366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d401c7fd579dae5b355a9f65b690cbcfdd3656c0e3d3423841f042f3bb9f57b`  
		Last Modified: Mon, 18 Dec 2023 19:52:46 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b43f11c2103897bbc8bb17f39cdac76ad402cbf3e2d3c7b41d10699b496c452`  
		Last Modified: Mon, 18 Dec 2023 19:52:47 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26615167d2a8bd9c805b3e6123ead3cb59192b518832a6398773bb9a7befb14`  
		Last Modified: Mon, 18 Dec 2023 19:52:47 GMT  
		Size: 185.9 KB (185908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057712c441357141114ac94ea9f987bd7294bd7ff8ab4e5a1ef363014097bf96`  
		Last Modified: Mon, 18 Dec 2023 19:52:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9329b84b1573c3863400b9f6bf08cf01bed289561335306fa5f1dba7c1b991bd`  
		Last Modified: Mon, 18 Dec 2023 19:52:48 GMT  
		Size: 109.3 KB (109258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2dbf922b48b074c66b22ec1824cd6359d0217716808b27990abdf46d25f28255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee51972bcafa4debf5af2dd3aa02b5e9b0d24146fe3a0b7db2f568f4a1dba777`

```dockerfile
```

-	Layers:
	-	`sha256:07c6401cef7b3efd03dfade9a32bdf9065947a6140ac0a00c0e2c238133af5e2`  
		Last Modified: Mon, 18 Dec 2023 19:52:46 GMT  
		Size: 2.3 MB (2339413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e70db64c9504d58bb6d4b29c2ee64f2a7f28a26a2cd462062230c473df6f23`  
		Last Modified: Mon, 18 Dec 2023 19:52:46 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.11.3`

```console
$ docker pull elasticsearch@sha256:58a3a280935d830215802322e9a0373faaacdfd646477aa7e718939c2f29292a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.11.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0e47a784b266b7f30d8071a25f774b10a38f3bb9bb41e23a2767ba464aafcb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.3 MB (673285089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1eef4151323a027507b73e0536f971b5a2181f3c0e77b37b335c84e37c1340`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Dec 2023 13:07:20 GMT
ARG RELEASE
# Tue, 12 Dec 2023 13:07:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 13:07:20 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T11:33:53.634979452Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T11:33:53.634979452Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["eswrapper"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88b906db9c15d2c19cbad2233f11145f77d05494442b029fbb62d21c7a17ad1`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 7.5 MB (7507922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02840f0dd2d9ceb41fa735b73717dd0f7d312194d56a2f3e99d49f8e666336a7`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36bf0362a7bdf86ca6ac3913102fe7d18545adbdf3396fb36630a83ada3cc1f`  
		Last Modified: Sat, 16 Dec 2023 10:50:44 GMT  
		Size: 637.9 MB (637947273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfad007f0aceab44ae4666c1f29057e4236068fb3c1d1ffded6e06943c9e8bf`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcb210dd3ca5dc1d2a3857f12ca89154853b676442284131db2777c7a265cd2`  
		Last Modified: Sat, 16 Dec 2023 10:50:34 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bae0d7353fa7ad39a03e97c711bee6887fefd83adabbf268eae420eaaff13a`  
		Last Modified: Sat, 16 Dec 2023 10:50:34 GMT  
		Size: 191.9 KB (191877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa937b89ef3ee82ce67b4d85be7fa6ce4fcdb9624ee855add8a84d6c0b1f374`  
		Last Modified: Sat, 16 Dec 2023 10:50:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132da5d7ea559eb1228766a02223dfe2df191fe6a0d4cf70547c2e6a5c76a14`  
		Last Modified: Sat, 16 Dec 2023 10:50:35 GMT  
		Size: 109.2 KB (109244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:42dd20e51b3a7472d4ad1ce3b60b1b7430dc28db4ef03f59913a65401f442432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf2acf6ca8c0bdc1c9740b9975e73217ee98de0014dadbe2b330382a190faf`

```dockerfile
```

-	Layers:
	-	`sha256:157f68bbcfb0e3689702ecea161c39617ea1ad353cbef195dc61d3faf06ae866`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 2.3 MB (2339098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1170dd9f7df6540aefc6c9f0ff475c564ffb9e4154021ae1f6fabb4fdb9d9c`  
		Last Modified: Sat, 16 Dec 2023 10:50:33 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.11.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dfd29b525bbcab4db2a4331ceec6afad439b575876a33031d20d28066636ddc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450766366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23562195abe6c4d92cc3fb2a37e4c03fe2c4fc475b409bc01c98e0c9ea527c5a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Dec 2023 13:07:20 GMT
ARG RELEASE
# Tue, 12 Dec 2023 13:07:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 13:07:20 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T11:33:53.634979452Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T11:33:53.634979452Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=64cf052f3b56b1fd4449f5454cb88aca7e739d9a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["eswrapper"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be98b1d6e32cc22228ec68b71e2945257970e71f3a550061a4abecd4492d29`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 7.3 MB (7328019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7cc25a9ed6ca506a18bf041b668a08ef9a82e1c729ffb8271bba1b89a972e0`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f72b7d4c4ec3505cc4135c5a70ee8bbcc88b666d40197b5a82553f7835e49f`  
		Last Modified: Mon, 18 Dec 2023 19:52:28 GMT  
		Size: 417.2 MB (417152832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3530ea43210936df1dc5fdf12d0def7dc630dc9a54be58a2474e0248942e7366`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d0e1d2c4e75c388ba013940e6307c7dc4f9181a2f6db5457c49b3830517dde`  
		Last Modified: Mon, 18 Dec 2023 19:52:20 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aae14f2951577930b78ec281868b8bccc0e9a7e542aabe78ddfbdb38dfa0fd0`  
		Last Modified: Mon, 18 Dec 2023 19:52:20 GMT  
		Size: 185.9 KB (185909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd08817fddb315b3a83c9e0e0c05ffa1044786e7bafa966db4a226815ad94d47`  
		Last Modified: Mon, 18 Dec 2023 19:52:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bf5c8dfa3bc005ba3c938c64dc2c1c2f4d51eedba5d7420842011d0368da73`  
		Last Modified: Mon, 18 Dec 2023 19:52:21 GMT  
		Size: 109.3 KB (109261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.11.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:00b79d2b09eeb064b7e0fee3cfc65f233331c34994f6ffb732da458bf1d4eb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e06f3af6e49318cb42c8703d7e82c15bdeff0486fdd32d79cd9268dd5bb6e9f`

```dockerfile
```

-	Layers:
	-	`sha256:162cd430d18ec39d110a9dc7fa60cd3a4cdbc726e60f06ede48432766fd7da6d`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 2.3 MB (2339413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e926a363efa04f8e68d084ae086f9ffda6bf646e591c796015fac6de9ef8e1`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json
