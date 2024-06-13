<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.22`](#logstash71722)
-	[`logstash:8.14.1`](#logstash8141)

## `logstash:7.17.22`

```console
$ docker pull logstash@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `logstash:8.14.1`

```console
$ docker pull logstash@sha256:1ad385cd40def83687a10665fbc05fef6c77b1cccddbb5458f32b8f73b182059
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.14.1` - linux; amd64

```console
$ docker pull logstash@sha256:e1e4a00dfc33ca1eb78322f41478f221afb83c347a9232e94eeb8cd948544de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 MB (487311695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7fbeff1027053c43023bff25fa7c7a0e885a8f26a1e5fba48de3cdfc181a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 13:14:46 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Jun 2024 13:14:46 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Jun 2024 13:14:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 13:14:46 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 12 Jun 2024 13:14:46 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
USER 1000
# Wed, 12 Jun 2024 13:14:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Jun 2024 13:14:46 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.1 org.opencontainers.image.version=8.14.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-06-10T18:33:17+00:00 org.opencontainers.image.created=2024-06-10T18:33:17+00:00
# Wed, 12 Jun 2024 13:14:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f740a95e77466a1204192dce5acfa540aa0a87f94d2a80860e4342fb95b250d`  
		Last Modified: Wed, 12 Jun 2024 17:57:36 GMT  
		Size: 48.4 MB (48391185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0926400059e9e04a692f8e73d81d485a970e6943705edbf013b27d3b2339605b`  
		Last Modified: Wed, 12 Jun 2024 17:57:34 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e4c1be29bcd574f7c4f9f7ed0627581a95eb89900c16a0eb113765a48ccb4`  
		Last Modified: Wed, 12 Jun 2024 17:57:44 GMT  
		Size: 405.8 MB (405808532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b765702d6714a64ab3e3c12eb19a6e17824d75cd75c9ca9e9c3ba6ef701555e`  
		Last Modified: Wed, 12 Jun 2024 17:57:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a80fd401c3bc65f335befaee5f4703f75305025a714278823c2d5b88b07ffa`  
		Last Modified: Wed, 12 Jun 2024 17:57:35 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00288d9bc8ef4f1a8f1e40789c1e6e157234714bf68aec74253f50d68a47b`  
		Last Modified: Wed, 12 Jun 2024 17:57:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246fb17e818e649e713ad9e4185314187540854e65cbbaa0a6a3f642acb7f93`  
		Last Modified: Wed, 12 Jun 2024 17:57:37 GMT  
		Size: 3.7 MB (3690805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7913e97da0401e85b591a4214506bbe8cccd126f1f6cced1ac70adca3729b8`  
		Last Modified: Wed, 12 Jun 2024 17:57:37 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3507216171459ac6164e3e938428488b9299c5748188581672a276d47d49b62`  
		Last Modified: Wed, 12 Jun 2024 17:57:38 GMT  
		Size: 1.9 MB (1902232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbbf5989011d6a8767ac881b4786f5974b0b9373ae26d17984930576c172974`  
		Last Modified: Wed, 12 Jun 2024 17:57:38 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3864f8d0ada3f7a865b670c5ee8c89761eec3c6a71939996899997694270bd`  
		Last Modified: Wed, 12 Jun 2024 17:57:38 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.1` - unknown; unknown

```console
$ docker pull logstash@sha256:56d6da42e54f8ab7e3e5fae2f4a08f5cdd63c2a3d4dad2d32ef9985662ba2481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3e5787c869bdb4c1e5cfc0e377e53545ecafd36bfeed2cea5df196d1f8345c`

```dockerfile
```

-	Layers:
	-	`sha256:d3b05e2ef6d9e501cfb09167741ff9fd2d1309fe2d774ea4a99b193ac9ae9100`  
		Last Modified: Wed, 12 Jun 2024 17:57:35 GMT  
		Size: 3.1 MB (3136115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899bf3e44b99cd0df2e38d856c4b5dd8aabf1a07891520f49dd0e92bf96b3b44`  
		Last Modified: Wed, 12 Jun 2024 17:57:34 GMT  
		Size: 34.1 KB (34128 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.14.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:735ab54e802a0dfb36a9dc061bc38d8c8200cb38943796e2a340e58bb5c7b39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.6 MB (473633665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65c31af78cd041692ecaa0a04e4b3ade36bda9007d6d966c3601769bef2a941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 13:14:46 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Jun 2024 13:14:46 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Jun 2024 13:14:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 13:14:46 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 12 Jun 2024 13:14:46 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
USER 1000
# Wed, 12 Jun 2024 13:14:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Jun 2024 13:14:46 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.1 org.opencontainers.image.version=8.14.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-06-10T18:33:17+00:00 org.opencontainers.image.created=2024-06-10T18:33:17+00:00
# Wed, 12 Jun 2024 13:14:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fadc34356d1dfeecbbe5fe1d94d4a07c65b12b1e1a7fc869682607d47c18ff`  
		Last Modified: Wed, 05 Jun 2024 16:07:57 GMT  
		Size: 37.6 MB (37573454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaad5940dd746a89be1e653af42ed08ac0e430cbf635510e652644a0730183d`  
		Last Modified: Wed, 05 Jun 2024 16:07:55 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8e9eafc2d3850a5ded035f1a2ce647776985f902a777af20147c1c4b4cb60`  
		Last Modified: Wed, 12 Jun 2024 18:41:24 GMT  
		Size: 404.6 MB (404600448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f5c59ddde214cb8066f329145f31d6a7abbd8053f607e3b1a92e81b82c6936`  
		Last Modified: Wed, 12 Jun 2024 18:41:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec65342303dbb30e4dbaaed20093c0bafd3454a06460f94aa7701fe817d7fcb8`  
		Last Modified: Wed, 12 Jun 2024 18:41:16 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d97b610ad79e8f082e38c8f3022e50b31d5e423b8a9a3d811287583c8c5afc0`  
		Last Modified: Wed, 12 Jun 2024 18:41:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd0b08c98c08256cd01d617b9555f3eea009166d2c9831a128f9fb85bc639b`  
		Last Modified: Wed, 12 Jun 2024 18:41:18 GMT  
		Size: 3.7 MB (3690806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785f1b9c29faca4966ae827838f0e0b9ea780b3037550c204cc7ba38ff773112`  
		Last Modified: Wed, 12 Jun 2024 18:41:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2914e0a4986614edd8aad480ebd585680f1c5d20b2be6b5ff50d67395fa089e`  
		Last Modified: Wed, 12 Jun 2024 18:41:18 GMT  
		Size: 1.8 MB (1787559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cfd521d25755021adc8726f3e33416e4f5c01996fc7f2d9fbac0d553f47133`  
		Last Modified: Wed, 12 Jun 2024 18:41:19 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea78e09e605e3e296083b1532e538ccef6ae504bd06a5a72aa5caf527a7d558a`  
		Last Modified: Wed, 12 Jun 2024 18:41:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.1` - unknown; unknown

```console
$ docker pull logstash@sha256:79048919e1824722d1d7af488b53571defb83d6d505666cc393f835a5d66bb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30fb174c6d28f1790f25973b01495574c7f3d1454e480ac882d1ea42ea0ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:8c2b77c82395edef606679a7a5d70660f2acc393edbc3974c412bf3509f07875`  
		Last Modified: Wed, 12 Jun 2024 18:41:17 GMT  
		Size: 3.1 MB (3136350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40306b90bee1d40f7f3fd31205d3e966d2128fa581fd7609c9d152b461fd5066`  
		Last Modified: Wed, 12 Jun 2024 18:41:16 GMT  
		Size: 34.4 KB (34392 bytes)  
		MIME: application/vnd.in-toto+json
