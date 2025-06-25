<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.17.6`](#elasticsearch8176)
-	[`elasticsearch:8.18.2`](#elasticsearch8182)
-	[`elasticsearch:9.0.2`](#elasticsearch902)

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

## `elasticsearch:8.18.2`

```console
$ docker pull elasticsearch@sha256:d29430e894e3722b11d2aad6f1b4158d760809f643f946351490a60b6f11cbfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8ff552443a662ab291c2ac2be4c362ee0342de0ee39d7deb12afbd9aa237cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.1 MB (697119118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9410db28bec53827c5a010e8582ff393f0b52b58edea9b94c9edb203d56113a1`
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
# Thu, 29 May 2025 09:13:46 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
ENV SHELL=/bin/bash
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.build-date=2025-05-23T10:07:06.210694702Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6b8d8d951c631db715485edc1a74190cdce4189 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.2 org.opencontainers.image.created=2025-05-23T10:07:06.210694702Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6b8d8d951c631db715485edc1a74190cdce4189 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.2
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 29 May 2025 09:13:46 GMT
CMD ["eswrapper"]
# Thu, 29 May 2025 09:13:46 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f15cdcca0b78207f344181c8286badb44c813415d8ec002537782a529afb7b`  
		Last Modified: Tue, 03 Jun 2025 13:36:13 GMT  
		Size: 15.7 MB (15655564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bb4f0a3cc9feab82989f249bcd38e655874dc04c2802ec78eef2edc73b55aa`  
		Last Modified: Tue, 03 Jun 2025 13:36:11 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b07de8f19e110e0b12632887679461e5d72e4fa532a3a98f9a44be9160b35a`  
		Last Modified: Tue, 03 Jun 2025 13:36:20 GMT  
		Size: 653.6 MB (653629714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f886d34f866d9804041b60cd64784eaa1e5536c3668b91aa2ad6fab022bf81`  
		Last Modified: Tue, 03 Jun 2025 13:36:13 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b8b2730a20649bcef1d1a222a5535a395847418501c489214e8719d658f71f`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dae11d449e29a32579f8874919007e53fbab922d6d6f11d680148b08dd38f6`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 191.9 KB (191909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1a0df057e350afd70fd945a488bafc37141b64c8dda4507ae42b387dff751`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423b5ec214ba3dcda12106d4933f7e97d2557248f9ec674cd388a449dd8608a3`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f5b862fb90bdfcb263b2950f78907767c1d9dda490b2323d891f6f2139eba0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc104e43c779988c667be6477849a984e11159c12b9bc6ffc5ac91bd821944`

```dockerfile
```

-	Layers:
	-	`sha256:f54ff84b9f546d389a7f7da6dd94e7854054247cf564f8ff8ad0a11d3c688d59`  
		Last Modified: Wed, 04 Jun 2025 07:05:16 GMT  
		Size: 3.1 MB (3111838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6483f52af8a9328eeae2d5f2779ae89730df95690550d61db64e10cfb33f7c8`  
		Last Modified: Wed, 04 Jun 2025 07:05:15 GMT  
		Size: 38.2 KB (38215 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a99f84b4603a3e746d26f1432487ba4b440ba9603b387c76d0082dc56d35467c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.5 MB (537499952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2e8c920645170c64aad4b81584f3bf08677231be2d217738b2c4b6c43dfea`
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
# Thu, 29 May 2025 09:13:46 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
ENV SHELL=/bin/bash
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.build-date=2025-05-23T10:07:06.210694702Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6b8d8d951c631db715485edc1a74190cdce4189 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.2 org.opencontainers.image.created=2025-05-23T10:07:06.210694702Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6b8d8d951c631db715485edc1a74190cdce4189 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.2
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 29 May 2025 09:13:46 GMT
CMD ["eswrapper"]
# Thu, 29 May 2025 09:13:46 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff6230b8050ea64ab1e6c71eea5173ab1c32766df28363e604f74ae625c1d72`  
		Last Modified: Tue, 03 Jun 2025 13:36:00 GMT  
		Size: 14.3 MB (14333305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e078af3dd11662dcc67b8652fda8a5a564d50afee2d774baa140a824da1c3a9`  
		Last Modified: Tue, 03 Jun 2025 13:35:59 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d12ba25c6e086dbc5ae2c62b3387d5e3beefe74d1631ef22e015a9dbd37a2c`  
		Last Modified: Tue, 03 Jun 2025 13:36:12 GMT  
		Size: 496.9 MB (496871952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9bb4ad495f78a8587afa0781771c5126e9b302188056e7de8f7808936aed83`  
		Last Modified: Tue, 03 Jun 2025 13:36:00 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe8a78f5102272c2ce04f370f9cbce5cf6522c6bf7e5247c01cd6b73383f119`  
		Last Modified: Tue, 03 Jun 2025 13:36:03 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b87e6b181a154860c3f9317ab82618006399f948a1c3807c738bc8f47233632`  
		Last Modified: Tue, 03 Jun 2025 13:36:03 GMT  
		Size: 185.9 KB (185920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b252d1ff1ef70de0bd74dda01d09abb22bc7c88ede94b8a0548c9e450fdcf402`  
		Last Modified: Tue, 03 Jun 2025 13:36:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c944b2ce209547630c541c21d2323abb7c1ff397d2356cdf3dcd9001f7db630`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:bc306eb3a1887fbd7897b2ed3b9218e3fe142f7905ae3bf854a68091d53f3d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50d4ff72542ce7f260addae82e68cd92c7af0c798a0220eb2f8ce22dd61cc5a`

```dockerfile
```

-	Layers:
	-	`sha256:58c5d3a441f45c50918e2b8da03cd0549366d7df8ef0a36980485e6496adaa5f`  
		Last Modified: Wed, 04 Jun 2025 07:05:16 GMT  
		Size: 3.1 MB (3111439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046432bf7c16d3d8dbee16a0309f236b33988961ddd8ab22b79a4e374353c4c4`  
		Last Modified: Wed, 04 Jun 2025 07:05:15 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.2`

```console
$ docker pull elasticsearch@sha256:bfa9d2126a5c3381ac272ee67264083ca04318def1d7b4ea9194ad0b0a8959bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2f19efcc30a4b9528c24ed489fe1b779f7078fcb184d475da5e7de25fbe5f2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700129731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326d884a38b184545bf2f56f1adb867c6af919691afe604da9f786c2c6e9ac6e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
ENV SHELL=/bin/bash
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-28T10:06:37.834829258Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0a58bc1dc7a4ae5412db66624aab968370bd44ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-28T10:06:37.834829258Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0a58bc1dc7a4ae5412db66624aab968370bd44ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Jun 2025 06:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["eswrapper"]
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddcc68fa4871a337363423d3b1f9c0a89cedd56053145fba4ee49ff5b2242cc`  
		Last Modified: Wed, 25 Jun 2025 17:56:01 GMT  
		Size: 4.3 MB (4285777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c87d3fe0ed3f8a22d068d9c2b5c9f33fde385ff68f995e192aa59448e24dd3`  
		Last Modified: Wed, 25 Jun 2025 17:56:01 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0138bfac1ee5223bfdad7bc7c6c3ef6ddeeb2eb183804040f35305b7c8e562`  
		Last Modified: Wed, 25 Jun 2025 17:56:01 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0be819af107baef84dc5187ea64954db8e5a5c0463cfe0748388e62134b191`  
		Last Modified: Wed, 25 Jun 2025 18:26:02 GMT  
		Size: 656.1 MB (656102751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f0c487b2ff8cac06ca35961c32510b60981836ebc557d08b9a0a90d3d02d25`  
		Last Modified: Wed, 25 Jun 2025 17:56:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa8bfd201e591fc0ab83e660e0900f7687c13175e777f50d3dfdba821fca67f`  
		Last Modified: Wed, 25 Jun 2025 17:56:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c49da919b3b1975f148fb7e3a14768867bccef32209577b0d3547e4e995504`  
		Last Modified: Wed, 25 Jun 2025 17:56:02 GMT  
		Size: 75.7 KB (75747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44dc1a977e44a6ec182eb13d03fe5c073760f2a0e3cc566424b9c1684f625`  
		Last Modified: Wed, 25 Jun 2025 17:56:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fab8702cd2a1f6b01eac69cac4f73c37806a5f55c1f22f235e19cc11b8685889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df1ebff65f922789359da8a71981c2f682882d7eedafe56f3b3ae060fa83f5b`

```dockerfile
```

-	Layers:
	-	`sha256:a5985e960d83746c8a5cc67f2e63934809a2547861debd10358bf2007ce8a20e`  
		Last Modified: Wed, 25 Jun 2025 18:25:20 GMT  
		Size: 2.0 MB (2033741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ec053d8134bf996c3fc7201ac571f9a896a03af2876bccb0342c64f829fd5b`  
		Last Modified: Wed, 25 Jun 2025 18:25:21 GMT  
		Size: 34.0 KB (33985 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:eb0f18a29d158a7e20cb23a9334f432d259556a765850b3093790693bfacfa10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538595143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadb6fc0bfc4cecacb6c51e67ed5e0b49d24c83b089db02d50bebfb39a0e90d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:837c51d2245269e7540005032254a14f4d0618334b5c45ecacf5b0c7968d0657 in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-24T16:36:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
ENV SHELL=/bin/bash
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-28T10:06:37.834829258Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0a58bc1dc7a4ae5412db66624aab968370bd44ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-28T10:06:37.834829258Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0a58bc1dc7a4ae5412db66624aab968370bd44ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Jun 2025 06:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["eswrapper"]
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ba92c2079b2b21a2f178ace5ca98b5ef2d5cd02901c30e48729b7afe34ecd27e`  
		Last Modified: Tue, 24 Jun 2025 18:09:22 GMT  
		Size: 37.9 MB (37864307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55461445230f402a74e4424d8b22b60a43c66f7dd2da16f9d282df92834c32a7`  
		Last Modified: Wed, 25 Jun 2025 19:34:20 GMT  
		Size: 4.3 MB (4297172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04db52cda08459751af50b8d9747851a602a8b9a63bd9cef4ecddc7aed506f8`  
		Last Modified: Wed, 25 Jun 2025 19:34:30 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8212e916e75c1cc40a1da75639d5e8c3b90b634724d204ca176486f7dfa2748`  
		Last Modified: Wed, 25 Jun 2025 19:34:34 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac7db66450218ff56934f58e5ae46bbbddd4cc844ba040dd19fb4629284cc8`  
		Last Modified: Wed, 25 Jun 2025 22:05:44 GMT  
		Size: 496.3 MB (496344666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd79f82b3ea5ceeb3e95d9e38b1c5e7fc326c728b62780c736a5a7aa9fe706`  
		Last Modified: Wed, 25 Jun 2025 19:34:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987c68a9d57713c874beef210be0aaeb6019b676adcd48791c43227d2f9f833f`  
		Last Modified: Wed, 25 Jun 2025 19:34:41 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfc8fe24b1258468a4173e8fc0edcc63b4629575a39b7e4963fd35f1d722375`  
		Last Modified: Wed, 25 Jun 2025 19:34:43 GMT  
		Size: 74.6 KB (74643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561c231ad2193037e519aa6006c98dff469de13d3e66b50894c518cbfce79cdb`  
		Last Modified: Wed, 25 Jun 2025 19:34:49 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:89d26ea4ebce2f440c91d13c774d6d22cb4819cbfad7f6ff7e2514e4d11f29a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f653d39778e4306a711c2662925d1ca41fb3efb9afd90f3b072051f1e655fa12`

```dockerfile
```

-	Layers:
	-	`sha256:84e14a86596fc37569670e49f2e9f18bf68535b3943409347426bfac1f0e5e18`  
		Last Modified: Wed, 25 Jun 2025 21:25:26 GMT  
		Size: 2.0 MB (2034305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5971d80c1ddd98ea0be7f0489f87dd71b1b87d90b73332b4754e0a218b3543`  
		Last Modified: Wed, 25 Jun 2025 21:25:26 GMT  
		Size: 34.2 KB (34167 bytes)  
		MIME: application/vnd.in-toto+json
