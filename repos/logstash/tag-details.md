<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.24`](#logstash71724)
-	[`logstash:8.15.2`](#logstash8152)

## `logstash:7.17.24`

```console
$ docker pull logstash@sha256:f285856ba018924f46867630843bfa4baf416383f0570923395afe11adb8dfd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.24` - linux; amd64

```console
$ docker pull logstash@sha256:60d2134acb0a1756bb0ececfce69ffe8c2e606e14a1b75a0bef7e6cede68583f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450754795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1349896546504a79f3817c9dfa43f399ae0fac3b48d621a33fc83490c8dc1ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.24-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.24 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/logstash
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 08:21:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
USER 1000
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.24 org.opencontainers.image.version=7.17.24 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-03T23:04:52+00:00 org.opencontainers.image.created=2024-09-03T23:04:52+00:00
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9d83e8528a10478393f9deeba53b03e5fc7f9adab7a6674896ba2407931c81`  
		Last Modified: Wed, 16 Oct 2024 16:14:21 GMT  
		Size: 50.2 MB (50179729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f095137b0f74de9a1138788a403f204f0e35889f820d1f5e90565bbad13d795`  
		Last Modified: Wed, 16 Oct 2024 16:14:20 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fb28eee7b06f925c2dd4efa2ff19937fc89f9219a744ffb59aa6cfe0b65a0`  
		Last Modified: Wed, 16 Oct 2024 16:14:25 GMT  
		Size: 371.0 MB (370998273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa40e25f09b93752ff07da674b9ec7ed0199091cbdbcae2a9fb5dbb700821bd`  
		Last Modified: Wed, 16 Oct 2024 16:14:20 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47d69f7a96be7fb73f3a7a0b98454cace455fdd43002836c2c8f2557a5e9559`  
		Last Modified: Wed, 16 Oct 2024 16:14:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589bdbac255c733430007968ffa1a28e30c7816d6e44d55655fb42a687d48a15`  
		Last Modified: Wed, 16 Oct 2024 16:14:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafe24e2ef8fd8aa1a575a3d54bbaa538670c20461e83cf9e7f7c122273b68f1`  
		Last Modified: Wed, 16 Oct 2024 16:14:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133594728e1b3dedf225479d2776a1a18d32e8494c1ac5603550fbafb86c242c`  
		Last Modified: Wed, 16 Oct 2024 16:14:22 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3753aebb317f4a5c52923b56fb59b4fa85c3f2ee5956b7fa2d417c74314b5547`  
		Last Modified: Wed, 16 Oct 2024 16:14:22 GMT  
		Size: 2.1 MB (2061142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ca777abc3462eae5990132e6c8a5182b9013f3b76cf9a3e662afcbf080fc7`  
		Last Modified: Wed, 16 Oct 2024 16:14:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:1c3e673ff5cc3dfa29b76425de529ff6dfa42779670b38b9b736ad58d8fbc4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89adbb02b585c1809d5431023ecb0b1736fa289d3a6505924bae8eea7762da18`

```dockerfile
```

-	Layers:
	-	`sha256:e674c75fee8334bd8e699bffe601b0e24801957a288e2f4293ebcdc96e789297`  
		Last Modified: Wed, 16 Oct 2024 16:14:20 GMT  
		Size: 3.2 MB (3246143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03dbd9d8a53e3dc6951f5174ed2a7be36af744d0bed154d334a7c706eaf2ce84`  
		Last Modified: Wed, 16 Oct 2024 16:14:20 GMT  
		Size: 32.0 KB (31969 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.24` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:4b201d870ce1231faa047760cdce936a86a1166ec4c721914dbb65002da6a31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434218426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02ccae562dc5534c2f3ab8631934622a83c086281a9846dfee4f2947fd5a8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.24-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.24 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/logstash
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 08:21:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
USER 1000
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.24 org.opencontainers.image.version=7.17.24 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-03T23:04:52+00:00 org.opencontainers.image.created=2024-09-03T23:04:52+00:00
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c34dfd1eb963cb835a5a0e604a4768107048ee6ca4ecee99897b3fb2c5cbd1`  
		Last Modified: Wed, 16 Oct 2024 03:38:13 GMT  
		Size: 38.4 MB (38362564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54e5fc3ef7a6b3b76ff7e9e3961121173417e47147e882d34a620bf2727a60a`  
		Last Modified: Wed, 16 Oct 2024 03:38:11 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278c07a5d5e0a8a69fe64bc517944fd555937de245660f67266c54b835097818`  
		Last Modified: Wed, 16 Oct 2024 03:38:20 GMT  
		Size: 367.8 MB (367816307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eeaf3aeb0ebd5e73d99dfe7cb5d141dc9b69c42ca343c5e2f4b63a16b57a8f`  
		Last Modified: Wed, 16 Oct 2024 03:38:11 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5025acec35ab7943ffdecd5e7f05a06ee588ac9a6ed2b0a2474d34e78eaa5b`  
		Last Modified: Wed, 16 Oct 2024 03:38:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9b72fbc084bdfd0296ed167626f5244ba073c89ef4a1502abca6e460ce89f7`  
		Last Modified: Wed, 16 Oct 2024 03:38:12 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248c5915cdfc485c66c61bd4706c917d8a605057fe552ad8789f886f0b95b257`  
		Last Modified: Wed, 16 Oct 2024 03:38:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469b2722c48bfbb1281c5b839783f3bf627e88597a4b2639e6651fc4d63adbe3`  
		Last Modified: Wed, 16 Oct 2024 03:38:13 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecc826639d8c3d2b5dfcc39e9774a4d1842e1168bcae94939bb664599a7485`  
		Last Modified: Wed, 16 Oct 2024 03:38:14 GMT  
		Size: 2.1 MB (2061142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbf94c45c44bd0715c4092ad990759b40d481d797aa7a32b35d6f0e6d2cca5a`  
		Last Modified: Wed, 16 Oct 2024 03:38:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:eb676aff457cb1ab7ed03e7a913c4f945b4009be51c7aef2ad051afe52444cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b163c93b8b326a40f586dd9758b41035e956c4265239f690cc6c1384443a7`

```dockerfile
```

-	Layers:
	-	`sha256:d6db6582a6352b52553d67b10f3b125b44efc45107bd0018d171046cdc720e45`  
		Last Modified: Wed, 16 Oct 2024 03:38:12 GMT  
		Size: 3.2 MB (3246378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fbc311d0d496a56be8d4faabe86f8a00ea802681b4b1a2d019159234a7633a`  
		Last Modified: Wed, 16 Oct 2024 03:38:11 GMT  
		Size: 32.1 KB (32092 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.2`

```console
$ docker pull logstash@sha256:179975b42cf16221bd85f10fc3b19e9d36063d1bda62dd6fa23b9a9a4919693d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.2` - linux; amd64

```console
$ docker pull logstash@sha256:3a0605eea29c8bdcd0272a38bdb9d649888db86e730adfbc2f1e0a203babefaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.4 MB (505376325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dd73033f1a34d51941cdc7e9b9f64f1fbe0f71b9c668b8ad174bc3fed6771b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Sep 2024 08:08:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.2 org.opencontainers.image.version=8.15.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-17T15:11:45+00:00 org.opencontainers.image.created=2024-09-17T15:11:45+00:00
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1d0ab6bcfc25031372208a82ad44dca40bf8727d931eac3295b4c7a0e40a6`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 50.2 MB (50189098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db76f63dfce2cbc6d384ff036d4e16833c0847c5d79ed62caacde2c74ce44f55`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c8cdd21f5f451db554fe0d88304bdeafa9a0322af9b892ed00ad67de2a9a1`  
		Last Modified: Wed, 16 Oct 2024 16:14:38 GMT  
		Size: 421.6 MB (421612307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eada6f1e48a59952e1c576f3ad923c173844cf643a08f63c083c73e8de91a9f`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4e81c237a02aafc7edd61249ff7ab6a99f92af567cffcbf860728cf4e099d`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f03bff9c7275f102804e10b4949fa449cfaeede46bd342e9671e4d67c6e3393`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51fa44c66ecac0bb1c896db7b9058f8d0c67d3938c0baa0af69b91c4b38517f`  
		Last Modified: Wed, 16 Oct 2024 16:14:31 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbf76f315e8410e1ea3101289017804ce303dae3a84f94797791e4a74bea57`  
		Last Modified: Wed, 16 Oct 2024 16:14:31 GMT  
		Size: 4.0 MB (3995868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32513fd72b655f770559e6eba84dcc6c5669a6bce84e6c54415053f8927f089`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 2.1 MB (2061519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c5b5f1513daa7a60173434d65495fd86320f9a795c9db3d0f6ecb78649989`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:4bda509be1a889be2704fbd9b3487dc3fc875f7ce20d550b6956c34c292e185e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4c353b10dee1b09c2bc236accc68b823dc785e5985084217453395db7023e1`

```dockerfile
```

-	Layers:
	-	`sha256:553ecaebe29575ee33a43ea6a096a90651aa7436eb86fa42478c4e11dd3127a6`  
		Last Modified: Wed, 16 Oct 2024 16:14:30 GMT  
		Size: 3.4 MB (3397535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d32cb4d2985ef7fe45187783c1a482d3f089946a66689b74b985360cbca060`  
		Last Modified: Wed, 16 Oct 2024 16:14:29 GMT  
		Size: 34.4 KB (34354 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:69752932b752f11a78807446f9b7e3a9ebaf708199773ec89c9b05960689408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.1 MB (490063402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2911b4f77cf70e757648247447b2ee95efabfc7def51e9a634aa4ce43d792948`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Sep 2024 08:08:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.2 org.opencontainers.image.version=8.15.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-17T15:11:45+00:00 org.opencontainers.image.created=2024-09-17T15:11:45+00:00
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a885b0211a43d804aed6dd355647df7a51390a8987bfa94d2bc2dc61ff599c`  
		Last Modified: Wed, 16 Oct 2024 03:36:19 GMT  
		Size: 38.4 MB (38371505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbf5c9ada372334204f621439e5fb28ef525da9372c35c689e4d9bcdd2e3197`  
		Last Modified: Wed, 16 Oct 2024 03:36:18 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd0dc986bb89731d458f43b0c751de48fc5dcff0ce7b4c23045453f8691d29c`  
		Last Modified: Wed, 16 Oct 2024 03:36:27 GMT  
		Size: 419.8 MB (419783018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11116a249fc063460d592208cd54caeb1be85b7f1015dee6a327f9ff2bbf3824`  
		Last Modified: Wed, 16 Oct 2024 03:36:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a2fc299e12769469fcd401611bdf9be8a5d4738b51ca3e4c0ed59980ddf3`  
		Last Modified: Wed, 16 Oct 2024 03:36:19 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c047a6387acacbb20cab05f3923115fe6ef3e58beae994b8cd342ed8257e2e8`  
		Last Modified: Wed, 16 Oct 2024 03:36:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518c9b482c332aa442efbc6871f83ade402001a89e179ed1025475a7db37ed15`  
		Last Modified: Wed, 16 Oct 2024 03:36:19 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f2f61ce58b69e7143d3d77051545ebe9fb6b864bc33de4633559fe40fba10`  
		Last Modified: Wed, 16 Oct 2024 03:36:21 GMT  
		Size: 4.0 MB (3995862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938bca649a2ff273a8155cacbb134bc496d30e3e4efce18cb051cc05ae6c7ffd`  
		Last Modified: Wed, 16 Oct 2024 03:36:21 GMT  
		Size: 1.9 MB (1932713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694b205d0911f31add1fcb1ad0c24b0dd84611cf376be6238d73538bc2d9ea59`  
		Last Modified: Wed, 16 Oct 2024 03:36:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:9dbaec38ae850f0866fa9384918200f91c977950e7cc2df59dff249b7032e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8854f0cdbda69707026f7869bdb5afd562f180902364cbf04a286a134e8864db`

```dockerfile
```

-	Layers:
	-	`sha256:74cbe817ad86f8a966c8102bce03df9edfae16f1874d826fbe80b979e3f86b68`  
		Last Modified: Wed, 16 Oct 2024 03:36:18 GMT  
		Size: 3.4 MB (3397145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e18a1c68d7e80a63b61f4d93d3b25f08b26502325d909465dc7679c3d936f78`  
		Last Modified: Wed, 16 Oct 2024 03:36:18 GMT  
		Size: 34.5 KB (34492 bytes)  
		MIME: application/vnd.in-toto+json
