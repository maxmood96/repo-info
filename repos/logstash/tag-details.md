<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.23`](#logstash71723)
-	[`logstash:8.14.3`](#logstash8143)

## `logstash:7.17.23`

```console
$ docker pull logstash@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `logstash:8.14.3`

```console
$ docker pull logstash@sha256:58be793b375ae69d2f0556cfcf209ad7883fb9403a51e86f3b7e241974d3a150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.14.3` - linux; amd64

```console
$ docker pull logstash@sha256:7803925262ab6b0fec11195bb3d3909d1e3551862a1f256295a957432b5eabbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487925686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd517722cb451865e26ce9293ce4bba6526b2714f0cac25a0ef1c16406c8688f`
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
# Thu, 11 Jul 2024 08:06:13 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/logstash
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 08:06:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.3 org.opencontainers.image.version=8.14.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-04T08:40:49+00:00 org.opencontainers.image.created=2024-07-04T08:40:49+00:00
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05142f1716b5c2b0cad49ee9513a95edbd0234aec3a1c4b7980b135bff57739`  
		Last Modified: Thu, 11 Jul 2024 18:00:12 GMT  
		Size: 48.8 MB (48794718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6a9e444ad8eba69c22be12daca40dacdd87dc54ae2777236f36a08db08e2a`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9144288baa0d75c203e81c0e0b186166b208392c87573347c6ed1716d1e7fef3`  
		Last Modified: Thu, 11 Jul 2024 18:00:16 GMT  
		Size: 406.0 MB (406020032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fe7da2c6e7935231f26fd4d44c5e401c44f4dae5439152dcd0fc147061de8`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c3db855c2395828ccbaed0ba4ba1314f8f0516679ea9ccf5c7e019a9407691`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce58992c6c296589778835fb9f0bf5f798701a3a793721294f295f0a5cf7eb24`  
		Last Modified: Thu, 11 Jul 2024 18:00:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65bf565c093668804a4c1a931184e54dacb3e37526bca68e2704ca8f07166ee`  
		Last Modified: Thu, 11 Jul 2024 18:00:12 GMT  
		Size: 3.7 MB (3690582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377eda39052c2ed7c664f88c31a4f5acfef709b8e2ac21c35aef4f0bccf4f128`  
		Last Modified: Thu, 11 Jul 2024 18:00:12 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c02baf130b451bf3647a4f40c162ac0c2db41e9dba65d2490b81a6d992969`  
		Last Modified: Thu, 11 Jul 2024 18:00:13 GMT  
		Size: 1.9 MB (1902100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c4d54794c74551cafb11d32e3e9560e0110a9972bb0b1579921699109f16a6`  
		Last Modified: Thu, 11 Jul 2024 18:00:13 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.3` - unknown; unknown

```console
$ docker pull logstash@sha256:492e795d6f60d819719ad56f9cb97be9830117d932a8cd36477e98fc100e0853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee747dff9464d278219271fd667fbe1c6bb80f804db163d4fd2cfd5ccd5b95d`

```dockerfile
```

-	Layers:
	-	`sha256:53150e57fb1d79fee8d58c262ae139d2d3925e5832734c2e5f818988ae4884c4`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 3.1 MB (3137264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b118d39b81c00f6149affc65e24367648f66fcd2183cc4b21ed3621db20b7e`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 34.1 KB (34126 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.14.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f7b0ab46c15ec1c81a0969ca5779332911389d54026fa09d8c126660e6bcdf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.1 MB (474065131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a8a121139dc4c28fac26262f6bbc5cf0cc6ca9821c9155d3549b9adba5013`
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
# Thu, 11 Jul 2024 08:06:13 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/logstash
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 08:06:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.3 org.opencontainers.image.version=8.14.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-04T08:40:49+00:00 org.opencontainers.image.created=2024-07-04T08:40:49+00:00
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22016c99f4b1eaa60a0dbf418d06655ada9612082dcdd79893edc4df3ef6932a`  
		Last Modified: Mon, 08 Jul 2024 18:48:00 GMT  
		Size: 37.8 MB (37806478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81526eaa62eda1ab282198e2d9de62fb2795dd9974d9d2715d59cf7c8ddf01f`  
		Last Modified: Mon, 08 Jul 2024 18:47:59 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49982f270c379f5d0df8acbb550950dfc3560e1823627a287da16f515c0f3026`  
		Last Modified: Thu, 11 Jul 2024 18:08:11 GMT  
		Size: 404.8 MB (404799831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741972cbe8dfdc972e3f83d306cc6cf825882ba0335ede3f182d9f4c305d3289`  
		Last Modified: Thu, 11 Jul 2024 18:08:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dcaac9c57bdf6a04890b6afac6ed44e17349755f336448cbf20b04603a7dc9`  
		Last Modified: Thu, 11 Jul 2024 18:08:03 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05583f3f9088d713c1a46cce595ad1924220fac49a2229c0085e5460fc665f44`  
		Last Modified: Thu, 11 Jul 2024 18:08:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b37b4752defbe8eb900569c2a4b1e12cc0b9e56b860c990740be6b928106cc2`  
		Last Modified: Thu, 11 Jul 2024 18:08:05 GMT  
		Size: 3.7 MB (3690580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd0d094ff49be07b5ec16b78f53f273192152ff6cc010f9fc373be19b51fe35`  
		Last Modified: Thu, 11 Jul 2024 18:08:04 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859c6a6916ee5fcd4a0e54c16a2f7c121afcf9fba369302f57e3db9826ed5ed3`  
		Last Modified: Thu, 11 Jul 2024 18:08:05 GMT  
		Size: 1.8 MB (1787530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270a7bd82bbf1693336f5b93e4f2997a98a21c3f02b1c6828af1698405ce617`  
		Last Modified: Thu, 11 Jul 2024 18:08:06 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.3` - unknown; unknown

```console
$ docker pull logstash@sha256:80e8ba2983c678927c4a29d4d551a7d87c7100a22cf494885bed9ef9b8f50082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6eb9c239d3886b518943eeb9aeacc3abf2b90ff9e422cbabf30473100e0309`

```dockerfile
```

-	Layers:
	-	`sha256:37694e54b275996baee2e2ec37734a3466a17efe902e75d50159b90c3b19694c`  
		Last Modified: Thu, 11 Jul 2024 18:08:03 GMT  
		Size: 3.1 MB (3137499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cbe23c58cb6358e450bacb090f15b5be300f5d56b9884d1accd8cf71ea0cd9`  
		Last Modified: Thu, 11 Jul 2024 18:08:03 GMT  
		Size: 34.4 KB (34392 bytes)  
		MIME: application/vnd.in-toto+json
