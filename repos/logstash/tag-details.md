<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.25`](#logstash71725)
-	[`logstash:8.15.4`](#logstash8154)
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

## `logstash:8.15.4`

```console
$ docker pull logstash@sha256:172f0f5876110eecfc4184927d784cd9db8e8817c4ab52be8806d444105349ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.4` - linux; amd64

```console
$ docker pull logstash@sha256:8db4496ec7d277f539acc1a931d822a42de4f1776859b1f68e6c3826361f8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.8 MB (505823578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4305f1a518142f4c9389c8669c34dbb7031b6b9f78b82155bf383ffe060bce6a`
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
# Tue, 12 Nov 2024 16:58:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Nov 2024 16:58:33 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.4 org.opencontainers.image.version=8.15.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-06T19:09:26+00:00 org.opencontainers.image.created=2024-11-06T19:09:26+00:00
# Tue, 12 Nov 2024 16:58:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad3148c487e71d720fce2b87530f5f6d4713a41bf21d109d990601dc894123`  
		Last Modified: Mon, 18 Nov 2024 23:05:36 GMT  
		Size: 50.4 MB (50392146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69af71881b1512af25f2346e6727f06f1443ebfb1e12c94923cae2ec86145172`  
		Last Modified: Mon, 18 Nov 2024 23:05:35 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37012b945ef719720985ddc796a050b5b2746cefc5eacef5e8ce91b0f372156`  
		Last Modified: Mon, 18 Nov 2024 23:05:42 GMT  
		Size: 421.9 MB (421855114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee7c5970d6608be335ffadf7366b7017c8fe03ea41396dcd9bc82c17f9274`  
		Last Modified: Mon, 18 Nov 2024 23:05:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98ab7076270b33f03fe64a6ff1d1bc2ca875102428f8298a0695830ac685969`  
		Last Modified: Mon, 18 Nov 2024 23:05:36 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93146b818e1e88f229dc08447eb03582f9afe41b19350f0732defc0eeaca101`  
		Last Modified: Mon, 18 Nov 2024 23:05:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1f2e9625fa185a17567ff22e484ca3a14d15cb9c0fbc6673804cb0359cf39c`  
		Last Modified: Mon, 18 Nov 2024 23:05:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c294c4eed1ff9f4f6922f4e00802748406340b10de11d5892d01c81b0001f75`  
		Last Modified: Mon, 18 Nov 2024 23:05:37 GMT  
		Size: 4.0 MB (3997017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dd3af941b941b2e19c5dfe62e8b6d8159aa385d60aec5531b1624b86faa3cf`  
		Last Modified: Mon, 18 Nov 2024 23:05:38 GMT  
		Size: 2.1 MB (2061757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f732f21f45dfdcb9eb3f706445418d10e7e5d394b0b2c995f8d45130c6aa9`  
		Last Modified: Mon, 18 Nov 2024 23:05:37 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.4` - unknown; unknown

```console
$ docker pull logstash@sha256:45d4ff7799f099ca2cd31fea2a72a90d1c416088414f6c2de2f3140e7b428e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa05f89b888f67c2302d41fab4bdf1a6f4030a53153648d5d14d540733d575a1`

```dockerfile
```

-	Layers:
	-	`sha256:938a17f3cd992a17e5c834dc29a46d7aed24edb397c19b30432cf12bcc082ab7`  
		Last Modified: Mon, 18 Nov 2024 23:05:35 GMT  
		Size: 3.5 MB (3484653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3586437028414710352fe841e73bda1c169a29421359d2296be859a70637c0`  
		Last Modified: Mon, 18 Nov 2024 23:05:35 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a47e6116b6b4bde7e514a435f5a280556909e8d44bc7b4904bf7350f36875269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.5 MB (490487029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125748a478701bfce73f671046b3cc95c90807f077bc2749932e995ad8b0553a`
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
# Tue, 12 Nov 2024 16:58:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Nov 2024 16:58:33 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.4 org.opencontainers.image.version=8.15.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-06T19:09:26+00:00 org.opencontainers.image.created=2024-11-06T19:09:26+00:00
# Tue, 12 Nov 2024 16:58:33 GMT
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
	-	`sha256:773ce3169bbb028a0eec29dc33fa4898da3b2c76688315f45afd40b6cd50ed48`  
		Last Modified: Mon, 18 Nov 2024 23:51:30 GMT  
		Size: 420.1 MB (420089221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc329d35106ba5e433e5f26b0f9c5a430504afebad88d83b72e060f4e6b0c1`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fecc5b478c11561879ad6e6115a3781bc3a540786edd259a3271300b18b0d26`  
		Last Modified: Mon, 18 Nov 2024 23:51:22 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5333adfc81f859cb09912924d505b04165cff23dc0d1f980c3673a7b0691d556`  
		Last Modified: Mon, 18 Nov 2024 23:51:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f391f424282a84bfa002c78e747ae6054c2857ccba830d17e345674daf449899`  
		Last Modified: Mon, 18 Nov 2024 23:51:23 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af1e9a19b3132ce6b2c6683d79150d4c209f10623e10bb57ef5bf9c9e61880`  
		Last Modified: Mon, 18 Nov 2024 23:51:25 GMT  
		Size: 4.0 MB (3997030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253517d5bb4eafaaffb01c940144efea9a9452a597acd75983b74bb717c55eb7`  
		Last Modified: Mon, 18 Nov 2024 23:51:25 GMT  
		Size: 1.9 MB (1933406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4479f45bf66e8d13f5c939be229e40978aef17cdfa1cc29365caf1541cd89b`  
		Last Modified: Mon, 18 Nov 2024 23:51:26 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.4` - unknown; unknown

```console
$ docker pull logstash@sha256:b242f5b09c5ef8715221b64b9ff792d462ac4c032093c15e16522123dd0a4975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99eb5e1565a2125ded570c2d657913e9425cb989a33153717791ad56054f05`

```dockerfile
```

-	Layers:
	-	`sha256:c742bb17f62259e790538187f999f3feb84942a93f4adc86a3ffa24b87195b21`  
		Last Modified: Mon, 18 Nov 2024 23:51:22 GMT  
		Size: 3.5 MB (3484263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe234febf278c9d7bb103de5ecd2c49a01efa6e1c11bf0e2eea49f02b0ec45a`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
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
