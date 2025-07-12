<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.17.8`](#elasticsearch8178)
-	[`elasticsearch:8.18.3`](#elasticsearch8183)
-	[`elasticsearch:9.0.3`](#elasticsearch903)

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

## `elasticsearch:8.17.8`

```console
$ docker pull elasticsearch@sha256:d5b040e9dd37a2cb1cfc8c7f6cc31194989bf6e0d84ea52f23dd061bc7e4fb66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b242a482015c694bd2e63fd1bc57b4fec28ccb31839502c2b43ef323c6e9ccec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.5 MB (678452417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea96d4ac9c6068ac17301a7a1dec55c03a2d4a6a6ee8b0b417ce7e846944772a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:55:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:55:56 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 09 Jul 2025 09:55:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:55:56 GMT
ENV SHELL=/bin/bash
# Wed, 09 Jul 2025 09:55:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 09 Jul 2025 09:55:56 GMT
LABEL org.label-schema.build-date=2025-06-18T22:06:50.825208715Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=03c9f64f104b1d5272d2ff2a8d8937441edd1cac org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.8 org.opencontainers.image.created=2025-06-18T22:06:50.825208715Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=03c9f64f104b1d5272d2ff2a8d8937441edd1cac org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.8
# Wed, 09 Jul 2025 09:55:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 09:55:56 GMT
CMD ["eswrapper"]
# Wed, 09 Jul 2025 09:55:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aab7dbe6df2193627e47e35b81466bd4cacdfeff32258fd8b9ff1b13f00c56`  
		Last Modified: Thu, 10 Jul 2025 21:47:02 GMT  
		Size: 6.2 MB (6245932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7991461a260f465d81ed1e5af2bb543aabb3ee4a86d796a5f925bdee8674171`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11678d2222cd6346452074c6afb4fa1032bac5954790319ce2c1a9f34134f6cc`  
		Last Modified: Thu, 10 Jul 2025 23:01:08 GMT  
		Size: 642.2 MB (642193423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4621048e75b236b9c31f023fecf616aaa318980bda5ac3b29086b742507f8`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4a70787ed9048600d4a09a71f12b5bcb4e0ab2aed3df98d66d83c3fe59f03d`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5c9cf36dbbf27b56f7515c71f62a7d33dc49b0964b5daedaedadb8612febd`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 163.9 KB (163943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56746dc6e8daf93b10208e6025dffd78887e84f76b072a9e91623df83a7572e`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcea86766877a36576242fc1612cc250e6d6e88d6592afb8b1e9b8b82fbe6105`  
		Last Modified: Thu, 10 Jul 2025 21:47:01 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8ea1553b044baa85e50e8414ab483cfacec31a025133eec69d07f06add84e083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73fb107c633f53a458f2796ac54cb6ad72dab0385c0bc15a6062fc453ad803c`

```dockerfile
```

-	Layers:
	-	`sha256:02e757dfb393bc1c7f273ac435b04a308dcaa0a159ef9d0cf5f79e075b1567b1`  
		Last Modified: Thu, 10 Jul 2025 23:00:50 GMT  
		Size: 3.2 MB (3164306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59acb0b1b604ef9e2e0be76243bb432bbe4ac247576ed176d895ee08e497a25e`  
		Last Modified: Thu, 10 Jul 2025 23:00:52 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:f0732d0e3d8239fc331d675f33f1d91fcf9e75ab38eb5cecac6b71dae67e190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.7 MB (522720119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbcfd0bfa557e17c42d438b4f53065db0f740f49928a3f31e70ffe804385184`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:55:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:55:56 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 09 Jul 2025 09:55:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:55:56 GMT
ENV SHELL=/bin/bash
# Wed, 09 Jul 2025 09:55:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 09 Jul 2025 09:55:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 09 Jul 2025 09:55:56 GMT
LABEL org.label-schema.build-date=2025-06-18T22:06:50.825208715Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=03c9f64f104b1d5272d2ff2a8d8937441edd1cac org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.8 org.opencontainers.image.created=2025-06-18T22:06:50.825208715Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=03c9f64f104b1d5272d2ff2a8d8937441edd1cac org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.8
# Wed, 09 Jul 2025 09:55:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 09:55:56 GMT
CMD ["eswrapper"]
# Wed, 09 Jul 2025 09:55:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac768303f4403ea72c9d7a2a2cdbd6915ab7d56f2850ef7bb036239342569c4d`  
		Last Modified: Thu, 10 Jul 2025 21:47:27 GMT  
		Size: 6.3 MB (6313645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396af4f9ef69412777d05576b25260408c795176ef8adfc0570454a4f7293a8f`  
		Last Modified: Thu, 10 Jul 2025 21:47:26 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecbba22f2707185613f2c7c3b588118376ed065688b8a494d1d0601a1072a1e`  
		Last Modified: Fri, 11 Jul 2025 00:44:55 GMT  
		Size: 487.3 MB (487259766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73795d1ab8ae35bea53d36a3e3b53af51abfa698d1ef4a4cf9f6393c1c0210aa`  
		Last Modified: Thu, 10 Jul 2025 21:47:27 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd337220b91524f05600d6dedfabbe8e2bc51125a1fcb16a3ec03671fff05373`  
		Last Modified: Thu, 10 Jul 2025 21:47:26 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bc2eded147df5e63929bf5e2477f6070eec8390ae43996e0ab722ae3750cde`  
		Last Modified: Thu, 10 Jul 2025 21:47:27 GMT  
		Size: 160.4 KB (160366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dc587c67a563abc7c1d0b7000efb882b89bf32e35473bae9115ac466260382`  
		Last Modified: Thu, 10 Jul 2025 21:47:26 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f62f3e031f0d631557852b665e098e5e5d758a028ff1d367d053f953007920`  
		Last Modified: Thu, 10 Jul 2025 21:47:26 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d5827df03ae7622cbb37d92b2dc221f6e3d69f0717a71023eab99860a0066a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d514e765b41dd54d9dad6436c04053a62a237e19ca025267cd57d369b0f38ba`

```dockerfile
```

-	Layers:
	-	`sha256:1b1144c10474503f2a817313098eab50b24373091d05d82e9a5fa1a289927a3d`  
		Last Modified: Fri, 11 Jul 2025 00:25:27 GMT  
		Size: 3.2 MB (3164090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692db5d39997bfce507120393d02270aa1f3a10c700f68760bc8b05cadbb613f`  
		Last Modified: Fri, 11 Jul 2025 00:25:28 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.3`

```console
$ docker pull elasticsearch@sha256:7fd163ed298bd2cfd5bb28d54edae7e8d0355ebe8ee08d5e722c8b2b40f19073
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:394801d62be53d607f67b4a77513775d7203e24ad8c839c6ff7ad48d69cc2975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.9 MB (689921166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a002d8541582535db8b3e26f1fd71c95ba452b228661e14781da62ca36722e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 10:05:53 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 10:05:53 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 10:05:53 GMT
ENV SHELL=/bin/bash
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 24 Jun 2025 10:05:53 GMT
LABEL org.label-schema.build-date=2025-06-18T22:08:41.171261054Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=28fc77664903e7de48ba5632e5d8bfeb5e3ed39c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.3 org.opencontainers.image.created=2025-06-18T22:08:41.171261054Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=28fc77664903e7de48ba5632e5d8bfeb5e3ed39c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.3
# Tue, 24 Jun 2025 10:05:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 10:05:53 GMT
CMD ["eswrapper"]
# Tue, 24 Jun 2025 10:05:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955df9bc51d88bb2d53bb949168f432c7bbdef281a8a8539fc94992bc2fde218`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 6.2 MB (6245962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d62dc78a51b56cc79ce1b74f579a62feb52ada374ca3bf483b1eadc94425ea`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 3.5 KB (3538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ab0f540834f0b5d6390a1b06e340d842ea5787fa7fcc3c2317c186ce71f3e8`  
		Last Modified: Thu, 10 Jul 2025 23:01:25 GMT  
		Size: 653.7 MB (653662129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e38155b08e7a98c1f266abff398bffe53fc27b3a7fe57b60308f54bec0ceccb`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d1c3977941be486f4bb585c3e71497fdc767b3292a00c97fcfda82d3ffac97`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0639186a10d6166a3f5533decbad81e40ea4d3d633acc06b086d305334b1562`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 163.9 KB (163942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1b6b81ce8043b6ba3d1176a0c54821918b7df0074f4c1827e02027d5ca0c0`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb370706678f1a07c4faa612cfd60d5b841dc791ab2043fff0d2015b3abae9c`  
		Last Modified: Thu, 10 Jul 2025 21:47:05 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:22ff1acd45575210428aa72f69f29f35e3aaa8d70d1cfa608910e7ab7621b79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f14649c9937a6eb7e557adf7627aaf50c15964cbbe5f8ff71d1d5f896ac7a45`

```dockerfile
```

-	Layers:
	-	`sha256:603ac51d97408bfe6d63f3ed22d5fec7c21ad846913497e133da28b39c73d408`  
		Last Modified: Thu, 10 Jul 2025 23:01:31 GMT  
		Size: 3.2 MB (3197480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428f771a8a2c782bb7b651cd90b7d7c4c507cc2b272835cf33d5d592446b0b19`  
		Last Modified: Thu, 10 Jul 2025 23:01:33 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4c60d136fc07742ada741f33660f8b19092772d22864b4f68d491c8e5f243998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532357801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853b7fd0572a774e58b30f27ec318547168dae3bacd685c5b564613559d2c66`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 10:05:53 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 10:05:53 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 10:05:53 GMT
ENV SHELL=/bin/bash
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 24 Jun 2025 10:05:53 GMT
LABEL org.label-schema.build-date=2025-06-18T22:08:41.171261054Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=28fc77664903e7de48ba5632e5d8bfeb5e3ed39c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.3 org.opencontainers.image.created=2025-06-18T22:08:41.171261054Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=28fc77664903e7de48ba5632e5d8bfeb5e3ed39c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.3
# Tue, 24 Jun 2025 10:05:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 10:05:53 GMT
CMD ["eswrapper"]
# Tue, 24 Jun 2025 10:05:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac768303f4403ea72c9d7a2a2cdbd6915ab7d56f2850ef7bb036239342569c4d`  
		Last Modified: Thu, 10 Jul 2025 21:47:27 GMT  
		Size: 6.3 MB (6313645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396af4f9ef69412777d05576b25260408c795176ef8adfc0570454a4f7293a8f`  
		Last Modified: Thu, 10 Jul 2025 21:47:26 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f9cee0e73c04afa4d98c9eaed954a35e1476b754828e4fbb193409b18b0539`  
		Last Modified: Fri, 11 Jul 2025 00:41:48 GMT  
		Size: 496.9 MB (496897448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff1cbcb44e6475728f68594069e37e8f0ae39c12cb3e844ae90128c7273e18`  
		Last Modified: Thu, 10 Jul 2025 21:49:32 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b569dcf3da6adc3540952502dbe756b920d941804fd89a1abaffb317f41ad`  
		Last Modified: Thu, 10 Jul 2025 21:49:32 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79b427c96b97c5366ad4bc8d016f72c46da1cb05429b45c3543fa0976b49107`  
		Last Modified: Thu, 10 Jul 2025 21:49:32 GMT  
		Size: 160.4 KB (160367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9176580642918f74b3a2307b00946686ef6e8bb9bc9da525c2a6553ec9ebf3`  
		Last Modified: Thu, 10 Jul 2025 21:49:32 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8b5ca991458de1254f14c2722c4ef9b6315c4be04df8702f05ba4f058c019`  
		Last Modified: Thu, 10 Jul 2025 21:49:32 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:516ed5e6dd37b444a394eded5996c28f4bb7491c551d5ea1295a7dd6bca4a7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9da4f2a653c53c0a66433c04f766489e4faaa83d27001032a87389999e9a0d`

```dockerfile
```

-	Layers:
	-	`sha256:9ca369329bcc9a3eefa28944d954454f50a37ebdef0adccb070242b24460397a`  
		Last Modified: Fri, 11 Jul 2025 00:25:36 GMT  
		Size: 3.2 MB (3197893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8573148cc8ecbb62cec84df9b8f7b850bfd113b7bc4ace56cdfee877bcfee2`  
		Last Modified: Fri, 11 Jul 2025 00:25:37 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.3`

```console
$ docker pull elasticsearch@sha256:e4b214ead12e1e54608c1640fff68e7e5365ca5d6a10c6d798b5476f468e5cc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e62193ea1928f2f34d68c1e5bd46647b21cc4d100fcf116ed2d0b7bfc25c618c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.2 MB (700213290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe48a936229411d32caf5b3f386fe35fc6cdee707e49cf924011179ba9839d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL url="https://www.redhat.com"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 24 Jun 2025 11:03:26 GMT
ENV container oci
# Tue, 24 Jun 2025 11:03:26 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Tue, 24 Jun 2025 11:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 11:03:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 11:03:26 GMT
ENV SHELL=/bin/bash
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL org.label-schema.build-date=2025-06-18T22:09:56.772581489Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cc7302afc8499e83262ba2ceaa96451681f0609d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-18T22:09:56.772581489Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cc7302afc8499e83262ba2ceaa96451681f0609d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 24 Jun 2025 11:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["eswrapper"]
# Tue, 24 Jun 2025 11:03:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c61fe4b936685342896f6ebfc544d5915fa2f487b2a33d2d837dae0e24ea7`  
		Last Modified: Fri, 11 Jul 2025 23:34:50 GMT  
		Size: 4.3 MB (4285503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc7794430c74092dff0b178df6cffeb6b40a9f5259f82b9723c75036a309d54`  
		Last Modified: Fri, 11 Jul 2025 23:34:47 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8eb5497bd784ff9094e5825e6ad46a043630b648e1ff57ee4afe73447f3fce4`  
		Last Modified: Fri, 11 Jul 2025 23:34:48 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc4ec39a377998d3b7feb07f498c3f28d4f6fa5f0b730babcf290f2f309f14`  
		Last Modified: Sat, 12 Jul 2025 00:34:37 GMT  
		Size: 656.2 MB (656180473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4b68785a76e7a75446916db056a4744bd10457296d198cd59aa720c129fe7b`  
		Last Modified: Fri, 11 Jul 2025 23:34:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b38dcabddb911bcbfc705ab22dd589b04b3c89dc5329487d8ba8376d7e6ea`  
		Last Modified: Fri, 11 Jul 2025 23:34:50 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dfe24a6209288dc4790bd1f1f4a2033c5948bb88726b6d966b4c49ace2c89d`  
		Last Modified: Fri, 11 Jul 2025 23:34:51 GMT  
		Size: 75.7 KB (75749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b029adfbc3dc1281ef77ae24a43b5695fc90bbe674e8627a430eec754c15dbe`  
		Last Modified: Fri, 11 Jul 2025 23:34:51 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2db1375bd6bd6e937420ca671872cc3554709321680246e4b5c7a8a6d4138216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79801c3a91efaa3c3ca63f8912d908e1f40be4147a4f05a103e2dcb44924505a`

```dockerfile
```

-	Layers:
	-	`sha256:976f5af2125be31f5dd276fa8c4ce9d4972ffba98a9292eeb89ec3b67ee4d9d4`  
		Last Modified: Sat, 12 Jul 2025 00:25:22 GMT  
		Size: 2.0 MB (2033743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11de41d5755f1cc0473332f9a7724ab5190ba5c0a0baec3617098cea76c75c09`  
		Last Modified: Sat, 12 Jul 2025 00:25:23 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2779f59634be95323b3d8fe87ca07f6f695241defee85b492df247d791326816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.7 MB (538681082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f8289871f646e0ac1bb1bba8ce64f79b863ce91fe776aad82ebec576179830`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL url="https://www.redhat.com"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 24 Jun 2025 11:03:26 GMT
ENV container oci
# Tue, 24 Jun 2025 11:03:26 GMT
COPY dir:b783331d27fd913eeb2432850fad52ee030371aaa92d5026fe285216c5bf07a4 in /    
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL "build-date"="2025-07-09T14:10:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Tue, 24 Jun 2025 11:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 11:03:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 11:03:26 GMT
ENV SHELL=/bin/bash
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL org.label-schema.build-date=2025-06-18T22:09:56.772581489Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cc7302afc8499e83262ba2ceaa96451681f0609d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-18T22:09:56.772581489Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cc7302afc8499e83262ba2ceaa96451681f0609d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 24 Jun 2025 11:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["eswrapper"]
# Tue, 24 Jun 2025 11:03:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20903621eaed1da24bbd033a1782d897d15ed92cf3430cd60e3ec0cda4a1bb69`  
		Last Modified: Thu, 10 Jul 2025 01:38:24 GMT  
		Size: 37.9 MB (37863034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2d359712b856ab702b5ad493484779ed3958a1d92bad666d85781dd9849a2f`  
		Last Modified: Fri, 11 Jul 2025 23:45:48 GMT  
		Size: 4.3 MB (4298306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb98f52640850967eb6f7d191b785f70cdeb616e00a3bfe0f08a66c3a250aef`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4566d901a71c78788698f861ac4017f2debe75f052e090c0a2fd08d87763673`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e373243299ff11aea3919bab19108046a2f804f2e3fef6afeef8012348ca8873`  
		Last Modified: Sat, 12 Jul 2025 04:03:35 GMT  
		Size: 496.4 MB (496430746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0177b93523eab5b51f59acf62526bb125a04e411b757238a786863659936bb0`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dced3e90f2f850e286948cbf9335f7ba328c0f79ac982e48144173700d6253`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2726c1e0f52a7ab9848d9d543a9968d7bf64719e9b75276eb00f91c06b8f5a`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 74.6 KB (74645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc011d7681430ed4b49817633fefb0595fcfc6ea8b0c5fb093a6f69908ee05e6`  
		Last Modified: Fri, 11 Jul 2025 23:45:47 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2d95b540088474d509cd45d56da5e7e6826b14ebbf2048e27ee79e07479cc411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b9fb400c0b7602ae6ec1f9aed1256655dd23d4557c411b4b6d3368ef054e21`

```dockerfile
```

-	Layers:
	-	`sha256:06cc3d8240008bd7e84b6067aaefa7860fccc210443e4bb2cbb660c16aa9d46b`  
		Last Modified: Sat, 12 Jul 2025 00:25:27 GMT  
		Size: 2.0 MB (2034307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c661ea6c83b75543b66af8f24cd004b77ad202ba1facfcb66f240f856ff6cdd0`  
		Last Modified: Sat, 12 Jul 2025 00:25:28 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
