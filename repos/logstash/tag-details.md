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
$ docker pull logstash@sha256:8f2bf2d7303ae62930024049e0d8b3336635afc042964b93a8a4db55f55f5a12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.5` - linux; amd64

```console
$ docker pull logstash@sha256:ffc8c226d9a33a64a4418e8169c12dc282698b10d2e26abaec5ed0cef8f2917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 MB (488774812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea505eb4d119ee1e8d0b97258cfa783cab11df2be09decf5aa2102be6e44fc77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:21 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:20:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:20:21 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Feb 2026 19:20:21 GMT
WORKDIR /usr/share
# Wed, 18 Feb 2026 19:20:23 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 18 Feb 2026 19:21:11 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 18 Feb 2026 19:21:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 18 Feb 2026 19:21:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:21:12 GMT
WORKDIR /usr/share/logstash
# Wed, 18 Feb 2026 19:21:12 GMT
USER 1000
# Wed, 18 Feb 2026 19:21:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 18 Feb 2026 19:21:12 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 18 Feb 2026 19:21:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28585a642d2feb09a2098ab5a305d9ad3f37206e5f74d8001bd6e838be22dc35`  
		Last Modified: Wed, 18 Feb 2026 19:21:46 GMT  
		Size: 5.2 MB (5157485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad0ba9e377630a8d054b129296d97580c79a48ccfa3ae5d1d2e46ada563a5f9`  
		Last Modified: Wed, 18 Feb 2026 19:21:54 GMT  
		Size: 443.3 MB (443318994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40753a7823e270b35ebc2a67f30130f0b8e41a9e6ebf7f4185522dec488edabd`  
		Last Modified: Wed, 18 Feb 2026 19:21:46 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243272791459df80b593ba7389fb2c49cd36e4a60ccce577bac33afd2e586ab0`  
		Last Modified: Wed, 18 Feb 2026 19:21:46 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe14ee4ada7cc6f741c754f8a03a92586064261cf53427cc6ff11a113c1257`  
		Last Modified: Wed, 18 Feb 2026 19:21:47 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2803597c07053cceb4ad211b528c05080ba615d9dbecfa9758412f153189581`  
		Last Modified: Wed, 18 Feb 2026 19:21:47 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab5882b20e96813f7ecea24871a3ccda66c3e42da7731614f4a6016ea78033`  
		Last Modified: Wed, 18 Feb 2026 19:21:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce219c01c6848a3368f5a9ad0688ad6ae88921b8f6ed8e736e4649c088f64c0`  
		Last Modified: Wed, 18 Feb 2026 19:21:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478e46cca42ba5c1d6a4126877fc16301642659c5840f9b4861fdbf8a2cb019a`  
		Last Modified: Wed, 18 Feb 2026 19:21:48 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:ec48ca33576714a4ae51cc1e6369df3800b41e6aeb8d50edaeb5cee0d37fd32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e0a7b1eedec8a8c74deb7ca274e9fe3ad30289e5076299e027f403c2fa8cfc`

```dockerfile
```

-	Layers:
	-	`sha256:8f11b2c5c982c9694192e62d808e80deb46b74dd2ba9402f9117daa4af25cd27`  
		Last Modified: Wed, 18 Feb 2026 19:21:46 GMT  
		Size: 2.1 MB (2103744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657cd838eb0875a37ace1aeaabc4e1cf158e6177c938e4961b3ecd01065b68f6`  
		Last Modified: Wed, 18 Feb 2026 19:21:45 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f8b0a9e6eceb80583bbd61869b8f51891522ef18250e66287b1166a33882f8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 MB (486942703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bebf54bb44060dbe2975c6e1af8a867c068cb7b297d7914f3ca04cbbce68d69`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:18:48 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:18:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:18:48 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Feb 2026 19:18:48 GMT
WORKDIR /usr/share
# Wed, 18 Feb 2026 19:18:50 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:19:20 GMT
WORKDIR /usr/share/logstash
# Wed, 18 Feb 2026 19:19:20 GMT
USER 1000
# Wed, 18 Feb 2026 19:19:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 18 Feb 2026 19:19:20 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 18 Feb 2026 19:19:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffbc6ba7d4aa61222efa20a8816a6d2d679ae93dfcfa11c7e2b18c11598766a`  
		Last Modified: Wed, 18 Feb 2026 19:19:57 GMT  
		Size: 5.2 MB (5155540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43ca3f44d589776ada31ba3fcb7336afb2c05524cb35a589146ab1925ff0d8`  
		Last Modified: Wed, 18 Feb 2026 19:20:05 GMT  
		Size: 443.3 MB (443319906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980a47b60b1722590701b5a421ed799c2a42630fc465ea2cd37e12635267af0`  
		Last Modified: Wed, 18 Feb 2026 19:19:56 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baba5bd9ab417d7ece3cfa4c45989ccd71762c24907dcb43e2da5d0cbc2247c`  
		Last Modified: Wed, 18 Feb 2026 19:19:56 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8965da3437ac0feed79b7956ab563fe5de636bce8cacc59caa01f6a3f41175`  
		Last Modified: Wed, 18 Feb 2026 19:19:58 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae14bf9a1db20e3399957c75253722f9c22bda69bdc956fa7a7959d4bee05704`  
		Last Modified: Wed, 18 Feb 2026 19:19:58 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7feef87970579d1ff5e81b085d6c9c515536e63805d095cd7960dca18a21fed`  
		Last Modified: Wed, 18 Feb 2026 19:19:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b154ffe93aa66d0c39dc75f47e4302890fcc6193b093e77826861ad724b48b2b`  
		Last Modified: Wed, 18 Feb 2026 19:19:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc7f03a1f3125f62ef572294afdb870f7389a1bd7841ff90951f2e32a7e67d7`  
		Last Modified: Wed, 18 Feb 2026 19:19:59 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:79b2034d636e291e73911463f5bc686cc27594aabab0020a5d88766cab2d8c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902f70124f2af5a826369a41105a895170e6a5ab1a89ea53806903892a608310`

```dockerfile
```

-	Layers:
	-	`sha256:df865480cfb03c3cbdaba965d23e4bc2a942c4e8e0a85b1b27c3e13177c23555`  
		Last Modified: Wed, 18 Feb 2026 19:19:56 GMT  
		Size: 2.1 MB (2104938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5e970c132c14d90ec72d307ef088d3b9d29fe4878508e6d740e4c7bfd382c9`  
		Last Modified: Wed, 18 Feb 2026 19:19:56 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.0`

```console
$ docker pull logstash@sha256:cf833a7a5c063badd2ec482d07ae56ea949c3682b072be03e2085027747a2a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.0` - linux; amd64

```console
$ docker pull logstash@sha256:a3d1b66babf68cdabfc2a2406b8f7f7bd608a4165fc97b850603c7ce3ae5582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504194219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6775c1557566c96d338038138f5b25c73a9c08cee15785abb1e49688518da893`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:31 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:20:31 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:20:31 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Feb 2026 19:20:31 GMT
WORKDIR /usr/share
# Wed, 18 Feb 2026 19:20:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 18 Feb 2026 19:21:22 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:21:23 GMT
WORKDIR /usr/share/logstash
# Wed, 18 Feb 2026 19:21:23 GMT
USER 1000
# Wed, 18 Feb 2026 19:21:23 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 18 Feb 2026 19:21:23 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 18 Feb 2026 19:21:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e706d2f9ab1def4aa718b75ce7dd00b36dc2a4d57aa9811e9d5705b2951f446d`  
		Last Modified: Wed, 18 Feb 2026 19:21:59 GMT  
		Size: 5.2 MB (5157487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d380ab25a8789cad0d2908abcbd957dbcdd56311967911f2af2532ed81849549`  
		Last Modified: Wed, 18 Feb 2026 19:22:08 GMT  
		Size: 458.7 MB (458738392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea978f984e5a9029a450662dc8c6eb336e711bcb0a11454459ba7eddcbd60068`  
		Last Modified: Wed, 18 Feb 2026 19:21:59 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f3486599ff81586135928c7a56bb3a86bdc8d3c9297c66217290b68320d6c`  
		Last Modified: Wed, 18 Feb 2026 19:21:59 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884672b89afd4801991efb7a78486cc62683a7a6c9f1587573c01cc70d8c524`  
		Last Modified: Wed, 18 Feb 2026 19:22:00 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c448ecfcfe7785cab742bfd1b81b74f389ca321a9859e7aa325c63b7a1f3c358`  
		Last Modified: Wed, 18 Feb 2026 19:22:00 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086d56d1f111dbd79cb349f6955eff23347684f88480273ad2a5994f3ba6561`  
		Last Modified: Wed, 18 Feb 2026 19:22:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534f67901434c5e0633c56317581cf10d9f62a281b03c412816cb0509fe74cd`  
		Last Modified: Wed, 18 Feb 2026 19:22:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229aa8ab7b92e92d7918026e4cf9bce056270359a6023ba30a63a876f8bdd39`  
		Last Modified: Wed, 18 Feb 2026 19:22:01 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:aeeb531c314e781d17345be5e2ac46c02240d0ead617cc784671aedaf5090f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2114251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96557befb3cbb9813eadab33c4dc951a99fb9cf2ef958691cbb26c194ae630ad`

```dockerfile
```

-	Layers:
	-	`sha256:d7906cbd5b477ac31e0f75ac9c605eb3e326ed35e7d44297a94be70b2f5c46de`  
		Last Modified: Wed, 18 Feb 2026 19:21:59 GMT  
		Size: 2.1 MB (2084051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82347692162cd0ad0820ad82d81d03ec78ee8fc06b2687e3766914deb661fcfa`  
		Last Modified: Wed, 18 Feb 2026 19:21:59 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:72784c728f69ce512f650d36c58b864756b984d3994b206e68f156cf5db323d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502361506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9492724a97b9d1ac3e416743b6d6f47715fff4d3f098c48d8a0cf45f16914`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:29 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:19:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:19:29 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Feb 2026 19:19:29 GMT
WORKDIR /usr/share
# Wed, 18 Feb 2026 19:19:31 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:20:01 GMT
WORKDIR /usr/share/logstash
# Wed, 18 Feb 2026 19:20:01 GMT
USER 1000
# Wed, 18 Feb 2026 19:20:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 18 Feb 2026 19:20:01 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 18 Feb 2026 19:20:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691fc9053ebfdbf43d5103e7775f216966523a3ca7ec749f3633695c21e945e0`  
		Last Modified: Wed, 18 Feb 2026 19:20:39 GMT  
		Size: 5.2 MB (5155553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218f597cf05abf9bffdaa7242349364d6588aa87f431ac15be9ab5d63bf5b528`  
		Last Modified: Wed, 18 Feb 2026 19:20:47 GMT  
		Size: 458.7 MB (458738680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc7dbc1c58274dc566558780518f20cd99037fa9d57ab8a16f3f9ffbb3264c2`  
		Last Modified: Wed, 18 Feb 2026 19:20:38 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c9dc055efa9faa239b7f95b291827acaf1e9cb09c1245291aa7e62b3131fa6`  
		Last Modified: Wed, 18 Feb 2026 19:20:38 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118cddd478398e58fa4e20ac9644877cfaec9e1deb3f0ce518bfcd967f7a5356`  
		Last Modified: Wed, 18 Feb 2026 19:20:39 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235cb8b19894951ba4dbfc26d881be2caaeb2211f10fe1cf2b45fc5e1c6bc17`  
		Last Modified: Wed, 18 Feb 2026 19:20:40 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0a587e1c15e7ea36dde9021cf6269d5ff0593f88d897d5622a2ced70489bc4`  
		Last Modified: Wed, 18 Feb 2026 19:20:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793832aa2134ddb5cd9050fa6acd6ad762280d0abda664a0c4b182cdcf30115e`  
		Last Modified: Wed, 18 Feb 2026 19:20:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf853c1f452b99346235b4e499cc91224be8d68b6c8f620358670037ebf332e4`  
		Last Modified: Wed, 18 Feb 2026 19:20:41 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:63aea9048af4c6bf6a1b8fa15726247408319a04eb3b9901a1c956263ad60663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa47c6e33ec4b7dcffca17b4b79aa7b0a0761bf64d2640d6b168f69146f86b8`

```dockerfile
```

-	Layers:
	-	`sha256:7d6051b6dd1910cbfd57dfd64599634a1b281ea376b6f7e8352dbbcb21e08f46`  
		Last Modified: Wed, 18 Feb 2026 19:20:38 GMT  
		Size: 2.1 MB (2085245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d03664b0b322e63c32bb3726f2c7a32e3c79116174292ae66d41d538fe9244`  
		Last Modified: Wed, 18 Feb 2026 19:20:38 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
