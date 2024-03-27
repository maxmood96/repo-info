<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.19`](#elasticsearch71719)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.19`

```console
$ docker pull elasticsearch@sha256:aa9da9bfb752c87ba7d3c381f40435489fd16951e5176cd3115476fe792e0cab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.19` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5aa1c4f05672d9138a584e3a64e33baaf8743e41bae5f20b1b2dccef9f0309d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362638683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5ff49b558d9abe0ba5a5c9edf422403c97caabe811ac89f0b5641f3acd637a`
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
# Tue, 26 Mar 2024 11:00:18 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 11:00:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 11:00:18 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 11:00:18 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 11:00:18 GMT
LABEL org.label-schema.build-date=2024-03-21T14:34:38.216751500Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=92f290e9537478f85ff3fe3ab39945c1a49a6c1a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.19 org.opencontainers.image.created=2024-03-21T14:34:38.216751500Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=92f290e9537478f85ff3fe3ab39945c1a49a6c1a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.19
# Tue, 26 Mar 2024 11:00:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 11:00:18 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8fe5aa4c56830021d4fe034618036cc669b68b37e0296172cf6584eaac9a8`  
		Last Modified: Tue, 26 Mar 2024 18:50:06 GMT  
		Size: 7.5 MB (7512528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a940dc1da9ed4d1cd8afb318526ec1ab27eacda230f7830721ec7a3d254ca19a`  
		Last Modified: Tue, 26 Mar 2024 18:50:05 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186665dfb6b39953fdd4a86fcfc7d5151eb1e59f9286485401be35e2f1c791c8`  
		Last Modified: Tue, 26 Mar 2024 18:50:12 GMT  
		Size: 327.3 MB (327294160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677984843f05591e368f0a333e06d4c2581d6e69667fe75f55f65b1c2c58b67b`  
		Last Modified: Tue, 26 Mar 2024 18:50:06 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ad25766c548e675077461cdf4bc0efada125b6d63b9afc717afe948c22443`  
		Last Modified: Tue, 26 Mar 2024 18:50:06 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d735da14533d7fdcfaec5831539a9122cff241be3c815573a7a410a70453391f`  
		Last Modified: Tue, 26 Mar 2024 18:50:07 GMT  
		Size: 192.2 KB (192172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68399012e85222b3790d09be199a4822d55b3cd8a1ae3f8bdc10bb7cdf7d415`  
		Last Modified: Tue, 26 Mar 2024 18:50:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b711d4c13c52350a738d83d49b08c42fe4510984dcd279833799ab0e8672fa9`  
		Last Modified: Tue, 26 Mar 2024 18:50:08 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.19` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:24b56c46ccc8bbd2981110a501a8acbda3cd637706edf7ea78062b1e4adb9de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c084a457d11e45933636dda9b1536230c2d7b97ecb3c9a4deb35b1998bf5f4a1`

```dockerfile
```

-	Layers:
	-	`sha256:d15acd11f1d686d1635ab1c7cf6390afb9244c6a318380adc8c694b743de923e`  
		Last Modified: Tue, 26 Mar 2024 18:50:06 GMT  
		Size: 2.3 MB (2311473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44beaed92eb3dfe948c89194c063a577e84114821b1e9adc4cb2c09d242c416c`  
		Last Modified: Tue, 26 Mar 2024 18:50:06 GMT  
		Size: 37.7 KB (37742 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.19` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:96930a9e52125d1bc33f50cee964cf5e7d13a6bb254ef1bc59bc9f3fd5e029f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358568758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6723ed2ea2efc0ab841923ffbc741fa81b2571fb80991541709b9a97c21ea99`
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
# Tue, 26 Mar 2024 11:00:18 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 11:00:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 11:00:18 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 11:00:18 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 11:00:18 GMT
LABEL org.label-schema.build-date=2024-03-21T14:34:38.216751500Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=92f290e9537478f85ff3fe3ab39945c1a49a6c1a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.19 org.opencontainers.image.created=2024-03-21T14:34:38.216751500Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=92f290e9537478f85ff3fe3ab39945c1a49a6c1a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.19
# Tue, 26 Mar 2024 11:00:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 11:00:18 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c50df22b286b32751200d045cfb4487c468d64927726c21ab4dcaa274ec8db9`  
		Last Modified: Tue, 26 Mar 2024 18:57:22 GMT  
		Size: 7.3 MB (7331876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57048565a15c1497df0d5d8c6297e5593193b7faeafbfae200beb93d72e946`  
		Last Modified: Tue, 26 Mar 2024 18:57:20 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2a85863a6b3bc0eb8dfd4db754e719e1b24c214999ff480c409a80b5756a1a`  
		Last Modified: Tue, 26 Mar 2024 18:57:27 GMT  
		Size: 325.0 MB (324951206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe348cda4d08a1cda6cd69ba3b328440fbbb21c2cecd8acad446d3df86a7617`  
		Last Modified: Tue, 26 Mar 2024 18:57:21 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136c2d5c55caf1ac1aeaeea65d5e5074312667f7737ccc8cba417496fade750`  
		Last Modified: Tue, 26 Mar 2024 18:57:21 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea82e62fe498a13ab4a1297156da4868379d935c3c8319a1ac19cadc94d54c34`  
		Last Modified: Tue, 26 Mar 2024 18:57:23 GMT  
		Size: 186.2 KB (186191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a6934a899acf6983f07ebdfc48e69479050a3d36f347d0cc7267621668ef2`  
		Last Modified: Tue, 26 Mar 2024 18:57:23 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61686eb12cf598bd45e2b155328a750f559195231cab08dfc9483a4af7a62f0`  
		Last Modified: Tue, 26 Mar 2024 18:57:23 GMT  
		Size: 109.3 KB (109256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.19` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ac739139f4e8bc81fda4e9e6aa54b554690578895c7703575bf09707707dc16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938f400130f0b8c63deb3864350ee75db23bbbdfc4b18fef08f8c34269cae73a`

```dockerfile
```

-	Layers:
	-	`sha256:b1e7387d87b96ee3b006a6cc5551d07b7352cfef85e8e9698efa10a9a5433d42`  
		Last Modified: Tue, 26 Mar 2024 18:57:21 GMT  
		Size: 2.3 MB (2311690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44eec3c9a5777311c9460803572f5122c764f1485dec155c715a6f2fbda6cc9`  
		Last Modified: Tue, 26 Mar 2024 18:57:21 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.13.0`

```console
$ docker pull elasticsearch@sha256:e70e2bc1f88987edac86e0b0a95f18e0e5b0b6e34eaf37074aa4aa5f6919b603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2e06e0c83c551485faf8d49c354dbcbe5757f66fa82f27e753b36e2d3aa4b746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615312389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba1a371c8e771b1af9dc46432534d20c7d630e67e27c3a7ba4924c99454fa38`
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
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b190db87e221cc1308d2e688ea9a83e09dda1b55ec50e9972f3dc260f0154f7`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 7.5 MB (7512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa109031a696acdb26e523b807153d6070daaa043d16fc00fbf2bf4defab3d9d`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08466127fcdb52493482da50e03efa0d702e3ae1a7c5d2823ae6513b9a9edd5f`  
		Last Modified: Tue, 26 Mar 2024 18:51:01 GMT  
		Size: 580.0 MB (579968400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5861b544bdb8bb365de4f07eb5ae84053d4f11ad0e955f4d7c72c9e3186d8ba1`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6b772957a38409db17e87e372cc3e107a3c53b7f2061c5692ab5bbd2ca838`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8288a7b93c5b6b6c37d89cebdbfad8082d65fad0dae864f472ec32b6ea7d9c`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b4d3945e0f22a1f0150a19f73c269d35767c45d686dadc31a5c74763e05bbb`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0122d88049315688a64c2a92b4b767e4dab2f3d874a3809f2f3db32c8549ec52`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a2d8ae470c19a09fbd4c542d256ea179fe7644f08eb810aeb74e19aa4c582fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb6512b147ac967b87700dcaf456d1e8faf1f678ba6d2590a2452d082f5c69`

```dockerfile
```

-	Layers:
	-	`sha256:be8677b7c6276cb489c32d8da09c93c7ac927be31371fff2551d27cbf6f0c6fa`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 2.6 MB (2590070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff309f0a22fe7d63df20b866644a34b82455e672f37ea622c1b72f69cadedc9`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 37.8 KB (37757 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:223e8fa0331a01364ba1ee7d5a4ec219d047ebadc8231d570ff87fca0b1da6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459420510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfb2697483e0bdc9d3c0208a4fb9f579455a75403c7be9d5945bfbad904848`
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
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14e5e1b762bfecd88ab86a4faf77d6a3199d588e85e7407913816371679657a`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 7.3 MB (7331903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf899c8d88bb7608d07eda424716015466893306895ab7e5d094900f153bdb26`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9969e4f4e4faabe36f710e31bbca65b235109f03bc43a6e7dd94c9b5f5dbe`  
		Last Modified: Tue, 26 Mar 2024 18:56:11 GMT  
		Size: 425.8 MB (425803447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1079e422fd69fed0509b31ce2fc1f3693607fec5e6f46e8c15ae5cdf4e55ee2e`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46279a912b6b1e38401f4b7d596a076a4e67bbf6b313878c66c6cc9ca52942e8`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb703192bdef9a2b254da889a3c1524adce873cda1f5f1a6f63352820d2a8e2`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 185.9 KB (185932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83a0c8d826e0a6159aa7233c85c9ebc232b80fe0c9479fef82752e5f16b1f7`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81667493e1e6af1edbc07bcf742326013af80e6a6824930665c5a0b14ae65150`  
		Last Modified: Tue, 26 Mar 2024 18:56:03 GMT  
		Size: 109.3 KB (109259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d7b8e95a5f259c766897378b2c2028350bf9cb3ca132445f3b2523ffe2d50008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b2569b2880376d1da7828aa0f2a8e4ab1ce781dc8f5f410b83733f391091e2`

```dockerfile
```

-	Layers:
	-	`sha256:40eb042c66842dd8ee05f2eb974a7139247f1be77e74cc218dfa24b658a5767f`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 2.6 MB (2590303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c56700f68e57448d8b6376e76f982da10345b8301993c12963c4d32ea5e65d`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
