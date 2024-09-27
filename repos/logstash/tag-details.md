<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.24`](#logstash71724)
-	[`logstash:8.15.2`](#logstash8152)

## `logstash:7.17.24`

```console
$ docker pull logstash@sha256:45dcd1b0f0a91e0da1b1e5f89c47993102d5226d9224b30d27d55f7e5aabd801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.24` - linux; amd64

```console
$ docker pull logstash@sha256:69ecb3fc1539b56a98c31608e6d1a7ac0396d18d5ea780b122567283ca0d233b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.2 MB (450213010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a52fbe6be95eb8467b45809d50705dda4ac0ddac252a448f2f7d06ffea617f9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d47d25f4dd69709e810e2575d5c607424ca3bd52f8554951ec7c74dc81c635`  
		Last Modified: Tue, 10 Sep 2024 21:58:14 GMT  
		Size: 49.6 MB (49637548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a51027dd7409518956ae238dbbc52a593b9ef152ebfbcb7de07e55c43b459a`  
		Last Modified: Tue, 10 Sep 2024 21:58:13 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ae03bcce0792f752f68bd8c08d81e03d1369aa0d61d64b460fa765905c60d3`  
		Last Modified: Tue, 10 Sep 2024 21:58:19 GMT  
		Size: 371.0 MB (370997955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc09b7dcd432ed145d8cb0a1a88f9faf5d73b5d5e9cf8397f6c19c86fdbead0`  
		Last Modified: Tue, 10 Sep 2024 21:58:13 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81ddd1b1ff30c7a38840f27b02f10bc16dd14e4a102722072827fa33c8de4d`  
		Last Modified: Tue, 10 Sep 2024 21:58:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb9a83bbad96d67499a20ab9bd0a1bcadabdb6760bc9f9c0d6429d2a31b173d`  
		Last Modified: Tue, 10 Sep 2024 21:58:14 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584ea00df2b1a9238605097ab8e4cf7e0b727a661313b7a99b4fe4247f098ff`  
		Last Modified: Tue, 10 Sep 2024 21:58:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332489d555560e49c742280d4d260c835fe2ceb253400ab32926226b9c5d1630`  
		Last Modified: Tue, 10 Sep 2024 21:58:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8255646e5cb22e96775f84ace69527fc66509c8b978573e1ad2b0b3a1eeeb8`  
		Last Modified: Tue, 10 Sep 2024 21:58:15 GMT  
		Size: 2.1 MB (2061143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1649ceaa78cd753f7e0e531e4ca48826f3a64f41737e47e4cd1065a35387225`  
		Last Modified: Tue, 10 Sep 2024 21:58:15 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:091a8d70d9442c91bd0101446dbb47cad394bd4ef75a1b97a4629566093bd09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b37a4e1038793c5d397d940cfb4522d4d3fc192ef0b1a67420569e5f1633cb`

```dockerfile
```

-	Layers:
	-	`sha256:433b41e4688cfc936e9091dc8454cdb685fce7ab238670bcf143f9f75cc07601`  
		Last Modified: Tue, 10 Sep 2024 21:58:13 GMT  
		Size: 3.1 MB (3068736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec21a542597bbb88f7d44bd99c732b514dce1125dcc13eaadc33ac6fc8f032b7`  
		Last Modified: Tue, 10 Sep 2024 21:58:13 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.24` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:958a899fd6d59761223f1fb1efb2ebc4ed4a73384466e23704a3670797ade4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (434036860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5815c5437fa0445caa8620ba2b8217f1410a3f5806962640977e543c5d7d051b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
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
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d75e0455933a035161db35f999c3e38bf8c0b81b4687dcfa767354d1e02686`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 38.2 MB (38181170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409621c5fec8bc93ed897492984b1c57bbb4cb33015f344547b8d29f6549521f`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd767bc60bb075e2cc749142d7b1d608eeed5e0fa6323d44ff0d4d420d9ce0e0`  
		Last Modified: Tue, 10 Sep 2024 22:05:35 GMT  
		Size: 367.8 MB (367815720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271b84cae8fc846f1fc4e9f5fdd18d8975821f44eae7fbd1c52f7dcc212e2beb`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0af25cfc27094aa8b071d3c0658799de71789ccf2a3ae0fdbe8b67fea7b40c1`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c236b104b5835c5b4ff568413054d2dadbf1c6871836caabb64374c875a4c`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01406b49c1cbd4db183311bc184f5d648dc91407218bcf39c163ee6fa261084`  
		Last Modified: Tue, 10 Sep 2024 22:05:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da609f70a91af0da3e33495522dadcb4eeb981148541519c5cfdaa7ae1848b8`  
		Last Modified: Tue, 10 Sep 2024 22:05:29 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca40dd4dcfc48e0e8f579fba1b7b451de44dc48d4d8412072e6a2b0ef5b03f`  
		Last Modified: Tue, 10 Sep 2024 22:05:30 GMT  
		Size: 2.1 MB (2061144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c7e4345bcfebdcf2a9d29e04f8d878a92f38564af865410a4ba3406396e19`  
		Last Modified: Tue, 10 Sep 2024 22:05:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:d2d6171d30ba98eeb64befaf0d70314e79060c604b488e16ed1faf902515ec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ae68588fa8363d2c49aee13cd1e8150b5bbe438b6fca0c84f92838803fef8`

```dockerfile
```

-	Layers:
	-	`sha256:be4e20bcc06547192e2fa021addb0bd9ced0582bd78580a0926e59791ea26109`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 3.1 MB (3068971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc30ebb1df5db46fdab69dc1a9e7d87e74e24c448dc73fed52379641d38eb8c6`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 32.2 KB (32197 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.2`

```console
$ docker pull logstash@sha256:87ae4db5a8807b81672af86348091ca73b984dd33ee0fda693d752eb51f0ae83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.2` - linux; amd64

```console
$ docker pull logstash@sha256:a38e0c587ac998ee84b14a456803a091d4b1bfe43420dc2c7dff06d42d1c9441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 MB (505591236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a091a35038168706c23879ff83d985adb4e958f1882e1b8334295e2be902f4fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0b72e7745c959916584771a67a473e6cd8bfab20ff13fd45fc2ab46bcc055a`  
		Last Modified: Thu, 26 Sep 2024 22:57:52 GMT  
		Size: 50.4 MB (50404324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de877ab5e4f8960fed903ee7999b3ec41464c4e75e8c4e3c1c0afd2082fc21a0`  
		Last Modified: Thu, 26 Sep 2024 22:57:51 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8640cc3e3ac433ff3b1c4059d4841b3e2179b803e8b2468f28d80f51f676916f`  
		Last Modified: Thu, 26 Sep 2024 22:57:59 GMT  
		Size: 421.6 MB (421611276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927d8d0a9a758e5c5b5f92acc2f13a16e451a80970786be0a234e0af2d4d6c44`  
		Last Modified: Thu, 26 Sep 2024 22:57:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8780a18905479c945a3168f9a5d78d56ede2884ef4c956efc3785e4965ccc8c8`  
		Last Modified: Thu, 26 Sep 2024 22:57:52 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3a806d66c958044365523af445c25efb5afbd5330a6ae91c24ac9adf14a14b`  
		Last Modified: Thu, 26 Sep 2024 22:57:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527df10869895aaeb16cb83f5436411a6bfd73d0d3345fb3c99c673bd4a2e480`  
		Last Modified: Thu, 26 Sep 2024 22:57:53 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66be2a6406f0ad5ddf8c9c24fbd8a3618c4bcf77d880a6011a72c8047abb42`  
		Last Modified: Thu, 26 Sep 2024 22:57:53 GMT  
		Size: 4.0 MB (3995870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affb7312389c605289417ede8da627683d1f77c502626fc7278f53a189fac3e`  
		Last Modified: Thu, 26 Sep 2024 22:57:54 GMT  
		Size: 2.1 MB (2061518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b86fe7d9365ec8d4a3ba7ce6082d79087901c2788e4c6e1b95b0097b99b77c5`  
		Last Modified: Thu, 26 Sep 2024 22:57:54 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:9b1bd67897b72259de029d67789550ad9a71abe4ffbd0d7bc4d4c2324485b8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084b9aa4f9a5154611a08433b892a8556ba4c081d1afaaf21e1d22dc7359ed96`

```dockerfile
```

-	Layers:
	-	`sha256:7d26cdeee771abe38216e662e6ab2cdb9506690f6776079574dd2e616ddf64ca`  
		Last Modified: Thu, 26 Sep 2024 22:57:51 GMT  
		Size: 3.4 MB (3397535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0a5da3cea891bd5e28f86a70bd979358fbfb75569ab0364232193fdb95710c`  
		Last Modified: Thu, 26 Sep 2024 22:57:51 GMT  
		Size: 34.3 KB (34317 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e3a481101eeccabaa8cdf74bf012ae048a279a326857e5fcae955f4de068f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.4 MB (490430530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd6ed9ec1d15386a66cb80c6703b2785eba6cdf1200515512f6416723bb31a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
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
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f0c809e52c4ad25ef616a794dacbaffc99ec873be4a4b04baaf67dfc06bf5`  
		Last Modified: Fri, 27 Sep 2024 04:37:29 GMT  
		Size: 38.7 MB (38738405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dbdc00fb7962d7932e5ccb71fa96442af5ade5bf7d057c782e20a24859ee4f`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a506ca864e096905155f02e3e0430bce2e068ca446b30568c432438c8cf9ee`  
		Last Modified: Fri, 27 Sep 2024 04:37:38 GMT  
		Size: 419.8 MB (419782836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78df8cd4298f3f636600a27e9b167656783d072065aa53ea2b3061d634301a6`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b062872a4e4db1d69e7722317c499014fcaf467f515cff22235aaa4b5b538a7`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a4873356872e077071617c540884310ba1e0f955f1aad25c87d8e8aa5b105c`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2c6a15f2db59377c38de9d5f82073700df93822922358274830ee9c0565f10`  
		Last Modified: Fri, 27 Sep 2024 04:37:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a273b9a11315cdc17431b229609fa56a0c1291143e594ba4b49786cba6d23`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 4.0 MB (3995873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827286224cca6e86d2e9969a38ca177cb6cbfa0dbd360dea7e502fac6c91b23e`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 1.9 MB (1932713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a8e4505935a4b7bfee050de877e4144dae459ebf2a400228642516c825310`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:0a05f4c01c284659e3f9156a55ebdcba72e5f33abad5487bac6cefc302cce890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8056d2f2b8f2277e162ff24a91537fa2d2dcd53df921630c9d4cb6cd6d15650d`

```dockerfile
```

-	Layers:
	-	`sha256:06b160024c2adf0fe5798c8c38abcbb2324da896f3774febb908667775c2e142`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 3.4 MB (3397145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d04485ead12dbc436d93b5e2da985e02cf9ad0bf7891f07778f65b38938043`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 34.6 KB (34581 bytes)  
		MIME: application/vnd.in-toto+json
