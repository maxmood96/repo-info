<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.6`](#elasticsearch8196)
-	[`elasticsearch:9.1.6`](#elasticsearch916)
-	[`elasticsearch:9.2.0`](#elasticsearch920)

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

## `elasticsearch:8.19.6`

```console
$ docker pull elasticsearch@sha256:e2d7e20893ad820bcad241bf47b89958787f6b38225478dfe100b66937840b0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7f4dbd1842d590569f42e6a91ac766d640b58dd3ec4fc90598e95ee93f4deb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.5 MB (707470513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff16432d42a8f8c5c6ce1d86c4a7f41873e9c0e3f1a06f73a21399d83b1e76fd`
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
# Thu, 23 Oct 2025 13:48:53 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:48:53 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:48:53 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 13:48:53 GMT
LABEL org.label-schema.build-date=2025-10-21T22:05:27.062491219Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d2c42d91a1eb9e14b1a37c4d87eb2533ec859e2b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.6 org.opencontainers.image.created=2025-10-21T22:05:27.062491219Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d2c42d91a1eb9e14b1a37c4d87eb2533ec859e2b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.6
# Thu, 23 Oct 2025 13:48:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 13:48:53 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 13:48:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb584a9283936471c7c8a11a0088aa7fb593f1b9015ed84601066409748296c5`  
		Last Modified: Thu, 23 Oct 2025 23:30:42 GMT  
		Size: 5.2 MB (5169355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e5ea1ee14fa597ed0ea793c1b46ae9ca5b84b38919dd05e90b9faaa521fa7`  
		Last Modified: Thu, 23 Oct 2025 23:30:39 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d4a446fcac82f91c398da3f251053f0b6287e188f469a1e79c3f8f86be417`  
		Last Modified: Fri, 24 Oct 2025 00:36:21 GMT  
		Size: 672.3 MB (672283342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384c6dbf2b19673e22c31d26a9436d8f14766482d9adc9a563809d430abf0311`  
		Last Modified: Thu, 23 Oct 2025 23:30:38 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecd57ecca156b4a78127fec7a43aad49fa5450048351f71b138ec8eb6705633`  
		Last Modified: Thu, 23 Oct 2025 23:30:38 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fefae5084bf74b67dddb0b8f76974ae283051a20a75562ce033f029dfcf8d6`  
		Last Modified: Thu, 23 Oct 2025 23:30:39 GMT  
		Size: 163.9 KB (163930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5a67c185d8d394a839926ccc1d228274203755089562e4593db970bf4e80e`  
		Last Modified: Thu, 23 Oct 2025 23:30:38 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ce44366139b99f1cb97031f635eb16d4cd1cf810199fe157dc06dd753d2c6`  
		Last Modified: Thu, 23 Oct 2025 23:30:38 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f0b24c735c179b2c3daa4803b11e202591140c4c0dc3a9de3369cb7a123727fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0d86fbbaff88ac5e232d4b7bf99dab3494fb2982de3cb8dc6381f78ede3a08`

```dockerfile
```

-	Layers:
	-	`sha256:de75f89d93a8228059ab7e5f90f24dec2433092664195a56649d2c24bbed3440`  
		Last Modified: Fri, 24 Oct 2025 00:25:17 GMT  
		Size: 3.2 MB (3215984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be20ac8f11aca8de07564c958001194b04d3790cefd0e2d8cb69071d4f8e66af`  
		Last Modified: Fri, 24 Oct 2025 00:25:18 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e8d7dc7f90c9c2db41c9a4ab0ccfecf3a9511f42d60e1828ce1024feaf3a62bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.7 MB (549667437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affeb09dd9592de250f3d217e61276a453b9ed2b28ae4b672a3e06a100aee13a`
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
# Thu, 23 Oct 2025 13:48:53 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:48:53 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:48:53 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 13:48:53 GMT
LABEL org.label-schema.build-date=2025-10-21T22:05:27.062491219Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d2c42d91a1eb9e14b1a37c4d87eb2533ec859e2b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.6 org.opencontainers.image.created=2025-10-21T22:05:27.062491219Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d2c42d91a1eb9e14b1a37c4d87eb2533ec859e2b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.6
# Thu, 23 Oct 2025 13:48:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 13:48:53 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 13:48:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c25ed2d98bffa07e634dcc7e8b36c251b9cca041d6196456d644ee745ac320b`  
		Last Modified: Thu, 23 Oct 2025 21:03:31 GMT  
		Size: 5.2 MB (5173573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296a9ec55b09920833444adfd0d57b9325c2687fce679c671b24a88aa8a6ef67`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df726f6479fa226c676ff073fd7e30436c93273310b33dc5b52055d25a095d3f`  
		Last Modified: Thu, 23 Oct 2025 21:59:03 GMT  
		Size: 515.3 MB (515341477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fbf9d106a6ad956a8d4e365bad5395e0a519ca115e68bf879ad515d93ea28a`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd551e2035f2ddff432738b143073addc77a8a165b80f2b47775fac764aa548`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a0f9f7a0a8959e6f07e9de49952e96a1ce04b5d7b3eb2b0ba56c2373652d0`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 160.4 KB (160356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5726718bafe7cc6bb74f3cdf20725dc547f627b8e1708e3bc97590e0c76e1cfa`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0e2a5ce680b21cf7c4f0d0d0e74a2a7771063cad405aece39e0b2cfbecf949`  
		Last Modified: Thu, 23 Oct 2025 21:03:30 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f7c5189388f2509b0519f493c9343ee637289a5543f858076331df33b46bc2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a818f84b18e0483de1d2410b71fdc8574b30b3998c5e7147e1ac036793755202`

```dockerfile
```

-	Layers:
	-	`sha256:23c0702c94cb55a817d6cb479305315844264b5207f3718b3eacfb4f1e379bec`  
		Last Modified: Thu, 23 Oct 2025 21:25:18 GMT  
		Size: 3.2 MB (3216397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdf40d3fd9bd1c375f25c4b1abcdf42d9c247b85e270efeb9b6553378ab2657`  
		Last Modified: Thu, 23 Oct 2025 21:25:19 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.6`

```console
$ docker pull elasticsearch@sha256:12f683c6bc903b972a33338d45469e9630a4ae82d89a43220755daa8c67654cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:930f08faeccd0b6f964129e46c851035911d3f02b061b851aec6e064cf9dddd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.0 MB (726960266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2dfc5fc6a0b7e533cd27b1a435487dc7d371735de57d3ef63b8048e1723b62`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 13:49:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:49:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:49:09 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL org.label-schema.build-date=2025-10-21T22:05:52.998642761Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=382e36e0fbb3c0c80703cd48691ea265d7f931d9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-21T22:05:52.998642761Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=382e36e0fbb3c0c80703cd48691ea265d7f931d9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 23 Oct 2025 13:49:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 13:49:09 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 13:49:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835dfe6a44ba46479bde09505bd265d7899fe2592895cbd76a046c0069c7777`  
		Last Modified: Thu, 23 Oct 2025 23:31:31 GMT  
		Size: 4.3 MB (4282595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed156bebf588b2c287885288cdba2287db6ccdadea9632d1d4f632f8c054b0d`  
		Last Modified: Thu, 23 Oct 2025 23:31:30 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c15f5cc1af241b956e47ee204d33464e298f9c183aa5bdea40cd0515e87c10`  
		Last Modified: Thu, 23 Oct 2025 23:31:30 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f67a7078bf6368d37248a963e09301f7d6bc8ec7364259e450eeb109e8d2e`  
		Last Modified: Fri, 24 Oct 2025 00:58:24 GMT  
		Size: 682.9 MB (682933617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fedd2bc21f9db8b64132c1f7ffb1254f157f4f9590d4d5fe4450781edf11346`  
		Last Modified: Thu, 23 Oct 2025 23:31:31 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed6d9790931d5e2916019bb015d24bfa54ac2ec5edf7c211a0e57ea29cb92f`  
		Last Modified: Thu, 23 Oct 2025 23:31:30 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591737661645a93ac1d14bfd7c25e7a92134030b70702e17b3cd8ed88ca6922`  
		Last Modified: Thu, 23 Oct 2025 23:31:30 GMT  
		Size: 75.8 KB (75752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abfebc8b952866022e1dbe4fb3bfc83c024f9e18bffcb97fc1fb78f338c775`  
		Last Modified: Thu, 23 Oct 2025 23:31:30 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e885c36e359a365475f0ff73dba5458b2c3262d46530e1cf9ec7e3912c118445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29148b91883b6f78e8c728b480fbd8416937275a39a438692040ccd837827451`

```dockerfile
```

-	Layers:
	-	`sha256:e71797bb4d7830ba07a6548e87df9f401eabd3958b6c0cac1cd87b87324da89b`  
		Last Modified: Fri, 24 Oct 2025 00:25:23 GMT  
		Size: 2.1 MB (2085205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7467119ac8ddb4f72793d9e04bd6c9b6c0941b8e7039b117b84b2c5617723923`  
		Last Modified: Fri, 24 Oct 2025 00:25:24 GMT  
		Size: 33.9 KB (33899 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:feced11a8dc8ebe4868d090e394c01d423e6193187366293086a3df2b55c7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.3 MB (565296439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1972df4307d85ecf3e1b3094f6a0567c7c9b49b88b4345eada24a7696527c6c0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 13:49:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:49:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:49:09 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL org.label-schema.build-date=2025-10-21T22:05:52.998642761Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=382e36e0fbb3c0c80703cd48691ea265d7f931d9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-21T22:05:52.998642761Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=382e36e0fbb3c0c80703cd48691ea265d7f931d9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 23 Oct 2025 13:49:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 13:49:09 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 13:49:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170480443bd49bd8dde10304215c98cde713607b7ffd8371f4b4603720d7336e`  
		Last Modified: Thu, 23 Oct 2025 21:03:48 GMT  
		Size: 4.3 MB (4290442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228f90bec4696dd05e3b703734605eab6ae6d574b0145b53cbd8cc3eb55c256e`  
		Last Modified: Thu, 23 Oct 2025 21:03:48 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec1bd1ef495275e704fde553aa1d2c803d1e5714ba1612f0e53b55d52884604`  
		Last Modified: Thu, 23 Oct 2025 21:03:47 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750cc88093cb9e1a1816cd673fccca44571b3343dcfe55ad9e24f43840e65bb6`  
		Last Modified: Thu, 23 Oct 2025 21:06:33 GMT  
		Size: 523.0 MB (523020732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f559137d54a8baf6b629ec39d2bfbd40713b3b8f76da14b36d75654e57562f91`  
		Last Modified: Thu, 23 Oct 2025 21:03:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e9ea06244f3a8075056ff08a83e3e823220d84ee204a79884deabeb08d6b81`  
		Last Modified: Thu, 23 Oct 2025 21:03:47 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9c574bf7da0fbfbc64368df200442fdb94749b8fa232f438eb91e8667b2d10`  
		Last Modified: Thu, 23 Oct 2025 21:03:47 GMT  
		Size: 74.6 KB (74638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b36a795a459692233142204f18e3027c1aa1a2e460c603b7a8fb38a56c77d`  
		Last Modified: Thu, 23 Oct 2025 21:03:47 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4e05225206423add51a5a34d15c2c80aa49f30967d6890c739c602b427993079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609f999228a25d96177f196ebc8cdb19070e2ad9edd3b5493161087ac3e54be`

```dockerfile
```

-	Layers:
	-	`sha256:f8e1854e8df77a134af1646b315e37798e81a11acc72733f9c28b8232d226d60`  
		Last Modified: Thu, 23 Oct 2025 21:25:25 GMT  
		Size: 2.1 MB (2085769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67f0c9478629944af1790dd9cc51555fd783662d966120f09db7ab3130f8212`  
		Last Modified: Thu, 23 Oct 2025 21:25:26 GMT  
		Size: 34.1 KB (34081 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.0`

```console
$ docker pull elasticsearch@sha256:c0e8efbd41e3bdc912293889bae4402f3166f8d5a642f7f4d711b58dd8c2877e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d3f15f7b9991933cdcdef49c9effdd9d942681cab4cd1d50a2a019e5ef2a83c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **736.7 MB (736693069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2bfe82d0f597e6f83003fe7ef69d6aed6bcc5195f4ff1e0d22d48385635101`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 08:40:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 08:40:15 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 08:40:15 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL org.label-schema.build-date=2025-10-21T10:06:21.288851013Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=25d88452371273dd27356c98598287b669a03eae org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-21T10:06:21.288851013Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=25d88452371273dd27356c98598287b669a03eae org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 23 Oct 2025 08:40:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 08:40:15 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 08:40:15 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16bb89d7b873426380e54207b7738d86826a92604191af40f96705de9c2d57f`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 4.3 MB (4282621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0cc181331121905fccb94511811c91e11abe113fb4e15130d477b9aab4959e`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f77302d25d2c515a2f58ee9986d2dc6eb5a2f513b4828ef3606939d3181ea79`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bad3ae1195015ec53aa4fd2a018c9a13e2bec442bdabf749b1bcfd01b8a40`  
		Last Modified: Fri, 24 Oct 2025 00:10:36 GMT  
		Size: 692.7 MB (692666402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8410acc9cd4049c8db3a9f5f5a758adf211f5f8918e60eac544a0d18d293c211`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f654fdcbc77c0b8e65d19f43ad0cc276e46fedfb6d68551cb5a09fba29e069`  
		Last Modified: Thu, 23 Oct 2025 23:32:20 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2667e7d6d872372a1ad5a8b49fea750965c339d95e52e1a71bc05df358419489`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 75.7 KB (75747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b68d25bad8a2f7544380281e52323afba4eb457e1ad80d255546c371e5304`  
		Last Modified: Thu, 23 Oct 2025 23:32:19 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:907f7dfb51b6f4b405ed27b8519fb00ad171be7ca25414ffbacfea7570fee5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e482f9c155921db466c089ccf55b07df85213858d51247d1052311aa27109cbe`

```dockerfile
```

-	Layers:
	-	`sha256:6c06c1c2016295655265847c867b10ef7cfdf08500c93c950eaa908435171f23`  
		Last Modified: Fri, 24 Oct 2025 00:25:33 GMT  
		Size: 2.1 MB (2091452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea974c63e19f40419e73215fe6a2bf5e2ad51e4893e1b56121a2631f0557782`  
		Last Modified: Fri, 24 Oct 2025 00:25:34 GMT  
		Size: 33.9 KB (33899 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:66dd0cf7bdc0b88c3a614a5f0a248a30bfa6ab9c80ccad6931212e85282bd495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.7 MB (580742856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa848b28104f5cf3899c323327b16b173f21ccd73d937f505a89fc38c8df62d8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 08:40:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 08:40:15 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 08:40:15 GMT
ENV SHELL=/bin/bash
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL org.label-schema.build-date=2025-10-21T10:06:21.288851013Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=25d88452371273dd27356c98598287b669a03eae org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-21T10:06:21.288851013Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=25d88452371273dd27356c98598287b669a03eae org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 23 Oct 2025 08:40:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Oct 2025 08:40:15 GMT
CMD ["eswrapper"]
# Thu, 23 Oct 2025 08:40:15 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a998be0af0b836125abcf61e1e967511848ceabbf3cf8f782365a396f6eecd0d`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 4.3 MB (4290391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15297e21ea54d704e090df615507561b1d9f1d28d2b131d33eb7ec9f36ea08`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a980f875cead50922aadcb813f1b50633700a746921755936e291a37996e865`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424ef9d14b5ce44612be959c013491407220dd0ee5374c46807fe16fdb0910c`  
		Last Modified: Thu, 23 Oct 2025 23:11:25 GMT  
		Size: 538.5 MB (538467200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ed398ddf3993fc9b704dd5daf74f457de80d11463c8212c134996e8307601`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13f6685425f20f2089e23251725ebb8c767960944dc20e2a88af777b621e75d`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711be2f9f33b6172ead87ef779952f66710e3709bf205c9256ce7129c5af002f`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 74.6 KB (74636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02184a91e4353d299e78c756df6f7695288e69c22892e713b9207119e2a4599c`  
		Last Modified: Thu, 23 Oct 2025 22:08:34 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5ca5ce202cb2408fc72149949110bf2867d5cdfbbe448f1f3cecac2e44164f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e45e2992219b5f477ad467b395b32efeea3b81ea364ffaafe18a6434a70447c`

```dockerfile
```

-	Layers:
	-	`sha256:ab63c215921f653a2afe7c5001f8329cc0f5ccadcbfa7b8f67efd546b6c90bc1`  
		Last Modified: Fri, 24 Oct 2025 00:25:38 GMT  
		Size: 2.1 MB (2092016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc17721b5aeb6b069239f43ac207c2efb5f3027e29143a495552de1163dbe17`  
		Last Modified: Fri, 24 Oct 2025 00:25:40 GMT  
		Size: 34.1 KB (34081 bytes)  
		MIME: application/vnd.in-toto+json
