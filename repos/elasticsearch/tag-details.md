<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.18`](#elasticsearch71718)
-	[`elasticsearch:8.12.2`](#elasticsearch8122)

## `elasticsearch:7.17.18`

```console
$ docker pull elasticsearch@sha256:5f99f2f450ca38aff315a4a8849e892934cafef0aee5e6ab5d894ede97a02ca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.18` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e37071c95df9e8eb819f3323f5d8de14318bac80e336eefed3d809adab6415e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364223882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a5dba942dc1a604d739296cbd097588b2929b91d7c82fdfe7c23b32049dfc6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-02T12:04:59.691750271Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-02T12:04:59.691750271Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e858496733df66d582d671188fe5a32d879999f6e22233948545221d75fd276`  
		Last Modified: Wed, 06 Mar 2024 02:56:37 GMT  
		Size: 7.5 MB (7512548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00006f089e5fdcfe66383f326aaf6910d6604e6d0166efb7a18df3ecd03c3a9b`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63412664497553acbf671d08daaeb6772dc4f52a539b327af4a13416ea7d08b1`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 328.9 MB (328879366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b9b433533ab72a0c9049301240ecc10fc85372882acd1dc45d658365ec696`  
		Last Modified: Wed, 06 Mar 2024 02:56:37 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026f863f13889207aa211d9f8fb54e6562bce834f7452b18fa661111b91ffa9`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0f08439f172b9454148b18aa1fd270075efb96ac110f5182c00d81ad2e129`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 192.2 KB (192157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7479eb498d328f959acd737d225ac2fc733e4bf9294c031e68e9d9862b5e2840`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67736223517e61d07263ce421bfe8865ced0fa6d876fe41ca6901c7be7463492`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.18` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1111403bc9c5554a6b94c3204929d2dffd3508b44eb96ff8caa5aabb06a86592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78bc42765277beae8000799495753551572276d17c5c725e3630cc18a1fcbd9`

```dockerfile
```

-	Layers:
	-	`sha256:9d28a4fc8ec5443ff78b3b40b38bc5f55c896b515179cfd8f0c38c820b07a375`  
		Last Modified: Wed, 06 Mar 2024 02:56:37 GMT  
		Size: 2.3 MB (2311488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77566e681da50b2cf7acd106b599ca1ee0f0581de7e5701fb74074f76ba3fbf9`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 37.7 KB (37742 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.18` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4a65043257e7b4e8ccf21e7534b862b3528265f77f7b5ac8e806ca0a4e7507d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c6a751982c1fbf70c439c1a88695724421234c681b5e4f2f56be2be96b17a9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-02T12:04:59.691750271Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-02T12:04:59.691750271Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8682172c2130b9a411b1bd5ff37c9792367de6b0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2331b6764f674008b2d3b9ebb6f5c1e87cc4f8910237de251518e26b6208e471`  
		Last Modified: Wed, 06 Mar 2024 16:20:12 GMT  
		Size: 7.3 MB (7331893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99651ec458c539ecb6d8d1abf8311038c832e25d5efb298c5c561926d4e9f89`  
		Last Modified: Wed, 06 Mar 2024 16:20:12 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3909dd38706e0198750bd01be37c0ac0c3d51e32cab55aae6fe63acc3af7711b`  
		Last Modified: Wed, 06 Mar 2024 16:20:19 GMT  
		Size: 326.8 MB (326775102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072a5c10290a4ed62f7338ca51bbdc6d55755c471886b63c591b19d5147dcc1`  
		Last Modified: Wed, 06 Mar 2024 16:20:12 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559a3a28448dc6f2743f4b3fe622bfd72aa4c3dbf1b236c71b3858a20d2c4aa`  
		Last Modified: Wed, 06 Mar 2024 16:20:13 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7eadabdd39009def2b09ced5d8492c500d8929110905cd85892720a66c1566`  
		Last Modified: Wed, 06 Mar 2024 16:20:13 GMT  
		Size: 186.2 KB (186179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a187b2ff5afc9ee6dea8c1ca7fe790035c7f827116040fd4ec0924602b4dfb5`  
		Last Modified: Wed, 06 Mar 2024 16:20:14 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8ab4812771e4aa42d81dfa8068912f38de4cba434d34e5b67b199d5a8402b9`  
		Last Modified: Wed, 06 Mar 2024 16:20:14 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.18` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5f91aff01dccdb38d256d1a488ee26ff56cea9d60a9001314b8f4d45bdb951e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cbe41c254b75765fc6ca447eb7debcd9f69c3934d4490a8589cdd8bc97eec3`

```dockerfile
```

-	Layers:
	-	`sha256:5195169ba0bd3b3c350578ae485cfb56df1ed3b76936b6bb92102014a735dee6`  
		Last Modified: Wed, 06 Mar 2024 16:20:12 GMT  
		Size: 2.3 MB (2311705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3dbcc4ad0547df09bbccebc5193b0d5db3d32d53c858095416ca1a6a48bfc63`  
		Last Modified: Wed, 06 Mar 2024 16:20:12 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.12.2`

```console
$ docker pull elasticsearch@sha256:1d183abc10a89d49a9a7c8c9aeebc32bbd9de91782b4b3d39a1318469f5ad8c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.12.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9b8dba1fe3ac181b2236465bed92d850c0dcdd7b019d58639fdf786e344ff3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.7 MB (663711676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d852841f3391ec7ad2a94048e65f7557aa60ab0fa6028b2e690949ad57a0e0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T10:04:32.774273190Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=48a287ab9497e852de30327444b0809e55d46466 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T10:04:32.774273190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=48a287ab9497e852de30327444b0809e55d46466 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["eswrapper"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe7ce0121c264b95ff81228389e3ca6c68ac23bce1083264ff1ef8ccba39099`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 7.5 MB (7512506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00006f089e5fdcfe66383f326aaf6910d6604e6d0166efb7a18df3ecd03c3a9b`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecb135b48beb3bc2bb27aeb5ed32f18c546e8133ac41650f81a2a7e31e6b1ee`  
		Last Modified: Wed, 06 Mar 2024 02:57:49 GMT  
		Size: 628.4 MB (628367706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d43a577817f336eb62abc6f09e634359a43126d1e449dede0d630771a2f75b`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75e114d603c789f879192389e29ffaab858e9893c6aed04ca6b06dd9866a68`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24ddd566f6a79ef93576d7b6a32f580081618052d7fe34f83928d947aa5a45`  
		Last Modified: Wed, 06 Mar 2024 02:57:40 GMT  
		Size: 191.9 KB (191902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb03bb9d4cc3907be5fdb615d6211aa7c5e1ce31f3e15ecfe564c75d5221d97`  
		Last Modified: Wed, 06 Mar 2024 02:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eeb4636ee3a3965522138e8e3d072f603f24dc24c5ed39accc4a5ca86df697`  
		Last Modified: Wed, 06 Mar 2024 02:57:40 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4fe5673f4229f748e3cbbd037bcbd5b252983f0760923facf10575b48da860f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73ad9fbe8c124b67bde3177bfd3526e1d3317d942fdb7c996505402ace6b38e`

```dockerfile
```

-	Layers:
	-	`sha256:6f7b956bdca19872678f3a5970010f878446e372a1e53f710338043adceffef0`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 2.6 MB (2588956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1e3cf3aa816755ab1cfeded067e13969bfd67224b8d0448f12ea81a782fe48`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 37.8 KB (37757 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.12.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:359d968038cb6143dbc10bf6b32e9f335b8d5e6c267fb56a399c3cf1fe0d914b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456652661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f845cb1f867a88082c7e47042e58d53b6c650d1f1fa820c627a03426e1b017e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T10:04:32.774273190Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=48a287ab9497e852de30327444b0809e55d46466 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T10:04:32.774273190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=48a287ab9497e852de30327444b0809e55d46466 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["eswrapper"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfb160300b93edbc418b9a98ce2539e39fa1a6f79a1199b2dec349e0b0f2b0`  
		Last Modified: Wed, 06 Mar 2024 16:18:53 GMT  
		Size: 7.3 MB (7331938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d9bcfba92f4923b01ca1f2d68160ce947cf2f76a87bab41e3b0ec77fdc8136`  
		Last Modified: Wed, 06 Mar 2024 16:18:52 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf7d150df091cf3175403a2d618eb94ca4e30d5fb25d560e522eb0db750da47`  
		Last Modified: Wed, 06 Mar 2024 16:19:01 GMT  
		Size: 423.0 MB (423035570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4f5648ee9068ea1529fdfda49cc8f511d5ee441abdcec5587dc3e58c604e5f`  
		Last Modified: Wed, 06 Mar 2024 16:18:53 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9498bdba4c08d550c8a138e0da4832a39b47c71e544a07966bec400d52637e6`  
		Last Modified: Wed, 06 Mar 2024 16:18:54 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426e3f2ba778fffdad76acba7a8c6eb0a1206c997e3aa4fb272b5721d7d06df`  
		Last Modified: Wed, 06 Mar 2024 16:18:54 GMT  
		Size: 185.9 KB (185928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d204d45dd07a491cab42dcc9c3bb9ad81680fc7e2a7e9da825767cf00ba48`  
		Last Modified: Wed, 06 Mar 2024 16:18:54 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6083314804ed399604e2759f07562a69aadc1feb48bf150374c156ccb1492a3b`  
		Last Modified: Wed, 06 Mar 2024 16:18:55 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:657e3a28abc49223ca93d6522563e23e906b4d865b64c6c8ab4c222ad9d4f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d1a381230246b9c7dbbc04f2626547a7a7c0a162c7acf5477384799a162368`

```dockerfile
```

-	Layers:
	-	`sha256:eacd0ed733c6e44e314a2eeaf9e661eba9f561f856353765bf44648368d8cb89`  
		Last Modified: Wed, 06 Mar 2024 16:18:52 GMT  
		Size: 2.6 MB (2589189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e26df06cb8a4600f352ef101bfdd234e0fdc70d4cf18874bfe6f2be40fd325b`  
		Last Modified: Wed, 06 Mar 2024 16:18:52 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
