<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.5`](#logstash8185)
-	[`logstash:8.19.2`](#logstash8192)
-	[`logstash:9.0.5`](#logstash905)
-	[`logstash:9.1.2`](#logstash912)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:9e5a140f2ad9a603c469d39603b82a1f21f28be1ef523d96c80a5d1089d37ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:3610df05756b327e70f3abe2538f2d4087b36bb47a0635b3ddc4da716f30e2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.8 MB (522799321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc3f08cf025cca763c2fc3291e16fbc7d209a4558671f95a835b056bbbf31ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:18:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.10 org.opencontainers.image.version=8.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:36:38+00:00 org.opencontainers.image.created=2025-08-06T09:36:38+00:00
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d5e3deb2e9e2b729c85b8cd49147aa96f93b8deae414e28aebda5bb7416760`  
		Last Modified: Tue, 12 Aug 2025 18:07:23 GMT  
		Size: 46.2 MB (46223100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bf8a8d2a54057cb1327b5f48ec41eb3635ddd1647380dbc0f779365b2c920`  
		Last Modified: Tue, 12 Aug 2025 18:07:14 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a435d1206ae1217ce53797da83faaf74a70373056f005e25b8d2f4dc6e49b299`  
		Last Modified: Tue, 12 Aug 2025 22:20:59 GMT  
		Size: 440.7 MB (440696809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6d7c44cff2a7d7edb4ab381dcc755f0563f1a725ffb9de7e64ae642c518fd6`  
		Last Modified: Tue, 12 Aug 2025 18:07:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3471676e6ed7154800b5e3ebbcc3612675d0591c815d76d7afdf2d7553aba1`  
		Last Modified: Tue, 12 Aug 2025 18:07:14 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6ee2b50c2943b2d93459ce26c02a862e1f64b6d2f3348db6624d888031d8d`  
		Last Modified: Tue, 12 Aug 2025 18:16:54 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44debbb018b7c29e76aaddc96be85e4c6fdd514cd0e763e6926cf90bb21dcbd`  
		Last Modified: Tue, 12 Aug 2025 18:16:56 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e872d50325264825b81df8c1d3f9eada3823570119ee1bc964f2db3d718714ab`  
		Last Modified: Tue, 12 Aug 2025 18:16:59 GMT  
		Size: 4.1 MB (4056205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977e6c2f4f8dc956320167718b7b4aeee4f9be002b9ffd6f3b236b0d2d00dc63`  
		Last Modified: Tue, 12 Aug 2025 18:17:03 GMT  
		Size: 2.1 MB (2094095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46bf5f68a98127adad8bd0372308ad53e78fdaeb086a8247024fc8f0703eb70`  
		Last Modified: Tue, 12 Aug 2025 18:17:07 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:6a4b4b08f2e25a5b7638860ac14e2c2977a9630b2dcb5d70abc563953e9b8ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42a220b1528779ce91b33daa61d8158d9b4f4f1b817fd0c250010e04c75129`

```dockerfile
```

-	Layers:
	-	`sha256:faaa8bde6d052b0c340206eedf9fa9977fe8325e504edd3500811c9d384623a5`  
		Last Modified: Tue, 12 Aug 2025 18:53:20 GMT  
		Size: 3.7 MB (3657086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d511ab85a0d1116eb7cb4b6e4bc2d39c038c32aad86d2bb6b20ab71764c86843`  
		Last Modified: Tue, 12 Aug 2025 18:53:21 GMT  
		Size: 34.7 KB (34664 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c93923b561be9ff36c191e17f4a18311b2d97f2fd7d0d9e955845cda4eac450a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.0 MB (521010489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b84c68154f2cec63d85bee543289cd55bacf7ca33a22dddc483750f9f87634`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:18:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.10 org.opencontainers.image.version=8.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:36:38+00:00 org.opencontainers.image.created=2025-08-06T09:36:38+00:00
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926cf1d4612405f02e18a341abdd333274c0ed10a7dfb131d663ce5d1957172`  
		Last Modified: Tue, 12 Aug 2025 21:39:04 GMT  
		Size: 47.1 MB (47144622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b9759e60f2608e1c3487215be27a8a63923137fae7f06198aa1f9864c24c8`  
		Last Modified: Tue, 12 Aug 2025 20:26:18 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ade546842462f0a35248cdecea30ad6830c2bd9cb7bbb3f6cf4e7cc9100e8e`  
		Last Modified: Tue, 12 Aug 2025 21:39:28 GMT  
		Size: 439.0 MB (438981751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae60927f3da4c22800ae8f17dfb2b69f89db82df98f5ba41485ebabd81297830`  
		Last Modified: Tue, 12 Aug 2025 20:27:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f62598d97724ff063f3dba2cbc64e2d162299dc9d96f005fcae6c2a4fcb47d`  
		Last Modified: Tue, 12 Aug 2025 20:27:42 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec600a87ebdf580c30af00fba9fbef5695423a0d7c88f86e6fe7b0c30b7aa788`  
		Last Modified: Tue, 12 Aug 2025 20:27:45 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34015f2854327f1ba739dd905d0611424ae967a0d437461993b421a9afc1b31b`  
		Last Modified: Tue, 12 Aug 2025 20:27:48 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98249089353a05defcdcf93888e0b24a38a76b599276d9d7b80434cbcd503291`  
		Last Modified: Tue, 12 Aug 2025 20:27:51 GMT  
		Size: 4.1 MB (4056217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6729200ce238151a874b8c6ea36a03eb39821ffd9eb57e5246d4d895f67d32c`  
		Last Modified: Tue, 12 Aug 2025 20:27:56 GMT  
		Size: 2.0 MB (1961622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8096c532d1fff85c030f204579bd90fbb87ced3e60003712a3dd5941b914011e`  
		Last Modified: Tue, 12 Aug 2025 20:27:59 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:019a1df09f4a22c23be2fb3b54996c1a3dc1fcc191801ecd1d82d02959901fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51571d66c834adc17d01d02e846a2824db760dce8e29c47a07e719df36ad1560`

```dockerfile
```

-	Layers:
	-	`sha256:dd3d7f722146b27e122074e94676f52056305534e3dc698caec23fb253669ec0`  
		Last Modified: Tue, 12 Aug 2025 21:53:21 GMT  
		Size: 3.7 MB (3657511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ec48dff9ff4d87e32752895ca98d83fa1f0f9eaed485911247c46d7c7861fd`  
		Last Modified: Tue, 12 Aug 2025 21:53:22 GMT  
		Size: 34.8 KB (34807 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.5`

```console
$ docker pull logstash@sha256:366c7b3711f6ef54630269f2fb552a370a19e1091c0482b6251a1028a56b8599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.5` - linux; amd64

```console
$ docker pull logstash@sha256:d6e475dbdc3df24a7080c51cfbb8d80c8044e62bcb6ac59ba5f829be7b916e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.8 MB (522848465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07724528ed9a7ced370f3ea642fa94dea30dc85b47288d030c09804b82788f5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:42:34 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.5 org.opencontainers.image.version=8.18.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:39:19+00:00 org.opencontainers.image.created=2025-08-06T09:39:19+00:00
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a4d6b85a3bb98ab717e030677dc7fafd348ca28b8bdfca2d6b2da2c2ebf8ca`  
		Last Modified: Tue, 12 Aug 2025 18:09:49 GMT  
		Size: 46.2 MB (46223089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4054b947d11d1569af61507affbe08efe59dfea3bc41368a8c2fac442979c994`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af38107cab63d6365d20e63a3895e89e35098a9b9c022c56f4531f189c4f73c6`  
		Last Modified: Tue, 12 Aug 2025 19:07:17 GMT  
		Size: 440.7 MB (440745945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f605ac0264f34b87a439b3680a3c07e0e5c454810f7b7bb2e0afb53d2935bc4`  
		Last Modified: Tue, 12 Aug 2025 18:09:42 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c8879060499887b5cea564e73b38412365063f9d7cd27696006529b1136c50`  
		Last Modified: Tue, 12 Aug 2025 18:09:42 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e12dbd78e77719184f05628b8b2eb42a3604715efc781a107db9cc7aa7725a`  
		Last Modified: Tue, 12 Aug 2025 18:09:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1766496ca8f3925190f62a271164261591a0dbbe1ea312b812a8e5225cd34f45`  
		Last Modified: Tue, 12 Aug 2025 18:09:44 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a5335452d8823d73c5bf71dc65543198c12a1bcca0d65e21f0817200133976`  
		Last Modified: Tue, 12 Aug 2025 18:09:45 GMT  
		Size: 4.1 MB (4056216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c48bb523df2c8e59b1fce2d816846a219dfe6dba78bdd0bab77f0f413ebd0e`  
		Last Modified: Tue, 12 Aug 2025 18:09:38 GMT  
		Size: 2.1 MB (2094102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1861f2d6c13ba682701bb4e0329d6144ff3ad9ec19e7161e52b8d4a0ede0dddc`  
		Last Modified: Tue, 12 Aug 2025 18:09:38 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.5` - unknown; unknown

```console
$ docker pull logstash@sha256:9e3ac46db7993ed960e819ec12749b7b23b75fed9ddac6dd311b0add58c31785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1046384b347b661f303cb622b992b0de472dbf45e9daf4fce731859372478a37`

```dockerfile
```

-	Layers:
	-	`sha256:7bc7610bf000cccae6990b87b6e724f96a90f3056807ee9a6d96dde0e37c6e5d`  
		Last Modified: Tue, 12 Aug 2025 18:53:22 GMT  
		Size: 3.7 MB (3657642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bf70840922ab2e1bf5f20b482105487db1eead9edd76a7d33229048f36c5df`  
		Last Modified: Tue, 12 Aug 2025 18:53:23 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bb184caa64f8f72484be781169e424065f5d70f9ce4f54672aeeab5117699a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 MB (521055709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af80acc578489f10bbbaa235d5df9d0876e64cf5b2398e3941553d3a23df6938`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:42:34 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.5 org.opencontainers.image.version=8.18.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:39:19+00:00 org.opencontainers.image.created=2025-08-06T09:39:19+00:00
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926cf1d4612405f02e18a341abdd333274c0ed10a7dfb131d663ce5d1957172`  
		Last Modified: Tue, 12 Aug 2025 21:39:04 GMT  
		Size: 47.1 MB (47144622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b9759e60f2608e1c3487215be27a8a63923137fae7f06198aa1f9864c24c8`  
		Last Modified: Tue, 12 Aug 2025 20:26:18 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f22654fa01c4dbf722bf35c015b43d369ddac88935c965602427a0c48a83553`  
		Last Modified: Tue, 12 Aug 2025 23:52:08 GMT  
		Size: 439.0 MB (439026982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccc9c81f1cd2c46fe72bd6e00071a9aa53354c5e55ed0006b5c6912c8e1b968`  
		Last Modified: Tue, 12 Aug 2025 20:17:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a81e7e5922c1b34b0e3a076124e35601c6f5a9d55161e8800e96403a1ad6e2`  
		Last Modified: Tue, 12 Aug 2025 20:17:58 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8453e1e11ce9f51baa6b8253e336f0ff6b5e4d24168a53e35ae1acf4b61978`  
		Last Modified: Tue, 12 Aug 2025 20:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6391b636088f12ecafce62637ce5b8d9684ac58e14fe5e124ed0c9b09e882eda`  
		Last Modified: Tue, 12 Aug 2025 20:17:58 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d662766a29a1b8be56fa54f62d5aa8b30fd27c0e941f452349ecbc99b330e63`  
		Last Modified: Tue, 12 Aug 2025 20:18:00 GMT  
		Size: 4.1 MB (4056207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eec1e074ca1049ea1824dec26941b6f6c11594e39abea73ea7fb2635eef8ed`  
		Last Modified: Tue, 12 Aug 2025 20:17:59 GMT  
		Size: 2.0 MB (1961621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb908f41f5f3247419d1c73b19060300d8068219ca8e722259b9f4dd6ec0705`  
		Last Modified: Tue, 12 Aug 2025 20:26:43 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.5` - unknown; unknown

```console
$ docker pull logstash@sha256:68fbf8f3d74923c9002c8854e0eb9cfb1404edb326adeda1b37d0867effd51b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e854b1872fd24bbe00a494c53f3b1d72310ff09e3a7cc624c273cc8544c0ad`

```dockerfile
```

-	Layers:
	-	`sha256:f992d3485a6af796be42a62c26204c3afe8584d907e67860fa0f9e03963a7c86`  
		Last Modified: Tue, 12 Aug 2025 21:53:27 GMT  
		Size: 3.7 MB (3658067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a10368373cbcbbee9919122085c7dfd914404f63a35c73eca6c105925dfb08`  
		Last Modified: Tue, 12 Aug 2025 21:53:28 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.2`

```console
$ docker pull logstash@sha256:1f92e95d78ee463eaafb9ce54fb84f7e3b013893d5e2a3c3b333cf2c14274bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.2` - linux; amd64

```console
$ docker pull logstash@sha256:ed34aa0fc31abae3b40e005d4f0665d17fe1b576fc7e9dd4b499f5fe7eedea7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.2 MB (523204190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd12e8a0db5bb55c9a02bd86baebce527cfcba0043962bf2b3afc9061968366`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 11:48:35 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.2 org.opencontainers.image.version=8.19.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-07T09:55:51+00:00 org.opencontainers.image.created=2025-08-07T09:55:51+00:00
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac132a48dadb22311084e5dcd103dd980a27296226ea3190c5e9b4aa59f3c7d`  
		Last Modified: Tue, 12 Aug 2025 18:09:41 GMT  
		Size: 46.2 MB (46223182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4054b947d11d1569af61507affbe08efe59dfea3bc41368a8c2fac442979c994`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb3b10da797158e90740c9a427cf34be11e24df9e52476debe6a372e7030328`  
		Last Modified: Tue, 12 Aug 2025 22:15:52 GMT  
		Size: 441.1 MB (441101585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8828aafb06cb71dcf990d8e0d88428b39f5e99138233302bd4e72b54af462d`  
		Last Modified: Tue, 12 Aug 2025 18:09:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a26d9b3aa09595423eac804ff40fe6ff438defab46613595775179ddefe1b4`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b4d637fb302e160ef9e0098198e2924ffdc19ad4c25327dffb07d2a0b8ffee`  
		Last Modified: Tue, 12 Aug 2025 18:09:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be58541d11d31f5e657d7ff38f5ca28435a2a2c27d12c43e51062a5531ea3586`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfec8abcda6a5dc7e92724f2b3f70b9fb1992e78e1334332bf799d96844ab6`  
		Last Modified: Tue, 12 Aug 2025 18:09:37 GMT  
		Size: 4.1 MB (4056203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66a186c5a4c3a77d47f8d335dd72ee19c6473d3d2987e8e66f1d4b53b905bb`  
		Last Modified: Tue, 12 Aug 2025 18:09:37 GMT  
		Size: 2.1 MB (2094102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec3f53378c84447f1144a5de3691b9e7b0731d2da6ff5646903bbcc31f82d8a`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.2` - unknown; unknown

```console
$ docker pull logstash@sha256:547979ec0d8fd5ee777a9be89fb6fc9bdfb0c4bef16774126529aa2388d71718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f5024cf05ccaaaf2b580d8e412e12f9dbf4d83437f528582d81aea0ee4b524`

```dockerfile
```

-	Layers:
	-	`sha256:04c926d61ad39e5c3684bcaea417546acd770c1b6de06b14eb88617d459e9a4a`  
		Last Modified: Tue, 12 Aug 2025 18:53:28 GMT  
		Size: 3.7 MB (3653198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d3d4569314a56f5d6012ddd9572c79168fd4342e4b2934886e4f70835279bc`  
		Last Modified: Tue, 12 Aug 2025 18:53:29 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ea6e3470f2e4563630305c62f045a1a0452b6b3c75dacf1fcd4d734317ed62e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521412996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4364e4081dcecb56e6c81036b01e7b43d462888b4038d2a881373e9c2533a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 11:48:35 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.2 org.opencontainers.image.version=8.19.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-07T09:55:51+00:00 org.opencontainers.image.created=2025-08-07T09:55:51+00:00
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926cf1d4612405f02e18a341abdd333274c0ed10a7dfb131d663ce5d1957172`  
		Last Modified: Tue, 12 Aug 2025 21:39:04 GMT  
		Size: 47.1 MB (47144622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b9759e60f2608e1c3487215be27a8a63923137fae7f06198aa1f9864c24c8`  
		Last Modified: Tue, 12 Aug 2025 20:26:18 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd381ae835831c810c8fabf40fe9e13cd3327e4c96a4bd4e22954d2f043c5b`  
		Last Modified: Tue, 12 Aug 2025 23:52:37 GMT  
		Size: 439.4 MB (439384279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbca165f8d96f423fcfda51f0a3fbbdaccb79c1c75501503959f3e4d42b5ad9`  
		Last Modified: Tue, 12 Aug 2025 21:07:30 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acbc5a4abcd650444b26f7a93dfe2877697eeadbad0c0b9a84746607afcdc69`  
		Last Modified: Tue, 12 Aug 2025 21:07:35 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b30a888304158194969a8e58fa0518308b40c707d686e10baee13a841dbc13`  
		Last Modified: Tue, 12 Aug 2025 21:07:31 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc066f6c8e429d1ac44ecec019c8f047361a3183e0156e361effbe9db6a7e377`  
		Last Modified: Tue, 12 Aug 2025 21:07:30 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ecc8dd3f62b067f5b147dd8d60d04683633e812ca9166f7d05b21b5f1d113f`  
		Last Modified: Tue, 12 Aug 2025 21:07:31 GMT  
		Size: 4.1 MB (4056204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cac3cab19aa886006ec2ddec6b4ba1ff14d084c06bc9faa6896583b68e2a11f`  
		Last Modified: Tue, 12 Aug 2025 21:07:31 GMT  
		Size: 2.0 MB (1961621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30feae04a820013eedc37ef19dcdd6d9390b2f646161441e1aa1e9c99f98e98`  
		Last Modified: Tue, 12 Aug 2025 21:07:30 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.2` - unknown; unknown

```console
$ docker pull logstash@sha256:6340dd4118f0f600b2549c9cf5de1c9ad65d91dee46b54411e284bf9871ba6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47f398ae755165555000c79f93b90b1c9971773ebc69781d7397cd0e9f00a1d`

```dockerfile
```

-	Layers:
	-	`sha256:1283754450f3f6011850bc4da9d92f29762988dd41695a08bc6d8b8aa00de1c4`  
		Last Modified: Tue, 12 Aug 2025 21:53:32 GMT  
		Size: 3.7 MB (3653623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16a0905de27367e60261f5c6b0bb853f35f2dff295658847afc556d93b42298`  
		Last Modified: Tue, 12 Aug 2025 21:53:33 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.5`

```console
$ docker pull logstash@sha256:5795a9fc53ac1652b64acf89314dc2f9a5a43e698c0679515d62f03f1db00d6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.5` - linux; amd64

```console
$ docker pull logstash@sha256:025bea6d722dc8c3c98b171278ccb022222e23179d7a040802e59fa2284bd8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484709688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4ac2b997174599622c0b103967fe47cb246079bb3bbc6940a7c1f32372f0c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T10:22:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T10:22:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad47444fc5a812eed8676264bcc40b923f412462ed42f731beb73b2b97f2fa7`  
		Last Modified: Wed, 13 Aug 2025 23:16:53 GMT  
		Size: 5.0 MB (5018161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873f0f25c07f48f4852347a80ca29c840d12b870ae4c99d70b95d91c0be647cf`  
		Last Modified: Thu, 14 Aug 2025 06:03:49 GMT  
		Size: 438.0 MB (437971264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0916f29dbad6f3dd22cfa0b602632b03fa09044bef9a56aa2f3bdb043d8f9`  
		Last Modified: Wed, 13 Aug 2025 23:16:53 GMT  
		Size: 2.1 MB (2066061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7b11f0ddc18e13d3412df84587c2efa2077306679f784536df9098c274645`  
		Last Modified: Wed, 13 Aug 2025 23:16:53 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378dffdb14ac0247a9a1aeba4830b64851697ec8624f1e47c4f1ec50203fe4fb`  
		Last Modified: Wed, 13 Aug 2025 23:16:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677ddd76860712f6eea786160bea337280c3b29ece5aa05d93565d8d6a3212c6`  
		Last Modified: Wed, 13 Aug 2025 23:16:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282ad7a6a61b8912e8fbdcad6835193e967c041795f4e235a9b8fdae649f005`  
		Last Modified: Wed, 13 Aug 2025 23:16:55 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.5` - unknown; unknown

```console
$ docker pull logstash@sha256:36e5682fa197a110b84d03b7626a890dcaa0f84e4c9e07413b6ba197d70930e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816261b6407cdcdb8bfe3b5d71fe2857379dc5bca832fac48b0bad2bae2904ac`

```dockerfile
```

-	Layers:
	-	`sha256:12665623aac8b80955ea194820280a306f1d4b83f5fab2fc9f11c31b154ff477`  
		Last Modified: Thu, 14 Aug 2025 00:53:18 GMT  
		Size: 2.1 MB (2142409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d57b69a65c883bd2d7459dd670bc536ef6723587342b958aaf03b39bb0d303a`  
		Last Modified: Thu, 14 Aug 2025 00:53:19 GMT  
		Size: 29.3 KB (29314 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eef2e0c221b1d37fd88f8d3fb2273d174a736192524c18c59396347e702fa58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.0 MB (481039167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbda4a157aa442cadb2d3dd1c4f47630e8ed5d0c886f14232386d89828e2098`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T10:22:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T10:22:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ca817d464075a675dad1f4df0e1bce238e85eb00f58a44854e305bc5243ab`  
		Last Modified: Thu, 14 Aug 2025 10:12:13 GMT  
		Size: 5.0 MB (5023587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b3daf6394042d3e54b32a06b547598d0288e78ee0634609642eb3aa8938f54`  
		Last Modified: Thu, 14 Aug 2025 19:11:41 GMT  
		Size: 436.3 MB (436255931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92becb04d0a2cf24abd926b6636eb1fd69dcabe91bcdef34bde6d1181e519cc3`  
		Last Modified: Thu, 14 Aug 2025 11:02:22 GMT  
		Size: 1.9 MB (1937633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8ab0540d32d6b6b796b3a27511f474b1e46adc71eefe06ab3478d0ae41f9e3`  
		Last Modified: Thu, 14 Aug 2025 11:02:21 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd46c53882897fdd4267c07822653dd5048fbbab3694f13f57c41ff673f5e560`  
		Last Modified: Thu, 14 Aug 2025 11:02:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edcb2c067e173e0ac7e207d4c6087d9ae8d2bc0ecad5f85e4911cfafaf91b84`  
		Last Modified: Thu, 14 Aug 2025 11:02:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557cc25d7d327266d1feb0643542234b967c6328ff5c1d08ac3e9839f109ad00`  
		Last Modified: Thu, 14 Aug 2025 11:02:21 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.5` - unknown; unknown

```console
$ docker pull logstash@sha256:fa3f8ef6ca9a01721fe7f421c802af2813feb00179f59c83279e6b3d13ee34f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dadac315e93eec076c2f39ff2867dc99df8cac11b096d7f2397e8dafc096c8`

```dockerfile
```

-	Layers:
	-	`sha256:1bb093faf783576d2d6ec0f3c7f103ec934393ef5780a8a2b0b7b1b192bbabeb`  
		Last Modified: Thu, 14 Aug 2025 12:53:22 GMT  
		Size: 2.1 MB (2142981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34db2f96ce661dbe5a113277e7f2e4ebcb89eac240a61cf434b3daf660a13d08`  
		Last Modified: Thu, 14 Aug 2025 12:53:23 GMT  
		Size: 29.4 KB (29426 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.2`

```console
$ docker pull logstash@sha256:d1537d2e7153e5b4dc782dd1921bb67684ddd9219959ffd32b97658930b2c62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.2` - linux; amd64

```console
$ docker pull logstash@sha256:984f91f7223baedf933b935f5aa15f8626a0a2166a7b92c398f7028863ce5ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476774147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435338f35022e619d3938cede01a06c07ecfccf8616eb91d8e626ee2d57ba405`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-07T09:34:04+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-07T09:34:04+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af42cfc228ff17414dedc8ee07e31c76886f8d4117f7030588d35a703c6efdd`  
		Last Modified: Wed, 13 Aug 2025 23:16:29 GMT  
		Size: 5.0 MB (5018180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafd5361609f945ebed08569f5b82b8bd2700047e1830b36449d98ade9f1d3bf`  
		Last Modified: Wed, 13 Aug 2025 23:17:28 GMT  
		Size: 430.0 MB (430035700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d612d949e7b44bd085fe3f28f5479e6f2ede928b53b70bc36a0aa56447e806f`  
		Last Modified: Wed, 13 Aug 2025 23:07:01 GMT  
		Size: 2.1 MB (2066059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa06f8edffc21fb62f5a828be87cf219ec26c47719552a7ce3c4549ed7baed6`  
		Last Modified: Wed, 13 Aug 2025 23:07:11 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91715cc11af4056584aee54dc30f251357585bc15f26bf5322f7e980dc9d345e`  
		Last Modified: Wed, 13 Aug 2025 23:07:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc79b7b0bc764c148922d46e6c4b7eaa3933e75553efdc9bd4b372c8c33daff6`  
		Last Modified: Wed, 13 Aug 2025 23:07:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ade8f1e5256831bfabc5758e887d579a85e7a5ac8862498a78844b26158c054`  
		Last Modified: Wed, 13 Aug 2025 23:07:21 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.2` - unknown; unknown

```console
$ docker pull logstash@sha256:1c4755f27241e5957b128e90b146b47f94c8f5580eb41d75812ef4bbabf59da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce4ff5065b80ea544577681b77a0807ca990e55ad477a54bdf5df80ec214dc8`

```dockerfile
```

-	Layers:
	-	`sha256:001237c9d4011e61e36ab0505c922da7bb778e147a4db29c54db00fe0254e5b9`  
		Last Modified: Thu, 14 Aug 2025 00:53:23 GMT  
		Size: 2.1 MB (2075932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e3f75a0d00cc9db58b43d07edb87b4359a17978f6e84511e5e185b80b571f8`  
		Last Modified: Thu, 14 Aug 2025 00:53:24 GMT  
		Size: 29.3 KB (29314 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2822e6388e7fbf0c728cd73fa393c9809573707a00d8ce2b97f620b243895a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473113170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5b68f714f2849ed7ba335f86f28c7c3c82f65d4e9e4f2d5fdc22de37de8b14`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-07T09:34:04+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-07T09:34:04+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ca817d464075a675dad1f4df0e1bce238e85eb00f58a44854e305bc5243ab`  
		Last Modified: Thu, 14 Aug 2025 10:12:13 GMT  
		Size: 5.0 MB (5023587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce98488b3e626546d3946c4d2d32964d2d80e533eea44e6867e1b78a4c9b80f`  
		Last Modified: Thu, 14 Aug 2025 10:12:23 GMT  
		Size: 428.3 MB (428329917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c394c74edc80b6b528839e90b2d0c3573f6ec8d2062bea39de040e6c22d1f82b`  
		Last Modified: Thu, 14 Aug 2025 10:22:29 GMT  
		Size: 1.9 MB (1937643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0243e1303538877022755f0f4ce349c9364a9a7dcc478222e3c057a8fe1eae5`  
		Last Modified: Thu, 14 Aug 2025 10:22:30 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566828c92df83555d1d26ffc83bd62270e6ce44a73bb947840e045d5442b73d`  
		Last Modified: Thu, 14 Aug 2025 10:22:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1757c4b50007235575cd03409f129012f6faa75cf46bc85ef01f7094cd326a8`  
		Last Modified: Thu, 14 Aug 2025 10:22:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16e7bca5e8880df0cd381e188d17b8b0c53ddc0443c6d65390f301b5ce9ff9d`  
		Last Modified: Thu, 14 Aug 2025 10:22:35 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b1ed75fa40c366a3cb358e0f39e88eccf5eeac7e6d4733f956a91db64646f68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebe332018980b3f36ef6766bd6d504e9724e02cd7924fc1631067ddd97daeff`

```dockerfile
```

-	Layers:
	-	`sha256:c54c64af71fc4db4a441f75b3a52fc80dace86361927e54b84a3f20988a49d39`  
		Last Modified: Thu, 14 Aug 2025 12:53:25 GMT  
		Size: 2.1 MB (2076504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59e8d74e691ec2d42cbc24950606dbbc9476f39cf88677f1e97a82b2d375b8f`  
		Last Modified: Thu, 14 Aug 2025 12:53:26 GMT  
		Size: 29.4 KB (29426 bytes)  
		MIME: application/vnd.in-toto+json
