<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.7`](#elasticsearch8197)
-	[`elasticsearch:9.1.7`](#elasticsearch917)
-	[`elasticsearch:9.2.1`](#elasticsearch921)

## `elasticsearch:8.18.8`

```console
$ docker pull elasticsearch@sha256:98dbdba49c516867885cb84558b76f99f3c7463230b63cd9e1ac20d6f4b2daa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9dee3e296691806e6149f0b589a5367e2b12a3df1bb18395c278f0e5daf2d5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700095793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b31487c6b3bcda2e3e9deac4d72541a87a7635ee3e57ef7d591394d93f06e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767bd80aa3e96203f0fe79f488dd8396afad619772ad6b46f2f59b0aeb4350ef`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 5.2 MB (5169275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d463ed9d998440f2298dd041dc6706696a68b5f937c0667f2921f9b4906de`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745141e1b7bddf3289f47905d3e9a3f5b12a17fb66d65b19231248de43b0569`  
		Last Modified: Fri, 10 Oct 2025 00:58:53 GMT  
		Size: 664.9 MB (664908705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e1dcaa020bc80cf995518d3214281296dddb6929ca630b8206d8914a3673a8`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6659622c6ac5a6460d61c66362194945f73c57beeb0d863bd57cb5587ea8c690`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cc353993c24183bc2b158391bb553e2378953cc21fa6fac53fd839d9c15648`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 163.9 KB (163927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6576d73f85dd503c1bbd02bcb5f4a6acd790d30e09225478a512d94be59b7636`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84906a5d7244c4d424537bacc7565af37af9134b64fa31b6f66b706bdef0474`  
		Last Modified: Thu, 09 Oct 2025 21:17:08 GMT  
		Size: 115.5 KB (115527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:583fb33b37f59aa1b7b7a523bd5de66ea81c83ed073164346a887c8c2871f707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4d7cc6550158ddc5755d7835c522726b0e042129f197cb1ebfc1ba32fc596e`

```dockerfile
```

-	Layers:
	-	`sha256:a5b7e4e2c571c6e004ee3da3f479c33e7e3f78d3f612f3fc6483c3397c83a75f`  
		Last Modified: Fri, 10 Oct 2025 00:25:46 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88015e54603339551d580163f662e7a661b3e35c73e50083e1dc1dd5f7c658d9`  
		Last Modified: Fri, 10 Oct 2025 00:25:53 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:35bdb3b7836e25bd668c422e87f3b5c6e61a4e5bc5bfa3e35cea48b1336a9564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542329268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663e44d51c2133b258684ab42178ee8d6f884ace46b523662b5189892c9a8e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef09c9af7481b35edf6c79b749e5f32d66919be2df62c77b9d90ddfda2b67de`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 5.2 MB (5173604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec3fe3c02a318a387136627999b3a1327565c99e6d20438b89208b98725ff8`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6881f7c0dc53a9f3b85477480345b9dce6127f66c59720a4d206c3e4b1959360`  
		Last Modified: Fri, 10 Oct 2025 01:16:47 GMT  
		Size: 508.0 MB (508003268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9098ffdd1b75a43ae8bbdcfbc3bd3003384d5322e0464f126290caf7d972f1`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2b1c461b627fd7a78b1c49d049d02155d709a82c15270ffb0e42eae8ceb2d`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c48aab091ac2fdd7f5f4f63a99ba3781b599d1e7761454a4afa3b8a049973`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 160.4 KB (160367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d43e898705ce7b24c4412c1c6dd23d1cff776abb7598064a573f43d117debf`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7151da738860448b3c3e863cda2e9fec24c419402b4f7d7ddb3ba5c06649b9c9`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2e1d46a717081e636329861de64e76e863aec337d28d634e2663d2a4434840b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70295bea9f3cbfe16c5de9ea3bdcca065c06314fd6d4ef438534f798e74a9b53`

```dockerfile
```

-	Layers:
	-	`sha256:f3ccee60d218ed20c68b9d8411293a6af10e03a3ef4322442a5d3501118ceec7`  
		Last Modified: Fri, 10 Oct 2025 00:25:58 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce7ed71d275f6b2092e7ed56697075dd3a23708d8877fca11917a5a4b1c912f`  
		Last Modified: Fri, 10 Oct 2025 00:26:00 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.7`

**does not exist** (yet?)

## `elasticsearch:9.1.7`

**does not exist** (yet?)

## `elasticsearch:9.2.1`

**does not exist** (yet?)
