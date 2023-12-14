<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.16`](#logstash71716)
-	[`logstash:8.11.2`](#logstash8112)
-	[`logstash:8.11.3`](#logstash8113)

## `logstash:7.17.16`

```console
$ docker pull logstash@sha256:ad9124dd863ed97bfdc54c22b0fddaa87fb53ec65b9530ab8869d581229a6e43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.16` - linux; amd64

```console
$ docker pull logstash@sha256:69fbc64343e6cc76baf8d2cf579ab8462d8f132fa9175effab031e64be53cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.3 MB (449288242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6cc2504e4f2f9424f1cf36508c26dfc34e3308beb1b516b82d88e1c92b9aac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.16-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.16 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 12:49:29 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
USER 1000
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.16 org.opencontainers.image.version=7.17.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:24:52+00:00 org.opencontainers.image.created=2023-12-05T12:24:52+00:00
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9330f58f5dac645b0f096f199df7048c20fd38a5dd1fdb37d4cac1261f837d9`  
		Last Modified: Thu, 14 Dec 2023 18:51:45 GMT  
		Size: 53.1 MB (53065470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e6b519235f387286cd30e4d5d51572bd0e213e02565c99b953ddb6353d7855`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936485e0cbd9a9c966bbb0b89fca4ce32e7d07fa43eb05f11bc9e1b06b333b8b`  
		Last Modified: Thu, 14 Dec 2023 18:51:52 GMT  
		Size: 366.9 MB (366860854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07caffcbccf51a5dea3920e7205c22a0748d7484bb8f12b89e00e8eeb5861607`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2966edb2eee92dca7117f5e669a6ab6b471bf9f2ed17f16067ec5989c2799e15`  
		Last Modified: Thu, 14 Dec 2023 18:51:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ced2c8335feac9f127b24e5897cc87e0c981434655d819cc2f48a7d361aa52c`  
		Last Modified: Thu, 14 Dec 2023 18:51:44 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c1d0056d9f0c247e5a01389007fa2f32d639b62cc7c5ec05f4d653a450136d`  
		Last Modified: Thu, 14 Dec 2023 18:51:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3059364ca2372df55087c82c23ae289febde2bdeedccb2fc8201c0add5e013f`  
		Last Modified: Thu, 14 Dec 2023 18:51:46 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edeffaf0a43b22e1c6264606727ce890cf8033933e8105ccbe495735a811d3a`  
		Last Modified: Thu, 14 Dec 2023 18:51:47 GMT  
		Size: 1.8 MB (1844764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a883f36edc2f10646e5d4ce0f3752800da3b24a90f93cffad050602200693`  
		Last Modified: Thu, 14 Dec 2023 18:51:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.16` - unknown; unknown

```console
$ docker pull logstash@sha256:b77c42229e2b628119eb4daa51744ce4fa5a9b050dd5f3518a5618abaff0891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3e912ca9d44df1a6b324083b557cb197cdaa76dfbb7b92f95d205b76042691`

```dockerfile
```

-	Layers:
	-	`sha256:a42c2bd24b7fd24a46a3f1b173c8efdd84af846dcba25c5d347199052daf080f`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 2.7 MB (2673367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eea64c0727450ad4b0e8111010a53568d5ca24dcfe250f81edbc4170d38b6c`  
		Last Modified: Thu, 14 Dec 2023 18:51:42 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.16` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3c7893c93002e50310c5acf7e4b2983079b891c7e4d3adf246742b8641c6062f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.9 MB (433917486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea72410b1c8cf671b08f81e0d0734da54d7c0cfed50c503394cf8c2934d130b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.16-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.16 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 12:49:29 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
USER 1000
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.16 org.opencontainers.image.version=7.17.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:24:52+00:00 org.opencontainers.image.created=2023-12-05T12:24:52+00:00
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483023149b3e363410a4efa610382d9c1895c71ab225b1e3aeb1f58abbe3d12d`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 42.5 MB (42496582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb2de4e64897810ce7b16621b7ce7c9e83e9fcc5599d663460bc239058b036`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2086a6382fdeb8710207fdb04b13c7c09acbedaaf88f3df1879a95f5c3cea565`  
		Last Modified: Thu, 14 Dec 2023 20:12:37 GMT  
		Size: 363.6 MB (363596021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7fc2a73197dafd060a0b3b7619c1f3e711b02322609ed18fff7afaa062d3d3`  
		Last Modified: Thu, 14 Dec 2023 20:12:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633f517c2366bef438309b7389ad8d821f351049f5f55d3e1f8e8ce8f77491a`  
		Last Modified: Thu, 14 Dec 2023 20:12:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf23d8b2254b754b8574ac5d934b117f2589eed8783289eaecfe08cc42bc111a`  
		Last Modified: Thu, 14 Dec 2023 20:12:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d6774bb58633b73bee0321f6a6763109c8e0b960231ed7da1143019f0bb3bb`  
		Last Modified: Thu, 14 Dec 2023 20:12:31 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090904a81160ab5c863d9db5ed52a4c2bbc9446b8bf349ba49aedd752231876`  
		Last Modified: Thu, 14 Dec 2023 20:12:31 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4ed7989161619758c4ac6a9b88ac4c980ee81942740394c0b0828ceeb80037`  
		Last Modified: Thu, 14 Dec 2023 20:12:32 GMT  
		Size: 1.8 MB (1844766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4622af1cdcd1ad1fa574aff2ce1ae2f642d84f63c9968b911e0735acb0d75352`  
		Last Modified: Thu, 14 Dec 2023 20:12:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.16` - unknown; unknown

```console
$ docker pull logstash@sha256:62109d774139f1d5fd87be017c8f501c4055353d8f65d7a5e54616f90d0d623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa3597438d4503bb6be7f1701de35cb320849525824ab71cedfe21968d46ab`

```dockerfile
```

-	Layers:
	-	`sha256:f42858484f101c5e24ae864a4c3c494ab17307b126300f4e0acdf26a4754aab9`  
		Last Modified: Thu, 14 Dec 2023 20:12:30 GMT  
		Size: 2.7 MB (2673699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f40c7e65737392e0cb3c519ca403bfc1b9332258c78a6794546dfefc5713825`  
		Last Modified: Thu, 14 Dec 2023 20:12:30 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.11.2`

```console
$ docker pull logstash@sha256:c6ec69fe508c504705917a05d1161e60be80ef03a513456773890352e746ba75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.11.2` - linux; amd64

```console
$ docker pull logstash@sha256:5a663035813e6845c667c6b0dbf012c08da81bef34dcde412fc041c98dc12bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.0 MB (432954582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319b9c65cb7aef8d556c3c9005c5f17901010f017ddc920434f9ed298808e8db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/logstash
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 07 Dec 2023 12:34:16 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.2 org.opencontainers.image.version=8.11.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:30:34+00:00 org.opencontainers.image.created=2023-12-05T12:30:34+00:00
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de80ee9ca535c83dc9087ffa438d19eeb20fade1125b388e2ca27b741788f676`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 53.1 MB (53065602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c914206695154f453ccb80a282ad99c0af643809acee3f7ac79ad1c1f0d59f84`  
		Last Modified: Thu, 14 Dec 2023 18:51:33 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549200b4fc85642b5a69a0c558cb288b1af2f4e2abe28827b78bee3d9bb75ecc`  
		Last Modified: Thu, 14 Dec 2023 18:51:39 GMT  
		Size: 350.5 MB (350524340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24519b0012084da1c2d4cf6697cab9d6f9048eb8c8d48f3f99238aba5ef1e4f`  
		Last Modified: Thu, 14 Dec 2023 18:51:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220150149a6395077b2c9c9fbb9e0e1e0a8330cfdd9902bbb72c33239075cf62`  
		Last Modified: Thu, 14 Dec 2023 18:51:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c736aa929062d51f8292847aca302e9a3b0b2bf8956ebdd54aac6e013d5c900`  
		Last Modified: Thu, 14 Dec 2023 18:51:34 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb83d4f71ec0bf5a43c598e358c54fa40410e1c190070b12531fdc95e9edab7`  
		Last Modified: Thu, 14 Dec 2023 18:51:35 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dac7a7e4b40dc62f71b36fabed5e2f298b27312052a2f647f142a254ac5f05`  
		Last Modified: Thu, 14 Dec 2023 18:51:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d390f2853bfd1cf5d905b9b4f026ee169c7440e96c67affcd33d4c471cd471`  
		Last Modified: Thu, 14 Dec 2023 18:51:36 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aedd76dfe35f1d71fea29d1c2b02f0f26da83cabd2013240065bab573c661b`  
		Last Modified: Thu, 14 Dec 2023 18:51:36 GMT  
		Size: 1.8 MB (1844956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded38cde053510ccb978202d59f8d5a9918b30b4fb3832660e73d254e68a66db`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.2` - unknown; unknown

```console
$ docker pull logstash@sha256:af4c90fdb21b501291fa8e4efb29971acfdd25d89a07f18e8e81928033dc1ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaca1a763cbb6d7ee2039cbf04a05ebaf194ddd4fbcac8427a2912590ea0715b`

```dockerfile
```

-	Layers:
	-	`sha256:e453dbb5e7f85ba9a1988c77c802c2599125e63d03625847105ed4bd8b86b3eb`  
		Last Modified: Thu, 14 Dec 2023 18:51:33 GMT  
		Size: 2.8 MB (2799896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6db7cc203ee9d677c1d26894be752effd759ed5aff0b562a1d8128fb5b2fa8`  
		Last Modified: Thu, 14 Dec 2023 18:51:33 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.11.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:034f9cfffcd468f72deea927ee0d7865c1fe078a03b11dfdf7593b0195d9146b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419663568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aebc00cd8b407cb256130d221d04aadca01a468f6c1e1dcb8524a25064e101`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/logstash
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 07 Dec 2023 12:34:16 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
USER 1000
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.2 org.opencontainers.image.version=8.11.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:30:34+00:00 org.opencontainers.image.created=2023-12-05T12:30:34+00:00
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483023149b3e363410a4efa610382d9c1895c71ab225b1e3aeb1f58abbe3d12d`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 42.5 MB (42496582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb2de4e64897810ce7b16621b7ce7c9e83e9fcc5599d663460bc239058b036`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2940e9675cc166deaabc968796424a5dddc67a63631e4e3108fe406031d838`  
		Last Modified: Thu, 14 Dec 2023 20:11:27 GMT  
		Size: 349.3 MB (349339413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dce82e32df43c373acc6597452e7b088511fd3e25a9f576abf19876a58d384`  
		Last Modified: Thu, 14 Dec 2023 20:11:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa5993b12bec24e35a11dce53ac03c0983a65c9cc6a83763e09f2cf76ecb62`  
		Last Modified: Thu, 14 Dec 2023 20:11:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae14061e17100ceaa71115597eb771c2b1f597a7ac6c653de8df53a08781ff`  
		Last Modified: Thu, 14 Dec 2023 20:11:18 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c37af170d2b17d6ec0bb26bcacc883ab05a30fe6a053099b8415c1ae14901a`  
		Last Modified: Thu, 14 Dec 2023 20:11:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92b81871162e7472a406b2eee18aed95f0918488c0e3428b1fe26df0851807e`  
		Last Modified: Thu, 14 Dec 2023 20:11:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d39a7f43e1030cf62ff58b257bc2a2ca0d85f4142f6c856f34483997ab1d9`  
		Last Modified: Thu, 14 Dec 2023 20:11:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f84adbe17068ac59d3977fe362d037b24073c27c16fa405df657d2bbd2ead5b`  
		Last Modified: Thu, 14 Dec 2023 20:11:20 GMT  
		Size: 1.8 MB (1844955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3280d62a08c5c2e9f03f8f3e431e0e3f3834d7d77ad942900a54bfd0e66c39`  
		Last Modified: Thu, 14 Dec 2023 20:11:20 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.2` - unknown; unknown

```console
$ docker pull logstash@sha256:a2d90645fb905894f1173dcfbce64633969affe9d7e36786b7bed80b7656dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec08b445ebbd13688f04f291a71baa745807fdd748c37b50166f0fbc1a99a59`

```dockerfile
```

-	Layers:
	-	`sha256:9f306e3d02da7db4163e267e5f010fb18da4d70531c7c084dc5b3a93bf0b9089`  
		Last Modified: Thu, 14 Dec 2023 20:11:19 GMT  
		Size: 2.8 MB (2800229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcba072ec261f297154b9e8155222daaa79aa2fcb2a2158816130b480d55f43b`  
		Last Modified: Thu, 14 Dec 2023 20:11:18 GMT  
		Size: 34.5 KB (34540 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.11.3`

```console
$ docker pull logstash@sha256:1e661ef08efaf1db32430cad78e44e1aef9153e3c76665c623dc44b023a88ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.11.3` - linux; amd64

```console
$ docker pull logstash@sha256:5e3d528d4c13897736be82b787648d48db06c106ec92cc488f3f2caf09f4c965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.3 MB (435345124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18340df8320b71f9d1b45cd223de46395e88375279928a05c5d879941d7c057`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.3-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.3 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 13:07:20 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.3 org.opencontainers.image.version=8.11.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-07T19:18:05+00:00 org.opencontainers.image.created=2023-12-07T19:18:05+00:00
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558880d0e97580f1185af79a7af5f115575e8af4c3ffeb0f1db4981045102b06`  
		Last Modified: Thu, 14 Dec 2023 18:51:38 GMT  
		Size: 53.1 MB (53065464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c65a89dc307e21d920b7b87c316fa32ef0b7e491012ccb0cf44b1281daa69`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54927fc057e571cc30c837179d9387d6c5f97b4b044f484152fad364f6843581`  
		Last Modified: Thu, 14 Dec 2023 18:51:43 GMT  
		Size: 352.9 MB (352915033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7626475c193ebee7a865ec1e65610332626faab6b3b70f49f510408b74333`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5a412d2ae6669bcf18aac45750f77e0f9db3cfba691b035d4e7939f37aa573`  
		Last Modified: Thu, 14 Dec 2023 18:51:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f28f52af53cee1849d362388e678dc05f87d0e6eafb5f25820717bc7a7a2a8`  
		Last Modified: Thu, 14 Dec 2023 18:51:38 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d4c17226e47970ad55a0c9c671862a4c38908570e2c9299b973cbb2e6f609`  
		Last Modified: Thu, 14 Dec 2023 18:51:38 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802cbc67bb0d730596ac4537b766821433c4b48daae4ba3a20a9981a1f8f08d`  
		Last Modified: Thu, 14 Dec 2023 18:51:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd84a33b31ca62216a6429bbe01c51c49c834c2a43e685efd2a30535f11a229`  
		Last Modified: Thu, 14 Dec 2023 18:51:39 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b078ec0a3b1f9790a797363c47454f5117596f5eeb51f0e7142c367bc0aef`  
		Last Modified: Thu, 14 Dec 2023 18:51:40 GMT  
		Size: 1.8 MB (1844950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774baa5abf434467521990cb3502f3059546049dfac4dd0e101cb2a7f6c49cfa`  
		Last Modified: Thu, 14 Dec 2023 18:51:39 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.3` - unknown; unknown

```console
$ docker pull logstash@sha256:83098a34c28f000a908a7b420919dca2f48c4cb5a9394a0fc3c9753b8c91dd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2831339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f963214696c290bd73a9662568b9d091ce45a1f03a7e14d10fa0cdfa491fd1ee`

```dockerfile
```

-	Layers:
	-	`sha256:8092bad5dcf4ad47d9eff23cde758c0dda525d327dbf4ad40df3b0660769548c`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 2.8 MB (2796640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36a322121de94369d0bf171ae1395bb260dc03393e65d7db225cad72f2aa4e4`  
		Last Modified: Thu, 14 Dec 2023 18:51:37 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.11.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d7007e6fe7cd6b973feb7bb4fd5cbe3281a1a44941f02ac1367a738926ee3beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.1 MB (422053703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fba0f63519f9b5af1a5e959584029274e5c857788dfb5cd2f9329f6ff097d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.3-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.3 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 13:07:20 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
USER 1000
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.3 org.opencontainers.image.version=8.11.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-07T19:18:05+00:00 org.opencontainers.image.created=2023-12-07T19:18:05+00:00
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483023149b3e363410a4efa610382d9c1895c71ab225b1e3aeb1f58abbe3d12d`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 42.5 MB (42496582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb2de4e64897810ce7b16621b7ce7c9e83e9fcc5599d663460bc239058b036`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229c8f20624824f07558822e35ce497a57ee6a8cd8848c58ddd3948670149ec2`  
		Last Modified: Thu, 14 Dec 2023 19:59:12 GMT  
		Size: 351.7 MB (351729537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9246513b637a4ecd7f593d289f8bee5d6275a8dd44c9f22ae8474f40810524`  
		Last Modified: Thu, 14 Dec 2023 19:59:04 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60741e70fd2a3e31df5a35b95269fcfa540e9d81686e2b385c5d5aa19284ba0b`  
		Last Modified: Thu, 14 Dec 2023 19:59:04 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2437fec7dea5b5fcf0edaa736394f54c75a4183fbbbe1c5dc4e8e8b91e414`  
		Last Modified: Thu, 14 Dec 2023 19:59:04 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d889c32ddbf6bf4dfe9905d9bf016a5423a25697b80fbcdf86e6b67938820ed`  
		Last Modified: Thu, 14 Dec 2023 19:59:05 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f825a5ce7589c5a3b5cbe2a7d265323c7734cd4edaa9a453c8b99af54ab27b2d`  
		Last Modified: Thu, 14 Dec 2023 19:59:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2a2507bcbbb6c588dafb91a16eb9df7bc2f507569d6b9b64e5139ab256b03f`  
		Last Modified: Thu, 14 Dec 2023 19:59:05 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0478def58651d86055a555971c4e72b55991963108d4397cf5727399e11d3c3`  
		Last Modified: Thu, 14 Dec 2023 19:59:07 GMT  
		Size: 1.8 MB (1844953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9e29c8c4e7d948b84d2510f02f67d650b7f34d200b9894232096529077262`  
		Last Modified: Thu, 14 Dec 2023 19:59:07 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.3` - unknown; unknown

```console
$ docker pull logstash@sha256:47382f920604306a8a633a4eed9f28507f23869073f5754bcf865f90cda86d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2831515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148fd7dd8c445d51d30f037a55c7a20d16050369f578362e7f1354e3f1513cea`

```dockerfile
```

-	Layers:
	-	`sha256:82c5fbd474b522bbca5a1190da400c8aed18b87a7dba43d91f38fe2844eceee9`  
		Last Modified: Thu, 14 Dec 2023 19:59:04 GMT  
		Size: 2.8 MB (2796973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3640b5120cc84a2988445504b6e70db1668dfcdae189044a76efde75423b2be3`  
		Last Modified: Thu, 14 Dec 2023 19:59:04 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json
