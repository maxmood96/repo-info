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

```console
$ docker pull elasticsearch@sha256:ec6cc5dc6aa9b1bde222296ac6944c7112f2aa729ed8e66b0b79ae2473f55269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:779e07d83dfab4d2f78eaa8696f2ca6c2e43b9c87b94ecc2debfbc70c790cc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.5 MB (707504490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6c7335b56ed2725fc6fe2e40c2d08f8363802e86b5ffa67ec2c06220f115c2`
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
# Tue, 11 Nov 2025 18:07:25 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Nov 2025 18:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:25 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:25 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Nov 2025 18:08:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:25 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Tue, 11 Nov 2025 18:08:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:25 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3039eedb2689c3c508d9cddc8f15f70678b8a785ec5e91db0c8b670bb8b1ffeb`  
		Last Modified: Tue, 11 Nov 2025 18:09:40 GMT  
		Size: 5.2 MB (5169394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83585fc5c0758e2aaf9d07eafd58a5a89c0e1e1fe189ba7498cf86dae33a8c77`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212d269630bc201b8a4920b6228f5a0ab57973fb092b3322bab40b7cc26272f6`  
		Last Modified: Tue, 11 Nov 2025 19:45:02 GMT  
		Size: 672.3 MB (672317277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4006eac18a3ba7476e02f355eecc83ddf66199995f96885d63b9923bece3e8`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e603f9f6823f4697f180fac50fe8e2d441e0f5ed621e5d9f0aa210c78a4fd88`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cd3502c57f8a51f086de40aa3ec7091e32c80975150223ecb6f5bf5c9896dd`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 163.9 KB (163931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292fad8d8068029ab5517cedb4e556cc4c1bd21bc84095d5017d523dc867c1a7`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3c79576c91739a5688cf4095623e898998d8a37b8a77ec0206702d92506d15`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b4f619f080aed5961ba22dae7c90e261cfcc59eb7e1d44d5ce936e00674678e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7731764aea525dcdcfa079c289640ce6ee5a06c6b7bb93aa983f2e5d7bb2f56`

```dockerfile
```

-	Layers:
	-	`sha256:123c9ff185b5deb5f197974bfd7ff0588a511b8f8fe426bde18663808c9d9b45`  
		Last Modified: Tue, 11 Nov 2025 19:25:21 GMT  
		Size: 3.2 MB (3215994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1298490454ec450b1993d5c71d8155d9eb8d92eccf040735367a4b409718713`  
		Last Modified: Tue, 11 Nov 2025 19:25:22 GMT  
		Size: 36.8 KB (36839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8bec9519d48b8877c5b1f74197baea0dc09be49cbd10b2547b6b7fcfcbc96b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.7 MB (549722068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c845c07ca6fa6569724f58780e077a3f03ce4c171a7a6b406d859df626b72c1a`
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
# Tue, 11 Nov 2025 18:07:43 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Nov 2025 18:07:44 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:07:44 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:07:44 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:07 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:07 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:08 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:08 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Tue, 11 Nov 2025 18:08:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:08 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f9d8ace7149a5fdae21fb12340bc8d6f7e42052ba0220a038a835332df2fc`  
		Last Modified: Tue, 11 Nov 2025 18:09:13 GMT  
		Size: 5.2 MB (5173734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803543969062c86dd8a1a3265bb174fb18327c278d5f28d3aa0e5b37b7a9212d`  
		Last Modified: Tue, 11 Nov 2025 18:09:13 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68344a01f9512d9f45dbf4294e7ab8910f18a261e6fbacba2c67e312717f404d`  
		Last Modified: Tue, 11 Nov 2025 19:46:18 GMT  
		Size: 515.4 MB (515395945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b57aa9303e29eeeee306af7d1ded5feae7a81bd0ad7541e39546d697c5592f4`  
		Last Modified: Tue, 11 Nov 2025 18:09:13 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a24583d003c1f633e20bcafa8b6b94a151ea0080cb7ddb96140036aacd70bcb`  
		Last Modified: Tue, 11 Nov 2025 18:09:14 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d5185c53121e042b98ec215168a414da3a933e259fa693332c85039f38bf43`  
		Last Modified: Tue, 11 Nov 2025 18:09:14 GMT  
		Size: 160.4 KB (160359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efda2fa363f9c3aa97b688ad297a275746c33f3b24de58c804e4501de964bc`  
		Last Modified: Tue, 11 Nov 2025 18:09:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00b033c8532a5e2e422a4e856f4aaac43f12263a824de7205b78890e2c8816e`  
		Last Modified: Tue, 11 Nov 2025 18:09:15 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dfb4f0c79b733a9877c207393a00982a56dfb0ed3f6da6a3ce688c0043fd952b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e88cd1821e3f4744b7542e79203947f8932d1d9ecc02c724eb1a649b1e5d559`

```dockerfile
```

-	Layers:
	-	`sha256:0bd29b2b8243ac5c419b6fbda435328d425e7a7adbacdb985fd9d86e28b460db`  
		Last Modified: Tue, 11 Nov 2025 19:25:26 GMT  
		Size: 3.2 MB (3216407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576fd06d891a589996de906493f70e2aef9f5b72ad9a263fa0e228035ebb8152`  
		Last Modified: Tue, 11 Nov 2025 19:25:27 GMT  
		Size: 37.0 KB (37043 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.7`

```console
$ docker pull elasticsearch@sha256:154c638e5bfe48413b347c81925b49f39df6b36ff6ab599edd91b39bbb32eb74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:cd510bac4bb55494e127132a449eacc392d6c4955c3c4bbd1964122e1ea2c782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.7 MB (727677539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d62e209ed2783bb8756d6cc2f270fdd26da30da88eb47a7d2d5648408403ff`
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
# Tue, 11 Nov 2025 18:07:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:07:30 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:08:14 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 11 Nov 2025 18:08:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 11 Nov 2025 18:08:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:24 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:24 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 11 Nov 2025 18:08:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 11 Nov 2025 18:08:24 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:08:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:24 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b0881ac0401b949101b7b579e0a6d2c2e49b8f8480e08e2121cda90c7d4dc`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 5.0 MB (4956343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceae901165e8218b4888b2789d50cef1dba1ab524e3b16c58ca4deb20c6d584a`  
		Last Modified: Tue, 11 Nov 2025 18:09:39 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d10ffde7a22eef8b1723fef5468ca030252f3f5e9371b2aa274a86a9ab98f`  
		Last Modified: Tue, 11 Nov 2025 18:09:38 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbff741d2b6505ec669de2cf10bf14bc3f308188bc293c950c61bc33ae2c9cf`  
		Last Modified: Tue, 11 Nov 2025 19:28:46 GMT  
		Size: 683.0 MB (682977708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8edff0e1dc21bf8273149d156e4ca791ca4f3dd460856038791c08e15a74b8`  
		Last Modified: Tue, 11 Nov 2025 18:09:38 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e58b51ac7ef93d7c035ab119581e124a7f971a3f01587b5fde55240ae23ed8c`  
		Last Modified: Tue, 11 Nov 2025 18:09:38 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e3bd818dd5d28160c5b563accd75fe0bd07e4532fb8c0121b479f585f9458`  
		Last Modified: Tue, 11 Nov 2025 18:09:38 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81180a019a4adad5de0d03cbe43957a92142a3925a88d7257876d518d488804`  
		Last Modified: Tue, 11 Nov 2025 18:09:38 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f98fa4817815e3b37fc3f23d2d07fb8c5c1237c3ed86b60a69bd6aa0d226b3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3aa26ca4b4872aaff7833e2bdbcf57784bef11bf8d126511d1163b8d9a0c52`

```dockerfile
```

-	Layers:
	-	`sha256:62a7e43fbc9f4b54e443f281bb1816f0bdf17b887561eca37dae97ab19894a2e`  
		Last Modified: Tue, 11 Nov 2025 19:25:30 GMT  
		Size: 2.1 MB (2085211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c220f7c940eb89e065f8862e168bdb3fc9e8972986172f9542c59785ab7b52a0`  
		Last Modified: Tue, 11 Nov 2025 19:25:31 GMT  
		Size: 33.9 KB (33855 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fd3c73cde6241f3b1c488c46f9cf3ac18fedf005ed0ea47a5906b00dcc5f4e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.0 MB (565999105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed77f2ea8c987ddcd3dc6ee8dff8132ce730dd7943189205814e8d251304c8`
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
# Tue, 11 Nov 2025 18:07:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:07:30 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:01 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:08:01 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:01 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 11 Nov 2025 18:08:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 11 Nov 2025 18:08:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:07 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:08 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 11 Nov 2025 18:08:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 11 Nov 2025 18:08:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:08:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:08 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd85bc8452cb7031c65912c24521498b572de3126b3428d7811bdee7205501`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 5.0 MB (4967665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5ffb9d4c35f4048fcba34c52c0fdccdc18d1b9475d47584f4102bd8170057`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5d9bf92cd53f878e3092a89ea93184a89b78e35f8b9af121929607f0e982d2`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b2322df01dab9552babca88d962b3f2b2f715e11828e6c23ec55fc601db665`  
		Last Modified: Tue, 11 Nov 2025 19:29:51 GMT  
		Size: 523.0 MB (523046694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade5075fd57f5ae88648ada338a0a99d65095c67a278f604cf891848f0884a02`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976445898ced9514ad26a315a638ee6f626e715d55b1d95b893628e662ff73e7`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60846fdf8580e04af577ab0fdebddb7d55fe2c537bae674a3bc6b6b78c7f1116`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd3449a135967caa499f25707a35a1bfda5e28d9dd93f11d88e12de71e2b188`  
		Last Modified: Tue, 11 Nov 2025 18:09:09 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1483865ebeb3c8d64094dc3fc4db134dffe261e5513379100c54a7d0576b841d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99e5032f63d4aff242d33bc3974a1268e6554659b949ad75c58d34f0a1b9ebd`

```dockerfile
```

-	Layers:
	-	`sha256:6dc9f0eadf1c4ebb1679ad3b9267af70250c6f4510e09604e3620c0616f21488`  
		Last Modified: Tue, 11 Nov 2025 19:25:35 GMT  
		Size: 2.1 MB (2085775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc40b28f535a9eda6e57cdf7b5dff4a354912986119c0933f0dcd194bf14b72`  
		Last Modified: Tue, 11 Nov 2025 19:25:35 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.1`

```console
$ docker pull elasticsearch@sha256:7c6a529fd36eaa8565cbfb45d9c34dae92e397a7f5b4101d66c944f74f3c7724
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:44a56a0da411b1f089bfd6557e885d1c70aea60969dedcba4b8b06275f20e300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.4 MB (737444105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50289473bfb678d860f7e970480465950611b7235ada1a81ed9ff45438049f9e`
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
# Tue, 11 Nov 2025 18:07:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:07:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:37 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:08:37 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:37 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 11 Nov 2025 18:08:47 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 11 Nov 2025 18:08:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:47 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:47 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:47 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:47 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 11 Nov 2025 18:08:47 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 11 Nov 2025 18:08:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:08:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:47 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5714744da21d157573434970bf2499533bdfb5a4a2d821523afbfa8efa2831ee`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 5.0 MB (4956312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f11730ee6bdaebf9b758df37ca62c4affb821f1067e8eec9a8b76d1fe81a4c`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6a0c589c94361f6f6447ee1cc49f944aa7de194cef531c84a98e36c0cbb87a`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46955eb855c9d217dc43ea353f8fe13c6a47fc692130a5966929c69f2a628c1`  
		Last Modified: Tue, 11 Nov 2025 19:27:41 GMT  
		Size: 692.7 MB (692744310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad8deeec7a10557539783cfb6054d723e99773ec83957e3de2674046a303b8a`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39524b86115c32cd0d09ba546ef0ba783b7c4ab893db412120623491007380`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e995c5d349f895de279b55ccb11878b6c84c4633fc22d55c52c1e230af576`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79084fa0bda03aea4512f28d2c86160186c190b64126b4294c890a1240749881`  
		Last Modified: Tue, 11 Nov 2025 18:09:59 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:652515a97b25916fdfb7a33c92d984b438a63c684875101bea8db17a48d4fd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059539d655a8773665cdc8f9b431047948dff923df1089264143dea408f36399`

```dockerfile
```

-	Layers:
	-	`sha256:c7fd30cd362bbfbaf74910124992becc9d85b036f4be09955d442a56df501b89`  
		Last Modified: Tue, 11 Nov 2025 19:25:39 GMT  
		Size: 2.1 MB (2091458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ecf763e91d89a5fce01474dc640c1193982ca07245fd0404cc84a52b3840a`  
		Last Modified: Tue, 11 Nov 2025 19:25:40 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6d2caaf59ff7ab3a0c9a6dfa77061d45ac39e0433d5416d712c46c6cb0baa432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581489695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46946f6dec24861f9c70450ee18d3a1be5bb66afff10cdf752c1a03ac77442b`
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
# Tue, 11 Nov 2025 18:07:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:07:42 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Nov 2025 18:08:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:08:17 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:08:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Nov 2025 18:08:23 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 11 Nov 2025 18:08:23 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 11 Nov 2025 18:08:23 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:08:23 GMT
ENV SHELL=/bin/bash
# Tue, 11 Nov 2025 18:08:23 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Nov 2025 18:08:23 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Nov 2025 18:08:23 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Nov 2025 18:08:23 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 11 Nov 2025 18:08:23 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 11 Nov 2025 18:08:23 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:08:23 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Nov 2025 18:08:23 GMT
CMD ["eswrapper"]
# Tue, 11 Nov 2025 18:08:23 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbc026f4dd59ea8584510e6e0adbefc5f1ce2f95ba8a4db17b290bbb512ad0a`  
		Last Modified: Tue, 11 Nov 2025 18:09:24 GMT  
		Size: 5.0 MB (4967667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258096cb5e5e268260230fdfa24f8be1de87f91ad3df63bb0804ae3f19c2dcf9`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5b719130257422b0dbe9ad7b3a49aea54d2e00c4bf25c2c8987516240a23a4`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c18afa183a211658f51c6edb24d0d601c91343a6bf869873506ebb7025618c9`  
		Last Modified: Tue, 11 Nov 2025 19:36:06 GMT  
		Size: 538.5 MB (538537279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ce12504178e42cd59e8cc9efdae9dacd77cfb65ea7e7d403f7dbda07f9f034`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc31f48e26cd848b540e2df6dd4b6e5acd97d2ab1a60d5c50121532003ac4eff`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86712e202ba836144e2983c6de8b21760b988d6e07ae14f2133343a103d055bc`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e79e0cb6f2b478f4bfc914752db610b16e9d32ff9fbc2980496ac71a2a1cdd8`  
		Last Modified: Tue, 11 Nov 2025 18:09:23 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e16b6c85ff30adf59e4978692827e253d1de3c428368b08480a726d592250e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a89389c57f23c121b37cea4d27037df831c5a27c70920379ab14501dacff589`

```dockerfile
```

-	Layers:
	-	`sha256:8bb6f7a53e48aafb3279ff336f3d2c0d8fb8c257e9c0a3151b6ba9255935fe35`  
		Last Modified: Tue, 11 Nov 2025 19:25:44 GMT  
		Size: 2.1 MB (2092022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548068bf2ec11883292bbcbbe3a78a52bb06ea1af2fead1cf933c6b45f1eb215`  
		Last Modified: Tue, 11 Nov 2025 19:25:45 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
