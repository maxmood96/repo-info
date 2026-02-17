<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.11`](#logstash81911)
-	[`logstash:9.2.5`](#logstash925)
-	[`logstash:9.3.0`](#logstash930)

## `logstash:8.19.11`

```console
$ docker pull logstash@sha256:076d49d87d57ac417cef34de98ad8e5ece562903b5e9c7bfeeb6b65a14939355
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.11` - linux; amd64

```console
$ docker pull logstash@sha256:ef55e1632d9467cb640bd94ba617f7aaa7a50faeacf51ce5ac7e2aeef696743c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.8 MB (526801439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b823e2949a7ee3e6ecdb3e4644ade39823579abd9ee52c928432d1fa5b65ba0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 17 Feb 2026 20:27:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 17 Feb 2026 20:28:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.11-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.11 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 17 Feb 2026 20:28:14 GMT
WORKDIR /usr/share/logstash
# Tue, 17 Feb 2026 20:28:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:28:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:28:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:28:15 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 17 Feb 2026 20:28:15 GMT
USER 1000
# Tue, 17 Feb 2026 20:28:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 17 Feb 2026 20:28:15 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.11 org.opencontainers.image.version=8.19.11 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-27T22:28:08+00:00 org.opencontainers.image.created=2026-01-27T22:28:08+00:00
# Tue, 17 Feb 2026 20:28:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fcab5e182d42eaa43188c855fca598f4a2752e2e5f37f695721b390064cb89`  
		Last Modified: Tue, 17 Feb 2026 20:28:54 GMT  
		Size: 52.7 MB (52735393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f7fe37ae347d83a30a7a4a9ac9cfb43c87883506ac6f3e160396f7ae57f85`  
		Last Modified: Tue, 17 Feb 2026 20:28:52 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396c9e770520a75579db7d8f067fb67d95970023ef567ab81d14b442ae1a7c8a`  
		Last Modified: Tue, 17 Feb 2026 20:29:01 GMT  
		Size: 444.1 MB (444070715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69b521bcf357484088667334ba2556e66eca4eeda1cac9583377ff27aaa4363`  
		Last Modified: Tue, 17 Feb 2026 20:28:52 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7f6bb4c653f8de6460530da20de51891b6aa9082d3bf6b316aad4828c2a6`  
		Last Modified: Tue, 17 Feb 2026 20:28:53 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a930e0b942a2b96dafb6a0d40c74234e7f6fc70000c71e576f214d1f9d6e9`  
		Last Modified: Tue, 17 Feb 2026 20:28:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547d81819236baa498037172fc88d4fc1b1cc0238b59d3d7b31f8d7b0b9e01f`  
		Last Modified: Tue, 17 Feb 2026 20:28:54 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6675029d547a03d87c9ed008af5d126737721f9e92a9fe86333b30424a0c943b`  
		Last Modified: Tue, 17 Feb 2026 20:28:54 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9398b1285c515d700674c1b0c587ec3fffe539d607f487c88b875b4a11277d`  
		Last Modified: Tue, 17 Feb 2026 20:28:56 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99833d46c84670386667348b268f38fa3b541d8c4b8aa5f9511470a04345a3f8`  
		Last Modified: Tue, 17 Feb 2026 20:28:56 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3acb7aef98c9d90eca76470f94b2f047e20b90cf01d4aae482d29093d5c6ac`  
		Last Modified: Tue, 17 Feb 2026 20:28:56 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.11` - unknown; unknown

```console
$ docker pull logstash@sha256:30b6cb370b9b8d564e60212d46cdf621b0d2d3589dd6ad275c6704fc3ed3e77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd90abd1c8f838f19afaed9f63af915bc2c97976abf0627c19acfd1f22fe5ab`

```dockerfile
```

-	Layers:
	-	`sha256:465f0d19aa93921add197ee10ebbaebce021cdd1fd225d7bb98b09604fb0ef40`  
		Last Modified: Tue, 17 Feb 2026 20:28:52 GMT  
		Size: 3.7 MB (3657104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7af88096796b124d87548241795db966d7f9630d0800c3db3a8764e8d67b34`  
		Last Modified: Tue, 17 Feb 2026 20:28:52 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.11` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:51e1969dafe9f1b231068eadcfe006d11684e7e89af817d7e065d3b402573f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528426029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc81d04cf5ca6295a14a12e8c0c6c51d67724089341ebfba7d290c7bd7806fa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:45 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 17 Feb 2026 20:26:46 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 17 Feb 2026 20:27:07 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.11-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.11 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
WORKDIR /usr/share/logstash
# Tue, 17 Feb 2026 20:27:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:27:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:27:08 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:27:08 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 17 Feb 2026 20:27:08 GMT
USER 1000
# Tue, 17 Feb 2026 20:27:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 17 Feb 2026 20:27:08 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.11 org.opencontainers.image.version=8.19.11 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-27T22:28:08+00:00 org.opencontainers.image.created=2026-01-27T22:28:08+00:00
# Tue, 17 Feb 2026 20:27:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347eac8ebd932104d4600efe0c7bb2b512baf928e0703a129be77d6d7243d86`  
		Last Modified: Tue, 17 Feb 2026 20:27:49 GMT  
		Size: 55.2 MB (55222132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0276f9bd9dab5250cfe43ff7f911b367418348c70662fb8f35bf64cbb0b7c`  
		Last Modified: Tue, 17 Feb 2026 20:27:47 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511b72008b05588768cc7f2fb9f3e8f00b1291599f39946e44b706ab6d04ce8`  
		Last Modified: Tue, 17 Feb 2026 20:27:56 GMT  
		Size: 444.1 MB (444071045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea049d463aa933505594b0e184607ed83deae9cb19f0f6a2bc053ec694d19388`  
		Last Modified: Tue, 17 Feb 2026 20:27:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82fa6badc045c28320167cae78521240947ff072b13c748fe8356efbc833c53`  
		Last Modified: Tue, 17 Feb 2026 20:27:48 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d04698c0d0ae8d55a4d9784e4b18a7d18f2ca221b03a996a79fa8ba656cf716`  
		Last Modified: Tue, 17 Feb 2026 20:27:48 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d914dce0bb9dc8f2ba82a63db3c08d7297ea556b1f6a1a8b7c808a0a5d0fcd3`  
		Last Modified: Tue, 17 Feb 2026 20:27:49 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74181ee8de5fc6823a4c07ecfeb58cfde93d6e219fa7e8fec2082651d27965b`  
		Last Modified: Tue, 17 Feb 2026 20:27:49 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5856d82745131b67afd09a2b9f72cb07795558b5fdccba9925017c08f7bda24f`  
		Last Modified: Tue, 17 Feb 2026 20:27:50 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89910ad36dbb24a873bbd6b7a1eedd68cd581043925b7d7510be11f40701af04`  
		Last Modified: Tue, 17 Feb 2026 20:27:51 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c47bd293fae4431ada5256d31df910e99f8e6026af0f0bf7ea0fa710716635`  
		Last Modified: Tue, 17 Feb 2026 20:27:51 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.11` - unknown; unknown

```console
$ docker pull logstash@sha256:8036e6052230fc9ca4925e3c83e58a75b811092388cbf126e6cda45d55056df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3694126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6877dedb038d572bf6a1980b096197c1299975bae5b48cbbdce812980f401e50`

```dockerfile
```

-	Layers:
	-	`sha256:e39d030d9813bedbc7f314578f71cfe426d3f5d73bfb983bfa709328db598d26`  
		Last Modified: Tue, 17 Feb 2026 20:27:47 GMT  
		Size: 3.7 MB (3658153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236b944a510e942a4c940581c3c0772ac327432fbcd75952da8b5704fc34ae7b`  
		Last Modified: Tue, 17 Feb 2026 20:27:47 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.5`

```console
$ docker pull logstash@sha256:bc2c92a2c127cbd37bfd46c68c6bed97675214abc5d82ae17b131bbfac2bb2f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.5` - linux; amd64

```console
$ docker pull logstash@sha256:f449e699739abca359cfb256b6bfd0ad0925b8ebe9374a54c5faa73cfc4abc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 MB (488799799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301d53b4defc2a52f52627b9f1c82bdab20ab2b8328ae6482f0ca1d50fafb30a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:16 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:16 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:51:04 GMT
USER 1000
# Thu, 05 Feb 2026 19:51:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:51:04 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:51:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc15a47de2ee719eecca0645d1aa0f7ce1013c8a44e00723938cd6d3580ea50`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 5.2 MB (5159975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc45e5b08a7a72d1a23e8ce47e047ddeae613a6628b51c1f8374bd72dd97343`  
		Last Modified: Thu, 05 Feb 2026 19:51:49 GMT  
		Size: 443.3 MB (443319199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6b3a3831a73abe84f75305ad66e280bac9b05e6ff5785a690e49dd3018f23b`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b3e6ea6a75512bf52e11612ba7ddd2ed0d2eeb4602fce67a1e74abcae9741`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9714590e469d7b75e04754f66318ea7cbd2b0ce6791932a526213dc0b7ee2ce0`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c38225e2f692ff02f7dbcccf220d000e6c30ce2ec52b3bdd3186afc0bf5abc`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46d6b1ea6436ed337b38fe61efcadb527a308e9cee4f9ba9d0963cdf29127e9`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847f3c6d5ccc3d1555e9ad0fe3ccf442b4a40ac916209d372ee581aa31bcd9a`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aeffc7ef03c787ab0534c11cb8e4f496e0b784d6aa7a2cbdbd999f260537d8`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:ec59245a9ad91f937972607a65ea3c0958d8e7b76a3e4627ec1227b3e4db9a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c8613926e6cb474c9da073f928fc222db25385e0ca07d8085953f6f9fdb99`

```dockerfile
```

-	Layers:
	-	`sha256:6bce3a9f36536e8d16f07bc2fac9180933ce0b7476d0c24a17054856ff550b18`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 2.1 MB (2103734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3801c2c3b4b98188381172c76ccd0cf2721b4a70bad7068c11f9f3e860e690`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:934239a2ef67b1437a628b92d23548f03ce2c0739d50fde22450a99004a154d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486956679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d838f05b76a3bf6c735de2a70b9b87c9a17ef56f886cfc8cb7e683281e7b26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:01 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:01 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:01 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:03 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:50:50 GMT
USER 1000
# Thu, 05 Feb 2026 19:50:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:50:50 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:50:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a40b6d59de3ec92b630156b5cb394534adb05a60aa7bc1bc20f854580bd08f`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 5.2 MB (5155914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d7df42f84c27e0419769fc61f2958860ad2b4b6a7c81155c94b93e5befac`  
		Last Modified: Thu, 05 Feb 2026 19:51:45 GMT  
		Size: 443.3 MB (443320227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b651f6a06edb773b6a2649baf0ae564943c83ae3c9d9990bdd43f681ec5c618`  
		Last Modified: Thu, 05 Feb 2026 19:51:28 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09d3a2ba7ff6a04b1306be87ab0fa21b71dc284e027bddf698717e8db17f2d8`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b805f59ec599796ae2b80ab63a10b72316741b1ce4963ef44af5d64a3a57d13`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d196d0a2980a1739d93180a40f787922b4969e02a2b0079ae908b663d0318`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6dd0e3dad83410f811bc6df2168f5fc20d04bad901824567353592451fa123`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab613139944f2809f5c9e1782f1f804d45b26a306f9a9685e1df38dcc74b3373`  
		Last Modified: Thu, 05 Feb 2026 19:51:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1bab64257e233dc79b1db714deff016b706eee49da0fb0243c7ca7092e4b47`  
		Last Modified: Thu, 05 Feb 2026 19:51:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:3c667bfa69adc2d2dad41e56b0ba2fc785a267ee2bed723ec34f1b30e34ac6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b1af19e969298e5e60fb43e02de93fcde8c40cb54ba93b46df9a5bd7c11adf`

```dockerfile
```

-	Layers:
	-	`sha256:05ce9f4ed79fe75f4a0ca087ee8a7fa03ea037057ac69ca5564fba9a925f3ca1`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 2.1 MB (2104928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa1e384088d733604b07c22983c3a7e7aa87b3bfeb932e8b2dd1af46c00802c`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.0`

```console
$ docker pull logstash@sha256:6741e21f63dae474a677e5c4727e0b4f7008cbd585eed85f211219c9b107ee19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.0` - linux; amd64

```console
$ docker pull logstash@sha256:e8128b85679ba543248120c5b8d6cf116ff3f79de16f4e463dd08dd5647a8e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504219219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61b243620ef67c73e14594dbddc073b132f7ad7ec8ae72f14ce07cff4a26f5a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:17 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:17 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:17 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:19 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:51:06 GMT
USER 1000
# Thu, 05 Feb 2026 19:51:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:51:06 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:51:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b2689788ebfd5033405dad057f7f828959baefa46b40db565df6fc5928ab16`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 5.2 MB (5160008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb298610cacf5b9ccbb214fe20c1fd2b372821a880b2f298e7462b707fc8dd`  
		Last Modified: Thu, 05 Feb 2026 19:51:47 GMT  
		Size: 458.7 MB (458738586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9548a120e0e61e72f3426385f33e952cadc18835371fab7355ddffea2f382ce`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc07b8e6681b171d8a7ea1d33caaa818250d700897d9be91a65add3322ca000`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd13efb788f02be74845036d469e1e38e6b03c40ece1786898afe4d056faa5f`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a622c853b703330881b883f31cc3839d475fc1b099397a74c9adb59b5b3bc6`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aaea3b01583d175b7cc76b5eb9d709655bbcce1bc0ddbae35d5f730d766df5`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4420e691c7c8cb17f44d3f1df06fa8abe632281bd888212526506285b360909`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50de45f97989054a16d1516fa7e2fd7a4346634d55b148c2573c850de6717fb`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:5e500d44a15a2e3fb7f8f5a9e60d35e70c9e722fe027786c4387cdd86d8834d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2114241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb4527f25834e5d7115308668be42100a779b797b645d190a999b7c5e982eb0`

```dockerfile
```

-	Layers:
	-	`sha256:584f719dca0e3e123d69d1219b9da541dd2f4e365cf62139446795675ef774bb`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 2.1 MB (2084041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5695628b4b2648245a0bc05306e3d824e725211acbb64fc0eb3839364c1e52`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e968fcea8a0923abd564ad9623124b2b61836df5fddf219a1a01efa7542b88d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502374710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ef4931fc4da3da531624b49628c6d275e3aa52624d1208cfc868b55614cd20`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:08 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:08 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:50:58 GMT
USER 1000
# Thu, 05 Feb 2026 19:50:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:50:58 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:50:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659990beb4076fb1c2255e471dc232922a40b125ee338a3addbf45e59c24072f`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 5.2 MB (5155898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c38274ccb2f2d29b80601d57a1bd06495a78f56f5bcb69042d0909ad8d5772d`  
		Last Modified: Thu, 05 Feb 2026 19:51:44 GMT  
		Size: 458.7 MB (458738265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0d452a8ae93dcd875db5adea9763f53ab7f90b7383ae396bd30bcbbe27f01d`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 6.3 KB (6292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a567133787ce2f900500f69c2a1e25011442e85d0a018691ffea4b51d1d453`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12111806aba0e8b018fb4c1be78b1bba4bd0698898bb9e7539f9d736179eb32f`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768604b9469e20096f8e9496f4c6c4cb8071667f79a788da7516e7a30658d89`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd3a4745e79a8dd0282c12330cd4859a9d077940118e8b4d6de0449465a927`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118c00e5e26a6d18560b844e32f4e32686403e66931ed9213f22ac998d13f9f`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ae2e419a2a8c30309f90e0d927a239a49a76f61ea82c0094616fa71ac19bc`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:e516a7e0ba11689715f4060034720480a31b5103b15988fefaca002d2b5aa8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b7417a8391c6fa9c274924842da7610aae9f8fd18c372f91d5dad3a48a1306`

```dockerfile
```

-	Layers:
	-	`sha256:3da0bdb537e9b6c4fc9f55ebc893a8ee45df7512aaad5a2e397c42769eb19840`  
		Last Modified: Thu, 05 Feb 2026 19:51:35 GMT  
		Size: 2.1 MB (2085235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa40faa93363455c6a7ef5663d1de1256f56a12eeb0d83dbbec7bec24a9a2ae`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
