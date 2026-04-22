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
$ docker pull logstash@sha256:9ef2b7519e468d7e7c43f56ba508faa5a8751ab073d04a3dd24f46b2f338be1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.8` - linux; amd64

```console
$ docker pull logstash@sha256:85ba56c4aca4e51475529a2fd0fa7021f19b5993e422faa703f36a7eacf3ae5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 MB (502219515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ec5c3a63bbbdd983c38c518e4cad2d8bf7c2bae6c1611dd8b17d6225bef3a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:17:59 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:17:59 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:59 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 18:17:59 GMT
WORKDIR /usr/share
# Wed, 22 Apr 2026 18:18:02 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:18:59 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:19:00 GMT
WORKDIR /usr/share/logstash
# Wed, 22 Apr 2026 18:19:00 GMT
USER 1000
# Wed, 22 Apr 2026 18:19:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 22 Apr 2026 18:19:00 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 22 Apr 2026 18:19:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eecd0b266bfa8651e4f325e976576d71406ac0ac2b2cdc3d9977db647d7e54`  
		Last Modified: Wed, 22 Apr 2026 18:19:40 GMT  
		Size: 5.2 MB (5150399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2415dcd6b135d5077c1d08cd30c3ececb1c3feb9413a026d9116af44b166386`  
		Last Modified: Wed, 22 Apr 2026 18:19:48 GMT  
		Size: 456.8 MB (456779606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6d8bffa5b1add563455c04d0a7dae555ccddd903c1452cf80bb14faf38995`  
		Last Modified: Wed, 22 Apr 2026 18:19:39 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13363fba82e58e998c0aada842ec169c1f2c84047859d881605d6558a2af7c`  
		Last Modified: Wed, 22 Apr 2026 18:19:40 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999bd48a35c41338973edd257452d345ffbf33042c237b6140177938679861be`  
		Last Modified: Wed, 22 Apr 2026 18:19:41 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b576592b1e8280f9a52fcc4607526a556df534564131757667b45446d3433f77`  
		Last Modified: Wed, 22 Apr 2026 18:19:41 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3c8359a02f0e8ca31c806038a022cdf3ec09484ce902bc487ecf6005c24c99`  
		Last Modified: Wed, 22 Apr 2026 18:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a080e7f77f6739411644a9b2b2ea74606ed6de01dee474d8fe95665b6c7de6`  
		Last Modified: Wed, 22 Apr 2026 18:19:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c2f2f4c92af61833bc3101837f2b4265282fb20768db355a560d7bf8e5b87a`  
		Last Modified: Wed, 22 Apr 2026 18:19:42 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:37b200a80d7fe1b7c59c36726e971d7eec9eae03af9c2719934eb216207b6c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca182f84c5be1fd0063aff755a58e94dceb8b9de2bb2ce3d11ca667b30fbfbb`

```dockerfile
```

-	Layers:
	-	`sha256:858c226aa189471af3f90dd98be67cadb134c60806867f47247a1b4c19d3b791`  
		Last Modified: Wed, 22 Apr 2026 18:19:39 GMT  
		Size: 2.1 MB (2139784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acaf83f2ebac67a880de02f39fb05e877ee00fea845ec7e9a649119c3c0eedf8`  
		Last Modified: Wed, 22 Apr 2026 18:19:39 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f59e8f027b97c2a7dfb39ee849bc11a9290be1919f986f1e8bac781b21571feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 MB (498680723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ed7405a58aca5e0c99059cc0d8d588637feef5750a51ccbe5c7565340dc59a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:17:10 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:17:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:10 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 18:17:10 GMT
WORKDIR /usr/share
# Wed, 22 Apr 2026 18:17:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:32 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:17:33 GMT
WORKDIR /usr/share/logstash
# Wed, 22 Apr 2026 18:17:33 GMT
USER 1000
# Wed, 22 Apr 2026 18:17:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 22 Apr 2026 18:17:33 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 22 Apr 2026 18:17:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defc4d499511f429b13eb018fe0efaaf7d0ac3af61b60f6ede759ef454b26fb4`  
		Last Modified: Wed, 22 Apr 2026 18:18:09 GMT  
		Size: 5.1 MB (5146139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecffc5c880a0be204ad660fd32f0938474138299356483504bf6d0ccf2a6192`  
		Last Modified: Wed, 22 Apr 2026 18:18:19 GMT  
		Size: 455.1 MB (455065365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8f99895c819f4f601bf7e699aaec58f9f76c6a3d6cbb12b5fb3ee6fe60c11`  
		Last Modified: Wed, 22 Apr 2026 18:18:09 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83e59d4f4e2965ac9ee59b1651def14d66e5dadca5903fd6467493226478ef0`  
		Last Modified: Wed, 22 Apr 2026 18:18:09 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de7e7489f7e46183ea887c7dac4f8310e5c6ac74885d3e184fe544030fad962`  
		Last Modified: Wed, 22 Apr 2026 18:18:10 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd6671e3147e34f69f655315c44873e4495edd3e87a7aa15d0f4d4084fe0d42`  
		Last Modified: Wed, 22 Apr 2026 18:18:11 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388b8b6ba8470e6bb1c78aa3cb5c099873b34d0588cb16e62545dc6c2121c47d`  
		Last Modified: Wed, 22 Apr 2026 18:18:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ba8035672428ae2dd5cfdf9c1fd5eb415d2c50c591758da333e352243363ec`  
		Last Modified: Wed, 22 Apr 2026 18:18:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b50a4f3c9659d3e04c0e70d05a6739bc5d4bd2e9b9b13e3b590e65134055bbf`  
		Last Modified: Wed, 22 Apr 2026 18:18:12 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:2b699d138b996b5df75572eb6f0dd793582b4cf46703890b45ec5045af7dd1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6561108dd4b7edb6249b936c9d2d72f727f40b21c6bbc1cbb3eff71af6927f`

```dockerfile
```

-	Layers:
	-	`sha256:d6725fbbb6d8de2f5665f4a6e1d363e2cf500313779c902991f5fb8c4cc22c80`  
		Last Modified: Wed, 22 Apr 2026 18:18:09 GMT  
		Size: 2.1 MB (2140354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fed48de335f198551b57d2e8604afaeab992cb00858fc2c49b707887ab980b`  
		Last Modified: Wed, 22 Apr 2026 18:18:09 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.3`

```console
$ docker pull logstash@sha256:64d9cdf0d118a00fa403ec591a3d0472a3802d89d71052764cd3a5b8261b3758
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.3` - linux; amd64

```console
$ docker pull logstash@sha256:a256ab208f8674cc7f05e02a742f3d85bf4ef2fa86bae17a9fe6988c077b337e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516523697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07892ad7c9753750a21797f03519d38a55d75f22211f183338ea3e5c6ec6e89`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:17:59 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:17:59 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:59 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 18:17:59 GMT
WORKDIR /usr/share
# Wed, 22 Apr 2026 18:18:01 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 22 Apr 2026 18:18:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 22 Apr 2026 18:18:22 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:18:22 GMT
WORKDIR /usr/share/logstash
# Wed, 22 Apr 2026 18:18:22 GMT
USER 1000
# Wed, 22 Apr 2026 18:18:22 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 22 Apr 2026 18:18:22 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 22 Apr 2026 18:18:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a452e352dc109b26693f34c7eed64183865934b506e233acc7653525e9146`  
		Last Modified: Wed, 22 Apr 2026 18:18:55 GMT  
		Size: 5.2 MB (5150374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3d918e9556361a4136cb332f44100ba5f2d25780de70a1cd21c634fc5adfca`  
		Last Modified: Wed, 22 Apr 2026 18:19:05 GMT  
		Size: 471.1 MB (471083821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846a6ac95abe85533e72326eeabceb420c74a7e269471f76ada4579faa7875b1`  
		Last Modified: Wed, 22 Apr 2026 18:18:54 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf644c9dbe05f0228ea28739743468bd3e24ef976a564f59fe84b4d8b593153`  
		Last Modified: Wed, 22 Apr 2026 18:18:54 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4295a97e7e8e125404a08e250fb02c3c3e482b582285512b6f5e966f13bbcc2`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e9562b48d0e7f859bbb017b66b3e886f3c729de334a7c7d5a6987e1d279d1b`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce8a869b623184365eb4d02a5e658c04a2203ea5a1f073def0f26d7481f82a6`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfce43b16b1a50353c1a85e05a6b86fb2bfcf31841efd59da1190dcf74ddf52`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a49d88985f38d7fc0b58c07ac20a3affc2a095e1d962f040e1e5762564acf7`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:077a4b6a4f3004c44cbdb5e8864a6e5af94759d5adc77313ecc57f280a58c7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd51b2013bf2c9e3f7b875ab385fba67fa9dec567486950692c2c3abcdc9765`

```dockerfile
```

-	Layers:
	-	`sha256:e2a9866de0d378cd6fe9de55a0594cc92fa659b2774dcf83668f8bba4d7e67e9`  
		Last Modified: Wed, 22 Apr 2026 18:18:55 GMT  
		Size: 2.1 MB (2119261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c35ee9d68ffc1191b5f2112a56ec656ae91da202294231a13d9fb1aa5f8894`  
		Last Modified: Wed, 22 Apr 2026 18:18:54 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bfc752962c0dae1a5e3ce6b05dcae8d9cfcde671d7f121ee7739a84adfbe94e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512983911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd9037bcdb63115160a395579131473680ec3d446584524c51e7e3f2d0e5811`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:17:25 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:17:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:25 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Apr 2026 18:17:25 GMT
WORKDIR /usr/share
# Wed, 22 Apr 2026 18:17:27 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 22 Apr 2026 18:18:19 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:18:20 GMT
WORKDIR /usr/share/logstash
# Wed, 22 Apr 2026 18:18:20 GMT
USER 1000
# Wed, 22 Apr 2026 18:18:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 22 Apr 2026 18:18:20 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 22 Apr 2026 18:18:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb8061b19adb8cedd292553e7d4cd59e5b5f35ea949f438fb1ed55f53aa889`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 5.1 MB (5146116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefbf0b6c3dbf568fc2f3ca752427cfed436b923fcd7d75e110a030198cd5af9`  
		Last Modified: Wed, 22 Apr 2026 18:19:07 GMT  
		Size: 469.4 MB (469368565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e768c1e46ea12b0f79193900f9dfe41e485ba4869279403b1a3708934ef0a31`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef696c48c013efeb0810cfa2bcd97a4e3f43d01ee14de373b41164b677acf3`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea06e073005ba63685d35db4b24c0084c35bdb96742943da3fe2fb15d3aef02d`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08901404e33ef75c5d1d3b0358a8d0aab62191555f1bee272942ef377cc9ea7`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edf3740fd0d058bd5ad760d5f47ec8a90c39d822a4910c0578dd293f1d79f23`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9d1cf971f6595e445579bb857fd4290eea94d13a303495482d9f6f8a7d5350`  
		Last Modified: Wed, 22 Apr 2026 18:18:59 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb5fef14f099a47a065f946dde115c5b2fc108365c3aa263515147e346cca43`  
		Last Modified: Wed, 22 Apr 2026 18:18:59 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:d801165ed59147315f2e0d3a3b84e868f101f2ffd526be5a6c95c387f91cd984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012b477e3840d1c6be68de16fd76537a523f32e2d6267c9eaa8cc229e7dc38c7`

```dockerfile
```

-	Layers:
	-	`sha256:47e93aacf1e3773a1362271adc313ba0da10157c1a9d04ea8e4714d214f790a3`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 2.1 MB (2119831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b2f3c39a4c97d0ccedfe46151e54e6bf6464de2d806ebd0ae5a17151b98eab`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
