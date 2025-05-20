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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8ae3c5cac1d89fe2a44334f31182007f12dfa91fee6939fc84c697ecfbf44`  
		Last Modified: Fri, 09 May 2025 19:03:13 GMT  
		Size: 7.5 MB (7525348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1945e0913748aa4a768b41c493413d3a5b031e90989814973a8e383d70de3f`  
		Last Modified: Fri, 09 May 2025 19:03:12 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f079048605e2e8cc51708456624115967f034a4355cbdea95f74b394c75a052`  
		Last Modified: Thu, 15 May 2025 20:03:11 GMT  
		Size: 642.2 MB (642206265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5bd73c78959bdefdd779389e572380601e1f653832970d6d3327ae1ca472a7`  
		Last Modified: Fri, 09 May 2025 19:03:12 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5219c57f40893073a3db8ee5a3864a24c7c460a496e978c4e3e3911a958f92c9`  
		Last Modified: Fri, 09 May 2025 19:03:13 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ca91ba1bc455fc5ec0bea47872b394324286d39b2cf4502b2d0198d9ac267`  
		Last Modified: Fri, 09 May 2025 19:03:13 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5812fe584da1f3063e75de3ba86000e5dc08abb23cd6a6305533889f4bfa55`  
		Last Modified: Fri, 09 May 2025 19:03:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba55862467553f5871d6fa25d9285cf0d41abffdf298d52ac70e290e141d387`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
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
		Last Modified: Sun, 18 May 2025 10:08:08 GMT  
		Size: 3.0 MB (3008901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5eb3eb0e8d51ceede2825b497f4180da62852f23685e4c002495f7f56f9cb29`  
		Last Modified: Sun, 18 May 2025 10:08:08 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96c7aa530755864047085f56a0d0bf33f6ac60d26e4b6a0c6c1c5277473cd7`  
		Last Modified: Thu, 15 May 2025 19:26:25 GMT  
		Size: 7.3 MB (7348348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ccd73b90331f2503d6acf2c8abd38f951721a9b2986438f168dc79f7b224c`  
		Last Modified: Thu, 15 May 2025 19:26:23 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9910f25fa76b3aeefab98f6f01004348a878cb8be740506854c2934362346f2`  
		Last Modified: Fri, 16 May 2025 20:04:25 GMT  
		Size: 487.3 MB (487266725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ededf7d50f55d98616d5e0474638be3a2ffa81e2c4c385c3b02f66f49d0265`  
		Last Modified: Fri, 16 May 2025 20:04:04 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54696eb5d394bebfdab641ced910c8efd44dbcd384a20b7ed59e5c2d410efec0`  
		Last Modified: Fri, 16 May 2025 20:04:10 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f5ee50c5341e2e708d74d848343ae9427906b1301a3ee7ade4e413a7ea010`  
		Last Modified: Fri, 16 May 2025 20:04:14 GMT  
		Size: 185.9 KB (185919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968ff2239fd83a5d802cfeb2d3bf3905e042d4bc48b01d94015cbe255daa0d11`  
		Last Modified: Fri, 16 May 2025 20:04:23 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f318f5fe6ad94ccb0094fc6ec9b9aff9d0b03589453f86a05666717d9bcc973a`  
		Last Modified: Fri, 16 May 2025 20:04:14 GMT  
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
		Last Modified: Sun, 18 May 2025 10:08:54 GMT  
		Size: 3.0 MB (3007873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50a898c60bdae2c2f50a290b90eabaf59ad993d3a71e3617d8a071bfa73b81b`  
		Last Modified: Sun, 18 May 2025 10:08:54 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85826ade9bfb20b4b35c572423dcaed6ceb2e4e4fd1129ea76c5041d578d2d7`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
		Size: 7.5 MB (7525309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f1daf49c01159cdaed3a2700f6c145a51310b1dc37bb0bc57c72fec14f456`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddb586cd26e993f01c2aaded849647b2e0589619ec5b0bbde3f8eda2add44ef`  
		Last Modified: Thu, 15 May 2025 19:26:37 GMT  
		Size: 653.6 MB (653624253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91c46a806bbf85fdf6a123651ebbe8a6eab870d8380f01060ee1d9e8314f61c`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109917bbabf2296182ace30b848e5d72bf1617a9692a3358a8247c593b1a582e`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398d841fe8ab203b8b73ada2cf819d11c044ef34cea822b1492ddd8ac5f2dc72`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 191.9 KB (191908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6639a79e01e23e13d73ef3493936f0eb1e7a917b0ee5e020ced4bcec567a753f`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ceb2e4b74f0327e5678c42d3648ee67bbb65b69c570e9b4802bb51498ba4b7`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
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
		Last Modified: Sat, 17 May 2025 00:00:48 GMT  
		Size: 3.0 MB (3041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f41d31676a5d8d65d59f1e519829ec96ac69d30c17ebb1bb5451d4b7bf51fda`  
		Last Modified: Sat, 17 May 2025 00:00:50 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96c7aa530755864047085f56a0d0bf33f6ac60d26e4b6a0c6c1c5277473cd7`  
		Last Modified: Thu, 15 May 2025 19:26:25 GMT  
		Size: 7.3 MB (7348348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ccd73b90331f2503d6acf2c8abd38f951721a9b2986438f168dc79f7b224c`  
		Last Modified: Thu, 15 May 2025 19:26:23 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0a1b059f440c5121a350eb6c186c1adb70ccdfa41195f16d961b19cdecd478`  
		Last Modified: Thu, 15 May 2025 19:27:20 GMT  
		Size: 496.9 MB (496865903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715b3926f0fe345d672694f8683b3a0177e926fd8e1243ebe310719b6dd456b8`  
		Last Modified: Thu, 15 May 2025 19:26:23 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7412b14d2916606cb628f430366d7f669ac8ce01761d153672ea99a205a0f87`  
		Last Modified: Thu, 15 May 2025 19:26:22 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa7767292ac97396351e273faf93f01521c917f9a854d99573dc338d383aeb`  
		Last Modified: Thu, 15 May 2025 19:26:22 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94b7c8ba0b441368df2beeaf5fef92c888329a396db209395464167f8e2f248`  
		Last Modified: Thu, 15 May 2025 19:26:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d39d04a43d63ae58428b1acaef43be734364ddc7fddd418c6366a982390d60`  
		Last Modified: Thu, 15 May 2025 19:26:22 GMT  
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
		Last Modified: Tue, 20 May 2025 09:00:35 GMT  
		Size: 3.0 MB (3040631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3662a7f2fc112536a7adced2bda5dbd0a48867353412899fcb09b7000ff2419`  
		Last Modified: Tue, 20 May 2025 09:00:36 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.1`

```console
$ docker pull elasticsearch@sha256:26abc2782ee790b76df4e0806ea492967d14bcddb8c58e0eb3cc8593b363ad6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8d786e9a57c1b4c47b20cb9161049d36db9ad683cc162348e42fb8add80a8507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700106793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c01a901c116d47490a6cd16c4cad2d3a09068af3da6bac9155ee0a6b70c831`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 09 May 2025 04:49:38 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL url="https://www.redhat.com"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 09 May 2025 04:49:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 09 May 2025 04:49:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.expose-services=""
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 09 May 2025 04:49:38 GMT
ENV container oci
# Fri, 09 May 2025 04:49:38 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Fri, 09 May 2025 04:49:38 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 04:49:38 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 09 May 2025 04:49:38 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8c556fe7e59edf464cca43d352d7c75ba33260563892e0cbaac0efd5ba7d2f`  
		Last Modified: Thu, 15 May 2025 19:26:10 GMT  
		Size: 4.3 MB (4287348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270b13109362bd4cdabc6ea65f165d9cba4ad03ddde32ea9de4b53a31a67eea5`  
		Last Modified: Thu, 15 May 2025 19:26:09 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab154f1f83de38e6058efd3498211bd4dc1ba5f14e39b6dacfe10ac156ced76`  
		Last Modified: Thu, 15 May 2025 19:26:09 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df2f015d50c01467e0cfef1a78813c1b31e893cf5057614846da93cbd25065`  
		Last Modified: Thu, 15 May 2025 19:26:38 GMT  
		Size: 656.1 MB (656083811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89831975df1b872568ba296bd2ae8a62fae3cee57db050e665382a27d18497`  
		Last Modified: Thu, 15 May 2025 19:26:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f367eab7f0335e39b64736f0088ffa9d019368e654b5bfb6177033d8c14c7906`  
		Last Modified: Thu, 15 May 2025 19:26:09 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea6de84745c446495be386c9db90636807214c7db186793ae83c5bcb49af2f`  
		Last Modified: Thu, 15 May 2025 19:26:10 GMT  
		Size: 75.7 KB (75748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67acf6b596006e7d88a7691e74a93d87fdefe4be6fca9e6b4b12f21653e78e3`  
		Last Modified: Thu, 15 May 2025 19:26:10 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:72bf690040375bba035d491d02a32f796b9b2bff0f4be4ca98fde42953a641ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c9dd31a87b0497a82341d40c0ae02007f0daa6e28fdcf6aa8282c31da8b0a9`

```dockerfile
```

-	Layers:
	-	`sha256:7b95b767d86d2de93b50fc0f28cf030beff0f00499daa6c4b2dd55635c2ce4c2`  
		Last Modified: Mon, 19 May 2025 11:06:08 GMT  
		Size: 2.0 MB (2033713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c727007712893159d2f26554e6306acf78fb07848b6f3c545f289bcfe69581c`  
		Last Modified: Mon, 19 May 2025 11:06:08 GMT  
		Size: 34.0 KB (33993 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:f7bea80d8b2c80faf7fcffd0a4743c507b0609a4983e666982db1ff0a3eb364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538582283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45962087868ffb0686f99837f7733a761f18a25311e34800d584864ccbad3bad`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 09 May 2025 04:49:38 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL url="https://www.redhat.com"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 09 May 2025 04:49:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 09 May 2025 04:49:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.expose-services=""
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 09 May 2025 04:49:38 GMT
ENV container oci
# Fri, 09 May 2025 04:49:38 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Fri, 09 May 2025 04:49:38 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 04:49:38 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 09 May 2025 04:49:38 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:9cf99093c2fb01ee3da769d664a9212c42b7d50516f9e77975132a6540ccdf3b`  
		Last Modified: Thu, 15 May 2025 19:25:04 GMT  
		Size: 37.9 MB (37876105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7b0a24b11ad46596848a5597f824844ad203913ea92b8c35fe71d8c2443c4`  
		Last Modified: Thu, 15 May 2025 19:36:37 GMT  
		Size: 4.3 MB (4297093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ee780803b2d3b3e4e54221ca3f0a3f686113633a3d2f95389099bf0b76c036`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de1ad9cd829afa46315b0aadbf549a8020c6d70365cb039f8e4c0766b1195b`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43940b5fb3f6e717b878d2f7d58e5fce0495d2815594d474fcad76d54492a9c`  
		Last Modified: Thu, 15 May 2025 19:36:45 GMT  
		Size: 496.3 MB (496320081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448425aa56b19c848464c81f7f04dfda9499e7cbb832fe287dc1ccc6f09f366`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ccca7ed104bd434cf421d7d6c725c0c354a5a02c4ede04196aa9575b59b10`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a48d2da5b2f4351c4a721532d3cb9bbb177779ea5ce78898ab67eb7358847`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 74.6 KB (74645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2b6860083cf18f27829161d9d212fe11453ba5ffb752637fb74e1be975a8ad`  
		Last Modified: Thu, 15 May 2025 19:36:28 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4b1d02908abe57bc5df9eaf163b8f8d662527ff8fc7a96fecb9d6d2199b82b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed00f3088c018074b9f84a8ed3b851c3ab4711c3106d76f001698a1eacbf29af`

```dockerfile
```

-	Layers:
	-	`sha256:fe68af109be008ffedca1ccb9c5411f75379b3039553ff7d34aa4dec3c72f855`  
		Last Modified: Mon, 19 May 2025 11:06:08 GMT  
		Size: 2.0 MB (2034277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a96965e30bf1747799aa6317314d01407807ef4a65625924ed3d78c5a473f03`  
		Last Modified: Mon, 19 May 2025 11:06:07 GMT  
		Size: 34.2 KB (34175 bytes)  
		MIME: application/vnd.in-toto+json
