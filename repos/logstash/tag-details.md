<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.13`](#logstash81913)
-	[`logstash:9.2.7`](#logstash927)
-	[`logstash:9.3.2`](#logstash932)

## `logstash:8.19.13`

```console
$ docker pull logstash@sha256:500d2457f2bd1bb59a5af5d3b76bdfd0d7221d13c1fa26a474db403bee784a81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.13` - linux; amd64

```console
$ docker pull logstash@sha256:e686b4cf06c69118e70ed5fbe714de67dc1db8d4355d6c9c5bb29408a9d7d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542156697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af91a7ef7f49e25d4185f187ba9a9cc9980edfe01c9ba388908d8173bbf6ccf2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 00:21:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Fri, 20 Mar 2026 00:21:57 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Fri, 20 Mar 2026 00:22:40 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.13-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.13 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:22:40 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:22:40 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:22:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:22:40 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:22:41 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Fri, 20 Mar 2026 00:22:41 GMT
USER 1000
# Fri, 20 Mar 2026 00:22:41 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:22:41 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.13 org.opencontainers.image.version=8.19.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-03-10T13:51:26+00:00 org.opencontainers.image.created=2026-03-10T13:51:26+00:00
# Fri, 20 Mar 2026 00:22:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413f1e6c2994306bc0e1cca2f9ef4f2a9538778771a6d8ab1c37f268bff54798`  
		Last Modified: Fri, 20 Mar 2026 00:23:20 GMT  
		Size: 55.6 MB (55566818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b66f2b2e420da521c52a5f5832ee7a17c822450094d655d6bd8e06927520bf8`  
		Last Modified: Fri, 20 Mar 2026 00:23:18 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637550c5dbace363dbfdfe3f73821972f7477a10c96f6912c1a0fee0aaf9b2df`  
		Last Modified: Fri, 20 Mar 2026 00:23:28 GMT  
		Size: 456.6 MB (456590156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69893fc6408514bdd6448ea0cc16d1744fc1ae03e1dbf755eb242e0d78b482b1`  
		Last Modified: Fri, 20 Mar 2026 00:23:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530880f3a372ff030ddb8ee8414e956d401f07105407779cf5d577f8a53863cf`  
		Last Modified: Fri, 20 Mar 2026 00:23:19 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f956b0a55dea6631a31a0df7facddeb3b8010c6b38d3bd6b4259df871053a8c2`  
		Last Modified: Fri, 20 Mar 2026 00:23:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc71f4455049181cbd3e47f87bec730d03d7048545f58c8bb1d94e174e3a1ff`  
		Last Modified: Fri, 20 Mar 2026 00:23:21 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f71d741c4ea4795ebb65981d7c7837f5659e5c5a70a5267dead07e6f009c81`  
		Last Modified: Fri, 20 Mar 2026 00:23:21 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5870a1e906df58a0fa087d1ef01dc35c9207490c53a12d4a48f3b92a69c8a9`  
		Last Modified: Fri, 20 Mar 2026 00:23:22 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cd42a0cb7a62a21976097be2f2a9d27ec793ab66d4a316b1c34e288a6e444`  
		Last Modified: Fri, 20 Mar 2026 00:23:22 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ff85fdc231fecf43f53b29e135ec43e0829a87a41011459b64c0b1d373666`  
		Last Modified: Fri, 20 Mar 2026 00:23:22 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.13` - unknown; unknown

```console
$ docker pull logstash@sha256:c7e2343a441b0a7c2a77db579715d66e63795f981b90f67c25738b7a13db8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36de193d2611728f85ec2bab1d9f26230ecf5f345c33157933ad920c11139c29`

```dockerfile
```

-	Layers:
	-	`sha256:62cbe29d5f191cd0e49126a59b90d220c7fb65e68ff68631997c2486cf254c0c`  
		Last Modified: Fri, 20 Mar 2026 00:23:18 GMT  
		Size: 3.7 MB (3695640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d9297e491467ba2f83af76b97d19aa312b5a7c091455c207a05eaee67106b8`  
		Last Modified: Fri, 20 Mar 2026 00:23:18 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.13` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c6142eec06c8671c2f5e38f575f4c40193c934666cededbcb4c44e7599c70e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542480725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c6b5c2a728197a7e77d89b9907c3c378abd6eac722c18795698584feb3fa04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 00:00:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Fri, 20 Mar 2026 00:00:20 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.13-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.13 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:01:04 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:01:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:04 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:04 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Fri, 20 Mar 2026 00:01:04 GMT
USER 1000
# Fri, 20 Mar 2026 00:01:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:01:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.13 org.opencontainers.image.version=8.19.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-03-10T13:51:26+00:00 org.opencontainers.image.created=2026-03-10T13:51:26+00:00
# Fri, 20 Mar 2026 00:01:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a5c16d7383d0954f64969d16ea430ff2b68b4694485f0901d67dea45eaa283`  
		Last Modified: Fri, 20 Mar 2026 00:01:46 GMT  
		Size: 58.5 MB (58478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb074b1b58adbdb0b11057b643c1257e3736d77f73051406e1519771567377a`  
		Last Modified: Fri, 20 Mar 2026 00:01:43 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771aee00bf78bb88806f1431a8a5824d15768c0e2f40a11761d99cd321ce388d`  
		Last Modified: Fri, 20 Mar 2026 00:01:53 GMT  
		Size: 454.9 MB (454864719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009871d6705548f3dd09cad462568090e8f227dcd188d342e8fcc6dead037cdb`  
		Last Modified: Fri, 20 Mar 2026 00:01:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82365522ff8e7ac61c63bb39d426e29271c8d3144339953c6fe5f876d61754f`  
		Last Modified: Fri, 20 Mar 2026 00:01:45 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0525effa59561ec8d41183edda73a5afa69e2074e014130d15f845ff4d0d19b`  
		Last Modified: Fri, 20 Mar 2026 00:01:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f4b39becf0465ddd322cab004413d455cceb1fd3ff4f156550d51b74d5156`  
		Last Modified: Fri, 20 Mar 2026 00:01:46 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b607a59a9a8567c8a45bebab51f1c359276635b345f1bbf63519fc4011ba3db`  
		Last Modified: Fri, 20 Mar 2026 00:01:47 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b2250f44285d1086c4f3ed50a3262cb0959e2d8ead79963367afa4f6f788c`  
		Last Modified: Fri, 20 Mar 2026 00:01:48 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707d226e2f4efb277d842f41ba7b82e03eeaf4117da7b581aedf85b138cdd43`  
		Last Modified: Fri, 20 Mar 2026 00:01:48 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80643d63ab5a583403c2f0298444f5d629efc612bc999951d4bec966fa780fe5`  
		Last Modified: Fri, 20 Mar 2026 00:01:49 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.13` - unknown; unknown

```console
$ docker pull logstash@sha256:0ce6b291544986511adcec55aeaa054c761abacb17568f16564b11ffa28f4e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6b8983513bcf3e43b86ed237388e557157e058be1b5724dda0aa0a718d90fa`

```dockerfile
```

-	Layers:
	-	`sha256:6fdfcc8160fff1ebf797e7a10d4bc4e9dc4acd09316d7029b065d3370614c912`  
		Last Modified: Fri, 20 Mar 2026 00:01:44 GMT  
		Size: 3.7 MB (3696065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98f2155feeef67c89364102d430d23da69a072bda584925cfab5ae41ececf22`  
		Last Modified: Fri, 20 Mar 2026 00:01:45 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.7`

```console
$ docker pull logstash@sha256:60c37510ec4251e72dc1a3f7005580be5631fc09a51b3c9a3b92fbcac89ab45c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.7` - linux; amd64

```console
$ docker pull logstash@sha256:89d564e252f131200c962a1f677fbd966a9148b822700775e75fc242d96d9aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502409211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073f77a29861a3956e284a24bd6bdbc811307e7a3093f3a3233d2f6b085c1b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:05 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:18:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:18:05 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:18:05 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:18:07 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:18:59 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:18:59 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:18:59 GMT
USER 1000
# Fri, 20 Mar 2026 00:18:59 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:18:59 GMT
LABEL org.label-schema.build-date=2026-03-10T15:01:58+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-10T15:01:58+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:18:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e7b58d85b237b45bf5050ef0b503afd6ee6ce2df515da61e9fdbf740093155`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 5.2 MB (5154854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847128f703b2806de98b724b841f7e2647922c3642e941decc39bae38d56428`  
		Last Modified: Fri, 20 Mar 2026 00:19:45 GMT  
		Size: 457.0 MB (456958510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054df0dded86ba9ac8e28abdc3146ec17dd6ed160da3cdb260caf2c82eabd410`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d7ba96df75eb0f99bea059616bda24e6f043524de1e672ab9a7934398dff8`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d260ff3d826e1ecb6d1cc66dbea0fe65fa3273eb87663cd208ad457f7829fa`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b1428d69bc744d30f1f657e44065547f640ad713b3722fa9bde2271cc4ba7`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e5715547713bf4e3610df03d14c810fb7289178b013a15854852adb2abe7d`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6070ab62aacea5c722cc391f40d5f8d161a191f9819a73538b00d80008627969`  
		Last Modified: Fri, 20 Mar 2026 00:19:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9894778709bef0909ac8c4d369e75c165b1aa3cd488502089ab1d0f01f9b3349`  
		Last Modified: Fri, 20 Mar 2026 00:19:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.7` - unknown; unknown

```console
$ docker pull logstash@sha256:933303f7d1fce03be532709db3ed0049bcbd5efe8f9959da396c204ec4a020b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c8898597c185b7290ecb46c893aa33033ebd55bfee2863c7da04fc912f82c9`

```dockerfile
```

-	Layers:
	-	`sha256:703b8b77b6bbda13bd8589639b117aee4b53a0dc6f96c90e921a83f646b3e981`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 2.1 MB (2139754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506188ad7b5865c31f4e1b0b2450e612b3537ec3383efdc2c2b868e9d6a38e7f`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:669b618330f0df2ae884f521ef1538508bfdb80abf368f63977f6acbdcfff464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 MB (498861347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1201e0b131ee750acab14e05dc439e9bf5ea2298e02cd4dba8b9ee42150a6ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:16:02 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:16:02 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:16:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:17:03 GMT
USER 1000
# Fri, 20 Mar 2026 00:17:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:17:03 GMT
LABEL org.label-schema.build-date=2026-03-10T15:01:58+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-10T15:01:58+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:17:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2437fdd1f7c6cfc16f57c95ace35edb7fd9b94194a726f5bdd5f6f1d0e4d30f`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 5.2 MB (5155548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671dccb3af213cf364cf75aa74a0e085a24bb595d129a26aabfb2fdb18df3c5d`  
		Last Modified: Fri, 20 Mar 2026 00:17:49 GMT  
		Size: 455.2 MB (455236164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3647ffc3b772978ed22673dfe936e0e68a27b08d419adb66a15c847265796f5`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5264484c1c29ae56ed3d8d4b701c646485cb1361cfb0396eafa2628de62ad2`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cde27b062d7698bc35ea45d2fd5d497d7dfda5911a87c12f9dd7fb496e2594c`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25177ff4a0aeb1976a01661e03312dd7698cb55ccc009b04de383c36e40e969`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06ada9e180efe4e2e7e5142b43f786fda821ec2f4ec3a047755076feac8f5f`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae6e2f126623be86f617019551bf617afe0e0c5e197e1fc5b211dd7dabe316`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83a2a05060333e0f880b1378fd46f7343d5a27f339c34ceaa5379f69bc9f6e0`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.7` - unknown; unknown

```console
$ docker pull logstash@sha256:c9a28aa3aca0683d1b0f8e6244a896f0968498a27ee1bd9438c8606cea2361af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ad69d8e785b5b207578c30ceb883466c119adb5b5114f585c8a66dd577bae6`

```dockerfile
```

-	Layers:
	-	`sha256:3a24ac637bdb9389965cbdb896316479e4cc0705684abbed70e135c5eb5cb35d`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 2.1 MB (2140324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2cc2839e112dec4a0a63cb96b51a4d37cb983d288f6ec694cfd54dfc9fa093`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.2`

```console
$ docker pull logstash@sha256:b1e953e7da9185efc6f190bacc254cf290eb9ca5f9dfbc82e77ad31bec6cd6ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.2` - linux; amd64

```console
$ docker pull logstash@sha256:e9a4f0f97876b6d81f03904212edf7f96f20d6cf29f8056fbca978450cd41648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.7 MB (516707307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a8891fcf262dbff13b019f13aee8514cb0cfaabcc0abff48523312d99e7cc8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:02 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:18:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:18:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:18:02 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:18:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:18:56 GMT
USER 1000
# Fri, 20 Mar 2026 00:18:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:18:56 GMT
LABEL org.label-schema.build-date=2026-03-10T17:13:01+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-10T17:13:01+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:18:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee56507cc2559f5db8f61bd30006f6d19a96edda91be6b1838bc78cc4c2c3cf`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 5.2 MB (5154880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635dd7b466f6629e69aeae8fcb5791cbaf7f61e4282be192177e4a3403b7ea3`  
		Last Modified: Fri, 20 Mar 2026 00:19:41 GMT  
		Size: 471.3 MB (471256583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e73e5480a258cbc92278fc066efed40cc5e4aa5f9652a8a6728486637ec6cc`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6008836bdb87362167ebd91df56a8b560c45386a44cccb6282480ed7251e565`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900dd28a2035ca5ddfd8647e8beb445b1072eef4603b0cd771172d3fded41038`  
		Last Modified: Fri, 20 Mar 2026 00:19:31 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53e97a112fc3e6c6a4ffe796fc68cfed637a90350f025a768ca3b6768942e9`  
		Last Modified: Fri, 20 Mar 2026 00:19:31 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118ab693bfc241bc13808cae4ad210f7d84c16865a6ddc85a23c903945785e48`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf68e20f9a00ddf7c4b9f2fb7ed716a25f28d5e7d6e2cdfcde06b352d9978d9`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938733d6a7c65feae2a8149cce310180085159902e2d89a52ca6e4a4adaa515d`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.2` - unknown; unknown

```console
$ docker pull logstash@sha256:fa56d7d5123abe3398d4360379e34be8e5b49c76dc06ee20810383b5cb261f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b804676aee140e1532f5b4c29722e0d85a7cd3ca1ffdcca410e698f24964a9d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1ae278acfd44d30d8a88b9895a7984e3a132e4fa96ee44c7da3cd9937d10f2`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 2.1 MB (2119241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4431ddb632f7401b627c072da63aa598cb6bc3fd1682bcd1ed166799c35f2b`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ae57b868421bfbed45900d9efc6dcc8884b0d39bdc571bb9f9feebe7bb14e62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.2 MB (513168767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea62d639412766afba4c14afab993153e73444e80dd96da8824c17be918dcd2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:16:05 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:05 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:16:05 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:16:07 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:17:03 GMT
USER 1000
# Fri, 20 Mar 2026 00:17:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:17:03 GMT
LABEL org.label-schema.build-date=2026-03-10T17:13:01+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-10T17:13:01+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:17:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc72d85834f8cad087247079c798657c2db0a4ebc1ee18f5e6a42a4a94085ce`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 5.2 MB (5155556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdbc91fa3bca48638fa344aa733d9dae90c337aba825db8578a0988a65b63e2`  
		Last Modified: Fri, 20 Mar 2026 00:17:51 GMT  
		Size: 469.5 MB (469543577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377cce27256deb0fc2b894d00130bedb1a4e90db70da650145896b098d60b1dd`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cbfc0fab9a6207df1c5aac228071a5189662bf136f9444c7bf48013daaecea`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f01639dd5c695dcc1bde49fc020818497e7eb859fd24dd4f3ef13687a595be`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775e40fe19bfe72587d315b60fd615ee8ff618baffccf1a641343ec8c51b513e`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea8f30a969067308b1182e341bd82a7a1445b66974e47b7e153210c97012`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9e48e5e6788e5966cb1f8ad92f753873837412990eae200da38d0f018461ca`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ba62fa5fc09006ef5d0e0868d14d0314623aaef11480731daa09205711fe27`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.2` - unknown; unknown

```console
$ docker pull logstash@sha256:072e825ec6b2543c240e72b758769e567c79a275228b7e42e1be5fbca343e94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047127a241b48bc942197e58af31f2061ba0e2b790e1870dedcf3e2a845fb732`

```dockerfile
```

-	Layers:
	-	`sha256:491dabe1eb37942f69273dc81267e7206b9994c7be28bde6cece7a73ea9e9e85`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 2.1 MB (2119811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf863b93bf752a073c4333c48c8144bc7651680cd2c330e0a0197564b3f0e7d`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json
