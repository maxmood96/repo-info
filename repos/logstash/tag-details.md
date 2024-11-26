<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.25`](#logstash71725)
-	[`logstash:8.15.5`](#logstash8155)
-	[`logstash:8.16.1`](#logstash8161)

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

## `logstash:8.15.5`

```console
$ docker pull logstash@sha256:43949b5fee039921115f78d79c318503cc3b8af1a8efa798240a30c353568186
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.5` - linux; amd64

```console
$ docker pull logstash@sha256:f3de51b13bea6897ac7496fc46342d073d132c8eba88c8cae61662fae0b7a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515357536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4891356a761f2a9370c13271a5aa237fd683d9969491981712105c7f82bede67`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Nov 2024 10:47:54 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.5 org.opencontainers.image.version=8.15.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-21T16:16:23+00:00 org.opencontainers.image.created=2024-11-21T16:16:23+00:00
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d467576d027ee917add60ed057027cbfafe9b6139f4e1f4112dad294c875ff3d`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 50.4 MB (50409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6706af1a07618caa8d4af859709eaaf55e715275af7db3e8ae930e64ff1ba`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f870dba6bf45b93d6c312446a20a53eb591da18477fec61880a38c38104e896`  
		Last Modified: Tue, 26 Nov 2024 18:25:07 GMT  
		Size: 431.4 MB (431363368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2055655aa54efbbc940b03cc105344f2be0ec6ebb65557a56401b238265c5d8b`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee372098071524c765125781865849f1e06107f02880b3fbc82511c8e640ddd`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ab42e604edb867443fc12e79875505daa2358932dc5115aa01969f204ab1a`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac059fae36e7c58b9481f299a9340e80c3ede5de3eb69aafe21b341db222ac`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374e3741fa9f41ab713883e6a4e968bc11ed4c763d675d662c58e949ad17fd6`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 4.0 MB (4001896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5cb76831869a918f7ab07fefc5effc351dfd4a5aadb32c15bd3839b00ed30`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 2.1 MB (2065124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dceece115d91a46ab37701619e4e168a784d07dbf3abf2da6526e76ae62e0bc4`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.5` - unknown; unknown

```console
$ docker pull logstash@sha256:00d89b30d6cd2e16f2a85e1e4b8ae09d44a0495920fb9ea005d991055744cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcf1d3888254b991f9c480924b24b694d11a22d3f40e105040f1b44e1bead20`

```dockerfile
```

-	Layers:
	-	`sha256:d6e0b8e2edf5c000459180edc48df5cd4bb7e96866ead0b5d1a708fed113f43b`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 3.5 MB (3528509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98661fd14c7f0d12a3a1d56ca390e9435fbdededb6e925dea4a2ebd0ce63cd08`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0081f5fc82a47b937b0155713f6dcdea4a35c1d24e42f3e1ed998e1da321db47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500009957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3226f150472b2d4b63bc994c368445512c9aead831d08e8711664f54f2815fd`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Nov 2024 10:47:54 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.5 org.opencontainers.image.version=8.15.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-21T16:16:23+00:00 org.opencontainers.image.created=2024-11-21T16:16:23+00:00
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79676800b9a2ae226dc384582a2bae1d0ddec86dc46fc29d0d8a5b8459060953`  
		Last Modified: Mon, 18 Nov 2024 23:51:28 GMT  
		Size: 38.5 MB (38487075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d025482904aeb44a113a53cf5d18a7d0af58be62c4efe85397a3e7abf888bff7`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdad7cbb33ea66d7fa0ad7c7896b2407744d2032f9462dc3efe10dfdeabde69`  
		Last Modified: Tue, 26 Nov 2024 18:35:59 GMT  
		Size: 429.6 MB (429603717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab8446a2b0b5c5aea02da8e4357842adee7c6980de0ba35298bfb659b4531c`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c50765c2d6c8d15a472d35a9e410cb907ddd33567cc4ae209c07021e3fdb5e`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2406cfa7359e0aba26cec4a80ad41cd9d550e7e7f4bcae3d84866949beea9`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72852dc912f589de751bf09cdbbe4df2efc80fcd72393edd2ca6c5edd2551bd2`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170ac01a72c1b7141476084cd0888fea3db75dc58bdead14aa6be18420d2eda2`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 4.0 MB (4001887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b149cab116c8bbdfffcdf5d4cb7cf3cdd691d8ff07fc9db3d25fff645f728`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 1.9 MB (1936982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f65f99bec163bdf85b20388e53e54c7206ecad9f5ffdaed47bed110fdae37ce`  
		Last Modified: Tue, 26 Nov 2024 18:35:53 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.5` - unknown; unknown

```console
$ docker pull logstash@sha256:334a1191d51b8f0c8cadb6f2838554df90da359febe778cfc0e3e171c49fe40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037435ee020fb8e8317f3f05792828708da75554109628d4fcd7acbc84f877d7`

```dockerfile
```

-	Layers:
	-	`sha256:211ae244ac25c0ec994a4771b090c64c22b8659938a389b37eb018b519382f1a`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 3.5 MB (3528119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3be302d019b01d07f980b3a45ffd6107f0a219af0445bdc1401af5abb469b8f`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.1`

```console
$ docker pull logstash@sha256:dca706ef2cf7b0ea326f49bec73647c04270fc763d73eabf93408161955793a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.1` - linux; amd64

```console
$ docker pull logstash@sha256:a40a832bb6326f09f7e838abb1173923cc047917469cff0a9a26b95d1f6f38dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.5 MB (515455318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd31c622a44e005068175bd014caf3f2cbedd5e298d64434366759413ed01b50`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/logstash
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 21 Nov 2024 14:43:56 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.1 org.opencontainers.image.version=8.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-19T01:53:47+00:00 org.opencontainers.image.created=2024-11-19T01:53:47+00:00
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80872c9925b6f48397a6937dc5be5e9373358f98508c764e9d929dc25689e3`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 50.4 MB (50408006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363de12eb4ff2aec1086ab4499aa06074f4ea13d96d0a07ded975719405a3489`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ebe8adab0a34021d4cd1cac5b802f8a6b8752df68935f97e47f848ec59df67`  
		Last Modified: Fri, 22 Nov 2024 22:26:17 GMT  
		Size: 431.5 MB (431462753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afde81803e1e75ddfa396bb408f2b6aae7ef763adab17fea78ff509375c7f38f`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66239faf6529a87f2645a6072cd214e7170c84c3122b320ef51564d3d79a908`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adede9264b3cba4e05f29c4a78b468a3cad6ad572534cd4a672e95d3f4ce12bf`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1439ce21dc366f956be64cd5a61f428c94134638365ed2e25d60ad1e2bbc8e4`  
		Last Modified: Fri, 22 Nov 2024 22:26:12 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534824f74d362b3b248ec465f8a17466c320bfb45ebd68bcccc4910b1632b92`  
		Last Modified: Fri, 22 Nov 2024 22:26:12 GMT  
		Size: 4.0 MB (4001890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35a282d07a3b67a7689c5a03f3bc07411ff413ac272773bc2a7c3f8a5794e5`  
		Last Modified: Fri, 22 Nov 2024 22:26:13 GMT  
		Size: 2.1 MB (2065126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6379766a8d4536ba8c0897f1f7be2dd83963d814e028fe91fef745e8837fa4c7`  
		Last Modified: Fri, 22 Nov 2024 22:26:13 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.1` - unknown; unknown

```console
$ docker pull logstash@sha256:d5f2272e6517d03bce5cbbdff7cdbefdf136d85c3ccb8394faf0fe79d4cc8522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e7bca2dc6c7c277467d5480c4ff9cd27dcbcc2df8ff54bdb860d88e63d1f82`

```dockerfile
```

-	Layers:
	-	`sha256:46427d5071ef08e19c9ea7546a46943c38364dc4445101225dec07b3a54d1a4e`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 3.5 MB (3524251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7a4f6710a06aaadb029a21d7ef106cfc61a95ecc62e4439d69ba50c8401660`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:df5af145fc4ca05deaf69963d6b51c54e5082b716cc83fefe41b1a3c812ef0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.1 MB (500102906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42c729c3ef93d4c1cc1d43a0a26dc70f56f965df020c218e646f5ca2e629b20`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/logstash
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 21 Nov 2024 14:43:56 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.1 org.opencontainers.image.version=8.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-19T01:53:47+00:00 org.opencontainers.image.created=2024-11-19T01:53:47+00:00
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79676800b9a2ae226dc384582a2bae1d0ddec86dc46fc29d0d8a5b8459060953`  
		Last Modified: Mon, 18 Nov 2024 23:51:28 GMT  
		Size: 38.5 MB (38487075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d025482904aeb44a113a53cf5d18a7d0af58be62c4efe85397a3e7abf888bff7`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47bed8a6240efdbe4462480b8e42d506fe2c4e71723181decba9c6582905498`  
		Last Modified: Fri, 22 Nov 2024 22:41:26 GMT  
		Size: 429.7 MB (429696658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07ba47bab9006d488a02f8272b30b6e4484c969109ee52d7974a0ec19f5b5a1`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf88e69d76fd18dccdb70bd45b0d010c3270356b44a067c98a69227f1305a74`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2978499e6052f9df9ebbda0ba05c3a72c0d492c396b69d2750980aca3331754`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793204f9ab56c7ef3b468874b288c107715b7fe90d87955c1e1d771210e1f23`  
		Last Modified: Fri, 22 Nov 2024 22:41:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ad38fb02eb2a5ab4a02c19cf3597494ac52ac9dedfdd896cdb3440162558`  
		Last Modified: Fri, 22 Nov 2024 22:41:12 GMT  
		Size: 4.0 MB (4001890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03350f2a738dde0c0e914e2e922b6dfba6bba204059c637192a588758fdc1ea6`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 1.9 MB (1936981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b84fad0ef32e07350f225582268892c3e83e5f17596942bc65e968222817a0c`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.1` - unknown; unknown

```console
$ docker pull logstash@sha256:4a53918afe3dc725e0fef6d04d1625a481091094953dab0aa8904672c9628141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1131906f3c3b1599ba30a4a4ee915d5bb4fdc29a2a2756af669b9b6342d88d61`

```dockerfile
```

-	Layers:
	-	`sha256:efaab9398f139731f147f5bd0000ef0ef5da739b6c8f183c14a8f15eef08941d`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 3.5 MB (3523861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c736e1ed149ee08564f6704126b7746ba67b7893727639c3e516246c1b5407`  
		Last Modified: Fri, 22 Nov 2024 22:41:10 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
