<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.18`](#elasticsearch71718)
-	[`elasticsearch:8.12.2`](#elasticsearch8122)

## `elasticsearch:7.17.18`

```console
$ docker pull elasticsearch@sha256:9dcd788e6f87ca44c5ffb36212c6cb3e45d32d4c1e4da181a19a436a3eaef2f4
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
$ docker pull elasticsearch@sha256:d880835979209e68c960c9688fd6ccdff42f7428d93c839e2b96220f4a50fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360390555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80789633bdf148ad39948455ca2e094354a748455a5dddc528bc224c9def3fa6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
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
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d4c2b87a53ae05073db1e549a497aaadab7083e7376fb16c0884a05e4f9d8`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 7.3 MB (7328596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159b8ae36baed42e8be2dfb6aff2e12ffadada674ae811498b9c4ff306f98a7`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d173a2008214885944ff13ba2f2adc23bb2ebfd2fc32f7a79f19557b5cf019`  
		Last Modified: Tue, 06 Feb 2024 21:38:54 GMT  
		Size: 326.8 MB (326775081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8330c0bdb51da9614a667fad0e026357a0c66047aefa629e120e1ec2a492e1e7`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8d7c2b10f2fd94e3a7b6807dd7b57005bf8e2d025d4c5880c8b0b14acece6`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5cee5442c51836394b1cda27917ea401865c13bc1c6c465ccef1a8bbdb7935`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 186.2 KB (186171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec18c76f929475458e4b6e248d56cd1ebd2081be349bc5901a363f010722997`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9c7615c9b1c8a4af79fb6e4781c52ca3e1443a78d0ebe22e8e53eb15a3cd89`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 109.3 KB (109260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.18` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c9b90d3501c8a56cdcba3cbfe255599f687493cf02d75d93413c693fc91012fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2111532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e36eab3af58734eed9532fe187385436171518137023dcde9860c69b83f42a6`

```dockerfile
```

-	Layers:
	-	`sha256:f89c3d2f2bbae19979c9a56f353a24e7db4e2200f7af11d99efdd2b97640082c`  
		Last Modified: Tue, 06 Feb 2024 21:38:48 GMT  
		Size: 2.1 MB (2073947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2f63f0e40f6a68d3da4cbeea8c2ca2826ee45bb49c25b67bc97655ae29a329`  
		Last Modified: Tue, 06 Feb 2024 21:38:47 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.12.2`

```console
$ docker pull elasticsearch@sha256:4cbcb658970fc3245f886fd73533567e40d48d89eae9baf893a36fe177c3920e
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
$ docker pull elasticsearch@sha256:0f7f04a6cb47287bfc1326a3e2411041a0f8de878e28a3b4a9b014e7c416c49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456650727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188e9f79ce971251d4813bb3433669173384e23df217b32f1a4859d0c4fa5d4`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
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
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7036eeda0b893893c3d530238575da4fe4c4ae51c9fd09e8694567e7d8780e7`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 7.3 MB (7328581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c108c9129f02502270742d354eb48ccdca567cdcf1a506749a03c9b3bf38d`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed1af1582bcbdfc15e0e37124a9ac0e29abc134def26f11f514966f0995a507`  
		Last Modified: Thu, 22 Feb 2024 23:53:01 GMT  
		Size: 423.0 MB (423035792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fab7803e220bc51b6c1e12c3b4847076d3aad1735550aa4921fbd6b5453d15`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5214107e0214f6078ffe344eac2fd5ae9a81e6f29db90fb5abbffb8ff1797211`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1189994bbdf2971d487e2f9cc481c450a2e708d17190a112ed9a9ff629bfbc9`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 185.9 KB (185910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2b1a362d38bd99c39fab367a8bf9360dbc50b441bc575fe2e5b2cc4964234`  
		Last Modified: Thu, 22 Feb 2024 23:52:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acf99084f29a4e9ce62ea5bdcb7ea15a8a5b65aebcf7ff60d4ad7431ac90ced`  
		Last Modified: Thu, 22 Feb 2024 23:52:54 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:65eec65893a1f00dd6d3bf2a4337285d8ae791fc09e2597ba2e673798564c164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754fdafc68c47235ac23187677b6b78b6e1a54ef1342bdce494ee79f9ae1ead9`

```dockerfile
```

-	Layers:
	-	`sha256:e69fa4a3a00bc8424ef49e9ad09865cfd5d9a0f3b7ae32922aab1025663c3202`  
		Last Modified: Thu, 22 Feb 2024 23:52:53 GMT  
		Size: 2.6 MB (2589189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46fb324f66000e60a058fad65d487a898dfc4f32ab0f798d86de16de6af1bb7`  
		Last Modified: Thu, 22 Feb 2024 23:52:52 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
