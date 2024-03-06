<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.18`](#logstash71718)
-	[`logstash:8.12.2`](#logstash8122)

## `logstash:7.17.18`

```console
$ docker pull logstash@sha256:cb910d351dd361487326ac34da734b61016eb93119c619fb61d571c8fdb0696e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.18` - linux; amd64

```console
$ docker pull logstash@sha256:75b9ed2a6dd0829fb5c13c6164f7b2eaf95a9495bd9ce701baddcc6880286393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.3 MB (443254266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16183b947ee608e34ccf2183ea627fa784c2f26b855a0e8c0f7f9df7e9902ad5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.18-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.18 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/logstash
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 Feb 2024 11:29:54 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
USER 1000
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.18 org.opencontainers.image.version=7.17.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-23T20:45:18+00:00 org.opencontainers.image.created=2024-01-23T20:45:18+00:00
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8186857aa53cb7b2ce9078a89c299a124c3cf46a85a6d601a8b0e625e860865`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 47.0 MB (47030076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8020c935b4b753b7cb3489aae73e17aff138ecd896135a53abaf2af3255e1fa3`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480c3db6a1795f23ffe55705603480ba5bcf5820fb62e50d30f1878299e66b13`  
		Last Modified: Wed, 06 Mar 2024 02:56:58 GMT  
		Size: 366.9 MB (366860382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a704b979f3516590ded619ec33632e11f293731f862ce1d4c5145c7c91b7d8b0`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7152df9aaf52046046fc74b778862b7e0d4959bcb7f13ce803b271877d8fa`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff214ea693306f25fdbd91d28b487d6fcb5978feddada9e785012501f44c18`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45934522dd1d78ecb2778acc16db6294f35dd116fe44726a36a346a748e4f292`  
		Last Modified: Wed, 06 Mar 2024 02:56:54 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33261515fd4a40fa008967c7c9eee8b1beaaf84fa3e7f97d4c2972d810ee82c`  
		Last Modified: Wed, 06 Mar 2024 02:56:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d312e78921d1abb8342176707ff9f1971fcb02dc0ebe9c8ff7492f27f7144981`  
		Last Modified: Wed, 06 Mar 2024 02:56:55 GMT  
		Size: 1.8 MB (1844905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d8d88d5abba5860199e4444c8546dc99709f053747540cb2d9847fcf58ba96`  
		Last Modified: Wed, 06 Mar 2024 02:56:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.18` - unknown; unknown

```console
$ docker pull logstash@sha256:83c499dd458892fc1f4f1cca81e2be5e1131c3335f4812eebf491c24aa34f7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3271321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513f6cbe485e0ef45e440fb90bd7874bdc721afbe67255da387f1784df00c1eb`

```dockerfile
```

-	Layers:
	-	`sha256:432a4e2b0a83ddd2c3c417e700e2adb5f91f6f326b233dbd669d2a64dd8cda50`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 3.2 MB (3239152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828bf20c9e0faed218ea7588d7bf516f266b08e577b5e8bbd5a723a626cbd1d8`  
		Last Modified: Wed, 06 Mar 2024 02:56:51 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.18` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:b3bf73c121e0dce78885d9986017653c8fc899abe3a0f1c3ae41913c1e13b84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428484618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbd8bfd5bb7a0a0c07439c40d0217cee979a1ff317eee27b20ced9e7ff98d1d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.18-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.18 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/logstash
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 Feb 2024 11:29:54 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
USER 1000
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.18 org.opencontainers.image.version=7.17.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-23T20:45:18+00:00 org.opencontainers.image.created=2024-01-23T20:45:18+00:00
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fad01ba4622494e01084b4f2c990390935d4356e0bee5305bfe23251d6d02a`  
		Last Modified: Wed, 06 Mar 2024 16:59:30 GMT  
		Size: 37.1 MB (37066112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b38331ee5d1b58ab110a6f2e4e578badc52708706c7e6b5e96395bbd067bb`  
		Last Modified: Wed, 06 Mar 2024 16:59:29 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d36d326520eae0ab419aa459d581a39f96a75ab8b80d666f2e90303533eead`  
		Last Modified: Wed, 06 Mar 2024 17:00:52 GMT  
		Size: 363.6 MB (363594612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac100fdd9f89c43f6d2079f9440db5a9e441dc807f6242ed057dc3dff64c3a2a`  
		Last Modified: Wed, 06 Mar 2024 17:00:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500140f7e5e95cd3803d1d77847795d8eff8fa6a20d02aa62672473b34ef3cdb`  
		Last Modified: Wed, 06 Mar 2024 17:00:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460de11e51b0b6168888dd236d7fcf2a6b6682230d848993f390709d332d5da`  
		Last Modified: Wed, 06 Mar 2024 17:00:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36c66f206c3db4418a56f4e81412bedac620438720546c1483247b98c7c2b92`  
		Last Modified: Wed, 06 Mar 2024 17:00:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86b8ea5b38a38f6584ddf4b2243d6fa3d2e625b18b39e26666f91df64827649`  
		Last Modified: Wed, 06 Mar 2024 17:00:41 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c307f42241801690879c9f021ff34fd5d928ad60dc33575f35dbe7d45cd133`  
		Last Modified: Wed, 06 Mar 2024 17:00:42 GMT  
		Size: 1.8 MB (1844904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2928fc2abbfc5326aff7ab112b42b55562b9f002bfe3387f2f37affe4dc142`  
		Last Modified: Wed, 06 Mar 2024 17:00:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.18` - unknown; unknown

```console
$ docker pull logstash@sha256:1834e47ee204472550a2176af08d93769129d4120fac30e436648d07cf4ce033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3271384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32696aa8d8041e0e318091b0bd2dd3d00becee6a24f3a8cbe260f91de336a026`

```dockerfile
```

-	Layers:
	-	`sha256:509cf5fecaadd7f6bac4fc6d2a1a57a75de3684fdd6c916b319ce28e39df2311`  
		Last Modified: Wed, 06 Mar 2024 17:00:40 GMT  
		Size: 3.2 MB (3239372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d909f92460347c467f9e1a1e33ab0db22afd175c8337c2fc127310d3c29df3`  
		Last Modified: Wed, 06 Mar 2024 17:00:39 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.12.2`

```console
$ docker pull logstash@sha256:71d5280020e849faf319f6bbb457cecc63bc37cb637f1d4e882a2dbc86fccdd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.12.2` - linux; amd64

```console
$ docker pull logstash@sha256:a15a827088a01c634bb4efe6676f3b5b9f2c8dd50728c56512d61e5cd145b8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426473321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431435ffc548307a5c05c898379c755985b508f5df8a75539704b3fd9c32877b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/logstash
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 22 Feb 2024 12:50:52 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.2 org.opencontainers.image.version=8.12.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-02-16T16:21:40+00:00 org.opencontainers.image.created=2024-02-16T16:21:40+00:00
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06487f034a6ce33e0209d9e4156742f8830caf4f433370cc6fecf70c75c3cc23`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 47.0 MB (47030137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c43214d2b3d3d7620ceaa7299ae59168d342cf53fade7caaf35ce522e54962`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0083a2fffe6a3a65783a62652630f398c25c04743caa28b89f62f027d9f42a5`  
		Last Modified: Wed, 06 Mar 2024 02:56:44 GMT  
		Size: 350.0 MB (350017662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c8daee1d77439f3909fe390f39cd1bb42906441c3011364764d868981d800`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f089b9a3e2a4dbfa337aebf874d8e11a33f2d692d342faca9b4c97079e62be6`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ed5b971ff4dd54cf834e5d211ac11635c1ad12f18891251663831c95be5d9`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de2b6f9e65f2e298ec60c209ed9b539fee80d393c5cb298ecfb2febece47dbb`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bf305ab938f068cd6e982e03f9c1996594f28ee7dcd877f74b369d59f54a`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329ac120e52abb6b2409a116fb071ece0e6a771f5ce1bcaff8888ba724d1ad87`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad5f6d6626aa280bc6895f88216d150e1da176bae728c637075edbaf41e1e9`  
		Last Modified: Wed, 06 Mar 2024 02:56:41 GMT  
		Size: 1.9 MB (1904103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b89468fac553ad6c9adad8d0a39af0df82f1fd2963d1cf5fbe1e1bbd77961a`  
		Last Modified: Wed, 06 Mar 2024 02:56:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.2` - unknown; unknown

```console
$ docker pull logstash@sha256:f12252962e9e68041e1488ab0ec8ba6177bb4bd2d54da70df89fe441927dc888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a2e40a4c91d726c774000563fba09272fea20f12d8088f82c000b85157829d`

```dockerfile
```

-	Layers:
	-	`sha256:079019ef62a7af2cc1fc8b76e177742c43add1ea80417ef9a78fed2fab6099e7`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 3.3 MB (3325957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c9334ce379f5d5689e86e42067f8fbef746918131d33c4ed30371ec1613b75`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 34.7 KB (34698 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.12.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:70c2341960ac22493ad8b40ede02cfae1e5ed204e2e15021fa574f5d51ddb324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413790153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a00402ad57f8b562ed3d86c571b140940157e239c81ebec1845b092ec8d3ef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/logstash
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 22 Feb 2024 12:50:52 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.2 org.opencontainers.image.version=8.12.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-02-16T16:21:40+00:00 org.opencontainers.image.created=2024-02-16T16:21:40+00:00
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fad01ba4622494e01084b4f2c990390935d4356e0bee5305bfe23251d6d02a`  
		Last Modified: Wed, 06 Mar 2024 16:59:30 GMT  
		Size: 37.1 MB (37066112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b38331ee5d1b58ab110a6f2e4e578badc52708706c7e6b5e96395bbd067bb`  
		Last Modified: Wed, 06 Mar 2024 16:59:29 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324a2ca183d61e5455eeb26854d853f3ce6d1d9c233ecb6592ad6bd63c62d2ab`  
		Last Modified: Wed, 06 Mar 2024 16:59:36 GMT  
		Size: 348.8 MB (348838423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8090dfbec32b046b05400d700a3ba63fc7156e8367c95bc67adf39edf5853b2f`  
		Last Modified: Wed, 06 Mar 2024 16:59:29 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b570c57449e88564e979cebe3347bf11ff47271c991f1457f3e81d773dfe142b`  
		Last Modified: Wed, 06 Mar 2024 16:59:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd083d2c3e6c795179d833f48f47d393db91a6cd80797bd0ef2c731da41b6d`  
		Last Modified: Wed, 06 Mar 2024 16:59:31 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d22330caa76d9b9ac6ad4281e8358d5e8da803a81588a524b14290f498a4b`  
		Last Modified: Wed, 06 Mar 2024 16:59:31 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f1fc71ea782457ff8fc4ef8918e3cc952858db192c3bd70e3ac6a7db09c413`  
		Last Modified: Wed, 06 Mar 2024 16:59:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a7501fdea52850c26ecc2d215d58cdc3d456b6579d86ab565da74b6de3341`  
		Last Modified: Wed, 06 Mar 2024 16:59:32 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5218a1d168145e8401725cae1841c2a2905037fdbc8336a040d8fc963919dd`  
		Last Modified: Wed, 06 Mar 2024 16:59:33 GMT  
		Size: 1.9 MB (1904107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d4993bac48a2359256ad04cece757498929fbfc261bc88c0d3f889d5d0f6e`  
		Last Modified: Wed, 06 Mar 2024 16:59:33 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.2` - unknown; unknown

```console
$ docker pull logstash@sha256:2875612a7562a25e5e1e24236937fef352d72a599e1bfc2a17321ed2ab1ef94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c501bd03efcae830b5d2ab38ca04df4850f90300f72e6eba93af7c4e6457a900`

```dockerfile
```

-	Layers:
	-	`sha256:8af015d95892b6be7732826a0c3e043307f57ff795b0f17d6f3a6409bd48efd3`  
		Last Modified: Wed, 06 Mar 2024 16:59:29 GMT  
		Size: 3.3 MB (3326184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a700b2fa4b8613a572fc1d2a6508b4f6ed331106055ef0fc2e731b5ba029330c`  
		Last Modified: Wed, 06 Mar 2024 16:59:29 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json
