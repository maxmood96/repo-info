<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.20`](#logstash71720)
-	[`logstash:8.13.0`](#logstash8130)

## `logstash:7.17.20`

```console
$ docker pull logstash@sha256:1203a1d70eef6ea07f71a14df96e4d043c27098ac461670238af84b19a9e0ef4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.20` - linux; amd64

```console
$ docker pull logstash@sha256:492956c9cc4bc80cfd2e5268d2329987597d4bfd9eae70f602e47b62ff37322d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.9 MB (446875527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08d4fb00ae2b23d7b9f19896d25e6fa06a95f42cec19069652a1d191738f838`
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
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82faf2ffb15e53e88d15ca53136ec9f9164637eef4b1180ef411ed962c11094`  
		Last Modified: Tue, 09 Apr 2024 18:51:01 GMT  
		Size: 50.1 MB (50121005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c7f65c8ff28b7393b11a2238d7de8c89dbbe6ea89f229fccf586acd81f7e8`  
		Last Modified: Tue, 09 Apr 2024 18:51:00 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4e736c2a45571386f846450580343ef13f82b131b1ccf9e33e750008c286f`  
		Last Modified: Tue, 09 Apr 2024 18:51:09 GMT  
		Size: 367.3 MB (367332613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a121388b176cbc723cb69c5ab99cb8e85376dd1d655baddc23e4d3de692ecb2a`  
		Last Modified: Tue, 09 Apr 2024 18:51:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c86f281d0ccd0d605a4078906bc5221c537f3129bbf42a2ea926585d145436f`  
		Last Modified: Tue, 09 Apr 2024 18:51:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ee62084d146844daadceabdf402051fc66ed548e002f32f1074aa7575cec1a`  
		Last Modified: Tue, 09 Apr 2024 18:51:01 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2614e5420746ec942e7ca508e5d08bfb7ae3d9652de9101dddca60584277515a`  
		Last Modified: Tue, 09 Apr 2024 18:51:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16c08715695e0f7a974f87567b5e889fdaa0a19a40625b8665574d8ae9a0ab4`  
		Last Modified: Tue, 09 Apr 2024 18:51:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2870976ab02b3f66f8c2f2127992edb64dc262ca796850c0cd859636a135a`  
		Last Modified: Tue, 09 Apr 2024 18:51:03 GMT  
		Size: 1.9 MB (1902996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad990e56c2e7956e5e3ed6560f63134f167a7b61d43812afd266dc9ce5b2af59`  
		Last Modified: Tue, 09 Apr 2024 18:51:03 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:7a8309751a58a03704b47d555563e5ba0e56bed4de4381f466d4f2a8f64c5359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18488e07823b93ef025d6f9506a6c41402862b0b5b4b54f630e1e80297a1f96e`

```dockerfile
```

-	Layers:
	-	`sha256:c5ac18c1ba0edea5500f51c7b758ee5d42232bcc6f4c9039d14c4c8de9d25e60`  
		Last Modified: Tue, 09 Apr 2024 18:51:00 GMT  
		Size: 3.0 MB (2977446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9784f2c6e38c689537cccb68d8dd68bc4f03510ab8cea7207f5bbdb3edd040b6`  
		Last Modified: Tue, 09 Apr 2024 18:51:00 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.20` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:38bb22a2f980124d5c8f8a2dea1ceb09d65a4547902652488f6596e4a924a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429142106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f662a8259f96b9db7b67a79e179a4fdde138489d2a95d2e3f215755f619ffe09`
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
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425fb225216dc969f3f10fa6812a6be467ea7c73fcdc1aa4c81534d48916720`  
		Last Modified: Tue, 26 Mar 2024 19:08:37 GMT  
		Size: 37.2 MB (37212876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b78517e16767316435e2ba9c047bbbc6d0af81f3c639bd7ee8f46fc542318d`  
		Last Modified: Tue, 26 Mar 2024 19:08:36 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7119906fff0f65e166780ca04762d4c39a22e3aa1ebfa9b231347796925be78e`  
		Last Modified: Tue, 09 Apr 2024 18:57:54 GMT  
		Size: 364.0 MB (364047239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d482483b8911d1de11dc61fc4d175e1ae1fc4ad9052a28fdd17ff604687e342c`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc5da3ae51c5c0891df8ef48dad34379a2564bb1270ee866ec7b1e8c7302d66`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5164f677dbf2154aff7645f677a1c3bd3de71666bb75682618bdacec7f96b3`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35636dea2513e4a41842b6f15d0668f281ae7aa033fad2f30795a12b91b51a62`  
		Last Modified: Tue, 09 Apr 2024 18:57:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5341eb1595212f49b142000198df4601097c31c59f6c14ab36a2006a75934a6`  
		Last Modified: Tue, 09 Apr 2024 18:57:48 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e74361b595961e5e36e511110a1c71f8b8199bd985285f65014f06345093`  
		Last Modified: Tue, 09 Apr 2024 18:57:49 GMT  
		Size: 1.9 MB (1902995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5048442229302a6ffed6368d9d80e4c0b7fa85a79268b2f0ddc0e9202b6143d`  
		Last Modified: Tue, 09 Apr 2024 18:57:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:a8d1a2679f4db6f9287017b96c0de97ca2d52d23b4440e116653e65dd476d197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a242a19b35ac874d2216131b34f75a3d6bcd2dd81b8603d741c6b7e04957d354`

```dockerfile
```

-	Layers:
	-	`sha256:4a4de0ca0938d145bd74924f2d8bebea4e672fa571c58df596cdcc1e5941a40e`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 3.0 MB (2977666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bea02595d6d4f358d901fe5a92209c5c399facf980ba01169fa622dfdc36df`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.0`

```console
$ docker pull logstash@sha256:a5e35b86db3e0ef0659f83f42833cd23e5b5a6321d9b7d8406d4837d3bd427b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.13.0` - linux; amd64

```console
$ docker pull logstash@sha256:b5fd49e36194a24cace2bef49d41aa685e15ef5b6702b0ecdbeecd988c298487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.4 MB (490388804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ad97a2ce120d2bf93fd671b59ea4d6fe3d400b00bcc48f40db0cf4e18c09e8`
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
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8674d7cba002bd25c9485e9b15a6814a3a9ba0b1d4d268a1a25063fd636045ae`  
		Last Modified: Tue, 26 Mar 2024 18:50:38 GMT  
		Size: 47.4 MB (47426428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416696fe99421abed26854768fe2ca3c45a0530b9d5b08985d4ebb8eb9396cc7`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe51e0c800adeb5e586a454257bb79d373808518a3eaf913fba03902701d445`  
		Last Modified: Tue, 26 Mar 2024 18:50:46 GMT  
		Size: 413.5 MB (413537495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b0df39b12ecdab95bcb8a1af0b38d3e1e08c5f8b8211d17f4ebbfbfb55e7a2`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dbf5b1ac5195141c60333c2d6b8b71bcecb76c33717858af31ab96ed886722`  
		Last Modified: Tue, 26 Mar 2024 18:50:37 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1400e21b86f9c2b574e0164dcabce11258a50723136c71ec1a9ff9a7f717f7`  
		Last Modified: Tue, 26 Mar 2024 18:50:37 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3a033f6accb967a48801af5ca6dba5a235b5939ff8024a828bd1409f712b47`  
		Last Modified: Tue, 26 Mar 2024 18:50:38 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec1bd999b1f59733b482f0fd09181125c15e256fcaf667c709e21bdbf8d116a`  
		Last Modified: Tue, 26 Mar 2024 18:50:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0fbac536ed04493182520715b0ee6815c2e8c0e9d7ba572101bb474722f85`  
		Last Modified: Tue, 26 Mar 2024 18:50:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a4e130adc8f385924b007988f7a47389fd0a12f535f1951f63f382c3879f94`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 1.9 MB (1903447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de83927b22492149387e94c6dbe43fae03e1137e02b770ae1805917690b6ee8a`  
		Last Modified: Tue, 26 Mar 2024 18:50:40 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:28651bfe74f16fe1d33143d686cd9c76ad54446f1afff0d20eaf8d2d04c35d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931cba84239092c2145258fc63ee129e6635fcf45998ea217299bc9731cd897`

```dockerfile
```

-	Layers:
	-	`sha256:1c88c3fc302118f8a8594be3d78df17b0de4f443535d534f3ac90161945b23b4`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 3.2 MB (3177191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41aca8e6521e78914434c04305cb2a9859b8c010130a57ff2389e70e96494c95`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 34.7 KB (34690 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.13.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ade4c45b58c35477ef61874237331f3bc3205e47044db8bd6552702e4a33df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.4 MB (477443668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b37048aaa72ef6be711e16b5f29b7aca2837044a71bf313893980cb04b42e`
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
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e80fd83213efbe9caa80d6a019635678ee5cc95745f6acfa6f90c52f46df5`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 37.2 MB (37212801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c22d41b53528ed35fbeb2bfe0dd2d51fedef7886026b6c9af30f1386365cde`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7a1df18c719dd5312ecb83d38bdb2400349fbaf551bfb43aacbe1d123254c`  
		Last Modified: Tue, 26 Mar 2024 19:07:23 GMT  
		Size: 412.3 MB (412345902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc524d760a392f0ee217dc0a3bf114ea645902012b5e43c736a5b1be7e2456e`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08401652822e12af3c388e4e1c94ef641cb4b20444a859479223d5356fe2c809`  
		Last Modified: Tue, 26 Mar 2024 19:07:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695271c2dfebb37d215cc8f3f3386432bf3c5576de25061e56325dd8c6c558f2`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe93bd8ccad9167870793206184cc2b9db4741147e37371b4b355869ed665d3`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd6dfb1d001a06ea354e4f6f92aa4743699da41e3cdc3615b095e38185620e6`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5881ee79406147fb77c814643140b4ef3619668b3d36a123c1531f5be89c939`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d7ad580d97b6bb27e16e11d62fbece68772e3a9edf7c2168a7a0d2eb47cd8b`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.9 MB (1903443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34979c15a1233c67bd0ec46dadaeb9569227dc9d89d950fee2a65c338a094c1d`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:0f2bab4cb10e5f91f35a44a6be840eb663d099d578295d8e43956c8989e8f7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba68b61c5a236dab9c41021948429c3f3b4c8da03c703286afe903251cb3590`

```dockerfile
```

-	Layers:
	-	`sha256:562ca2a5070b8e2035df29e6c634bbd953ec6a8081b1808052ab752cff4abf2f`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 3.2 MB (3177418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aed4827ecf2de08bb7abf88eee3dea2fb807541ee82fe2502604e610ef7ef2`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 34.5 KB (34533 bytes)  
		MIME: application/vnd.in-toto+json
