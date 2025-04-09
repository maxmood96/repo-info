<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.16.6`](#elasticsearch8166)
-	[`elasticsearch:8.17.4`](#elasticsearch8174)

## `elasticsearch:7.17.28`

```console
$ docker pull elasticsearch@sha256:0140bed187eb2cec0738ea0b00f3ec7cb87683413d441043577af88d94c297a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.28` - linux; amd64

```console
$ docker pull elasticsearch@sha256:138232477ce54b0d26a33eccbb66745eaf8707cca21f2daf7c91850bcc526d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362608698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91a5f5a5934b61c774c19217ae1047937a88d21bd419811ee6b9f3269c93a08`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Feb 2025 11:58:14 GMT
ARG RELEASE
# Tue, 25 Feb 2025 11:58:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Feb 2025 11:58:14 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-20T09:05:31.349013687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=139cb5a961d8de68b8e02c45cc47f5289a3623af org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-20T09:05:31.349013687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=139cb5a961d8de68b8e02c45cc47f5289a3623af org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ac13c89373803e9e092ea79355580f7f13098a32dc959c416c2bb6fdd8a3bd`  
		Last Modified: Wed, 09 Apr 2025 01:16:52 GMT  
		Size: 7.5 MB (7525331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0263335bcf1d00833f34b788ed56a988b5ca90dc07c77320e8fd9b8128c38155`  
		Last Modified: Wed, 09 Apr 2025 01:16:51 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d01f39eb478384a149b1512740ce63d78c127c69e70703841d960f1522b25fa`  
		Last Modified: Wed, 09 Apr 2025 01:16:58 GMT  
		Size: 327.2 MB (327249015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a94b9d6905cb8186a24a00a08c4bd34919990033e3c2f7cad9432ee3bab07b2`  
		Last Modified: Wed, 09 Apr 2025 01:16:51 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6c679663bd89579cd452e5f7fb09f17e717aa72469c0bf22ce1bbf42c10e1c`  
		Last Modified: Wed, 09 Apr 2025 01:16:52 GMT  
		Size: 2.0 KB (1975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfadd42d4c8e2f3184a4e2c92bea965a0a2bd1b3c1379f3785252eeab610f76`  
		Last Modified: Wed, 09 Apr 2025 01:16:52 GMT  
		Size: 192.2 KB (192171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c1ba8d09185ff68bd945253553ecfccd3626109762138b9987497d02acf2fc`  
		Last Modified: Wed, 09 Apr 2025 01:16:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d243b18ed982d51b8644a020fe492ba5be526c7182b91923793a363418866f`  
		Last Modified: Wed, 09 Apr 2025 01:16:53 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.28` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f479efe3712cd78f9fa14c93b15b648d333cae5c7b3d387337b642d58a9479fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1840e8688fec164053e34735465e8ef808ffc842d0b49639e64d1371001d3f3d`

```dockerfile
```

-	Layers:
	-	`sha256:220c4f9255842b201421bab4c112f3f089e7d402be11bb2ea39692a4f9633cf8`  
		Last Modified: Wed, 09 Apr 2025 01:16:51 GMT  
		Size: 2.6 MB (2551194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ac966e0e73df40ea62ef38c33c8e6a7e1c13cdb2c47ec799c4f12aa33f3cff`  
		Last Modified: Wed, 09 Apr 2025 01:16:51 GMT  
		Size: 37.9 KB (37888 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.28` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c1b3d83e3a491ef45b666a1971a7af3a601000aba697fc9bc95267bef9057759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (364955657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55327d50196b341710a8b4cdf91c0bb05a017b6dc61078c8afe0f09e5571c4`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-20T09:05:31.349013687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=139cb5a961d8de68b8e02c45cc47f5289a3623af org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-20T09:05:31.349013687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=139cb5a961d8de68b8e02c45cc47f5289a3623af org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b133d5c02ffb14a9c6e6ac94c32dadf32f97af646b31c80a855514c4931f4d`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 13.8 MB (13751417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d330b7cf948d0f619255ac08f295788e85a820c6e52b67902c9756bcd6c7e8`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e89805206fdb8432916dc6560a00ae443669c44d7a09151cb6349c88b484f2`  
		Last Modified: Tue, 25 Feb 2025 23:40:44 GMT  
		Size: 324.9 MB (324912862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8002871af38cc7be0a2eebf218d126f51c10b412966de90d60a9c5f94f8159be`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2669410c65046a62db0ba3df2e88597b2de8bc96dadfcd351033d56e8f336d`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7747397d0c311890ea63bbc873f60d871d6e4fdd24c861ecb2bd7a2b0d822`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 186.2 KB (186180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714e911a00a541bbddb81fab83d24740b31db75953537789eef197eee32ec39`  
		Last Modified: Tue, 25 Feb 2025 23:40:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505b1c53c82d2f484aa0c5c0b57ac1f17d700a7b4334573d9a8397a23f18129`  
		Last Modified: Tue, 25 Feb 2025 23:40:35 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.28` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c313ff7c830e1e09ccf30164de34db52281bf4cc226d57ddb12c14c1640c10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371cfa09214ad38aeed4e2a0a3d9aeb9ee33d0f041c24c4407224aecf3d5a3a2`

```dockerfile
```

-	Layers:
	-	`sha256:991a884ae21011ae96e96f66c15a7e7f0067982813928727d483a3407bfe849b`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 2.6 MB (2550126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596d93db3ab022ef7a4baa58e6ac5e03b4f0c02fd2fd5908b5e7dce3951c27fb`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 38.1 KB (38099 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.6`

```console
$ docker pull elasticsearch@sha256:3910bb23849bfd25b6d0177450abe36a7bc1bd2e83e427bfad916557c5d32242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6a2454b98059fe0cf61275e549844a8ee2f5e17a0c5f3bc145390973aab73146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.6 MB (676616722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb0241cb9c75cd0c2c55246c4e143b7037095984b4f3d19acdbd92514a5f23c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Mar 2025 08:54:09 GMT
ARG RELEASE
# Tue, 25 Mar 2025 08:54:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 08:54:09 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T10:07:27.754027795Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eabb32aee47ed0c4ba71c169f098d0379402efe org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T10:07:27.754027795Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eabb32aee47ed0c4ba71c169f098d0379402efe org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35ae636ad739a439b3ce4ab6848100fd310b1929faa893f3cf3169ada7067f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 7.5 MB (7525252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731692c7af47a88f9332cddd1595cfbeaa80ca16a50eb20cd318d3257fad6cf8`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fabe2dd4a13201b4d867de9a8c22fb0e3f6d8e0b80224e90bc4613b0a66ded7`  
		Last Modified: Wed, 09 Apr 2025 01:17:57 GMT  
		Size: 641.3 MB (641257641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7936eafc67cfc76964411b90dffd4825554193806746851979708187d161598`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3620e290983ff5aafe530801fe6bd5b6203f7f879ceb98c0ef85ec118cc43`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf90c972b8682f0a30eb65cb11a393a225beba00d86ee78b7e011488b9d35b1`  
		Last Modified: Wed, 09 Apr 2025 01:17:48 GMT  
		Size: 191.9 KB (191902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dce968524f51fe44fa8545088d6c9e37977a5a69f7e1cda9938751cd15ae27`  
		Last Modified: Wed, 09 Apr 2025 01:17:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84448ca9455fee33d2f06269c6ac7823ac8ce9b179eb2b016e43b88d2fc78f9a`  
		Last Modified: Wed, 09 Apr 2025 01:17:48 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8e0ebc599e6733e7597a556d0e73b60452e7956e22a5801efb21565213636d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288a3a25f39a1acde836afa7ab9088b2880d6f759f67b3f4a45eeb78a5e9660b`

```dockerfile
```

-	Layers:
	-	`sha256:4505a60b11dfd2d360e1e1ef8f9d600bd45f6c451fc0a656e615ef62dbe11eef`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 3.0 MB (3002701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443f080041f0ac1cb225e57152a5e50f55832fe1a9ca467b9ca0dac483a3d807`  
		Last Modified: Wed, 09 Apr 2025 01:17:47 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:46361de8b04efa356a763b1f30be384817e55e585674be8da247e44988844ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.4 MB (526366510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63269b9fd03952ca052032714d6750fc3bd1774250b911438d25e5621e830e8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T10:07:27.754027795Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eabb32aee47ed0c4ba71c169f098d0379402efe org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T10:07:27.754027795Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eabb32aee47ed0c4ba71c169f098d0379402efe org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c2366281558c3fd6d4aa155d04ace1d089bf5eddaa8f02d51dedadf212541`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 13.8 MB (13751835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287c434f4bcc57ce95e84644d46ac9e8f3f4fa25e320e2a6d77508895a40175`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7a14a9b09d7b4dce65d0d019b91129bd64364d04be6c066a41ccaa46e13635`  
		Last Modified: Tue, 25 Mar 2025 19:44:33 GMT  
		Size: 486.3 MB (486323822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206641e45ee45a3d961b5b2ab1318cf491b64cb51da5eb310639795206220f1`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbd57782e82acd156df6b54c5169f01dcdce7dc49a0a29196d77948a0f25774`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3c6aaeeb254431e665d8be4d4bbb64c28d4ffa0ab60fbcf8176a8454a6c8`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 185.9 KB (185914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed167ef1f03dbb75fc9f4395ff693c587701fc06b3eca7c5234c8fedf1c8ae7`  
		Last Modified: Tue, 25 Mar 2025 19:44:25 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c77f54fd0f6743e093c589548a2c4e4602840cefde8bd19ed631533f33dcd5`  
		Last Modified: Tue, 25 Mar 2025 19:44:25 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:67861c6469782c19521c8711a624037b33e3afd06b0c5c0010959b4f953efdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df280673d79bab4fdd71e05fb198067256d34bfa607c3a2f0d6febdd9b5083ed`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d4d5382914cc7eb977992600ca75d0456e3466816627a0887d739edeb871a`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 3.0 MB (3001633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a461b86d6d946853a2e5bbdca88a7318ddb8ab6548a491fe588eabb9d31880`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.4`

```console
$ docker pull elasticsearch@sha256:ee03de0caf099580577f8b9452b7c9860717eda2c2cfa477abe1db5bb89c42a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f3c2220e3ef1a97226f8074dbcdba3409804228fd81fd62b410f49fb47924dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677564625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f7eca0daf85f759b0cddffb2af421f197b18b716909783921683a27415aed0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Mar 2025 09:28:57 GMT
ARG RELEASE
# Tue, 25 Mar 2025 09:28:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 09:28:57 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T15:39:59.811110136Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T15:39:59.811110136Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f138183723da099a9edb02db3746d500f60e9b0e7e46a7a5955eff7c0c12ae05`  
		Last Modified: Wed, 09 Apr 2025 01:17:54 GMT  
		Size: 7.5 MB (7525297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8af62aae17e6774ae5c2a4724710b35f2512457a63fa58e24b725fa06f804b`  
		Last Modified: Wed, 09 Apr 2025 01:17:54 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f471a6678f614998c242cf7dc7b24068ab3cfef494b00cc8d45bd0f8ecc8473`  
		Last Modified: Wed, 09 Apr 2025 01:18:05 GMT  
		Size: 642.2 MB (642205499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834b69ddd66c85f1872ceccc16f45009599226e022f67d64a3ea61aad905fc`  
		Last Modified: Wed, 09 Apr 2025 01:17:54 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac5704ddf10972c71c6e2751fb70583f9e697b44c3ee6e494ecbe5a7811b44`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2fce7d99ff262bc742578b5440bf4644d15ed554449c33ae5d332d2bb8cabc`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 191.9 KB (191903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed26184824e1abedd52c55a4dec3010f9c02d5e8db2efdc00f698c3e7f10be9`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a62456fa947007626cbb28a2834666e7e243b73aa3d522efa2da8dff1baeb84`  
		Last Modified: Wed, 09 Apr 2025 01:17:56 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:cfc6e99c748966b39570a430bbce438ff8463930d5a2de69852ec4206ebf5994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aec745d0b22916d042e7e9a248bd16090d121a1f7b3bd5e0399d6c10a334354`

```dockerfile
```

-	Layers:
	-	`sha256:b9a69b2f37bc94a4529e5a714706dacf2cd8384ac874b810ee20537d38932c94`  
		Last Modified: Wed, 09 Apr 2025 01:17:54 GMT  
		Size: 3.0 MB (3008901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209dd32cc7719b50a91a71a0a980c5635a0e16aae4ac60ef2308249207f149cb`  
		Last Modified: Wed, 09 Apr 2025 01:17:54 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fec9dd9861e33c7966f7cbc83c0fcee1274b60c9e68930fc6560956ffe49d3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527307058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91f43df96db428e4404a2e6dec5584a7b527755dded3a1c072c178f33ab288e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T15:39:59.811110136Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T15:39:59.811110136Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c2366281558c3fd6d4aa155d04ace1d089bf5eddaa8f02d51dedadf212541`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 13.8 MB (13751835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287c434f4bcc57ce95e84644d46ac9e8f3f4fa25e320e2a6d77508895a40175`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b38059e64908e99d982b25be15d64748be0656791fc0bce37fc8c101c420e`  
		Last Modified: Tue, 25 Mar 2025 19:56:51 GMT  
		Size: 487.3 MB (487264360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2575204bebd49dca5799047ab6e3a9d7dc04c884b567329f8bf8b8ddd0e8ca01`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf271c7c6f82131b0d9fc6ccbfa6342c201a0bace9bc571938a790a06acac8c`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4848bb6cfb7c74932e6cffd7ddbb39c4e0191e50fd23620b6fb091ab2f23e3e3`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 185.9 KB (185920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e1d4bbfb5f0aa78027619b3cd1cfcea023d50d2a9c9ea09040670e605b4b34`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4489603061e1f096fff9b1375795fc37ee904b18a9dcc0b36b793fbf20be1b46`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:658568a13bc614c3a4dc150f49e96d100e35f46f9d560bc80aedbb8b8ad9d714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef581eb893f4c4355cc45e6f1876b83b083fdfff170598c3074897f4046bca85`

```dockerfile
```

-	Layers:
	-	`sha256:3826b65fbac469198569266d13f91a13064b5e623fef96864b6905132a9c97ad`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 3.0 MB (3007833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a4ccaed599968cf007482fb7413c618fac6160cf9d97669654928eccfb682d`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json
