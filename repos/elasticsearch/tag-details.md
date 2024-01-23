<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.17`](#elasticsearch71717)
-	[`elasticsearch:8.12.0`](#elasticsearch8120)

## `elasticsearch:7.17.17`

**does not exist** (yet?)

## `elasticsearch:8.12.0`

```console
$ docker pull elasticsearch@sha256:45e43f49ed38406db6f65d3d76c441784fb712d8c17aad3f8a033731b82ef29a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.12.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:03ad15bfc6b20e90bdc3b55520e494d8c08a17f79cba6d6009a1cfecb800efb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.0 MB (663965624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40104e7fdf326f8dd0d2237d668e51f211624472c8bcf86d6be14cd9a1f97806`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-11T10:05:27.953830042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-11T10:05:27.953830042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["eswrapper"]
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6b7680fbd62303c469990a87c7ab403312ca723ea55727d8a36a6895cc68cf`  
		Last Modified: Thu, 18 Jan 2024 18:14:57 GMT  
		Size: 7.9 MB (7893945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e8de800e5c29cb7168b84e7d2ba3e986ac7f7bead07ef832cb88a2ab347089`  
		Last Modified: Thu, 18 Jan 2024 18:14:57 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922eb3b50d3c658a0cdc51d45623d6691e676d101cd10f2c08c029f1f01653a6`  
		Last Modified: Thu, 18 Jan 2024 18:15:14 GMT  
		Size: 628.2 MB (628241777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfdbe0cb077f361baecf2bedf22b21f62c53b1f0b5ca0f778e585b7696e4bd`  
		Last Modified: Thu, 18 Jan 2024 18:14:56 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fe551812ff09f10a46b1c45b2d8d9a56bf749223c619c64fbc9125419a6af6`  
		Last Modified: Thu, 18 Jan 2024 18:14:57 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a374eee622f1b48bfc81ec3081efd4e04d3b7f574203ddf7b2073b9c5af4e6e`  
		Last Modified: Thu, 18 Jan 2024 18:14:58 GMT  
		Size: 191.9 KB (191879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2d6250f9972046f6ba764204108fdc47bd918cdc4c9154e24eb9c7c28e358`  
		Last Modified: Thu, 18 Jan 2024 18:14:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5043eeeccc6838a55d07db93530d223ed3fb075bf4e186db35b575cb67f25c43`  
		Last Modified: Thu, 18 Jan 2024 18:14:59 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:98a706f502c7ee84f46b52eb4a93fabae0c1273920928e46b8f76a93a7e627d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc774d94a6010d7b4bc9eeed6a85b233ffa28a694d74b54212d52fb142eadf8`

```dockerfile
```

-	Layers:
	-	`sha256:36bd52e7f1ee95b7a74748ee504aaedcf6da86203bfb057c620e0f25587307a5`  
		Last Modified: Thu, 18 Jan 2024 18:14:57 GMT  
		Size: 2.3 MB (2342807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e226f94d0b8bb423c660d7b981e32605bce744649c297703a2e58b48fff3e238`  
		Last Modified: Thu, 18 Jan 2024 18:14:56 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.12.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8d679e3a9e9bb8147bc723952c869043a7cacadd864a9b70b5aa03a7ef123cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456553538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7be44706d939c595090b31091af233113acfcf875d5fbf99d8284eb666d53`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-11T10:05:27.953830042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-11T10:05:27.953830042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["eswrapper"]
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be98b1d6e32cc22228ec68b71e2945257970e71f3a550061a4abecd4492d29`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 7.3 MB (7328019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7cc25a9ed6ca506a18bf041b668a08ef9a82e1c729ffb8271bba1b89a972e0`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091b041a789776af7adba81d26c6efbc74f9a4d2ad4bc282d7899a907e276fd`  
		Last Modified: Thu, 18 Jan 2024 21:43:44 GMT  
		Size: 422.9 MB (422939990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d76c21e6adb4dc1fd4c625bd8ebf04434dfb707c6746641d8c2461edadd2e`  
		Last Modified: Thu, 18 Jan 2024 21:43:35 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a26d3f8b9182d47cb56cc4744b10be8488804df9c4bc63a739e6b87c9ce53f`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb70a37b34d31a60c1099ab434464b52858ce81a0d4747b7f0e4e409eedc67b`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 185.9 KB (185914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a75caff16ae8b7df99372f287b8f565c289c0e0130fa9c388a41393b491b85`  
		Last Modified: Thu, 18 Jan 2024 21:43:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264d475555cdb858fc449a1f14a576fefea236a224e0b115aba46b96636d9f65`  
		Last Modified: Thu, 18 Jan 2024 21:43:37 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c3ed85e02cbf1d2696b10e87f30d8e67a5b08820f4220c2f29c8c04a6e9e6b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c57b4375682decd855049c97a70cb3aaf1132d00fb46d0e34d7ff8dd157fcf5`

```dockerfile
```

-	Layers:
	-	`sha256:6fe8d46232747704b92c860621c53724478b96131fb3acdf65df938cc63ed39f`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 2.3 MB (2343114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a989a80f955ac24c0a80a695895b0ce328ddbe382849c566dfdc51fd43509449`  
		Last Modified: Thu, 18 Jan 2024 21:43:35 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json
