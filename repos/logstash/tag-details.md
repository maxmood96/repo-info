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
$ docker pull logstash@sha256:77013bf8dc01b594ca6e09f94f1ac1010fe31d1febec27773a3788ac938f8f48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.8` - linux; amd64

```console
$ docker pull logstash@sha256:5935ec2677adb271739cd5ab05fbc89c4728db6e00b6c3579f543c70d455bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 MB (502209106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92004aff19199b385ce206f4e32a64d3238a6ce7a0f3edb04acbc8bf15f592`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:07:03 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:07:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:07:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 20 Apr 2026 23:07:03 GMT
WORKDIR /usr/share
# Mon, 20 Apr 2026 23:07:06 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:07:37 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 20 Apr 2026 23:07:37 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 20 Apr 2026 23:07:37 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 20 Apr 2026 23:07:37 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 20 Apr 2026 23:07:38 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 20 Apr 2026 23:07:38 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 20 Apr 2026 23:07:38 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 20 Apr 2026 23:07:38 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:07:38 GMT
WORKDIR /usr/share/logstash
# Mon, 20 Apr 2026 23:07:38 GMT
USER 1000
# Mon, 20 Apr 2026 23:07:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 20 Apr 2026 23:07:38 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 20 Apr 2026 23:07:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2989b53007867b1f05c3a5145c7977676234a06c471c04b28b83889e3671c8c6`  
		Last Modified: Mon, 20 Apr 2026 23:08:16 GMT  
		Size: 5.1 MB (5148506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97464fe26f785c2efb11f04d9775ad89fb225c8009b2b1b9064dd276b682d9`  
		Last Modified: Mon, 20 Apr 2026 23:08:26 GMT  
		Size: 456.8 MB (456779570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679781f65a16db35a4e8279c0354e378eb1b4a59f3754373dadffcacc106f437`  
		Last Modified: Mon, 20 Apr 2026 23:08:16 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b89aedac471cccf811cee89d08305aceebb4513aebc4c73acb90cf2157525d`  
		Last Modified: Mon, 20 Apr 2026 23:08:16 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158c7b2cee46e0455c99dd76a9d26fc653c2d2a6aa63a57031a9f41c39765d2f`  
		Last Modified: Mon, 20 Apr 2026 23:08:17 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85290cc4d3822fb020b425f74f387696f85699720c512ba7c16b88e0070902c`  
		Last Modified: Mon, 20 Apr 2026 23:08:17 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4e8261820088846ea4bec6cf6146d31da8ec0cb691c76b18a40a8312f05c56`  
		Last Modified: Mon, 20 Apr 2026 23:08:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea95b0f766f69e6290c88b2125cfe90298a56278004a5995978860bbbae224c`  
		Last Modified: Mon, 20 Apr 2026 23:08:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7b6d4e188a74c3fd1fd88985c7bb8ef7baafc904da5f8bc6b50488f4a6bf3`  
		Last Modified: Mon, 20 Apr 2026 23:08:19 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:aac9203390e4edf683e814ed78331466f30b00e3539d087575a9ab5a475bfaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd6414564a8a866a0da6d8204a8aae1775b5bce3a2efb724cf3fa3764202341`

```dockerfile
```

-	Layers:
	-	`sha256:39b0f84f8d45d8d5fd259a661ebbbc46fd747cb02342d69e9a866b81928bfa1e`  
		Last Modified: Mon, 20 Apr 2026 23:08:16 GMT  
		Size: 2.1 MB (2139784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3711b422ce77494ffe549f80add2ea2f7d7b60c919a1e7fa36d2e0e2803ccc9c`  
		Last Modified: Mon, 20 Apr 2026 23:08:16 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e07c06001ac197fb4a327c197d01b15307b176253e633d5f90c88ec14d3f7a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 MB (498678544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6ee20708f7ae05d813c3ffc10757d0f932dff9d85451f9efbbd22943d45809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:04:51 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:04:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:51 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 20 Apr 2026 23:04:51 GMT
WORKDIR /usr/share
# Mon, 20 Apr 2026 23:04:53 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:05:42 GMT
WORKDIR /usr/share/logstash
# Mon, 20 Apr 2026 23:05:42 GMT
USER 1000
# Mon, 20 Apr 2026 23:05:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 20 Apr 2026 23:05:42 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 20 Apr 2026 23:05:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3283c67307db46f817786dbade1f5c0122df32db0abed9c543dcf97e851e1831`  
		Last Modified: Mon, 20 Apr 2026 23:06:19 GMT  
		Size: 5.1 MB (5148392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517a64b6ee7bd03f27b79d6d0947dbd04b369ede4e017258000147cc5999214`  
		Last Modified: Mon, 20 Apr 2026 23:06:28 GMT  
		Size: 455.1 MB (455065292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb72f4129714e1675dfa640d94d4ca94cab1b9e70e7be0cccdec6e12b399771`  
		Last Modified: Mon, 20 Apr 2026 23:06:19 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690c47c1b544531b0f1adaee0af9d509d2fcbf8b75b144bdf45a321dd7bcb616`  
		Last Modified: Mon, 20 Apr 2026 23:06:19 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d641128f675b810d7a4e1fc262786c6ff23121d21c454726e69a7d69f86f8e`  
		Last Modified: Mon, 20 Apr 2026 23:06:20 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c281cb690222d684d5ab0392010c5d1171ff29f098e07cbc74268be0a0830884`  
		Last Modified: Mon, 20 Apr 2026 23:06:20 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb300dda655096d24fc4659ccfcb7d80674777d1e5f74b5254ae8011315e746`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d19fb181d9ba69045e0ece8a845a37944efb51b708ab7d6be3426e74364185`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9de0878e74f9db635862747179f0ef787d5a958d13340a26f4dea7696d4b20`  
		Last Modified: Mon, 20 Apr 2026 23:06:22 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:785537e4e85897fe3b7d0c12dc6bf32e883888f3e4cb55beb1ee4cd843b8dcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c24d319f715563f62bd4058771f379239f122e4307a7fd6b851b07b5f6b52`

```dockerfile
```

-	Layers:
	-	`sha256:6747fb2b17e2673d1175012406812f6fdf2e7e9da2d8cd3c49089a9dfb40ef39`  
		Last Modified: Mon, 20 Apr 2026 23:06:19 GMT  
		Size: 2.1 MB (2140354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42e22a77b43eada1196533593d75dce5eff0e493c1885b72dbe7ac14c7b9382`  
		Last Modified: Mon, 20 Apr 2026 23:06:19 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.3`

```console
$ docker pull logstash@sha256:e9434896c4175e1b5bced1df0dda224ffd0cad0ecd9353a6b8d8b2ade64014f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.3` - linux; amd64

```console
$ docker pull logstash@sha256:7ceaa0938c38806056d91b30cc077df2ed346caf4f1179673d25a766094516f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516513908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9873d96be76214d972977f88a659f5892ec826f1dcf049f425f7309ae605173`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:07:06 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:07:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:07:06 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 20 Apr 2026 23:07:06 GMT
WORKDIR /usr/share
# Mon, 20 Apr 2026 23:07:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:08:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 20 Apr 2026 23:08:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:08:01 GMT
WORKDIR /usr/share/logstash
# Mon, 20 Apr 2026 23:08:01 GMT
USER 1000
# Mon, 20 Apr 2026 23:08:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 20 Apr 2026 23:08:01 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 20 Apr 2026 23:08:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8283a98c06358deda86193b793a51b959640c155b8c1a1243c94ddbe426dc0c7`  
		Last Modified: Mon, 20 Apr 2026 23:08:37 GMT  
		Size: 5.1 MB (5148457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9e1a09e5ddd404e6361da6539f7671adf95b1ac936ebc3933d683cf549fb3c`  
		Last Modified: Mon, 20 Apr 2026 23:08:46 GMT  
		Size: 471.1 MB (471084411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573ca84a641d178e86273251ed1be02d0b09332c0c7f8ab0abadba0926fdbe3`  
		Last Modified: Mon, 20 Apr 2026 23:08:37 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b06fc625b229164786bfe67f7d39cca896e7ad8c2ffcb0936ee8493f5fdffba`  
		Last Modified: Mon, 20 Apr 2026 23:08:37 GMT  
		Size: 255.2 KB (255190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad83a3838cebc02f38c3266f8f3fb47dfe933a4fbbf00935a4948a5cda63cc5`  
		Last Modified: Mon, 20 Apr 2026 23:08:38 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda0ae633b12d93bec64c73232e7a76ed00886a05399db7b9c82f2a68145400f`  
		Last Modified: Mon, 20 Apr 2026 23:08:38 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1532f63ea9c269cfdcc1f9f693fd80cdcddf649839893279d7ceed33b9eabbd`  
		Last Modified: Mon, 20 Apr 2026 23:08:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f766ad2f8673bf59651d875860ab0adb45b7265c109e4c29f4f0342a6f36e3`  
		Last Modified: Mon, 20 Apr 2026 23:08:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e2f98e7143c1245007d606bdca6fc9727bf33cae1b7760cdaba047e3dfdb82`  
		Last Modified: Mon, 20 Apr 2026 23:08:40 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:0c8321e246458f7792da8c753ac039ba011cb808fda9189dc94159aa525bea60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963e9b62e73d6e101d46040db84ed6fcc49569d58a21bfec0d1619bd3bfea27a`

```dockerfile
```

-	Layers:
	-	`sha256:711d0e35042e62021dba5a2285aff6ede83d86a4ec9c8f7a9086d4b68f4c24d8`  
		Last Modified: Mon, 20 Apr 2026 23:08:37 GMT  
		Size: 2.1 MB (2119261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b7b3d2a52f47f283f7e34b6a8a39baf054b4b1b94652b1b30317605a78244f`  
		Last Modified: Mon, 20 Apr 2026 23:08:37 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:34307fadda8053ce305704fcb23938440a23985515d2849583bfd9813a52ec21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512981828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3af150f12ed6e677d18c4a1e303f11beb4053f52deccac0cc1e4e4493f852e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:04:53 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:04:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:53 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 20 Apr 2026 23:04:53 GMT
WORKDIR /usr/share
# Mon, 20 Apr 2026 23:04:55 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:05:45 GMT
WORKDIR /usr/share/logstash
# Mon, 20 Apr 2026 23:05:45 GMT
USER 1000
# Mon, 20 Apr 2026 23:05:45 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 20 Apr 2026 23:05:45 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 20 Apr 2026 23:05:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dea6797e90ee3fe02f10a24eb64bc806094b9deddc6f7936cd0765c04748220`  
		Last Modified: Mon, 20 Apr 2026 23:06:23 GMT  
		Size: 5.1 MB (5148367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcecc568ed501c27ea3256acab160d39ebfb92837bb65a1af62fd36ab60cb08`  
		Last Modified: Mon, 20 Apr 2026 23:06:33 GMT  
		Size: 469.4 MB (469368616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74363fd1a93f040f3808fc9f344fc5db4bb7408481215da1d28da88dd13776e1`  
		Last Modified: Mon, 20 Apr 2026 23:06:23 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757674429d4f2bbd2eb25c5825767b1afd1835d8058022aae2608777c7a5b8f7`  
		Last Modified: Mon, 20 Apr 2026 23:06:23 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d8062ba78c1bb997e76306c40f5019e7569246d703b7a28d414945fa8300b`  
		Last Modified: Mon, 20 Apr 2026 23:06:24 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3a83bc8afd51435dbe7aec8db6d1110fb2c86892e1995187d172f0dda8bff4`  
		Last Modified: Mon, 20 Apr 2026 23:06:24 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f5f151ad4c6fa27ef8e6976036b862e66e962bac991f179ab4505e3785f35`  
		Last Modified: Mon, 20 Apr 2026 23:06:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d9c10235cc0c36ee1b802cbadeca79bd361263e1f8e62e89e58ffc55979b9`  
		Last Modified: Mon, 20 Apr 2026 23:06:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e2f5bc326ac81eb47e81105c2cef0d2012705263e064f7dadb8a2c12a39dcf`  
		Last Modified: Mon, 20 Apr 2026 23:06:25 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:6eb93da5f7169089d0ca8eec3d1c4dfd3b7ef2a56e97ccd8f942e939ae8ebc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd45de386e9db317ad583fc8d715b2ae9b519a53a7f9dfb429bae10bec7b0377`

```dockerfile
```

-	Layers:
	-	`sha256:0a3e510c83ce1582d2788642cadd3658f7328a74fccbf74a52be70fd34317c7c`  
		Last Modified: Mon, 20 Apr 2026 23:06:23 GMT  
		Size: 2.1 MB (2119831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cd04524e9bc186c9322bd64d208ec8cd6a4f98c288289ea7100dea24b6fe89`  
		Last Modified: Mon, 20 Apr 2026 23:06:22 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
