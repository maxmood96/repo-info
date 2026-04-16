<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.14`](#logstash81914)
-	[`logstash:9.2.8`](#logstash928)
-	[`logstash:9.3.3`](#logstash933)

## `logstash:8.19.14`

```console
$ docker pull logstash@sha256:7ced20a67d3674d1693459e7eec5f6e6ddb588b823b2fc55d54fd8b0f639a647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.14` - linux; amd64

```console
$ docker pull logstash@sha256:073fefce3f66ea40f70d679aada527d0b02b9fb15673b32db94aadfac4ef02c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.8 MB (538824330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d114ee9337abc21b33eba1baaeae5d58418596acaee97ff6dd3c235dd85b480`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:30 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 15 Apr 2026 20:44:30 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.14-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.14 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
WORKDIR /usr/share/logstash
# Wed, 15 Apr 2026 20:44:51 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:44:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:51 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 15 Apr 2026 20:44:51 GMT
USER 1000
# Wed, 15 Apr 2026 20:44:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 15 Apr 2026 20:44:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.14 org.opencontainers.image.version=8.19.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-01T10:06:20+00:00 org.opencontainers.image.created=2026-04-01T10:06:20+00:00
# Wed, 15 Apr 2026 20:44:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1c7ae89cd7ca3a315ca785b4ed86636a5435ebe6410c057a766cf87f06709e`  
		Last Modified: Wed, 15 Apr 2026 20:45:33 GMT  
		Size: 52.4 MB (52358193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078eecc0c58d78b7946ad0e3394a1627499d428b3a1cdc433fa0bf74ec85109d`  
		Last Modified: Wed, 15 Apr 2026 20:45:30 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6496a725fdddccbcd4e0b04e0addbecb44b7d3c61f9fe3c077677d0cb0d478`  
		Last Modified: Wed, 15 Apr 2026 20:45:44 GMT  
		Size: 456.5 MB (456465427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0df968f5fb5ee7bbdab05d93008f4eec10890ae33e85e9831812c3f5cfcd64a`  
		Last Modified: Wed, 15 Apr 2026 20:45:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f0f31c483c1b0c9e70250766785d78b28c5c66fa5acd3f999592718d915f88`  
		Last Modified: Wed, 15 Apr 2026 20:45:31 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0fe90079e845d81026a8633509136f38e693fae59fae982480a7397f6ef08`  
		Last Modified: Wed, 15 Apr 2026 20:45:31 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a433106f6ebf89e7ecb8dbafa6f76b0fd188348735c66bd04943b28af9f33649`  
		Last Modified: Wed, 15 Apr 2026 20:45:32 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776ae6a41a4311346a29fbb10e717410500d2eaf39a956064447c5681fd19ba9`  
		Last Modified: Wed, 15 Apr 2026 20:45:33 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4eabacdd022219754df47bd4ea65b865c892cdb639b389ca106c5db128355`  
		Last Modified: Wed, 15 Apr 2026 20:45:34 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111e7417a4f54af7129c3cb67e4888d756ea2074e0724f9429e800fd2444a098`  
		Last Modified: Wed, 15 Apr 2026 20:45:34 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152190013c8deab786863db5f8b94da2dbb736f5a1b77d2de972e03f9cd2eed`  
		Last Modified: Wed, 15 Apr 2026 20:45:35 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.14` - unknown; unknown

```console
$ docker pull logstash@sha256:9179b8424671f6f417d5c7ce9e23a643ba27dfc2ac898d68043d5f6708e169ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3601e72e7cb2ec7f12be440cecdf966f06e3fa60ee5f4b0b3d329f891f6a71`

```dockerfile
```

-	Layers:
	-	`sha256:d09d631cd8336c1efda18995fd0d2714091315fb408055632495360dcbfb8430`  
		Last Modified: Wed, 15 Apr 2026 20:45:30 GMT  
		Size: 3.7 MB (3695661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad16e08c4e144831e9bc4633f1d02543ae5621798c9cf34b5e14ddec6ddfdb1`  
		Last Modified: Wed, 15 Apr 2026 20:45:29 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.14` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:132dc5d0b955186a04efec8265b8bf2e80dde75ee5099fca13b125a056f4be10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539327001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7f405223a3c4947d35e68d99ab355cdd61af21ebb9da82f3ca0e69a1de1e2b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:32 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 15 Apr 2026 20:44:32 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 15 Apr 2026 20:44:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.14-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.14 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 15 Apr 2026 20:44:54 GMT
WORKDIR /usr/share/logstash
# Wed, 15 Apr 2026 20:44:54 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:44:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:55 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 15 Apr 2026 20:44:55 GMT
USER 1000
# Wed, 15 Apr 2026 20:44:55 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 15 Apr 2026 20:44:55 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.14 org.opencontainers.image.version=8.19.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-01T10:06:20+00:00 org.opencontainers.image.created=2026-04-01T10:06:20+00:00
# Wed, 15 Apr 2026 20:44:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cdbfddba949f66864a30975c51cb8d266f844fce32aadae0f213b5977931ec`  
		Last Modified: Wed, 15 Apr 2026 20:45:36 GMT  
		Size: 55.4 MB (55439536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86de455e6dae87ca36959203218089b6592b7a88562ed0ecc85dd46c6e459792`  
		Last Modified: Wed, 15 Apr 2026 20:45:33 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2caf979fe5be0b4d000a006bb83d4d1b52a1789ace14b72a84987c8e12d50`  
		Last Modified: Wed, 15 Apr 2026 20:45:43 GMT  
		Size: 454.7 MB (454743949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef3ccfe3ab5203a82e77355f6f3adce4ba6fc2bc445af75b51dcc8a5c2cc6f`  
		Last Modified: Wed, 15 Apr 2026 20:45:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cfc6764ccff470a994184c7977e08da23eba5faae7bdc37727311220187370`  
		Last Modified: Wed, 15 Apr 2026 20:45:35 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716bcf27c1d7f6e0466de5ea887694b012b7c14e566ca242524ac0afd3883ca`  
		Last Modified: Wed, 15 Apr 2026 20:45:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018af48770a48271c2490b849d9bbd52aaa815fd045efe1deee7d6c0f22da7e3`  
		Last Modified: Wed, 15 Apr 2026 20:45:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcd1b1edf29fce20d0d8ce34894e55250792ec0b4675c7591adf667f2ae4d14`  
		Last Modified: Wed, 15 Apr 2026 20:45:36 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2ffe672d68b5b19ddca886ef8773a5ecbb0b6fd134c53b849fcd8965eea582`  
		Last Modified: Wed, 15 Apr 2026 20:45:37 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b539a10d427036fb1d77372cba2a5c184879028978eb7dd49648c819920c886`  
		Last Modified: Wed, 15 Apr 2026 20:45:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3e358ec372652ad42d5e67eac97f0cf85413dee17e7c838cefb5e059dc636`  
		Last Modified: Wed, 15 Apr 2026 20:45:38 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.14` - unknown; unknown

```console
$ docker pull logstash@sha256:5133cfa338486766382c075b773c850ae2ae6112e6ad7e179ba3abceb22dc86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794e6b2c44a76c6d913f372d53e7d0564fa67caf9cc1d3abf78afc91a90f2e5`

```dockerfile
```

-	Layers:
	-	`sha256:bd24d85c88b5229850d4867e6790d3b5c78437a30aec388a0fef6ca0df9bb75c`  
		Last Modified: Wed, 15 Apr 2026 20:45:34 GMT  
		Size: 3.7 MB (3696086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902d1668ab93bb1796ad436c1c76adc1ff35c60b2d6f49a9da864c4daf6acbe3`  
		Last Modified: Wed, 15 Apr 2026 20:45:34 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.8`

```console
$ docker pull logstash@sha256:6ec79aaf01acfd8d249449491ce540b427fc85dc4c885c16ad89d5583627a7b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.8` - linux; amd64

```console
$ docker pull logstash@sha256:b084a7fb2621c3c01aaf755a69a1b8384af1e929913b5b91572a6b4e7772cb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 MB (502209292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc45b228e90ec8099435501fe22e0bc3f3c2b16812e8f61bcb42b8f8b08a212`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:46:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:22 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:22 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 14 Apr 2026 20:46:22 GMT
WORKDIR /usr/share
# Tue, 14 Apr 2026 20:46:24 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:47:12 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Apr 2026 20:47:12 GMT
USER 1000
# Tue, 14 Apr 2026 20:47:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Apr 2026 20:47:12 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 14 Apr 2026 20:47:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2adb44efeaf04731dbf87bcd2b655f9f36dd9b9f356720ec386047d56d67eb`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 5.1 MB (5148733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974e78d004cb1f87c0d4b74e3b7936d701a9782381d39db8cc0ed5c7e61a7a90`  
		Last Modified: Tue, 14 Apr 2026 20:47:54 GMT  
		Size: 456.8 MB (456779264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93666399022bb3c308a40a5411007dccf767080c2900390e59c236445ab78746`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a442530da5541b98e3d9ff0ca0b2bd1a6d91ae4c229f722b7c0cb49f78864f6`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cc50646edfd19a4ede3ffe785acb9059a037d31b3abd7cc8a0218d45ef6bbc`  
		Last Modified: Tue, 14 Apr 2026 20:47:45 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e15b7cd8f8e78d8780a5bf6f28180490c71e7b7e9473d3d1514e34a58dba6da`  
		Last Modified: Tue, 14 Apr 2026 20:47:45 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2ac2c60e954ab0c645b6b09ef5c627a0c6ad1499f58bf1c5bbe333a64018bc`  
		Last Modified: Tue, 14 Apr 2026 20:47:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebc51da9722477dfc6e7b8d3a4cc4a4cd4c4bff9712e3314ab061c130aa835a`  
		Last Modified: Tue, 14 Apr 2026 20:47:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708f315124376c319c87528f66ea3e1f90f881854f86b46ca3c6b1f7d75dc4f3`  
		Last Modified: Tue, 14 Apr 2026 20:47:47 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:52e43593fed664888e9078971a7d1016516c98ee74fd5b07d70788e575deb108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773260008eca2af77cdb856a40c73280b6f26e2abfdc9b53e9bfa0e4a1339143`

```dockerfile
```

-	Layers:
	-	`sha256:e6468a12654b33315cb856bb78c768adba787c8210905fe185b71c7f25a7e05b`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 2.1 MB (2139784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c172a53405ac5c9cb43d7107a843510f0b45ce3b5101680161a984a54dc99657`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3bfdffbc7b2a0db53bcf089c478252965a3d31e2bbeb7cf29a2a97d6acbc8906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 MB (498677627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b10ea1ee91d6e477783c2503005607cefd16196da750036dbadbbf782fe81f5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:46:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:09 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 14 Apr 2026 20:46:09 GMT
WORKDIR /usr/share
# Tue, 14 Apr 2026 20:46:11 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Apr 2026 20:47:00 GMT
USER 1000
# Tue, 14 Apr 2026 20:47:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Apr 2026 20:47:00 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 14 Apr 2026 20:47:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6437c294178eb5f6b988b14e7096a7ea580b86b1f2c2cfa7226b64b8970009`  
		Last Modified: Tue, 14 Apr 2026 20:47:37 GMT  
		Size: 5.1 MB (5148124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f252a2c0041d47f5760a7269bbe98abddf2036d8a73ee8148c321ad57e8ccf14`  
		Last Modified: Tue, 14 Apr 2026 20:47:45 GMT  
		Size: 455.1 MB (455064668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b56d5dcc2e612e74b330fd535678dc7b9bdd6a72be13eb20f3183f54e70e92`  
		Last Modified: Tue, 14 Apr 2026 20:47:37 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bd5f289b3b0160b2eeb07ce6a2185df4021935f284a29bb47f14122411a178`  
		Last Modified: Tue, 14 Apr 2026 20:47:37 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03edbcba8b9d21d295b0af2e5b63d607b2e13d69bce24c962de722bb3a4efb6d`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc64d2fc98e0ec0ad8b52f6e6b066670bd3266094285b83082803198e53bb16`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4175e572e7b30e8aaaf1f48ce8506edfa61839c730d6576f1205666313a3587`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3808fb64fec4f446615b12da41919ffc80b28db1e16dbf9a471c1ed55a3279`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17275af5ce1b0f5e4b6c7d30a7fb13a84253900d431eca40481cf213cfae1a2`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:bfe75c23ef2b004e0b262927305b1eb3942f1dfe6eeec432badbbdce60bcf07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798b52f725942d945185d2d70287d8877822bba63ed30f76aff77d835f6c480f`

```dockerfile
```

-	Layers:
	-	`sha256:c0c2ba395c30dd2aae1206a5e674f0cfd9b1d87b28cb0f32c8939205b21ee612`  
		Last Modified: Tue, 14 Apr 2026 20:47:37 GMT  
		Size: 2.1 MB (2140354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4abbb49a25322813629e6a6124d90aeebaa53bcb218c0e4c37d4410adad2b1`  
		Last Modified: Tue, 14 Apr 2026 20:47:37 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.3`

```console
$ docker pull logstash@sha256:dc0d1bf5b4fd7eadf7ebf3cf419c1df11288649ebd5cf91ef82dcafe5d6a106b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.3` - linux; amd64

```console
$ docker pull logstash@sha256:a59717015a0c30a63386350b3d4be9c569ca20b9152daa3f0993611222444588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516513039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf52b880fa8e065e03c1c1b6de0d3a6f33f4bc77e2cd2bd48d78d9e23a52c03f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:46:32 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:32 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:32 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 14 Apr 2026 20:46:32 GMT
WORKDIR /usr/share
# Tue, 14 Apr 2026 20:46:34 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:47:23 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Apr 2026 20:47:23 GMT
USER 1000
# Tue, 14 Apr 2026 20:47:23 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Apr 2026 20:47:23 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 14 Apr 2026 20:47:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8c5d97188a24c149710b30abfc582297cf899fde12539411bbfcd6aef5caa2`  
		Last Modified: Tue, 14 Apr 2026 20:47:58 GMT  
		Size: 5.1 MB (5148592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d7bd2224639e33daf6d564065b6660158bb4077d7a3b66f87f1068a92bae3`  
		Last Modified: Tue, 14 Apr 2026 20:48:07 GMT  
		Size: 471.1 MB (471083150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa76ff325753ede4aaf4e8a3b2a9bc8161019c35e6367a4afb91a5a0151692`  
		Last Modified: Tue, 14 Apr 2026 20:47:58 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f452820b0e27d1cb69c281a46c6646eec9ca404cd1eb8ed2daf3cf0d61c5da`  
		Last Modified: Tue, 14 Apr 2026 20:47:58 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1859c89a0517867110102ec7bbbea2a659a93702bf8d7ee1662abff202d6901`  
		Last Modified: Tue, 14 Apr 2026 20:47:59 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a385e74174c465f4fbc7e8c8d352b8cf79df7e208e1ba18260ae44b49a07f5`  
		Last Modified: Tue, 14 Apr 2026 20:48:00 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868954e28d072cee06656e0f202fc0f13f8ba1da316bf270e3c05b0a9fefec95`  
		Last Modified: Tue, 14 Apr 2026 20:48:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918f294e91f761472f5e9c2e10e2ebd2f84b66645b97b396be20bb61d2daf5c`  
		Last Modified: Tue, 14 Apr 2026 20:48:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3826ef4f126f66c1130bed02f6cf9f26eb521b07a7d423ef6ec4d579d98faaa`  
		Last Modified: Tue, 14 Apr 2026 20:48:01 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:43aa2c0ca8f816b1b95e314bf9d2a98511f662c2e47719b3792001cf5216e144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cc26977dd266451aad526be6b55219515a91c51148b02cbd5a3b6354a7decb`

```dockerfile
```

-	Layers:
	-	`sha256:a79b2a7cc1e6545d5d3a320b993a49c36364dd133b11d61de821344a93129198`  
		Last Modified: Tue, 14 Apr 2026 20:47:58 GMT  
		Size: 2.1 MB (2119261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283858f0ec221f279c07a44e2d869ab849ac8ca6ad1f3e57ab1c05f65bec8d5a`  
		Last Modified: Tue, 14 Apr 2026 20:47:58 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:cf91a61d9983b51ebbd636cfa6695800b103fcfb6883ca6619a5501d0e26cfc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512981696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ac5e88488af3d8d158bd88d8b59ed8a0cf9ea5402433a080445dfb781bbf6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:46:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:09 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 14 Apr 2026 20:46:09 GMT
WORKDIR /usr/share
# Tue, 14 Apr 2026 20:46:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 14 Apr 2026 20:47:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 14 Apr 2026 20:47:01 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 14 Apr 2026 20:47:01 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:47:01 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Apr 2026 20:47:01 GMT
USER 1000
# Tue, 14 Apr 2026 20:47:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Apr 2026 20:47:01 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 14 Apr 2026 20:47:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998adf538112c1dfbec026338c993ce2dfa820db070be63252f76291b50b238`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 5.1 MB (5148131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f773b7cbb6997cefcb9173425890abd7b2ea3dc0942de771577566af84987ae`  
		Last Modified: Tue, 14 Apr 2026 20:47:49 GMT  
		Size: 469.4 MB (469368730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae04de2024250751cc3c0bb3b4c1dbcc76fd16de21f417384e4359a78f4bfd2`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed6aed4ef9715a99393054cb9c9a7b0547806e8dd1aaacac97cee6670c54c1c`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03edbcba8b9d21d295b0af2e5b63d607b2e13d69bce24c962de722bb3a4efb6d`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dff1c1fa2848006d8b93465af711d9b2d1e327d5cab226517c9866f73badf7`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d313624eb08fb5f6d4878d1ad21ec5522a886050da2cd74c752863549756eb4`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bdafb483f41c2593271d7b0b98eae083c02288dff83e389b989714f453f9c`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b29e4066f06b6ca52309596e23664506666f14a4731da97267c704927169f3f`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:2ba35dd3312281e4aa23411c96da2bcf6e126b10e86fd83c2e8e0b2b528470b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82a301b1a0e2437321074ee490e553551e5c7782fa8bdbf4a6ca69c03f4b56d`

```dockerfile
```

-	Layers:
	-	`sha256:e8f12cec8b2a931a2e2cf3c4fae96e5360fff2d44797d4c35d9eb9517e2f4a9d`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 2.1 MB (2119831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6fc7abedf1eaa0e5c560688d5c8a97b5d7d89b00c804b68b87918443b12b032`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
