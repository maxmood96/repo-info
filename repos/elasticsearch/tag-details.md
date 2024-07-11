<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.22`](#elasticsearch71722)
-	[`elasticsearch:8.14.3`](#elasticsearch8143)

## `elasticsearch:7.17.22`

```console
$ docker pull elasticsearch@sha256:432f21444d8b70a4ab5fc64f9ef7112aaf0c21361948f2deb26d7a5c7333cf35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.22` - linux; amd64

```console
$ docker pull elasticsearch@sha256:cf256cfb76bc1d5f481458f270a3f990e47beec5fcd6cb8a1cc35c05a9a9415d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362597016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce3c4c30eb550962fddc973ba91603bd9cf1c61f628ce269c1d0ae29355a4bd`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 13:25:43 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Jun 2024 13:25:43 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 13:25:43 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Jun 2024 13:25:43 GMT
LABEL org.label-schema.build-date=2024-06-06T07:35:17.876121680Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=38e9ca2e81304a821c50862dafab089ca863944b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.22 org.opencontainers.image.created=2024-06-06T07:35:17.876121680Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=38e9ca2e81304a821c50862dafab089ca863944b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.22
# Thu, 13 Jun 2024 13:25:43 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 13:25:43 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d57607415812620c166891160d912a2612be29570ad73933d07f872e12035e8`  
		Last Modified: Thu, 13 Jun 2024 18:15:25 GMT  
		Size: 7.5 MB (7513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8a589db2833c9a4dad3faf88bc85525de631fc8d3af33da4cf1e2b496aa92c`  
		Last Modified: Thu, 13 Jun 2024 18:15:24 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de852cf9394c4fd64cf02d039c915d57a61a4cd6a65e3c52108d9e065057e9`  
		Last Modified: Thu, 13 Jun 2024 18:15:29 GMT  
		Size: 327.3 MB (327254495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe3521d24f8a025810085140bfbb3a7d646639ab040303eba6e067a2f8a6ee4`  
		Last Modified: Thu, 13 Jun 2024 18:15:24 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e89d681f9c6a0be1cba940f76f7b950058ab299aed13b72777c42e7919dad3`  
		Last Modified: Thu, 13 Jun 2024 18:15:25 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e41cdb072e4efecf0ac1e31360b4cab5740237840f3bfc2be1e181b80c792`  
		Last Modified: Thu, 13 Jun 2024 18:15:25 GMT  
		Size: 192.2 KB (192175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05de06c8de786d9fc0d74625b72ca310d57a6a2dfc1b3a5f1a534d479a9c174e`  
		Last Modified: Thu, 13 Jun 2024 18:15:26 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a76b606d1330b462c363fa5f2a184c22a4b2dfa6326a94745031dc79a6eeb6`  
		Last Modified: Thu, 13 Jun 2024 18:15:26 GMT  
		Size: 109.2 KB (109246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.22` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:81d4be134bd6c1bdcb9bedf2a700b589e1438cb06cafd5cde55319996230c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11bf3c8a8ab83a5bd2cbce587adc967f1bff73882d5f8de7702c921290785e9`

```dockerfile
```

-	Layers:
	-	`sha256:90b96777fc7cc63c232ca0d26e6a7cad6b942ed4fe5e928fe7ec2c3693a9f3f3`  
		Last Modified: Thu, 13 Jun 2024 18:15:24 GMT  
		Size: 2.3 MB (2312535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb23490574ecb52055f0be275e382a7632d85c9e4755ec16221b21290ea63cc0`  
		Last Modified: Thu, 13 Jun 2024 18:15:24 GMT  
		Size: 37.6 KB (37633 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.22` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:27a7c1226f95c3ce882ff73fd0b7abc19f6da1f473e965048a7ab0460ee6a373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358539876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ff1f697c87f0d1d0eb9e3487ec2a46ba7be382f43388272ffabdb5ada58e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 13:25:43 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Jun 2024 13:25:43 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 13:25:43 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Jun 2024 13:25:43 GMT
LABEL org.label-schema.build-date=2024-06-06T07:35:17.876121680Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=38e9ca2e81304a821c50862dafab089ca863944b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.22 org.opencontainers.image.created=2024-06-06T07:35:17.876121680Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=38e9ca2e81304a821c50862dafab089ca863944b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.22
# Thu, 13 Jun 2024 13:25:43 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 13:25:43 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b1fd8f908356040db6d18b5ecfcbcc3827b850649a748aaf4572907ae307aa`  
		Last Modified: Wed, 05 Jun 2024 14:31:52 GMT  
		Size: 7.3 MB (7332205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4867208bc43d949659aef9fec85dbfcce32ab469974fe29a4262b930a7e82e65`  
		Last Modified: Wed, 05 Jun 2024 14:31:51 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04c22a767d6bcda0a2cc139619394769f36dab67910532c43193752af9bdc0`  
		Last Modified: Fri, 14 Jun 2024 03:29:48 GMT  
		Size: 324.9 MB (324922149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba3621c33dc7b404827749a92c5eda05fac8770b99a378b9ee753662c0c5fd`  
		Last Modified: Fri, 14 Jun 2024 03:29:40 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfdd83a65b2881ff31215a8d93f3c3e9e7a9cc16d5e2115aa3a4f1fcf79fe53`  
		Last Modified: Fri, 14 Jun 2024 03:29:40 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a62a76727bcd0a97aa5d715344748ed3067d27fc6dfd80725845b44e503d2e`  
		Last Modified: Fri, 14 Jun 2024 03:29:40 GMT  
		Size: 186.2 KB (186195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354d7a8b0a8237fa31c6ce9df9ca34fb1e87fb7225112b98581331627e99d89b`  
		Last Modified: Fri, 14 Jun 2024 03:29:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcebe71e1f394e9155dbe020c5e266018ed2bd13558674127b963a37b022c0b`  
		Last Modified: Fri, 14 Jun 2024 03:29:41 GMT  
		Size: 109.3 KB (109255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.22` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:affe2795136e38798cb1f274382e01ae1f010bd9f6fd745d01fa983cd121a56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fb522602062c31b243e743c81d27959940af8becfdb4b8436aaeeef82d0b0e`

```dockerfile
```

-	Layers:
	-	`sha256:c36efa1e570911041434643cca47499ec5514167bb39d0b24840a1a527694858`  
		Last Modified: Fri, 14 Jun 2024 03:29:40 GMT  
		Size: 2.3 MB (2312767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca9db866c32a9030ad2b84611c78ae8c64df541c33e4e8d73f759f247816f64`  
		Last Modified: Fri, 14 Jun 2024 03:29:39 GMT  
		Size: 37.9 KB (37898 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.14.3`

```console
$ docker pull elasticsearch@sha256:1ddbb1ae0754278f3ab53edc24fcc5c790ebc2422cc47abea760b24abee2d88a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.14.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a2dd3751a14b3065599b6c9a03b98e3ccdea38b4cce3e6175e06b2e687c09b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 MB (629677670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482b5962b08aec7c83a8af3c8aa2213d9a55ff6d6fea7ae2c2fcd9721dbf7299`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 08:06:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.build-date=2024-07-07T22:04:49.882652950Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.3 org.opencontainers.image.created=2024-07-07T22:04:49.882652950Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.3
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Jul 2024 08:06:13 GMT
CMD ["eswrapper"]
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f01394c961642feba99833afd6e5b72eece97f65788aa93e14b758678b5156`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 7.5 MB (7513089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14877811f740b24a4ce715b7e9f6e52121aefe6669ba1da1420292c13f47347`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947b5a7f8b6172d2c03c73c9a4c46718125d632a8e45327eec9b945d152b495f`  
		Last Modified: Thu, 11 Jul 2024 18:00:19 GMT  
		Size: 594.3 MB (594335675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d31234dbb5c647aec75e8a5701a7c6bedc26002fbfc9577ba11e4993a7196f5`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70362de5376682e204928a75204d38e725fbbdc7593ea9ac6bb00d37985d1573`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe6af6dc09451dabafaa0926aa68948a1298355069d3497fbadb49b7fc73f4e`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 191.9 KB (191897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f706f54d11b27ba064bbfe047fb467de2f4c81f283b2bb293743fea4014f20`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fefb920fd9f78d5ffe5c3c3ea77265236113e02e4f3fe2145fce54f8ad1040`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 109.2 KB (109246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c045006a04b803f37200f40377ade88060a9ae07aaa71512a0aa3e2f8f53fc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6b2a3a9c761aff1bfc5a31d09f779605681b826bd37147bfce4533a13e593d`

```dockerfile
```

-	Layers:
	-	`sha256:077a6cb3069fc09a9d65910d2ff385bbc63018f3500c5e11e420caacdceb5435`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 2.6 MB (2594341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8943902b07f158122ad468d85ae3ea806a5aae8ffab710eaae43f58a63457251`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.14.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c36e6d78c75781986589729963e3a7bfb08ddea67d862f6bd2cfe319ce5ab1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.8 MB (473779581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c359bb77b58216a54a4d53a7fa95f9ded45f3b19a647e85be1f7e87bca48953d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 08:06:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.build-date=2024-07-07T22:04:49.882652950Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.3 org.opencontainers.image.created=2024-07-07T22:04:49.882652950Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.3
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Jul 2024 08:06:13 GMT
CMD ["eswrapper"]
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ce06f3ebdd8fad176f7e7b06b32bb2e58ec533924c4527290efd4a012f77d`  
		Last Modified: Mon, 08 Jul 2024 18:05:17 GMT  
		Size: 7.3 MB (7332124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c67457edb7cfc5cffdf9c4e2a2536ef5c4fe78798f863acba17125b6abc9cb`  
		Last Modified: Mon, 08 Jul 2024 18:05:16 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f8b5c24e985cacf1919d6c8b5481fe963700b5581ad5ae65c38f043a08145`  
		Last Modified: Thu, 11 Jul 2024 18:00:45 GMT  
		Size: 440.2 MB (440162470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d597e584ad2f31416c78f48ed5d578dad22000115d736687303116b4583a5c5`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8544774e1fac869670e803191ff2377e7c980698c7ca93da45721295505bbaa`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e862c67af347a812c03add9c36551a02c05e5beced08318607f5b1c4a591a2fb`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1c2618377d8ad25fb22e9ca63d26389631b6e2a8ca4b1673b93a2cba1a05c`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9837b875bdb12ffc59e0fbe2171f864cc7bd57f33f0a77874eb7f125f8b29fc`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1c38a9fc78bafda1590eebddb512f8ef796066f8257f5040a7da3f15c586ba91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1b1b96511eadc0acbb1281e0e40a27a6f85edb57e880f645467d53c2e7093e`

```dockerfile
```

-	Layers:
	-	`sha256:43d531fb533c2d291cf1a6620b0aee99df32f97529bcc04f8b13210db42f540a`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 2.6 MB (2594581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b23f52db7b28fa8c0f4fcb0827d414082f73a1fc8b25566329b96e3abe070d2`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
