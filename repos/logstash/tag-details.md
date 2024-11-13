<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.25`](#logstash71725)
-	[`logstash:8.15.3`](#logstash8153)
-	[`logstash:8.16.0`](#logstash8160)

## `logstash:7.17.25`

```console
$ docker pull logstash@sha256:c4d1ad71fbf51af03f2c0e67fc0307f52542ca06d472ed194ebff8c05857763a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.25` - linux; amd64

```console
$ docker pull logstash@sha256:effb66cb457febee62e97d9c142b43985c68ac45526dcb924d6ff253adb8c620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450776586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3bcaf9b963180b41783dc41060473438496a67f6acc2d39a4868746b9f92d0`
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
# Tue, 22 Oct 2024 09:34:17 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.25-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.25 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/logstash
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 22 Oct 2024 09:34:17 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
USER 1000
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.25 org.opencontainers.image.version=7.17.25 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-16T08:48:26+00:00 org.opencontainers.image.created=2024-10-16T08:48:26+00:00
# Tue, 22 Oct 2024 09:34:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1f2e94b3dc8babe7ef8531b0794f783d57f9243cfe4cee39d9186ab2d01330`  
		Last Modified: Tue, 22 Oct 2024 17:57:39 GMT  
		Size: 50.2 MB (50200478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9b1b5f4bed46ea07dbae785ee6cc26251dd17a6bc3465aaf3b0323e70f1dfa`  
		Last Modified: Tue, 22 Oct 2024 17:57:38 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e1ae89a01179682c3d9832543ef1ea74221ea2c958d69f48832c54f01d0ac0`  
		Last Modified: Tue, 22 Oct 2024 17:57:43 GMT  
		Size: 371.0 MB (370998644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab85800bfc73507213e0a9b1e3010a6909fc97a64739ea6a162178f5db29c60`  
		Last Modified: Tue, 22 Oct 2024 17:57:38 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa0e990e0604307393a83767fed3c9dbec30b095b32eeea6b55a46b89018b1`  
		Last Modified: Tue, 22 Oct 2024 17:57:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41220547e57c6b0d4698f790031e652e77ddad3579b56e6cf7c7e83e9a1d14f`  
		Last Modified: Tue, 22 Oct 2024 17:57:39 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef324fd4f59a8d25e503b7e2189e713d1d461b4f202e6aac7f38dcf43220266b`  
		Last Modified: Tue, 22 Oct 2024 17:57:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed332ae8422579919db201a826d8d14503c48bf36202baebdcae52d923c3324`  
		Last Modified: Tue, 22 Oct 2024 17:57:40 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec51a9fdf88ca7baa49e02fb25f019b6c2cf05ec26b5dd0c859aca0f392e355e`  
		Last Modified: Tue, 22 Oct 2024 17:57:40 GMT  
		Size: 2.1 MB (2061814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc063274449fbdc93f82b1cbc9327eb66b7609d640f58df6ddfe8fae6c44bb48`  
		Last Modified: Tue, 22 Oct 2024 17:57:40 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.25` - unknown; unknown

```console
$ docker pull logstash@sha256:0551721bf8c4e7c1c7f39b7000f6eccc01b490dd527c7bf65cbe50efa81e7a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135c250b9feefee8101aa474f66921552155c41353b58674be6f048e7a706f3e`

```dockerfile
```

-	Layers:
	-	`sha256:fb4c4c392bbb8803ab065104e2fbd4dcded55845e738d3290d4113ec2cbc63d8`  
		Last Modified: Tue, 22 Oct 2024 17:57:38 GMT  
		Size: 3.3 MB (3310475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0068ad433d52fb6ac0d993f82e4897f24e9b95aa7b49c3875150e0b2807b60`  
		Last Modified: Tue, 22 Oct 2024 17:57:38 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.25` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ea653bb0fad15eb11556561ca0f446bf2e7781b43eab72b5bc6f63d4dec1fadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434218928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9676f38928733fefc69df2429f8b63dbb19fdb4b438d14d6e1ef5b068360712`
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
# Tue, 22 Oct 2024 09:34:17 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.25-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.25 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/logstash
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 22 Oct 2024 09:34:17 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
USER 1000
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.25 org.opencontainers.image.version=7.17.25 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-16T08:48:26+00:00 org.opencontainers.image.created=2024-10-16T08:48:26+00:00
# Tue, 22 Oct 2024 09:34:17 GMT
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
	-	`sha256:817aa90e897f4dea2c6fabf3cddb60c645e69b1c7fab63c82a4946b81023db15`  
		Last Modified: Tue, 22 Oct 2024 18:04:58 GMT  
		Size: 367.8 MB (367816144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2347c47df2211378ec42293f37c9f3e610c8fefd7f881a012484430c655c84`  
		Last Modified: Tue, 22 Oct 2024 18:04:49 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b006b0df303061e0ba4502d2ffce98e4b2d46139c062d058f3551e49cabf451`  
		Last Modified: Tue, 22 Oct 2024 18:04:49 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c45bfeb1d25127f1d45769af22389f1e6dd55a4dc6b41faf451c9a39ebc8d`  
		Last Modified: Tue, 22 Oct 2024 18:04:50 GMT  
		Size: 469.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c87e94284e77ca03614dc5749605556547cdc13e80c1014043d71514f109b`  
		Last Modified: Tue, 22 Oct 2024 18:04:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df90fa04f7d5a4b67e387efc46482c2790d545f5aeb9e8429431a302702680b`  
		Last Modified: Tue, 22 Oct 2024 18:04:51 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79588efaa9016c01ff8878388299f88b3f6dcc5b8f774668605743418f6e7157`  
		Last Modified: Tue, 22 Oct 2024 18:04:51 GMT  
		Size: 2.1 MB (2061810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca7d70fe9c9afea64be49fde2aa344ce683dbd12a4a633bd8f9761ad458d156`  
		Last Modified: Tue, 22 Oct 2024 18:04:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.25` - unknown; unknown

```console
$ docker pull logstash@sha256:14d5a7b88e7ed73a177340a96bda7f6c1d2ae784c84d2081d5184250256c75b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49805c357e2a5cbbaa1f2317dd2707c8e123ca0b5e0e97e35d0857efa16aa01`

```dockerfile
```

-	Layers:
	-	`sha256:f57957deb86970c47499af32e04c4e960fc4bd2befb95935b54159faad5c2c90`  
		Last Modified: Tue, 22 Oct 2024 18:04:50 GMT  
		Size: 3.3 MB (3310710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0904b3e68311c24f6957c5fb80d8d207919d0d3327fdc7bcd7ecb1dfa33ba4`  
		Last Modified: Tue, 22 Oct 2024 18:04:49 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.3`

```console
$ docker pull logstash@sha256:e9c584e7c54a5f59d56b1a3a3f02753af7918a14978d12e9bcbf73bcd8417202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.3` - linux; amd64

```console
$ docker pull logstash@sha256:1f10c7bcb61cfe267b29e21ebb56a5ca905f9179ee76027d7574ce6572761579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.4 MB (506355449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe62e5af9aeff6aa83741bb7227ec5965a170c834109a6b37e6aaa2bec6b7cd`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Oct 2024 12:21:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.3 org.opencontainers.image.version=8.15.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-08T16:06:14+00:00 org.opencontainers.image.created=2024-10-08T16:06:14+00:00
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea98d10c2cddc08a4a118d3b6d0c6105acd13da5f697aba23ac9490713b7901`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 50.2 MB (50203370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c692d5a1244728c73b78455d73be73fdabab85266d2b839f1ae7f6128492fe8`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca356e735bae81f2212307c80c87253e91f7b7cc3d159795909e2fe59537f08`  
		Last Modified: Thu, 17 Oct 2024 20:59:26 GMT  
		Size: 422.6 MB (422575765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3454ff7c6dbad80fc9ae756e2798edd06445d21e13b5e3d1d80ffdc60c28c06`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d416e980a959bc33ffaa1f7b60b34169be87cec4f54a2e38696702d6ef687a0`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e167900bdd3006653b4dd141acf697006700d41effcb8f14e6dfc26813d933`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421832b8f4ac099ad24a158f06b8b91a8b962ac943f95e45dcc103e2a9546cac`  
		Last Modified: Thu, 17 Oct 2024 20:59:22 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac661e059e18181bf57be7789fdf96dbff69c5cbd60fcae0a7654a9932b7f8a7`  
		Last Modified: Thu, 17 Oct 2024 20:59:22 GMT  
		Size: 4.0 MB (3997025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257a94b584e0e83208cfba6e5b1a75ddbcb1e2379020a63808ab309394a0d6fb`  
		Last Modified: Thu, 17 Oct 2024 20:59:23 GMT  
		Size: 2.1 MB (2061753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9b00de5df8cb48b25b59821ab8bfb10cc64b261ea0222b9d37100e6120ef81`  
		Last Modified: Thu, 17 Oct 2024 20:59:23 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.3` - unknown; unknown

```console
$ docker pull logstash@sha256:868332a845b12cb3aadf0174f9b44107b3a380d856b09dcf9766ed6e65171905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3435280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914b4640544acbcaeaafe150854cb9e83253ffd52fd10b6dbeac06df22ac552`

```dockerfile
```

-	Layers:
	-	`sha256:f15d81b8311925b1175dd46fa53600d49a18586515fdf6d6efbed5c7ec5614f2`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 3.4 MB (3400925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa1cbc1168161e9d4b8c563aac964f86e7b23d943f58a6850469f6d369dd09e`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 34.4 KB (34355 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:8296992de05a249067ab0e0cf9a7f9af3f084c3b415d950fa0da7fa7a5acb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (491031712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc94175444da27f95df57340ae93c90db6fb50f8052fadcabcf21458830354cb`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Oct 2024 12:21:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.3 org.opencontainers.image.version=8.15.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-08T16:06:14+00:00 org.opencontainers.image.created=2024-10-08T16:06:14+00:00
# Thu, 17 Oct 2024 12:21:47 GMT
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
	-	`sha256:4d8ec2b910729266f502e6a476f5207d7da5869f2f115f50060b2644266da783`  
		Last Modified: Thu, 17 Oct 2024 22:22:35 GMT  
		Size: 420.7 MB (420749476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c6c31fbfb5fd3725320dc3b3c9692718f6e473f3cbe4500da6762ecca2e53f`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253c92098177faf6220d827801fed4f7850f2fd92b973f4662221e8a268968f`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e47cfbb41d5a05f67f28230be204fd448ea51ab1cb6c7c1baa282d7fccda8fc`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9677ea5582d44bd4c3dec770bd34ccd3ed888d7540916ed9c4e7d91034544ecf`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16aa31c894b1d6e99cbc8e1b9fe662d5f258f1234a3a3107a7a11740660b9fb`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 4.0 MB (3997022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c9d22509209078c415186fe73a30f690aacc76505201f540df8071a1751196`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 1.9 MB (1933407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d996ad56bdf53ebcc29e734a8c5a6770ff090fdcc605f344e9f9ed4f3a7f7`  
		Last Modified: Thu, 17 Oct 2024 22:22:28 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.3` - unknown; unknown

```console
$ docker pull logstash@sha256:93de7eeb86e5b87336a5c145b163bb6a7b18e01b5b0a5a26d7ba4108dd7869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3435027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2316e0ee359a7baa8cd3cc308328de8830486d312af41f14fe83c542a2ca03ea`

```dockerfile
```

-	Layers:
	-	`sha256:a22c6a54f481a1ccface5e1c828e8552b5fd85b1ad43e12ba7eebfbb3df14227`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 3.4 MB (3400535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ea3278c5d802e96c91c7dfa6450b98d8e1bfe4f4e079d5c0c39a147b86848`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 34.5 KB (34492 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.0`

```console
$ docker pull logstash@sha256:a183d891806141a0820a05c9b914568007288d465da08b746322a41df6cefed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.0` - linux; amd64

```console
$ docker pull logstash@sha256:7a065833d07cc8340c8e3242b2ece8366e07acc310a43c0c65f6fdd1f526763d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514604128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c64e898c8214867d81f1d71d47f40a36c2cd26532ac19dcfde1c51785995b`
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
# Tue, 12 Nov 2024 13:42:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Nov 2024 13:42:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 13:42:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 13:42:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Nov 2024 13:42:14 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
USER 1000
# Tue, 12 Nov 2024 13:42:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Nov 2024 13:42:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.0 org.opencontainers.image.version=8.16.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-06T18:55:01+00:00 org.opencontainers.image.created=2024-11-06T18:55:01+00:00
# Tue, 12 Nov 2024 13:42:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad966883e5cc1e80ef31fe2f4a03e377baa21bd3b665131ab39f771ffab21828`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 50.4 MB (50380191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785e45217de27e8c1520c6ad8dc7d0a737578d21759a08cd6b81eb2b8c3509fa`  
		Last Modified: Tue, 12 Nov 2024 20:09:53 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c335fb15619873f4760a4f2feabaf12edeb10cb7d28654bd0de496de74b5a`  
		Last Modified: Tue, 12 Nov 2024 20:10:01 GMT  
		Size: 430.6 MB (430647620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87411635e9e63a7c199465485fbea83720b3b2cb6c2a97144f29509b5d7d3ef0`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb6d6c2b662d0871fe0748c11f45126dcb05b89749690a1d2439f8ce1910463`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2e9beb3309427f27e9e36afb8e75a402f7da08ce647b490a280ad707f22dde`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fc0350bd4dc24b04cbb641d7e4644a9c5c944a46313844c8fdcf90060335d0`  
		Last Modified: Tue, 12 Nov 2024 20:09:55 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921e90be1df081412721f65ddf7d6bee9f32acc55bb9fc605936075e06af4fec`  
		Last Modified: Tue, 12 Nov 2024 20:09:55 GMT  
		Size: 4.0 MB (3997014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e861fb9d5eb23bb50f745a33f5559ebf8d631a79f245bed6b0d4ffd143eb428`  
		Last Modified: Tue, 12 Nov 2024 20:09:55 GMT  
		Size: 2.1 MB (2061759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ee52137ec5bee5712951eb165bf6365e926db90a4395b0f4575cae645e8e1`  
		Last Modified: Tue, 12 Nov 2024 20:09:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.0` - unknown; unknown

```console
$ docker pull logstash@sha256:737797bd86efb4265e475a67d87d5d1bd397d5a32f98411138bdf8f983f8e123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4a95906671c4da0fe1a0bfd63432e63d6b9515b3aee0d9114dde34fab5f5d`

```dockerfile
```

-	Layers:
	-	`sha256:57ea1d2ee9ff0d0970ab0db366914689a633157092ae5350c771c67f393ae637`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 3.5 MB (3529151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fbb8b86b7a2d2f621abca784b10ed07c304f73b62ca99afacfd7f874d84bdf3`  
		Last Modified: Tue, 12 Nov 2024 20:09:54 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:26d19f4d86efa326f6d3c8d04feb3592ab3b702078aee354545ab432bc7a5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.3 MB (499262203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd8b471acf3e0d073a3ae5467885bfe17fd5452cc08dd4c20b6c8a16728c45d`
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
# Tue, 12 Nov 2024 13:42:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Nov 2024 13:42:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 13:42:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 13:42:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Nov 2024 13:42:14 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
USER 1000
# Tue, 12 Nov 2024 13:42:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Nov 2024 13:42:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.0 org.opencontainers.image.version=8.16.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-06T18:55:01+00:00 org.opencontainers.image.created=2024-11-06T18:55:01+00:00
# Tue, 12 Nov 2024 13:42:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff23e64ac746b912ab7f30399f8e7d4ca55207ca95415ca913735b145742503`  
		Last Modified: Wed, 13 Nov 2024 04:46:15 GMT  
		Size: 38.5 MB (38477693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6048047e135a54fc09ae37a6800831eb2d24523170230007b52a987b4e67b233`  
		Last Modified: Wed, 13 Nov 2024 04:46:14 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d326d04c8af4af2916f8072d4dfd34a7dd922ad079428adb5fb9dca0ac4fd8a`  
		Last Modified: Wed, 13 Nov 2024 04:46:24 GMT  
		Size: 428.9 MB (428873791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041c3cf14823d38e3d8e5353abf984c3f2142ec1ccaffb67b9361c8a02ae605`  
		Last Modified: Wed, 13 Nov 2024 04:46:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7adeb89fda43c78f747a63be89bf86df7f92cf60a8ae0efba51ac5f8fddaa94`  
		Last Modified: Wed, 13 Nov 2024 04:46:15 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e5e8a5605c9dd247f634e3d6b5932b6c92e7db9e65ff7fbfa278229df3148`  
		Last Modified: Wed, 13 Nov 2024 04:46:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f33063db204c4feee3da5b1e2efebbd868dec70896c5b217da688000c15ceb`  
		Last Modified: Wed, 13 Nov 2024 04:46:16 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbc412adb87cab31f4f9e6774ae01b9a4ff7c4f5154885275348777f21a347a`  
		Last Modified: Wed, 13 Nov 2024 04:46:17 GMT  
		Size: 4.0 MB (3997022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac4c45622dcfc0c2ffa62046757aaec7e7e1230765e8f2f3640673ec61e8e7`  
		Last Modified: Wed, 13 Nov 2024 04:46:17 GMT  
		Size: 1.9 MB (1933402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27f4332f6bccaf08b69382f019c2a2680b188b14957cf4c7b3e38d2ea671543`  
		Last Modified: Wed, 13 Nov 2024 04:46:17 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.0` - unknown; unknown

```console
$ docker pull logstash@sha256:14ec7156c4e2ab4ea21848e7885622c31361ff8ee5d28554b0276876ca201abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d5672a52b75a624ce562201694f1f2be2b00b02f7793818467f92cde8ae6ac`

```dockerfile
```

-	Layers:
	-	`sha256:e97629adaadcaa1df59718c08dbdd138c403794eabf4ea52fd1f22fad75f9754`  
		Last Modified: Wed, 13 Nov 2024 04:46:14 GMT  
		Size: 3.5 MB (3528761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc63458c3a066c74f1771e1b0eb899e991e61ebdd812c21d7d379b43935e49e`  
		Last Modified: Wed, 13 Nov 2024 04:46:14 GMT  
		Size: 34.7 KB (34713 bytes)  
		MIME: application/vnd.in-toto+json
