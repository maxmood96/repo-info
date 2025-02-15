<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.27`](#logstash71727)
-	[`logstash:8.16.4`](#logstash8164)
-	[`logstash:8.17.2`](#logstash8172)

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
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33058be4cd2506de6cb2935b1e7d68b36f7e5c015de5b7ac0a23b90e0243b5`  
		Last Modified: Tue, 14 Jan 2025 22:54:18 GMT  
		Size: 50.9 MB (50934588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1594f29e7c4e5e8ab33efbe8cccd45fa6aede07941212b5aaa4ea2ee0b97af`  
		Last Modified: Tue, 14 Jan 2025 23:14:40 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14880be545b185b83525b5b94dcce04c08098168af0ff3240c51f87bddc78ce`  
		Last Modified: Tue, 14 Jan 2025 22:54:28 GMT  
		Size: 371.0 MB (370999278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a51655eebfe06bca503122097285751ae898dbc9dae344705772ff82bcac75`  
		Last Modified: Tue, 14 Jan 2025 23:15:16 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8038b148a04c56b03c30ad25e675e9c265f2a52fe741f20257bd4e4303c1c`  
		Last Modified: Tue, 14 Jan 2025 22:54:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60e9b8156b8774126c46f06b0870ec5fbe34bd632d442188da373a1230fdd8`  
		Last Modified: Tue, 14 Jan 2025 23:14:42 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18f28c337a79a98b1ce53470028968202888d840d28c582825e9047a55306a`  
		Last Modified: Tue, 14 Jan 2025 23:15:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f154696cacfcce12dd854a60355f6733d4ceeb41085940e1bc80644ed72348`  
		Last Modified: Tue, 14 Jan 2025 23:15:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4e13ffed2ce3cba3275c264fd8c67e9488354337b5c802383d138059f31e1f`  
		Last Modified: Tue, 14 Jan 2025 23:15:20 GMT  
		Size: 2.1 MB (2066395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c17004626d6ef861a2a85e5d3fbc31cf9cfa482857fcd11bcdb8b51a2161a8`  
		Last Modified: Tue, 14 Jan 2025 22:54:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Tue, 14 Jan 2025 22:53:21 GMT  
		Size: 3.3 MB (3303537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcca1374a9dee9d50a32c5da34ad23ace32ba0bcb304e7cc68a4e6a7752c2959`  
		Last Modified: Tue, 14 Jan 2025 22:53:20 GMT  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af073690597bfc4ca0e4dfdd69b447cf8151d7c570e4e18230ee66984d01d04`  
		Last Modified: Thu, 06 Feb 2025 02:20:49 GMT  
		Size: 38.7 MB (38696778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4886c4599b33738089f98ce9a0be9a732cdd11eeff5018efa3b60b365053897`  
		Last Modified: Wed, 05 Feb 2025 12:31:09 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec038de81a327a3f936a747905fe9986f1a5597d5889035a2b78fe9a87bc56a`  
		Last Modified: Thu, 06 Feb 2025 02:21:03 GMT  
		Size: 367.8 MB (367817027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbd2087d60a20ef56ff4d8781bac6062e53985a68c35bc799d4c2d50c9b0435`  
		Last Modified: Thu, 06 Feb 2025 02:20:48 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb69b326d5dec416a62d67f8f0f39256a1e655f749056aeb9a9f1c831f266db`  
		Last Modified: Thu, 06 Feb 2025 02:20:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd052e8091f10cf29bb01467ebef3f128c90f11d489108b03081a67dd5aaad24`  
		Last Modified: Thu, 06 Feb 2025 02:20:52 GMT  
		Size: 469.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed4d942a8801b20910dfd41b3a80eb969bdb918d266573de6d0146b08e1e91`  
		Last Modified: Thu, 06 Feb 2025 02:20:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d942768bb1c341e815e7c2f0fdacc5b144bf0512b3cc536407b54729adad2f39`  
		Last Modified: Thu, 06 Feb 2025 02:20:56 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a5eae265d70e1d7bba607dde93b1d3adf5138a4ac1fd8a4aad69e9901de07`  
		Last Modified: Thu, 06 Feb 2025 02:20:57 GMT  
		Size: 2.1 MB (2066388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c04a03336c608093a30a5c2d85be8db60b916a24b96292713631f4b99111c`  
		Last Modified: Wed, 05 Feb 2025 16:21:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Wed, 12 Feb 2025 11:50:34 GMT  
		Size: 3.3 MB (3303773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c9bb134b683781945c6a813d2a81b7ca22e77cf8c5f4b7888b25ad9534d113`  
		Last Modified: Sat, 15 Feb 2025 12:14:20 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.4`

```console
$ docker pull logstash@sha256:f44375526aeccbf692008a558a84c8cb2a9f996d4ea79e61b1c114d779977b80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.4` - linux; amd64

```console
$ docker pull logstash@sha256:4111ae0703e3336bc6a67e63feae63313fd56aeac547b341157c92fcd309df14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.6 MB (529583575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ce58aa39e4b188acf5c753b0010347f64635ee50db5c69d4529c9cd84a372`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:46:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.4 org.opencontainers.image.version=8.16.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:47:51+00:00 org.opencontainers.image.created=2025-02-05T18:47:51+00:00
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e49f0148fedbac5c18ce0120683b7f360670e7c58872768911d3209806aaf`  
		Last Modified: Tue, 11 Feb 2025 19:30:39 GMT  
		Size: 57.7 MB (57729045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ab29b63179eabb60324ee92398e947705fb1940d883f2fe2536077d04bb4d`  
		Last Modified: Tue, 11 Feb 2025 19:30:38 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190911b25f5cb3f2c330912c5e15500a336bbf68219019c6358faedaf144ff40`  
		Last Modified: Tue, 11 Feb 2025 19:30:51 GMT  
		Size: 438.3 MB (438269071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e578f6fa8c9559aabacbf758175295ae893df7c2e313ba95d7573ee59e81380`  
		Last Modified: Wed, 12 Feb 2025 09:03:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21d7db151587e06fb40b1fa173aa2464dc40c25d420aef4f0bf6e0cb7f63ad`  
		Last Modified: Wed, 12 Feb 2025 09:03:31 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5486f7e2c5f76ba68d3b9978af05c596a23ecf0a667c72f5a1bd6e2e4a72036`  
		Last Modified: Wed, 12 Feb 2025 14:06:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6631f989db1c046a4d2b33ed9963dbe463b9f553f15245e477f59964ba998d`  
		Last Modified: Wed, 12 Feb 2025 10:11:33 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd1ccd757063671a96257d0d236a62aee870dee7b3aa1ecc987b83b24d85a17`  
		Last Modified: Tue, 11 Feb 2025 19:30:39 GMT  
		Size: 4.0 MB (4002549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0fc59212173e7baba9cf72f0178f9c8d19b8b8b9a34cda33c55d061da2737`  
		Last Modified: Wed, 12 Feb 2025 17:22:09 GMT  
		Size: 2.1 MB (2065365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cd1128f19d036c68826c77d5385cabfc4d80ab8e6aa3f7a282034443a2522`  
		Last Modified: Tue, 11 Feb 2025 19:30:39 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.4` - unknown; unknown

```console
$ docker pull logstash@sha256:f6bab828c80c1e232bb3e1a8d2d72c84ce8776d7c1122f79749ec8906073a154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5222cb2a4576c6d19b0060fda1ffdf1641f3dd4d8361b5f8f2c211a105fcfb7c`

```dockerfile
```

-	Layers:
	-	`sha256:f3d4c6d6e4418fe82382857558341222f96fed9aa76f9f1555c15ac621c4a95e`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 3.5 MB (3520019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e414fee78a7c0e80e913b2a811de29bbd621d6596437b3354a2eca609002b31`  
		Last Modified: Wed, 12 Feb 2025 10:11:23 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a051a3ddd0d7d0c40a5646d4a7688cb9cfc450379e3c8ea47a633c5cc585c2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512768325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b74aff4e8cda145c47024112aaaeb560654c6000e8e796c0de004f5b12b7b`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:46:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.4 org.opencontainers.image.version=8.16.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:47:51+00:00 org.opencontainers.image.created=2025-02-05T18:47:51+00:00
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651092bb7bf62c6844dc81b0a938d4067dd5bafe70c6ed10922a5aaf08eff87`  
		Last Modified: Wed, 12 Feb 2025 01:53:14 GMT  
		Size: 44.3 MB (44294656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef0a54360ec84df15a8be824f6cbdcc417fb33f38f49de22a02735cd175287f`  
		Last Modified: Tue, 11 Feb 2025 20:37:38 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b3390ef1dc4ddbbba9d2b65b48025c99a97574f1012dec99d1cf6833ef7375`  
		Last Modified: Wed, 12 Feb 2025 17:24:05 GMT  
		Size: 436.6 MB (436553516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0d5f286ec85a7b3dbea46893f55c065a974c10e7774b8bdf805a097716d044`  
		Last Modified: Tue, 11 Feb 2025 20:37:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daf130f0ee702f5019935ddda2e21e99c0ddd97449b7e71a22d989c6dd63d0e`  
		Last Modified: Tue, 11 Feb 2025 20:37:47 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44178f8c742359d8d2809da03d5ffd7b04e3149f6522a9ffccedd0d8b0e381dc`  
		Last Modified: Tue, 11 Feb 2025 20:37:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29994eab0865dd258a8578902658107dbd7ee8c0b39ac709800b4802a6ac4895`  
		Last Modified: Wed, 12 Feb 2025 08:32:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d70a6a4c98f3d2beecaf46f4975b0fbbfa4d2d8d4fe89f8f56676db365f19`  
		Last Modified: Wed, 12 Feb 2025 20:17:05 GMT  
		Size: 4.0 MB (4002539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127126e646c17131afae840dd5a6e8bc2c0f102b43b3992c58007e061f4385c`  
		Last Modified: Tue, 11 Feb 2025 20:37:49 GMT  
		Size: 1.9 MB (1937306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77c089fd3bc24ded136c5bebe2c89d2ac114fb5a2531e24eaabb98fe03902c3`  
		Last Modified: Fri, 14 Feb 2025 03:19:01 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.4` - unknown; unknown

```console
$ docker pull logstash@sha256:8c4f30764f638747358bed3da32e5bf514659e975ec676d2cb58277273ef3672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e71eb743ef4b2a3d534de8dd7b2d515c1ac4d6acfb7ee94601fd4a2bf265b2`

```dockerfile
```

-	Layers:
	-	`sha256:6d6bbbf6f77add08a4c5a7dfaac70e5a91547f4ea1282f70d029f3403dc817c5`  
		Last Modified: Wed, 12 Feb 2025 09:02:17 GMT  
		Size: 3.5 MB (3519631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c833678a9c854d3e8bebb88d546e07aa732ddcefdcf7da98771251a3c76345fc`  
		Last Modified: Wed, 12 Feb 2025 10:11:29 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.2`

```console
$ docker pull logstash@sha256:c59e15f0cbcf8422c6ebec0fa1d5c567c7784acf814d81c71d3d410a6c4c6116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.2` - linux; amd64

```console
$ docker pull logstash@sha256:c126b006cb1e3633e430d4da4d245bdda4dafbafd8ddfbea4b23fe61196ecc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.9 MB (529857237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760c7f40c4f5da2e5ec59c96ce54ed36dd2146e6022c36807448231b79b1437d`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:44:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.2 org.opencontainers.image.version=8.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:46:19+00:00 org.opencontainers.image.created=2025-02-05T18:46:19+00:00
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511019e58f7cab84eaa566b6922e35c5e52cb0e9bd083c82d6388b9f6c29d46`  
		Last Modified: Tue, 11 Feb 2025 20:35:55 GMT  
		Size: 57.7 MB (57729030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1cc28a8b72f3dd235a6a41009526b2cf500be1a8b7d5bdc7560340350ae669`  
		Last Modified: Tue, 11 Feb 2025 23:11:49 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4a50bc9490087e4f74909a67b192e8c60c674270e1046b503f6fc4167a7bf7`  
		Last Modified: Tue, 11 Feb 2025 20:36:16 GMT  
		Size: 438.5 MB (438542755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd8c599b81b02a9c6c3b85c16e70361f2de497f788b02202139bb635f113315`  
		Last Modified: Wed, 12 Feb 2025 00:28:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d466263f283b32177f32bdac8dae52a11b1a265472b674134f973863bceac0`  
		Last Modified: Tue, 11 Feb 2025 23:11:49 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706caeb0c635fe5962bfd406d5c7ae6764fd03f78f2cc3b1b89e77fa0af6da4`  
		Last Modified: Tue, 11 Feb 2025 20:07:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c13380124205f4fd4185a223095afbd7990c8ca4f8b1f96ac9d978b86d01bb`  
		Last Modified: Tue, 11 Feb 2025 20:35:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34c1b6f4fd2c5750a03a68308ae24c3d2f539260906452247beec6910ad1f68`  
		Last Modified: Tue, 11 Feb 2025 20:35:57 GMT  
		Size: 4.0 MB (4002545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9337fa80046a8f68b46a9c2b8e8b943a721b932fbd215b7b3615e10d1924a`  
		Last Modified: Tue, 11 Feb 2025 20:35:58 GMT  
		Size: 2.1 MB (2065361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396503d29a8111426487a4a32322a6a34179365193d3f9276dc614513a0c520`  
		Last Modified: Tue, 11 Feb 2025 20:07:47 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.2` - unknown; unknown

```console
$ docker pull logstash@sha256:0edd3eabca68c4b8a3663c630160ac177666cf00bacf04917ce17b4be00a5695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf5ff6476494d241b558230051411c0f002f13e89d0e646b380717857e36276`

```dockerfile
```

-	Layers:
	-	`sha256:2a2598ef13ea9ea9d531028fa3ea41033cf236e61fc4b6a8b52de499536f576f`  
		Last Modified: Wed, 12 Feb 2025 03:59:33 GMT  
		Size: 3.5 MB (3521540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e41750deffef9bb46a50912e8647dc450622418dbe78a1b1688f9049c4afc20`  
		Last Modified: Sat, 15 Feb 2025 12:14:28 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1795a0fc8de1ca866ea39cccaa0c1309a5bfb72bca1e39ae1aa9d7cb543f965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513050961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4313bc2be39f46e5b87a49b18b98206f9b730edddec66f5fe2662103f9ef40c`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:44:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.2 org.opencontainers.image.version=8.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:46:19+00:00 org.opencontainers.image.created=2025-02-05T18:46:19+00:00
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651092bb7bf62c6844dc81b0a938d4067dd5bafe70c6ed10922a5aaf08eff87`  
		Last Modified: Wed, 12 Feb 2025 01:53:14 GMT  
		Size: 44.3 MB (44294656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef0a54360ec84df15a8be824f6cbdcc417fb33f38f49de22a02735cd175287f`  
		Last Modified: Tue, 11 Feb 2025 20:37:38 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9153ec654bedbd7c7ee07a985b9f50f35adb9f1b4b9c136d70a596d68e89eb8f`  
		Last Modified: Wed, 12 Feb 2025 04:00:08 GMT  
		Size: 436.8 MB (436836162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d697a5ca2b32444f6a6a9d05161cb67ea3729a05ffc8d38c706ee73cd20ab0`  
		Last Modified: Wed, 12 Feb 2025 01:42:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f29dbfe48e925e9edb57f27e658ba2ddd9bbbd38ad8582c892f5037e9f1b49`  
		Last Modified: Wed, 12 Feb 2025 01:42:39 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d56f377f60dab95d1d15491ac5af4f26c99ace81f878239a1f5638dbe4e3aa`  
		Last Modified: Wed, 12 Feb 2025 01:42:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64c84c306b15670f2473a3ba6599ccb408707a7f5bc232005cb841548aab4b`  
		Last Modified: Wed, 12 Feb 2025 01:42:41 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25da39a01781ec16b78525fe74357c37aabcdda80ec4630c5f04550aef291c8`  
		Last Modified: Wed, 12 Feb 2025 01:42:42 GMT  
		Size: 4.0 MB (4002537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ccb4fa82211672240629c8e9473524e858f4d7a804286f183a1d959b583b96`  
		Last Modified: Wed, 12 Feb 2025 01:53:45 GMT  
		Size: 1.9 MB (1937301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a47824cf2982f3f293012501607e08f4c334373b16b04a0cf124569d9fd9`  
		Last Modified: Wed, 12 Feb 2025 01:53:52 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.2` - unknown; unknown

```console
$ docker pull logstash@sha256:38fbd3ae00eccfb68bc73a2d5b0d03efc308c659989e31fcc9d0238bfa9d2bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aece22668badff04d176180876034a166125fcb2449d371cffcb930f30512`

```dockerfile
```

-	Layers:
	-	`sha256:0812960bdc467e819d082e1a69de2a0d96259bca5063a5ec23a5df1aa01c3f48`  
		Last Modified: Wed, 12 Feb 2025 04:00:17 GMT  
		Size: 3.5 MB (3521152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a087180fefe8af2d975276e751a146f2118ec810e032f6ee6d3c9bff3415ac5`  
		Last Modified: Wed, 12 Feb 2025 04:00:15 GMT  
		Size: 34.7 KB (34713 bytes)  
		MIME: application/vnd.in-toto+json
