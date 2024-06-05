<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.21`](#logstash71721)
-	[`logstash:8.13.4`](#logstash8134)

## `logstash:7.17.21`

```console
$ docker pull logstash@sha256:8ed42ec52f38018da43cf45d68f1e638564f8f5c09b0a8600fa6e6a521192d7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.21` - linux; amd64

```console
$ docker pull logstash@sha256:4b9f4948bcc76efb632c0dcc057a00823d72f88d7f0f99b49f2a203d4b6faac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.0 MB (444979767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ef8065975401a5f32e2e561f2c327bd0094b92bcf7db001c86dd39bd44d4fa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cba70f324522678988bcb1f0d546469f7c4a7173b759f657071aa32670a8957`  
		Last Modified: Wed, 05 Jun 2024 02:20:51 GMT  
		Size: 48.2 MB (48226494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec42bb6466ee8c7e6aed53169737ab94a39a0bed4cb76b22d1d61fd876c6771`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80afdc55cdcd137a2efa41de9e2f4aa4f2686d7a60dafe91f705e6a37623cc2`  
		Last Modified: Wed, 05 Jun 2024 02:20:55 GMT  
		Size: 367.3 MB (367333713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c1060cc1577a519741f50cbf339da73742e0a90ecdeaeea5d067758296edbb`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911313e6a40712ca5a2508a698d1d30cd4ffc5dd3c41931985f6f171d8f51071`  
		Last Modified: Wed, 05 Jun 2024 02:20:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf863567fb05da126fb42f0353b2742229b053d4a729af3fecf3587255ee98b`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf0392f4ba0d47d2bbff044ea2ae0ee404deca48f1d31360de6e93d9a46733`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd44c39d3df2e6b2d4c87ffd19725892e5b677fd2e8dad5aa7e50a5583ea7a7`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e234b0088f10c914e7675c6b79f8b5946ed9eb4f9c807da765283104b164d15`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 1.9 MB (1902745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba34c737e8b3bfea312e2f1433d01fa6ed2c1eae51a7106a88cf7561227f2a`  
		Last Modified: Wed, 05 Jun 2024 02:20:53 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f69d82d74007b90acc9d3e3cafa6f97387341be0f7f57e7eb8263a18b20f040`  
		Last Modified: Wed, 05 Jun 2024 02:20:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:a819e5be1382a3ea273146366f9e1227677e8af902e140a8af8b22555cb5aa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d01b66270560989a4acba7d7de47eb8b525fc6916aa1871040b0d9083d71187`

```dockerfile
```

-	Layers:
	-	`sha256:1dab30abb4ac639a5dbf858c6f58abf7be4e6d97b43ea51de202a3ff59d27002`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 3.0 MB (2979398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4769e0138cd16306efacaedd4dafd0658efc6f30aa5acc84d290748ecf6fd061`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 32.0 KB (32013 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.21` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c4eacbb75b8c0120edf026f860c8ef6f8723d894cfe8979661b7ee46192b4bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429323818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67109d704ba19b4fb4eedca24024bfa8484d9038ce8820b86065b7ed33c8a1e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421bb92fcde17234c65ded00edea0a5733401dbc11f167efe6cfc7199320932d`  
		Last Modified: Thu, 02 May 2024 11:53:33 GMT  
		Size: 37.4 MB (37393222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd9bd267d032bf3ee2a77d78f3005e8ea29651716b45de12034591f0c189473`  
		Last Modified: Thu, 02 May 2024 11:53:32 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9a4d4a25fca1775b4d604ec707fc6407f1444741c9d7f4fbb544a3a6c177c0`  
		Last Modified: Thu, 02 May 2024 18:17:41 GMT  
		Size: 364.0 MB (364047750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c03f6f420f1cdc193282e52088dab3198425efdcbbb1b55e7eaef934edcf82`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aef8ebf5d97a618116b78cb54269e70c3bcbcfc5eccc8a959b60cec4ec375a`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c140f8d3231974bfe85cffe71469cf2fb005a866aa951bd193bab71ab7b287`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2707967f8be88e72b6e7fbb42c57e6148aac6ebace5f68be5965f390dc4a6b5`  
		Last Modified: Thu, 02 May 2024 18:17:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842547debd7494a508b24beb3e960da836022b0cab7685ce3e7218ef7f946400`  
		Last Modified: Thu, 02 May 2024 18:17:35 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54365b377fdd20acbc04ac5b308b301176eeda7174ecc65f1f646864f37a2b8c`  
		Last Modified: Thu, 02 May 2024 18:17:36 GMT  
		Size: 1.9 MB (1902742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442fa5deb3208971fd720cac18bd0f60701dd84f3c1440b8474911576fac58b`  
		Last Modified: Thu, 02 May 2024 18:17:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:eac24405411e4ce76865b276c7d3229b1b25c6cc5095bcd7cf10f5d2239e65c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910ac514591de5d2895a8a28fb7c88502d882232161cc6fc94547760e1e73984`

```dockerfile
```

-	Layers:
	-	`sha256:49c7172e5e798ea5538aaa8ddc9ced9c37d53eb4488720862adbe5fb0d100f1c`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 3.0 MB (2978688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94c99c8ceeeb65591dc9cd35f188c0165dbc6c17f107284987e0a77b7ea9b24`  
		Last Modified: Thu, 02 May 2024 18:17:33 GMT  
		Size: 32.0 KB (32016 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.4`

```console
$ docker pull logstash@sha256:cb287e5632fb8709e1d504ee0fdb56b3e27ee7864454f3a604da4b3c4e40ed6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.13.4` - linux; amd64

```console
$ docker pull logstash@sha256:2523d4633b59b6e2f2726a3882679e8b0cc9b7b51a54fa80f17e5e0b7a533dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.6 MB (486591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de32da14527f5a997afacd7cefd948a6739f64df3828a1e8f7daac9e73d04b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 09 May 2024 12:07:29 GMT
ARG RELEASE
# Thu, 09 May 2024 12:07:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 09 May 2024 12:07:29 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 09 May 2024 12:07:29 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.13.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/logstash
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 09 May 2024 12:07:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 09 May 2024 12:07:29 GMT
USER 1000
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.4 org.opencontainers.image.version=8.13.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-06T13:27:14+00:00 org.opencontainers.image.created=2024-05-06T13:27:14+00:00
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58aede7421fd02b5629b9f32e87b052f67c345a8e58a6df2a679f50753a26e2`  
		Last Modified: Wed, 05 Jun 2024 02:21:04 GMT  
		Size: 48.2 MB (48235940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467b02f73080ea687a79fbc9758d0ccfb910e4646d3c935041ba3bba66424f4`  
		Last Modified: Wed, 05 Jun 2024 02:21:03 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c668235390b1e1bd88e1de716f9a54b1dcea4a3bcfdf6ea1b38f5c72930df36`  
		Last Modified: Wed, 05 Jun 2024 02:21:09 GMT  
		Size: 405.2 MB (405244083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7525f19dcea25f96c359d48a89759d1415cf3c84008faea301aeb5a530c8ecc`  
		Last Modified: Wed, 05 Jun 2024 02:21:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2055ef791099b622ccc911ecaebc9154bb3456cb64279d6b639c72cad9fd1dc9`  
		Last Modified: Wed, 05 Jun 2024 02:21:04 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea5386cbdfa2d0a0b19926726a719b5660d463a337f87629a61070ced249db2`  
		Last Modified: Wed, 05 Jun 2024 02:21:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509edd0f9e4dd36d3be1395714695782bd5f089c7644027680b74eb99a1aa46a`  
		Last Modified: Wed, 05 Jun 2024 02:21:05 GMT  
		Size: 3.7 MB (3689843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c3d8e4e809166b6aeb150baf68ff9bffa5b0a6979da8162441d9f79b489d2`  
		Last Modified: Wed, 05 Jun 2024 02:21:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0144771d5d4fad450efb417539d34fabcd8c068fb62944929384dd3b568da25a`  
		Last Modified: Wed, 05 Jun 2024 02:21:05 GMT  
		Size: 1.9 MB (1902236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb27d8feddc2844d4bb02437916a5408a17654796e1a674c2c01addb1b71fc8e`  
		Last Modified: Wed, 05 Jun 2024 02:21:06 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ccead4f3b33fc543dc34e3a7f6c00af5cb15cbe2020d4f15e55733cb6afddd`  
		Last Modified: Wed, 05 Jun 2024 02:21:06 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.4` - unknown; unknown

```console
$ docker pull logstash@sha256:0a02b1d6e3ac8f408065faae9e64d1f977de6ee41e01b368283e4f222f1003e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657c0810bf2bd804cd59efba7a3ab1a29d10d0632460cb069442638e6ec64ee1`

```dockerfile
```

-	Layers:
	-	`sha256:8948c234f137dc64f6ede8bb538a59c5ec97b3cc651a14cd96b874507628f605`  
		Last Modified: Wed, 05 Jun 2024 02:21:03 GMT  
		Size: 3.1 MB (3126182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce914ed8df0c0ddd3f513bec16df9c9a8b10c6c995b555007eeab2a223451f7b`  
		Last Modified: Wed, 05 Jun 2024 02:21:03 GMT  
		Size: 34.1 KB (34079 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.13.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2a8f5caf7f98688e6f8b76a7b2c90c1769d73a702fd8636cffabe10e78dff6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.9 MB (472943389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5ecfaab43691199a5c4e99b8aa260f1846d8b3320ca52ffdcdcd913b07071c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.13.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/logstash
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 09 May 2024 12:07:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 09 May 2024 12:07:29 GMT
USER 1000
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.4 org.opencontainers.image.version=8.13.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-06T13:27:14+00:00 org.opencontainers.image.created=2024-05-06T13:27:14+00:00
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf2cde5e60c8329ed9b0b0b574ae72031616bc3ea206ab612d15fe96c1e02e`  
		Last Modified: Wed, 08 May 2024 01:25:28 GMT  
		Size: 37.5 MB (37457136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b5fa041d75f5d97e054f1749bd2bf2c8a5075a86511d83204c98af7c546ce`  
		Last Modified: Wed, 08 May 2024 01:25:26 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e9d4c44bb1c7c29bea025ae728db4153753646ccd862f1532083f7518dd620`  
		Last Modified: Thu, 09 May 2024 17:23:05 GMT  
		Size: 404.0 MB (404027704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acafd024b2a038db9f86b1304cad79c3bce13a4a1e5eae58d7de01125db76045`  
		Last Modified: Thu, 09 May 2024 17:22:55 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ac430a225f4d2a1dfa3e8d8ad452f265df17e4730a9a4c0dba08e9b3978f1`  
		Last Modified: Thu, 09 May 2024 17:22:55 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f737c1eb70d515d772891fb4871c1108f381d6eb4c133d804579262ab6a9f7`  
		Last Modified: Thu, 09 May 2024 17:22:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a035fe49b2f36478f5941b8d47bfbedfeef00578e8c6efe9dfeffdb7c64d0a`  
		Last Modified: Thu, 09 May 2024 17:22:56 GMT  
		Size: 3.7 MB (3689826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac67dad44e75727037f61943b3f3416be3db3aae7c89b6012fe85933f7d25e6`  
		Last Modified: Thu, 09 May 2024 17:22:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff7c295f8d51cd8df975a919750579e3399070078a086a870d60e35914b95d`  
		Last Modified: Thu, 09 May 2024 17:22:57 GMT  
		Size: 1.8 MB (1786739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abee51279e5f7accaed156dd630a965f49d8fc4fc6e8576b24e746f213c2ce93`  
		Last Modified: Thu, 09 May 2024 17:22:57 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.4` - unknown; unknown

```console
$ docker pull logstash@sha256:a5a96c03d518be70cebf05e7b95838357e089c1d60f288caac48cdcfd133a42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8db4b95fde9c64977acf0dd585cbbf2649d2f684db536cb87aa7335cf1967f`

```dockerfile
```

-	Layers:
	-	`sha256:c1e71368d1708be084910cb73c61fb9c7fe19363a319055a99a57893eabcfcc6`  
		Last Modified: Thu, 09 May 2024 17:22:54 GMT  
		Size: 3.1 MB (3125472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fac84365661fc863cc2f266ca6186a64e3fb48b728902603a15fc7e0f9f7321`  
		Last Modified: Thu, 09 May 2024 17:22:54 GMT  
		Size: 34.1 KB (34082 bytes)  
		MIME: application/vnd.in-toto+json
