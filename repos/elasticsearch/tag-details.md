<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.17.6`](#elasticsearch8176)
-	[`elasticsearch:8.18.1`](#elasticsearch8181)
-	[`elasticsearch:9.0.1`](#elasticsearch901)

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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daba52b3ee0e1cf293f1e799bc34aff58db06cbbea9bbbf91e5d8b2f00df20d5`  
		Last Modified: Wed, 09 Apr 2025 07:14:17 GMT  
		Size: 7.3 MB (7348268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb2f367eb7b6c0a5c424e5c26aef7989018787439f1d51ffe12cf20eac8f`  
		Last Modified: Wed, 09 Apr 2025 07:14:17 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57744e44e24c68b5b1ed773f7a4a7af87e6f4eff9da3fb2d92d86a51f00c8aab`  
		Last Modified: Wed, 09 Apr 2025 07:14:25 GMT  
		Size: 324.9 MB (324912818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac9b2fe3d7dbd6ee539f850b195591ebe42bf0675d72822533dc5860813e69`  
		Last Modified: Wed, 09 Apr 2025 07:14:17 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3849e414a417bf481779d36f0608cea8bc3cf42ce5861a7ff8431099c240b`  
		Last Modified: Wed, 09 Apr 2025 07:14:18 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fca7af8aea6072d1397d107af24b3bfcaef9504a82f7821756397f23922e05`  
		Last Modified: Wed, 09 Apr 2025 07:14:18 GMT  
		Size: 186.2 KB (186176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1051cef15717f8f37760ebdb86e4483fe460d9acd3c9f45d8fcd0f2d6928fde6`  
		Last Modified: Wed, 09 Apr 2025 07:14:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802283160d1a0755ca3c755bb05b374b812ed0382019faacd4c4178cc83886b4`  
		Last Modified: Wed, 09 Apr 2025 07:14:19 GMT  
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
		Last Modified: Wed, 09 Apr 2025 07:14:17 GMT  
		Size: 2.6 MB (2550166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9813a4422dc683c9f8be09bfc9cdd8dcde7a53d8fba30f14846487da9801f644`  
		Last Modified: Wed, 09 Apr 2025 07:14:17 GMT  
		Size: 38.1 KB (38091 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.6`

```console
$ docker pull elasticsearch@sha256:ff418785f2b6995c472fa16fbece7d95a328694cf776fef0c96882e7ba7442b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:cc5541fdf78060882e4ca1f462a23473b61f9b3c3b2b5db5be9223a2311f23ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677565433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bfd1afebf91ddfdc3ee916d38ab283483b57a7909150c59006212ba7a44a44`
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
# Tue, 06 May 2025 08:53:36 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
ENV SHELL=/bin/bash
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.build-date=2025-04-30T14:07:12.231372970Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dbcbbbd0bc4924cfeb28929dc05d82d662c527b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.6 org.opencontainers.image.created=2025-04-30T14:07:12.231372970Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dbcbbbd0bc4924cfeb28929dc05d82d662c527b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.6
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 May 2025 08:53:36 GMT
CMD ["eswrapper"]
# Tue, 06 May 2025 08:53:36 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8ae3c5cac1d89fe2a44334f31182007f12dfa91fee6939fc84c697ecfbf44`  
		Last Modified: Fri, 09 May 2025 19:02:21 GMT  
		Size: 7.5 MB (7525348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1945e0913748aa4a768b41c493413d3a5b031e90989814973a8e383d70de3f`  
		Last Modified: Fri, 09 May 2025 19:02:21 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f079048605e2e8cc51708456624115967f034a4355cbdea95f74b394c75a052`  
		Last Modified: Fri, 09 May 2025 19:02:34 GMT  
		Size: 642.2 MB (642206265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5bd73c78959bdefdd779389e572380601e1f653832970d6d3327ae1ca472a7`  
		Last Modified: Fri, 09 May 2025 19:02:21 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5219c57f40893073a3db8ee5a3864a24c7c460a496e978c4e3e3911a958f92c9`  
		Last Modified: Fri, 09 May 2025 19:02:22 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ca91ba1bc455fc5ec0bea47872b394324286d39b2cf4502b2d0198d9ac267`  
		Last Modified: Fri, 09 May 2025 19:02:23 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5812fe584da1f3063e75de3ba86000e5dc08abb23cd6a6305533889f4bfa55`  
		Last Modified: Fri, 09 May 2025 19:02:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba55862467553f5871d6fa25d9285cf0d41abffdf298d52ac70e290e141d387`  
		Last Modified: Fri, 09 May 2025 19:02:23 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:611b530286b6b80276a9aca35640ad08751f13acbeee89953db5c31f6a3b5c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5d6acec6412896188e357405de1b666af9a7b40ea08cf88db32158952e6a4`

```dockerfile
```

-	Layers:
	-	`sha256:17ec41651aea91deafaaf5f51f43b26ece684d45c192397e232db78508100a69`  
		Last Modified: Fri, 09 May 2025 19:02:21 GMT  
		Size: 3.0 MB (3008901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5eb3eb0e8d51ceede2825b497f4180da62852f23685e4c002495f7f56f9cb29`  
		Last Modified: Fri, 09 May 2025 19:02:21 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a048b83ecaa1b1afe51784ed647e655b44e45ce6506a61f46beaf307bbb2c828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520909765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0d1958203184a260973c3bcc2c200cbb38382ee2f96a9dd28b311136c4bb63`
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
# Tue, 06 May 2025 08:53:36 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
ENV SHELL=/bin/bash
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.build-date=2025-04-30T14:07:12.231372970Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dbcbbbd0bc4924cfeb28929dc05d82d662c527b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.6 org.opencontainers.image.created=2025-04-30T14:07:12.231372970Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dbcbbbd0bc4924cfeb28929dc05d82d662c527b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.6
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 May 2025 08:53:36 GMT
CMD ["eswrapper"]
# Tue, 06 May 2025 08:53:36 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96c7aa530755864047085f56a0d0bf33f6ac60d26e4b6a0c6c1c5277473cd7`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 7.3 MB (7348348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ccd73b90331f2503d6acf2c8abd38f951721a9b2986438f168dc79f7b224c`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9910f25fa76b3aeefab98f6f01004348a878cb8be740506854c2934362346f2`  
		Last Modified: Fri, 09 May 2025 19:40:55 GMT  
		Size: 487.3 MB (487266725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ededf7d50f55d98616d5e0474638be3a2ffa81e2c4c385c3b02f66f49d0265`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54696eb5d394bebfdab641ced910c8efd44dbcd384a20b7ed59e5c2d410efec0`  
		Last Modified: Fri, 09 May 2025 19:40:45 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f5ee50c5341e2e708d74d848343ae9427906b1301a3ee7ade4e413a7ea010`  
		Last Modified: Fri, 09 May 2025 19:40:45 GMT  
		Size: 185.9 KB (185919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968ff2239fd83a5d802cfeb2d3bf3905e042d4bc48b01d94015cbe255daa0d11`  
		Last Modified: Fri, 09 May 2025 19:40:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f318f5fe6ad94ccb0094fc6ec9b9aff9d0b03589453f86a05666717d9bcc973a`  
		Last Modified: Fri, 09 May 2025 19:40:46 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:472797445ad624db4c7bb154026bb81ea69823399405ea5eb954facdc8c85b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d667978d1c37fb1b3ce1701fe75e2c9e1f10c6ca450f90c83283ed4dbca4d`

```dockerfile
```

-	Layers:
	-	`sha256:d382823fbb37401f29948548a2625942a004120af5b6e2f57622f118a14266ed`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 3.0 MB (3007873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50a898c60bdae2c2f50a290b90eabaf59ad993d3a71e3617d8a071bfa73b81b`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.1`

```console
$ docker pull elasticsearch@sha256:5823091e62c231e68301ff68d9643e023e82e749d343737c1fc26457505dca1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:db3fa218c0b8a6d065dc36a0bc263c9a6e68a0a7eec0b5f5b7888d462be43bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 MB (688983396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e8c2d5c77ce549dea630cbe9f37d2649034c1b67b6a4d9a5f47a21dbaca61b`
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
# Tue, 06 May 2025 09:07:22 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
ENV SHELL=/bin/bash
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.build-date=2025-04-30T10:07:44.026929518Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=df116ec6455476a07daafc3ded80e2bb1a3385ed org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.1 org.opencontainers.image.created=2025-04-30T10:07:44.026929518Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=df116ec6455476a07daafc3ded80e2bb1a3385ed org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.1
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 May 2025 09:07:22 GMT
CMD ["eswrapper"]
# Tue, 06 May 2025 09:07:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85826ade9bfb20b4b35c572423dcaed6ceb2e4e4fd1129ea76c5041d578d2d7`  
		Last Modified: Fri, 09 May 2025 19:02:18 GMT  
		Size: 7.5 MB (7525309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f1daf49c01159cdaed3a2700f6c145a51310b1dc37bb0bc57c72fec14f456`  
		Last Modified: Fri, 09 May 2025 19:02:17 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddb586cd26e993f01c2aaded849647b2e0589619ec5b0bbde3f8eda2add44ef`  
		Last Modified: Fri, 09 May 2025 19:02:28 GMT  
		Size: 653.6 MB (653624253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91c46a806bbf85fdf6a123651ebbe8a6eab870d8380f01060ee1d9e8314f61c`  
		Last Modified: Fri, 09 May 2025 19:02:17 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109917bbabf2296182ace30b848e5d72bf1617a9692a3358a8247c593b1a582e`  
		Last Modified: Fri, 09 May 2025 19:02:18 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398d841fe8ab203b8b73ada2cf819d11c044ef34cea822b1492ddd8ac5f2dc72`  
		Last Modified: Fri, 09 May 2025 19:02:18 GMT  
		Size: 191.9 KB (191908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6639a79e01e23e13d73ef3493936f0eb1e7a917b0ee5e020ced4bcec567a753f`  
		Last Modified: Fri, 09 May 2025 19:02:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ceb2e4b74f0327e5678c42d3648ee67bbb65b69c570e9b4802bb51498ba4b7`  
		Last Modified: Fri, 09 May 2025 19:02:19 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:efbeffb06f689b16571713526f084eeb3c090d2e71a0db678b76b2ceed350077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e9aa5fe476e4f86473261f2efa436d70569d7abf06046d33ee41e1bdd4dea4`

```dockerfile
```

-	Layers:
	-	`sha256:6bfd63495fc0e5c037a959dee32f7e140d218c36c0f0d6886c68daaf0b06ba17`  
		Last Modified: Fri, 09 May 2025 19:02:17 GMT  
		Size: 3.0 MB (3041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f41d31676a5d8d65d59f1e519829ec96ac69d30c17ebb1bb5451d4b7bf51fda`  
		Last Modified: Fri, 09 May 2025 19:02:17 GMT  
		Size: 38.2 KB (38205 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:64fe1a8eb3958a6f39ec6fc150e39d1c864296bee307e16355560899f213a91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530508956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da28f50c4ee492ccd60ecfac6536fc82ab38f8bc13ec4156156f09bfba08183`
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
# Tue, 06 May 2025 09:07:22 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
ENV SHELL=/bin/bash
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.build-date=2025-04-30T10:07:44.026929518Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=df116ec6455476a07daafc3ded80e2bb1a3385ed org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.1 org.opencontainers.image.created=2025-04-30T10:07:44.026929518Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=df116ec6455476a07daafc3ded80e2bb1a3385ed org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.1
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 06 May 2025 09:07:22 GMT
CMD ["eswrapper"]
# Tue, 06 May 2025 09:07:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96c7aa530755864047085f56a0d0bf33f6ac60d26e4b6a0c6c1c5277473cd7`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 7.3 MB (7348348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ccd73b90331f2503d6acf2c8abd38f951721a9b2986438f168dc79f7b224c`  
		Last Modified: Fri, 09 May 2025 19:40:44 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0a1b059f440c5121a350eb6c186c1adb70ccdfa41195f16d961b19cdecd478`  
		Last Modified: Fri, 09 May 2025 19:43:25 GMT  
		Size: 496.9 MB (496865903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715b3926f0fe345d672694f8683b3a0177e926fd8e1243ebe310719b6dd456b8`  
		Last Modified: Fri, 09 May 2025 19:43:13 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7412b14d2916606cb628f430366d7f669ac8ce01761d153672ea99a205a0f87`  
		Last Modified: Fri, 09 May 2025 19:43:13 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa7767292ac97396351e273faf93f01521c917f9a854d99573dc338d383aeb`  
		Last Modified: Fri, 09 May 2025 19:43:14 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94b7c8ba0b441368df2beeaf5fef92c888329a396db209395464167f8e2f248`  
		Last Modified: Fri, 09 May 2025 19:43:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d39d04a43d63ae58428b1acaef43be734364ddc7fddd418c6366a982390d60`  
		Last Modified: Fri, 09 May 2025 19:43:15 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:eb877d2f3b85d38342e38a6c38d844768edafd9d5e5deb90168615c19b2e76ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb0100c7053cb8b0f14eea23c8f9995a37bb2ff924e90fad64cb581a3345658`

```dockerfile
```

-	Layers:
	-	`sha256:93fcd04e1443d86e36ca6d60d7fdbea35e9062b6a9d0e638511d0737035a6ebe`  
		Last Modified: Fri, 09 May 2025 19:43:14 GMT  
		Size: 3.0 MB (3040631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3662a7f2fc112536a7adced2bda5dbd0a48867353412899fcb09b7000ff2419`  
		Last Modified: Fri, 09 May 2025 19:43:13 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.1`

```console
$ docker pull elasticsearch@sha256:577aee5810654e487ad30f84eec14b0c9789332d6d76f2ac5879eeebd3c578e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:51a542c88d9953a2487a60cd96805ac1210d5b1f2ac0100e91c3f44cfb08ca77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700141027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c859fbc6d4c968f579bf3de21dad3df363d9c9ff23e7fe88bbc67ab8b3e41`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:46:09 GMT
ENV container oci
# Mon, 28 Apr 2025 15:46:09 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Mon, 28 Apr 2025 15:46:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:46:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:46:10 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:46:10 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:46:10 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
ENV SHELL=/bin/bash
# Fri, 09 May 2025 04:49:38 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-30T10:07:41.393025990Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=73f7594ea00db50aa7e941e151a5b3985f01e364 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-30T10:07:41.393025990Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=73f7594ea00db50aa7e941e151a5b3985f01e364 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1
# Fri, 09 May 2025 04:49:38 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.1 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 09 May 2025 04:49:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 09 May 2025 04:49:38 GMT
CMD ["eswrapper"]
# Fri, 09 May 2025 04:49:38 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Mon, 28 Apr 2025 16:55:19 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0afd3e57749691096e9f36097b49ede1f43146c226a537e8a30fc17383b407`  
		Last Modified: Fri, 09 May 2025 19:01:58 GMT  
		Size: 4.3 MB (4252407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bf33719bfcfd6d1a3c3977b67b1511f5e510dc51928cee829fcae0e19c1aee`  
		Last Modified: Fri, 09 May 2025 19:01:57 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ffb6cb0100a4f4d7d22e491618f1b23c6168d1a78d0e3bca9f9e22fb2ae4eb`  
		Last Modified: Fri, 09 May 2025 19:01:57 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f6b91152f791dc98712e84b514a88ea7f6c0ea1df973579415c4884c0f0cf8`  
		Last Modified: Fri, 09 May 2025 19:02:08 GMT  
		Size: 656.1 MB (656083657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb94ff207c7906a0fd3f1815ec08146339929caf3662c61129a0cdc2028c660`  
		Last Modified: Fri, 09 May 2025 19:01:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36ff6bb9470b807d25aa1287591d9b6bd028133744ca262d51ca5cb68ec2180`  
		Last Modified: Fri, 09 May 2025 19:01:58 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54a5b6065c5b597cc5e9dfa5e102f35a9e52c5b4c019e256c43a38f86abcb2a`  
		Last Modified: Fri, 09 May 2025 19:01:59 GMT  
		Size: 75.6 KB (75622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ce2afa59cfb0a4a2576219579db7b37a7b71ab4dead3d6218a1023fae388a`  
		Last Modified: Fri, 09 May 2025 19:01:59 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:44038b75eb5ebc22474d11b791c59467fbfd133e9d5a684811b8e6747d9b9051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a57380e81ea185d3a82fb2e887e00fb1632e074429a99623bd079e7f40de835`

```dockerfile
```

-	Layers:
	-	`sha256:d2b063f6a2ecc22b75ce3b3eb3b98b517ce98b8da7cd97aefc788a094952bbe3`  
		Last Modified: Fri, 09 May 2025 19:01:58 GMT  
		Size: 2.0 MB (1972828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4dcf9e42cf57a68dab8a711969e4287cb1fead7579f81d8824989a7295e9d05`  
		Last Modified: Fri, 09 May 2025 19:01:57 GMT  
		Size: 34.0 KB (33993 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:af49f325a7e1ed7c2d063689848f7ba1f28a81485afd814feba5f4e6bde523d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538562760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d296f521b5652f7b36b74376f64301d85003b0b4908c3104dd992a23389850`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:48:53 GMT
ENV container oci
# Mon, 28 Apr 2025 15:48:53 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:48:54 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:48:54 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:48:54 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
ENV SHELL=/bin/bash
# Fri, 09 May 2025 04:49:38 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-30T10:07:41.393025990Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=73f7594ea00db50aa7e941e151a5b3985f01e364 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-30T10:07:41.393025990Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=73f7594ea00db50aa7e941e151a5b3985f01e364 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1
# Fri, 09 May 2025 04:49:38 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.1 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 09 May 2025 04:49:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 09 May 2025 04:49:38 GMT
CMD ["eswrapper"]
# Fri, 09 May 2025 04:49:38 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Mon, 28 Apr 2025 16:55:35 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a85f98284b5469b799701cca7e666da9b2c4614a6d16b6dbe4c5eb1b0241b`  
		Last Modified: Fri, 09 May 2025 19:45:35 GMT  
		Size: 4.3 MB (4266243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc8330bbe4bd69b0c22ea545b8107aa5e53ef73507077fe3c831106e8816efa`  
		Last Modified: Fri, 09 May 2025 19:45:35 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc36b1ca35a272130d9c58e395b3674de79187dfaa74d67228baad707595e20`  
		Last Modified: Fri, 09 May 2025 19:45:35 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff28aa8f6d9ac657257647ce3ed80dcc06362ed12c251bb380c88044dedbee9`  
		Last Modified: Fri, 09 May 2025 19:45:45 GMT  
		Size: 496.3 MB (496320146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b1cc5e1b4aa384bdf188371a830078c3ad69b5dce491df63f07f16bc67c3c8`  
		Last Modified: Fri, 09 May 2025 19:45:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f05db8e6c5574460d2c9a361477a9f929e5e73efd8727211c65e4d1384899f`  
		Last Modified: Fri, 09 May 2025 19:45:36 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824fb0223565b77d21f1fbc96c831fe3db8dd2c80813231a63f58ce9913f1d1`  
		Last Modified: Fri, 09 May 2025 19:45:36 GMT  
		Size: 74.5 KB (74545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c2067c13854a576127ef766aa4ba04377cb6e28243913d35f545f89d7b2272`  
		Last Modified: Fri, 09 May 2025 19:45:37 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a8ac110fb6ec61a1793f56f72595b91f9da9d60a20e1636d07a2073d01ab710b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2007390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f5c6e0a930b7c006cdcf3d77b504d08105c0b3bab009107465ccf3a5c4df48`

```dockerfile
```

-	Layers:
	-	`sha256:bf5cd1a628ecf6b9fb9dd5d9d5ee61e2d02fa45b33d0d6eba8a90501f490aa3d`  
		Last Modified: Fri, 09 May 2025 19:45:35 GMT  
		Size: 2.0 MB (1973215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a994bc2c80bf6c6f38587e5f6eb8b7933bd531b590bae75d1802824a70e6077a`  
		Last Modified: Fri, 09 May 2025 19:45:35 GMT  
		Size: 34.2 KB (34175 bytes)  
		MIME: application/vnd.in-toto+json
