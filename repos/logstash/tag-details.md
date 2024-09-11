<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.24`](#logstash71724)
-	[`logstash:8.15.1`](#logstash8151)

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

## `logstash:8.15.1`

```console
$ docker pull logstash@sha256:8441647ce0abfc94f1ef93abcf2bfc7be220ce9a485608f84483fc30c7f0a7be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.1` - linux; amd64

```console
$ docker pull logstash@sha256:8f0a7473c31341aab78cac43bb6004192c806cf3799d1d1d46e2c712946a5070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 MB (505074787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43bf9243567ae5192cfba7aa6cec6737c96cd0c3584fa89ed33b23ab804fbb0`
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
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 05 Sep 2024 16:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.1 org.opencontainers.image.version=8.15.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-08-27T11:22:51+00:00 org.opencontainers.image.created=2024-08-27T11:22:51+00:00
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3964864a8a755ba1d20688172476c54b810d6d46deb8d666d36f25a11f49b`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 49.6 MB (49569249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b4af60cc5ba8c40111d54cd8b1b5dd74ba591f8b61b59bf88c4d249ed8311c`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f95e883db8d0019de1cd75cbc2f17905d10ccbff80c9401c4fb6fd109a20fd`  
		Last Modified: Thu, 05 Sep 2024 22:04:03 GMT  
		Size: 421.9 MB (421929826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88c8cb15e0a587bc7e25b2aab041b6e4140c42540df52ca834f15fd9b2ab54`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac626b2c2a6ab81c24dea47da04cca1d42419983c36a3e523d0466f6fb7e2c`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236776d6d73a7693a48a5b501f1cc254ef4cf26544e295d3f701008dd680b80`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d26797fc2c046466f7f52e1927799536e3b332b3486d07c263650e6140d92`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc49abbfa60dabe26a7f208d350bfbc71d1ad0f1cc598aff44397ffc150e30`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 4.0 MB (3996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e048852c7186b4402ae01a9d8470a142d76af961e3c3e5db9d6610e9871a1c0`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 2.1 MB (2061205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21d9a6cc95d2d4764ac8f7ee2653168942620d5777565e11c2d40c35a51eac`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.1` - unknown; unknown

```console
$ docker pull logstash@sha256:26639e0279894f026b57c038ac752f4ee0334a1257db7ebd026cca5a45942717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371aca4113f997fc41faa0da0f9576d59c4bda7af78c6a30115474877f1648b2`

```dockerfile
```

-	Layers:
	-	`sha256:d274f1203f6ab60fd59531f05ca3ababdade3970cea92deb39db6d52de7875a4`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 3.2 MB (3238794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f041eab31b6989a9290386290074a4e52f1d21b16a4994fe1d1c3594878af4`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 34.3 KB (34316 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3b16149c83377c0785eaaffd90175a04dfb1a9bd51095f69fbd6fa94c9cfda7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490048139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d045529c42f6a6a31260d9859a682821d1381cfd9043651255cd52ea15fb5d1`
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
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 05 Sep 2024 16:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.1 org.opencontainers.image.version=8.15.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-08-27T11:22:51+00:00 org.opencontainers.image.created=2024-08-27T11:22:51+00:00
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2664964c9665a54df6a105494b1078f790d0014d3fae1269b982310300cecd66`  
		Last Modified: Sat, 17 Aug 2024 03:07:02 GMT  
		Size: 38.0 MB (38036370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1daf002207d63c5b53c5faaaea31dcde78b569ada6176326e42f184e780b49`  
		Last Modified: Sat, 17 Aug 2024 03:07:01 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f89da44ca73a5a5252f89b19251df709a6ee274a4bee182e4a0c76ced70a1a5`  
		Last Modified: Thu, 05 Sep 2024 22:21:22 GMT  
		Size: 420.1 MB (420101771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a90c423044da8a865688f044fc7f10157aaa6979b7582ce57c6b5c769da6ab`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9843e4fa3be4fa1d5479e4caa3212e5a96ca7535693c7890440802ab94e702d1`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290fbb4bf3a4e70a05928439be48fe05caea232fadf5e4abc4c1d9b7f0e0102`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a58f9daa156317d55bfbcf884a4c9c8df9f491c68b5a9711094189cd4624d`  
		Last Modified: Thu, 05 Sep 2024 22:21:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383dd3c264aec39d030fc547091b48e0c3007b010996f0e5297d84ac84520793`  
		Last Modified: Thu, 05 Sep 2024 22:21:16 GMT  
		Size: 4.0 MB (3996251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb8baf7b7eeb5970af1da49e71e07a32a51064f4449e8beb7aa3edbde57d708`  
		Last Modified: Thu, 05 Sep 2024 22:21:15 GMT  
		Size: 1.9 MB (1933040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7f642fc48eccd14c9f2ac0383b4e39a0b23e52529572d803a665818b36ee11`  
		Last Modified: Thu, 05 Sep 2024 22:21:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.1` - unknown; unknown

```console
$ docker pull logstash@sha256:a1fb3bad9e5682ecd61eacca2d6f3d8140134ce071061a27d155cfb6e12950fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029f42a08374d117f5185efa67dd3ee0ec8c4cd4fd8836c5466d39bcec2c95b0`

```dockerfile
```

-	Layers:
	-	`sha256:164fc588f27d0d578d45a0c24450ae29daf1bbc3ee544a8a15218cc476124b82`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 3.2 MB (3239029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e23e2659c028d4cf21ea949286739823d27b62bd48b384fdc798b2d201b9657`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 34.6 KB (34581 bytes)  
		MIME: application/vnd.in-toto+json
