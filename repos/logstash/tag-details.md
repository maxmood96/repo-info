<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.27`](#logstash71727)
-	[`logstash:8.16.3`](#logstash8163)
-	[`logstash:8.17.1`](#logstash8171)

## `logstash:7.17.27`

```console
$ docker pull logstash@sha256:93536af4d7c944d39aada41bf9dd4fa13b995a661f2b940bfcfef29fc0154374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.27` - linux; amd64

```console
$ docker pull logstash@sha256:437cb89a43d71203e3d4b0c983e3f3b342e99b2035a4389f47060be791200744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451515920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a6d1f20b254f588918594eab84f8174a0312b3216090fb776194179c816b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 19:20:58 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.27-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.27 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 19:20:58 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
USER 1000
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.27 org.opencontainers.image.version=7.17.27 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-07T18:11:24+00:00 org.opencontainers.image.created=2025-01-07T18:11:24+00:00
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33058be4cd2506de6cb2935b1e7d68b36f7e5c015de5b7ac0a23b90e0243b5`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 50.9 MB (50934588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1594f29e7c4e5e8ab33efbe8cccd45fa6aede07941212b5aaa4ea2ee0b97af`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14880be545b185b83525b5b94dcce04c08098168af0ff3240c51f87bddc78ce`  
		Last Modified: Tue, 14 Jan 2025 20:28:37 GMT  
		Size: 371.0 MB (370999278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a51655eebfe06bca503122097285751ae898dbc9dae344705772ff82bcac75`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8038b148a04c56b03c30ad25e675e9c265f2a52fe741f20257bd4e4303c1c`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60e9b8156b8774126c46f06b0870ec5fbe34bd632d442188da373a1230fdd8`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18f28c337a79a98b1ce53470028968202888d840d28c582825e9047a55306a`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f154696cacfcce12dd854a60355f6733d4ceeb41085940e1bc80644ed72348`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4e13ffed2ce3cba3275c264fd8c67e9488354337b5c802383d138059f31e1f`  
		Last Modified: Tue, 14 Jan 2025 20:28:33 GMT  
		Size: 2.1 MB (2066395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c17004626d6ef861a2a85e5d3fbc31cf9cfa482857fcd11bcdb8b51a2161a8`  
		Last Modified: Tue, 14 Jan 2025 20:28:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.27` - unknown; unknown

```console
$ docker pull logstash@sha256:2d55c8e10a1042ed07546183a616fc4e71ea0293988984aecac26e9657effcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3335723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a02fec3e07772e71e7f2fc05e9f8471f2ee973b4776895667fd315d0c2d330`

```dockerfile
```

-	Layers:
	-	`sha256:528ea07606b5a7bbc49ad7fe6b9671f3a515f7c5c5eb7ef47aa1cc34d91f9376`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 3.3 MB (3303537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcca1374a9dee9d50a32c5da34ad23ace32ba0bcb304e7cc68a4e6a7752c2959`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.27` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:6b7404bdf7a7f96bf611a173eec269285c701535b9a99a09bf97458f51155183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.6 MB (434558606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6955bc798f85efe96e80b969aa6ff9f16f2d4bdef4df9d1b736f5f92902bf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 19:20:58 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.27-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.27 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 19:20:58 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
USER 1000
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.27 org.opencontainers.image.version=7.17.27 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-07T18:11:24+00:00 org.opencontainers.image.created=2025-01-07T18:11:24+00:00
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af073690597bfc4ca0e4dfdd69b447cf8151d7c570e4e18230ee66984d01d04`  
		Last Modified: Wed, 15 Jan 2025 01:34:32 GMT  
		Size: 38.7 MB (38696778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4886c4599b33738089f98ce9a0be9a732cdd11eeff5018efa3b60b365053897`  
		Last Modified: Wed, 15 Jan 2025 01:34:31 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec038de81a327a3f936a747905fe9986f1a5597d5889035a2b78fe9a87bc56a`  
		Last Modified: Wed, 15 Jan 2025 01:34:39 GMT  
		Size: 367.8 MB (367817027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbd2087d60a20ef56ff4d8781bac6062e53985a68c35bc799d4c2d50c9b0435`  
		Last Modified: Wed, 15 Jan 2025 01:34:32 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb69b326d5dec416a62d67f8f0f39256a1e655f749056aeb9a9f1c831f266db`  
		Last Modified: Wed, 15 Jan 2025 01:34:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd052e8091f10cf29bb01467ebef3f128c90f11d489108b03081a67dd5aaad24`  
		Last Modified: Wed, 15 Jan 2025 01:34:33 GMT  
		Size: 469.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed4d942a8801b20910dfd41b3a80eb969bdb918d266573de6d0146b08e1e91`  
		Last Modified: Wed, 15 Jan 2025 01:34:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d942768bb1c341e815e7c2f0fdacc5b144bf0512b3cc536407b54729adad2f39`  
		Last Modified: Wed, 15 Jan 2025 01:34:34 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a5eae265d70e1d7bba607dde93b1d3adf5138a4ac1fd8a4aad69e9901de07`  
		Last Modified: Wed, 15 Jan 2025 01:34:34 GMT  
		Size: 2.1 MB (2066388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c04a03336c608093a30a5c2d85be8db60b916a24b96292713631f4b99111c`  
		Last Modified: Wed, 15 Jan 2025 01:34:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.27` - unknown; unknown

```console
$ docker pull logstash@sha256:e8a29e138c0ec573c7c09d68ae25a6aede777ed97f4833eb2439cf5f400bf9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3336087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8c617daaff3559185b8554886f74dfccadb0d166581f6c2317dfda89e3b87a`

```dockerfile
```

-	Layers:
	-	`sha256:78972c7779636cf49ecd5b35eaaf3f60bc0b9d94b8ec49d963722d55ae7168d9`  
		Last Modified: Wed, 15 Jan 2025 01:34:31 GMT  
		Size: 3.3 MB (3303773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c9bb134b683781945c6a813d2a81b7ca22e77cf8c5f4b7888b25ad9534d113`  
		Last Modified: Wed, 15 Jan 2025 01:34:31 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.3`

```console
$ docker pull logstash@sha256:c5b75efa687388d63953e7ffe2fe1c9067602b2b4c451fc4627958ddf85b7003
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.3` - linux; amd64

```console
$ docker pull logstash@sha256:7f9f123b0f68f25e6b482009020162eaf984ab85cfbb2996c4dd23c8adfd6fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.9 MB (521884090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d20faefd1974cbd863b78d0af01c2fabfa9a198e68e9290c01ff139295fdcaf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:29:25 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/logstash
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 08:29:25 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.3 org.opencontainers.image.version=8.16.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-08T06:49:55+00:00 org.opencontainers.image.created=2025-01-08T06:49:55+00:00
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31187ec49ce3f6b264668e683d6c7bc3783f85e8a74ff6b4a1593506062ca4c1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 50.9 MB (50941974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a00481d89f0beaa93b26f54a433405001beb4b1db23d09d19930a532027e5b`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2077d3aaeeab3e600b29608864efe84e3ccb0d7ff666c736dfda906b126f84`  
		Last Modified: Tue, 21 Jan 2025 19:29:44 GMT  
		Size: 437.4 MB (437353701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64907c8141b0f4cb9385ad0bc6faf99c0904be20af45e46edd0b124d49f589c1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270f6f6de901d6980d726139579d37b47e492afc15f1737ceb71409b83d23ca8`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4519bd94f89a4cff50e6e8bb22fbf83fa70f170cdda09df1fcdc5709705edb5`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273f8b014b7be26bf76848fc6e85d38978fed93ac53f3341aa2cc176d09d58a4`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8fe0e7f21ea7eaad626c649f07495a8c9393d03097ff6e1f1a50001618e285`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 4.0 MB (4004305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2378f60cb3b3072ebae40df714bcca9d50bef643047958032eee0b5d36001d4c`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 2.1 MB (2066571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6ef63e496c7159f814fb52c8c794736c7f75056c22c381b774ecc167bc313c`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.3` - unknown; unknown

```console
$ docker pull logstash@sha256:509e2fa43f3f88b3bb1f5b1b692e81f157de210d75ea635e3bdad436df470e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af80881788f62be9a80af1637ac4b728e89c9fa51b5c3904abc4ff0d168d6137`

```dockerfile
```

-	Layers:
	-	`sha256:6408e931952284444fd8907d24183b9011d5916a0d1980e0a693206f453fb983`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 3.5 MB (3515615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4923103549af78efbf9bd9e3c3ff09d81b8deb459acf7f6e5bbb6f478eefa412`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1957583416f31baa3b826a1c5fd66304022a69aa0d7a1282a745bcef8f3c2fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.2 MB (506202171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9830b2c970a2d90d091739cf0bef444a86bbdad1620d35e0ad28b66373d0a0a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:29:25 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/logstash
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 08:29:25 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.3 org.opencontainers.image.version=8.16.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-08T06:49:55+00:00 org.opencontainers.image.created=2025-01-08T06:49:55+00:00
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f293868bc0fa1046ad20cc586b26437cceef74ee9e15b94e8a82531f48fd4`  
		Last Modified: Tue, 21 Jan 2025 20:20:39 GMT  
		Size: 38.7 MB (38707601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b38a28dc1cbfdc3e29567150705b427bfadbabd1419ed628e1b6c1633b2301f`  
		Last Modified: Tue, 21 Jan 2025 20:20:38 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616b3185e182b78274cac765c24602816cc945f8b29325dddc18210207f5f2f6`  
		Last Modified: Tue, 21 Jan 2025 20:20:48 GMT  
		Size: 435.6 MB (435572290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88ce162f7130727820fd094161d7a081e5ec5cd3c872e3eafa35043a636fd96`  
		Last Modified: Tue, 21 Jan 2025 20:20:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88660e57497a4db43d0351867526f81fb13171067b4c9f82814262a78bec6607`  
		Last Modified: Tue, 21 Jan 2025 20:20:39 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef204b8eb4f1a7160c4633ec59a6f6befb97110a979b774ddf54cbece32dcd0`  
		Last Modified: Tue, 21 Jan 2025 20:20:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c35ab18a1965b01309a96c3fc3c6f495ef31da73a9da14de86ff45bb10f135`  
		Last Modified: Tue, 21 Jan 2025 20:20:40 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f44b62cdc89e6800ee5de6dbe75361f4852d026bc81d9e67b9b094b8ec407f`  
		Last Modified: Tue, 21 Jan 2025 20:20:41 GMT  
		Size: 4.0 MB (4004303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308ffeb671db4317c98a503360f81abb49c3b411ff065c568daffe10e97a5053`  
		Last Modified: Tue, 21 Jan 2025 20:20:41 GMT  
		Size: 1.9 MB (1937676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016b74e04ee503bd9d4d1da77afda48008eb23c14d16cdc7b1836dca1687709`  
		Last Modified: Tue, 21 Jan 2025 20:20:41 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.3` - unknown; unknown

```console
$ docker pull logstash@sha256:f69f0496e451868a125fe782f3e9644994ea6ced9d511e9aca416ccc2c3b9ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1181a2bf17ebda9ceb7169c8dc5de7460582e486e87d075ed4621012b7196ac1`

```dockerfile
```

-	Layers:
	-	`sha256:847d4e1c562d0991fadbf96ba12480ffd10ee4e711c9fb4901d4aad1be06d9df`  
		Last Modified: Tue, 21 Jan 2025 20:20:39 GMT  
		Size: 3.5 MB (3515227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058aa36f12df82c7eb4c04304b8e599fe622aff88cc4439eea2db0fef5f0126c`  
		Last Modified: Tue, 21 Jan 2025 20:20:38 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.1`

```console
$ docker pull logstash@sha256:cfb1e25d9dcaced56f3582dc64c61a28461b6519589b587a6054f5afcd604c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.1` - linux; amd64

```console
$ docker pull logstash@sha256:0dc237d69cef5e26909f42102ffb7d4bcd4a6dbbc0c2dc5fb3d4afe5f16c2f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.2 MB (522152509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5b3f6e0b1fbe3951308af7ecc5eb43b49d6b06a114d8f0d766e33ec825c3e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:22:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/logstash
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 08:22:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.1 org.opencontainers.image.version=8.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-08T06:41:04+00:00 org.opencontainers.image.created=2025-01-08T06:41:04+00:00
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952922082746be1309235934cc5ea93e70e29017aed5810f23ed0f4c79467777`  
		Last Modified: Tue, 21 Jan 2025 19:29:57 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb1bb3befa6d4a4659d319d5e8e3629abffea06afe3856b2f3aba695eed42d8`  
		Last Modified: Tue, 21 Jan 2025 19:29:54 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11359633f80a1d7b8b30e473a652a968fef15af79e6f1d3db91b98a5146551`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 437.6 MB (437622063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61189d35a0c98e747d79a0d9159e7876451e755b96597511d955933060ccb310`  
		Last Modified: Tue, 21 Jan 2025 19:29:55 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66aa605ea553d810da4afae978fbebf0071f7443296607175dbf5cda3c97852b`  
		Last Modified: Tue, 21 Jan 2025 19:29:55 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e4a42cf9016e487506b5885a77d316e63ab3aee9fa6917e7133950c7518c5`  
		Last Modified: Tue, 21 Jan 2025 19:29:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cdea0cd3d911f334f0483429c64fbea648caf70cd8c5f51432a8a7dec34b2b`  
		Last Modified: Tue, 21 Jan 2025 19:29:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adffd88c16b5b923bc6407547f2444abfafeb3ce4e5982abb148c2db95ae726`  
		Last Modified: Tue, 21 Jan 2025 19:29:57 GMT  
		Size: 4.0 MB (4004300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d2d97d4ab5680057442ecf794c31cbff183baaa4d97266101e2959d856a47`  
		Last Modified: Tue, 21 Jan 2025 19:29:58 GMT  
		Size: 2.1 MB (2066565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927ea0c8f89063e3de2de1a1d6c75df7fe330193090c61567756f1b172539b4`  
		Last Modified: Tue, 21 Jan 2025 19:29:58 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.1` - unknown; unknown

```console
$ docker pull logstash@sha256:8ab1329a490a8449023357f10025eda41daa7bb1dcca287778f3bfdade4b60e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3a2b2534cff8b605c4b84355929507749c034d5b72757ae46768011095462e`

```dockerfile
```

-	Layers:
	-	`sha256:e15abcccbd23f1f7cb661ed2cff02b20e92de4bd99fa8a09ea733ed8a9b7aaed`  
		Last Modified: Tue, 21 Jan 2025 19:29:55 GMT  
		Size: 3.5 MB (3517136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba16b7bc458451a050f902961522d6ea89df87887f413edc0adff998649287f3`  
		Last Modified: Tue, 21 Jan 2025 19:29:54 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ccd1e4c4a32c2b62a7ef5a19ca5887646963f7f7b867478d689b8b3b6176e85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.5 MB (506478572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e85198f4388350a93a2c6e1c9a395c12950030c2e413fddb94cfd0351e8cd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:22:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/logstash
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 08:22:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.1 org.opencontainers.image.version=8.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-08T06:41:04+00:00 org.opencontainers.image.created=2025-01-08T06:41:04+00:00
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f293868bc0fa1046ad20cc586b26437cceef74ee9e15b94e8a82531f48fd4`  
		Last Modified: Tue, 21 Jan 2025 20:20:39 GMT  
		Size: 38.7 MB (38707601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b38a28dc1cbfdc3e29567150705b427bfadbabd1419ed628e1b6c1633b2301f`  
		Last Modified: Tue, 21 Jan 2025 20:20:38 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd9459d884e5304fa29dc762c427a6734c001c1420bb18d1188aedf9d35d43b`  
		Last Modified: Tue, 21 Jan 2025 20:22:22 GMT  
		Size: 435.8 MB (435848693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ca6452902a38596fcab863885efc704896a0e7ccfd6143bf4f165d64596f59`  
		Last Modified: Tue, 21 Jan 2025 20:22:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c24457206a732f0ad4aecdeb8a375e0a2ae43352c7dbce27c08a3987e686d7`  
		Last Modified: Tue, 21 Jan 2025 20:22:13 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bb9fa06b0fcc7d4b90304b624e272d6348bcc6bd70d3668fc2c3afa55b589`  
		Last Modified: Tue, 21 Jan 2025 20:22:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06e53e6fd59022352c1456ee740a2cede0be5e5329f76edc7fc8578b612e9d1`  
		Last Modified: Tue, 21 Jan 2025 20:22:14 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce51d2536dbc72d1f01c7246a00e78d078bfd49447dce073c24d59be27ddabaa`  
		Last Modified: Tue, 21 Jan 2025 20:22:14 GMT  
		Size: 4.0 MB (4004301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e8f38594574c28efca2e065a5361e9cb8e5791c588b190039639cffd91f05d`  
		Last Modified: Tue, 21 Jan 2025 20:22:14 GMT  
		Size: 1.9 MB (1937669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca893fef50e94396cbd85b06bb188e8034406d38889bb1fd26ab1d7b4ab17e75`  
		Last Modified: Tue, 21 Jan 2025 20:22:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.1` - unknown; unknown

```console
$ docker pull logstash@sha256:c902167f4d20f4f2a1531a8ec18cfb89c722505544f6171c14ae649d794b7181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8b91577917532bf97bc1b3c98ba09fef9c971fec1c47887bf786182421c7cf`

```dockerfile
```

-	Layers:
	-	`sha256:8a947e44896472043310a4180faf7333398cbbe46b57e5c3da93d45de31dc92a`  
		Last Modified: Tue, 21 Jan 2025 20:22:13 GMT  
		Size: 3.5 MB (3516748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b4cbc0803dccc531e3f924c1477e8b4f1812021396c0a44762effcc26b96c7`  
		Last Modified: Tue, 21 Jan 2025 20:22:12 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
