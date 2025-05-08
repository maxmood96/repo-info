<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.17.5`](#elasticsearch8175)
-	[`elasticsearch:8.18.0`](#elasticsearch8180)

## `elasticsearch:7.17.28`

```console
$ docker pull elasticsearch@sha256:a06b03a2db8db2be43d3c3851e7bcebdd4fff79f4db08c7da6bad7a8776d3e15
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ac13c89373803e9e092ea79355580f7f13098a32dc959c416c2bb6fdd8a3bd`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 7.5 MB (7525331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0263335bcf1d00833f34b788ed56a988b5ca90dc07c77320e8fd9b8128c38155`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d01f39eb478384a149b1512740ce63d78c127c69e70703841d960f1522b25fa`  
		Last Modified: Thu, 08 May 2025 17:13:36 GMT  
		Size: 327.2 MB (327249015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a94b9d6905cb8186a24a00a08c4bd34919990033e3c2f7cad9432ee3bab07b2`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6c679663bd89579cd452e5f7fb09f17e717aa72469c0bf22ce1bbf42c10e1c`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 2.0 KB (1975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfadd42d4c8e2f3184a4e2c92bea965a0a2bd1b3c1379f3785252eeab610f76`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 192.2 KB (192171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c1ba8d09185ff68bd945253553ecfccd3626109762138b9987497d02acf2fc`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d243b18ed982d51b8644a020fe492ba5be526c7182b91923793a363418866f`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
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
		Last Modified: Thu, 08 May 2025 18:57:49 GMT  
		Size: 2.6 MB (2551194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ac966e0e73df40ea62ef38c33c8e6a7e1c13cdb2c47ec799c4f12aa33f3cff`  
		Last Modified: Thu, 08 May 2025 18:57:49 GMT  
		Size: 37.9 KB (37888 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.28` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:be68618d3bef93f04847acad4b40bb192a3256d1eb4bebe0405a7b6fe85157d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358556286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4858c36ae19a0932446d44843940a4fd544da717c6289d28548935efc1e66`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daba52b3ee0e1cf293f1e799bc34aff58db06cbbea9bbbf91e5d8b2f00df20d5`  
		Last Modified: Thu, 08 May 2025 18:11:31 GMT  
		Size: 7.3 MB (7348268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb2f367eb7b6c0a5c424e5c26aef7989018787439f1d51ffe12cf20eac8f`  
		Last Modified: Thu, 08 May 2025 18:11:30 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57744e44e24c68b5b1ed773f7a4a7af87e6f4eff9da3fb2d92d86a51f00c8aab`  
		Last Modified: Thu, 08 May 2025 18:11:41 GMT  
		Size: 324.9 MB (324912818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac9b2fe3d7dbd6ee539f850b195591ebe42bf0675d72822533dc5860813e69`  
		Last Modified: Thu, 08 May 2025 18:11:31 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3849e414a417bf481779d36f0608cea8bc3cf42ce5861a7ff8431099c240b`  
		Last Modified: Thu, 08 May 2025 18:11:31 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fca7af8aea6072d1397d107af24b3bfcaef9504a82f7821756397f23922e05`  
		Last Modified: Thu, 08 May 2025 18:11:32 GMT  
		Size: 186.2 KB (186176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1051cef15717f8f37760ebdb86e4483fe460d9acd3c9f45d8fcd0f2d6928fde6`  
		Last Modified: Thu, 08 May 2025 18:11:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802283160d1a0755ca3c755bb05b374b812ed0382019faacd4c4178cc83886b4`  
		Last Modified: Thu, 08 May 2025 18:11:32 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.28` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9bbd1f61ed8374f4a4acb9f971cef4fd7a3597ea50c3ebe831150ee87d1295ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b0e3d6e8ae67933af732c9232e2292e50b14a7d9c23c16500c021be1dc570b`

```dockerfile
```

-	Layers:
	-	`sha256:6b24d54b97712ffb2fd9c89c0e3c844f3eb06462b455da36ed621ca15cbd3e13`  
		Last Modified: Thu, 08 May 2025 18:57:49 GMT  
		Size: 2.6 MB (2550166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9813a4422dc683c9f8be09bfc9cdd8dcde7a53d8fba30f14846487da9801f644`  
		Last Modified: Thu, 08 May 2025 18:57:49 GMT  
		Size: 38.1 KB (38091 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.5`

```console
$ docker pull elasticsearch@sha256:c0e2fdcad592928332b57cff5c45446b306fe8fe780ea11d955e5b36d06facf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8be5d8066774a3fb42209d43b289a148c1c7e14cd901f8f1a7e2b5ab9ca4e35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677578330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5d6cef336dfbf754ed1871ae2e6f642e43410dd4da91cf976788ea897b3a10`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 11:26:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 11:26:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 11:26:34 GMT
ENV SHELL=/bin/bash
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 15 Apr 2025 11:26:34 GMT
LABEL org.label-schema.build-date=2025-04-09T22:07:03.265074501Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=55fce5db33c28431e3a504c47d359ddbeadde69d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.5 org.opencontainers.image.created=2025-04-09T22:07:03.265074501Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=55fce5db33c28431e3a504c47d359ddbeadde69d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.5
# Tue, 15 Apr 2025 11:26:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 15 Apr 2025 11:26:34 GMT
CMD ["eswrapper"]
# Tue, 15 Apr 2025 11:26:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e067d1fd8fc8893b961c63336631e52701aff38e4cfff46be4475a133a3bad5f`  
		Last Modified: Tue, 15 Apr 2025 17:57:14 GMT  
		Size: 7.5 MB (7525313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89220fc070633e33268587e254e35056f65352601168a209a9073d4fa7527ed0`  
		Last Modified: Tue, 15 Apr 2025 17:57:14 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5887003d81ba16055ce3c1e35e450718b031edeb49e5c3183f48b2f23999b7a6`  
		Last Modified: Tue, 15 Apr 2025 17:57:25 GMT  
		Size: 642.2 MB (642219197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7752dbb17826623c3ce8cebcb933f40ce926f71499382fb97c336405245810`  
		Last Modified: Tue, 15 Apr 2025 17:57:14 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47caf6a2a7e5010aa95e6b50f40c86e427432f761f66de3c03d8159d0726c5cf`  
		Last Modified: Tue, 15 Apr 2025 17:57:15 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b77933bf9b0759b5ed09bc39f83b34dcfb17aaa18110a894fdac9da02aac81d`  
		Last Modified: Tue, 15 Apr 2025 17:57:15 GMT  
		Size: 191.9 KB (191898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f933bb5b868b4e2c7838631ca2a31bc90958d124a7acea01b7ed1f6415dac72`  
		Last Modified: Tue, 15 Apr 2025 17:57:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067acd2bf26f80c37739d457ff88f028a2a7973bb67b11c91040d4ffabb7c5ea`  
		Last Modified: Tue, 15 Apr 2025 17:57:16 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:844e851ec3d9e385e6d49db46b55073a2a493d97ed095d3ccc0b5df98288aa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c18eb50b509b9488385f60fbcc6576a47f1383a24a0dca00be7f2b1ddf263dd`

```dockerfile
```

-	Layers:
	-	`sha256:79e3ec73339357494297a7407d1c57b930cbab1599bf1af9549bff74fe8b4653`  
		Last Modified: Tue, 15 Apr 2025 17:57:14 GMT  
		Size: 3.0 MB (3008901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104c9bc914058f0688fbe2584d7ed07c809c608035f8c84d4be1b03662f78402`  
		Last Modified: Tue, 15 Apr 2025 17:57:14 GMT  
		Size: 38.2 KB (38203 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9201989ed09677ed3f491570ad1748f0dbfc9e13d7340281a1966883a7b2cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520919795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6450a509041cb241ea3b3a8c543f900228e5557b59d1e2137aa869b224519d24`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 11:26:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 11:26:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 11:26:34 GMT
ENV SHELL=/bin/bash
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 15 Apr 2025 11:26:34 GMT
LABEL org.label-schema.build-date=2025-04-09T22:07:03.265074501Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=55fce5db33c28431e3a504c47d359ddbeadde69d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.5 org.opencontainers.image.created=2025-04-09T22:07:03.265074501Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=55fce5db33c28431e3a504c47d359ddbeadde69d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.5
# Tue, 15 Apr 2025 11:26:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 15 Apr 2025 11:26:34 GMT
CMD ["eswrapper"]
# Tue, 15 Apr 2025 11:26:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcd8f73d70ee3efc43c4acccc6503df1857638d0d3eff132a56b861e0a3c74`  
		Last Modified: Thu, 08 May 2025 17:43:45 GMT  
		Size: 7.3 MB (7348337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fdd84476023d04d784209b1c5160414958658a04b714efd7f90a00c875b5bb`  
		Last Modified: Thu, 08 May 2025 17:43:44 GMT  
		Size: 4.3 KB (4327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9a47def8a859383dd4d9443cccda5c49128df22919840e78e7d5735e7136d4`  
		Last Modified: Tue, 15 Apr 2025 18:12:16 GMT  
		Size: 487.3 MB (487276740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4a510ec25abc217420d88667a677978839b7e767edf865490122e209a4d8ea`  
		Last Modified: Tue, 15 Apr 2025 18:12:06 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ed7d27666985e8b3c9d57744ca3bf43e0a6086cf1b981c621cfc77cc2e0d6`  
		Last Modified: Tue, 15 Apr 2025 18:12:06 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1a879559cd768150b800de4303f2581bc7091136f9cd8f8d7a3608492e264`  
		Last Modified: Tue, 15 Apr 2025 18:12:06 GMT  
		Size: 185.9 KB (185926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ddbd28268964c8aec33b9988e63ae33e1d4efc0e5c74661f2a3d1275808c9`  
		Last Modified: Tue, 15 Apr 2025 18:12:07 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ee3f7c124906930f30b39ced1a8cd61a61282d289a5dedc1edadb735b04f1`  
		Last Modified: Tue, 15 Apr 2025 18:12:07 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6e55751ee0d1bc05732002575d8ce7c41425b2b6fe2068abfbf5a1acb4067e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d987a20ca4a3889daac403bcf30557a7fac235f666c6dac9460a46dcc5a9acd2`

```dockerfile
```

-	Layers:
	-	`sha256:7141e9c70e7215932b57f3cd61c647acdb2f6cd7c2c28d4efe2e8e15e522f777`  
		Last Modified: Tue, 15 Apr 2025 18:12:06 GMT  
		Size: 3.0 MB (3007873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9773c661fbf947e169c3e33bea59aca6ff6f7c59702ede52a2a0d0e77f85959`  
		Last Modified: Tue, 15 Apr 2025 18:12:06 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.0`

```console
$ docker pull elasticsearch@sha256:658ea54de8d38c9ee69389e7fe226d6fd589816d7ed7f7cc911017ed646216d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ef7bb0f872488a4333a2967473b0c1202cfd0780d0ec2d7ebdefd11f68e61e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.7 MB (688726864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9016be4cb0d00b4ccceed478b5bc83923d834738f76356b906e713d91c4a0e0b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 06:36:04 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 06:36:04 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 06:36:04 GMT
ENV SHELL=/bin/bash
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 15 Apr 2025 06:36:04 GMT
LABEL org.label-schema.build-date=2025-04-10T10:09:16.444104780Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=04e979aa50b657bebd4a0937389308de82c2bdad org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.0 org.opencontainers.image.created=2025-04-10T10:09:16.444104780Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=04e979aa50b657bebd4a0937389308de82c2bdad org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.0
# Tue, 15 Apr 2025 06:36:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 15 Apr 2025 06:36:04 GMT
CMD ["eswrapper"]
# Tue, 15 Apr 2025 06:36:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27369ff986ec4a87d3c19d6d00919bf9fa0cba3ae17293eb6a49185853859975`  
		Last Modified: Thu, 08 May 2025 17:11:38 GMT  
		Size: 7.5 MB (7525242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8debe542094676b2ef39cd2a678e494cf4cef504f5a85f1a596e6bdee0559c40`  
		Last Modified: Thu, 08 May 2025 17:11:37 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b4b6b1fbdb8532c658c50db0bb41be521bf07f78a2f80e69b53f556a1be7c4`  
		Last Modified: Thu, 08 May 2025 17:19:59 GMT  
		Size: 653.4 MB (653367785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231def5f0d37145ae5e2458b98c84ebe0deca6e2f61a3751379df2d9fa8bf9`  
		Last Modified: Thu, 08 May 2025 17:11:38 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b7264313a4f565edb85a3ee2f96e439a2b7eae8debe16346d8d1c8bdfabc87`  
		Last Modified: Thu, 08 May 2025 17:11:38 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9983bf36c7645eebc69b682f5bbc6b0854ab641601c9da2ad98f0ac3ed154de`  
		Last Modified: Thu, 08 May 2025 17:11:39 GMT  
		Size: 191.9 KB (191909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5b73b8c4c8ed8787ce1823afdf550072aa2b0eeb845ececbdf61f69554ce8`  
		Last Modified: Thu, 08 May 2025 17:11:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1c71e9c868da3dd6638f12983571e159b87a6d2452c82c4d50b8b01af8cce8`  
		Last Modified: Thu, 08 May 2025 17:11:39 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:474b4d1fbbe335ed429e701a02c7871e498112952924eb90ce20032a8fdf6eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768e1dd637b382876592df2356287dd1cacd0bb0db4fbb484021ccd5ca873e0`

```dockerfile
```

-	Layers:
	-	`sha256:0de61d79e7ed566f3ba64804314c2eac83d614229f8795cec78f143c8d6db2f2`  
		Last Modified: Wed, 16 Apr 2025 17:18:03 GMT  
		Size: 3.0 MB (3040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bbc1076f7b7d2680af526911581bbaa89e65cd44beae2ec82b7851a47f50c5`  
		Last Modified: Wed, 16 Apr 2025 17:18:02 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:254c587b8e76ecb7cb6bf6f38d604725375b11a88fd11b167568ae4eef0233ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.3 MB (530265348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce874ba278c3b09c62cc9013647ef002d1b01dd49310ff1f5bff48e156d2c6c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 06:36:04 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 06:36:04 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 06:36:04 GMT
ENV SHELL=/bin/bash
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 15 Apr 2025 06:36:04 GMT
LABEL org.label-schema.build-date=2025-04-10T10:09:16.444104780Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=04e979aa50b657bebd4a0937389308de82c2bdad org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.0 org.opencontainers.image.created=2025-04-10T10:09:16.444104780Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=04e979aa50b657bebd4a0937389308de82c2bdad org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.0
# Tue, 15 Apr 2025 06:36:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 15 Apr 2025 06:36:04 GMT
CMD ["eswrapper"]
# Tue, 15 Apr 2025 06:36:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcd8f73d70ee3efc43c4acccc6503df1857638d0d3eff132a56b861e0a3c74`  
		Last Modified: Thu, 08 May 2025 17:43:45 GMT  
		Size: 7.3 MB (7348337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fdd84476023d04d784209b1c5160414958658a04b714efd7f90a00c875b5bb`  
		Last Modified: Thu, 08 May 2025 17:43:44 GMT  
		Size: 4.3 KB (4327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdea997a20a8dddeba241c231043922c70e222a64aeb2496f2c87f86685214`  
		Last Modified: Thu, 08 May 2025 17:48:17 GMT  
		Size: 496.6 MB (496622286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a55616eb873bbf4a39710eb65dcb97124f6838e3effdfcbdfe2e6b9f4ce3`  
		Last Modified: Thu, 08 May 2025 17:43:46 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651bafba4b95f62d3769453b16df7e68495e67d13d4655d6f2085fb5002fe8f`  
		Last Modified: Thu, 08 May 2025 17:43:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0b7b57639c6c00528cad16ec166fed4f9e4b174e1d23b265c8596790d4896`  
		Last Modified: Thu, 08 May 2025 17:43:47 GMT  
		Size: 185.9 KB (185927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbc7f10c9bb4339035711b0fef82910eec2882f59a5d514135a149f0c8c162`  
		Last Modified: Thu, 08 May 2025 17:43:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755edc19036118525b873e32e418d393d8948e1ce99e25cc1533656ad12ad502`  
		Last Modified: Thu, 08 May 2025 17:43:48 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:413760aa379c00ee29c8599af5ec3ae56f8babf1b2b71e661f385a0b4e4f180c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ac5b6fad94e31acfde6956fdb9376cca5aef7e60effdd813430bb714945d3b`

```dockerfile
```

-	Layers:
	-	`sha256:abf805bd230931748cda5f4c208737a8b6b809928dc9461cd2f72a3d4c8e69f1`  
		Last Modified: Wed, 16 Apr 2025 17:17:44 GMT  
		Size: 3.0 MB (3040587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4577e9ed867b8db6e1b924f387b2ad5d898bc20ad675399dceb098343499e11`  
		Last Modified: Wed, 16 Apr 2025 17:17:43 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
