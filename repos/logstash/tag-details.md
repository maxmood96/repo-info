<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.23`](#logstash71723)
-	[`logstash:8.15.0`](#logstash8150)

## `logstash:7.17.23`

```console
$ docker pull logstash@sha256:79670fd182fca950a59d315bb08ff38097e1b9fe629a803298d2cc174e1274d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.23` - linux; amd64

```console
$ docker pull logstash@sha256:f07a12e0b28343853f3c87992fea55b661228abe1e90c038477dc2105d4e0ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.5 MB (449452541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6561078e83c098c1c8c781c419cfd322d742a3dca5c5a50d3b9b35de8dfeed44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.23-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jul 2024 15:39:57 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
USER 1000
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.23 org.opencontainers.image.version=7.17.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-23T07:27:01+00:00 org.opencontainers.image.created=2024-07-23T07:27:01+00:00
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c40608739ca38f887754aa3a3d57431088a8f4b314854bb3279a0afbe0987`  
		Last Modified: Sat, 17 Aug 2024 02:01:59 GMT  
		Size: 49.3 MB (49307190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c9d3b5a4031cfd35eb6a26864b1d710f117dd8bc0ac3f37077311fe50d03f`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffd22da6a994f051321c1162e9370b27f8479f8bd491cde35252c0a8010ba78`  
		Last Modified: Sat, 17 Aug 2024 02:02:03 GMT  
		Size: 370.7 MB (370726306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86ddf6bcac303aff80bac762750a82476e7c0973801646411df0277c5fe0cfe`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa786e3d3b44ad68e85ae1712b06093fe9423d52f0eb83e5cdc1978345edd`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5be3dc133bfa830ef975bccca75c7e7d05e0069699c04ddebfc8d4147f5c448`  
		Last Modified: Sat, 17 Aug 2024 02:01:59 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a4d3bde18d7273ab7841aae7f30c3bc6b7cad6bc4906a75d29cbf42a5a14ab`  
		Last Modified: Sat, 17 Aug 2024 02:01:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a1868eeb65bfb63f6b03b885c74fb78e9c29fd30c0b8a907bb8e59cfba6d3`  
		Last Modified: Sat, 17 Aug 2024 02:01:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9d85ae3cdf61543a4a5631d1f2104f3edb1bd89a165101f6592bfc9cb1acb6`  
		Last Modified: Sat, 17 Aug 2024 02:02:00 GMT  
		Size: 1.9 MB (1902684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b47767a009e28f7b446e75dee6fa048e7444a18e72dd755f749de822820d70`  
		Last Modified: Sat, 17 Aug 2024 02:02:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.23` - unknown; unknown

```console
$ docker pull logstash@sha256:9fec0f5cc9f3cd7f5227e2834182793a95410a3418f6e639752873e79d95989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba4e1ba6de20bc1e07e8388a6086627e975aecdc6de07def1cdcfabf994ec2`

```dockerfile
```

-	Layers:
	-	`sha256:1e947763b93d8788f95f8b4add745f6ead00300b528224bf1c7876bc72d46e17`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 3.1 MB (3068736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a764c1aacd1b4de590cff9addac9270c73d4f7a59113b7419703b69955b6164`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.23` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:96773eacda894fc062726dc81209c9de5a6b156e6e4498fc9e85b6c89efc8aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433372073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564c084adfe203344fb8b33708da5cc96c303fbcbcfb98637d1145b2fcd621de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.23-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jul 2024 15:39:57 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
USER 1000
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.23 org.opencontainers.image.version=7.17.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-23T07:27:01+00:00 org.opencontainers.image.created=2024-07-23T07:27:01+00:00
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcbd1668d668fec8d18534a5c4eacd100a669b4759e885c8d4b5f5309acdb45`  
		Last Modified: Sat, 17 Aug 2024 03:08:40 GMT  
		Size: 38.0 MB (38027941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a28cb5c20725c0213ea34a4fd6ca873b6520943de0bf6634aad0f6dce2059`  
		Last Modified: Sat, 17 Aug 2024 03:08:38 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acea12ced88a923e6e383974a4750195de9784f6d1be285e04524aa107dc1a9`  
		Last Modified: Sat, 17 Aug 2024 03:08:45 GMT  
		Size: 367.5 MB (367462633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b23a91dfc6d6c8e9c796cc6dc4183ee2427f06701cdba7bdf519e047ede316`  
		Last Modified: Sat, 17 Aug 2024 03:08:38 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f251b44603ea07ee87a24b00ba3d1643269db71d6fdb2fa7cf0ab5db0afbb8a9`  
		Last Modified: Sat, 17 Aug 2024 03:08:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec8a52603a1059066a914ce6b959ce71fa2fbbf44000d8bcf31a4179ea46ea6`  
		Last Modified: Sat, 17 Aug 2024 03:08:39 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0d909595f613a36dd7a1a8b25955296542862c0c2f76e252f786f227c7a66`  
		Last Modified: Sat, 17 Aug 2024 03:08:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5916891130c3f571025ea2386a035cd1f705c374f6a22f77b8c338f945db049e`  
		Last Modified: Sat, 17 Aug 2024 03:08:40 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1fa9bff76cf07b4986a90cab457fc62acff1c410c99f3d157ba063c4897719`  
		Last Modified: Sat, 17 Aug 2024 03:08:42 GMT  
		Size: 1.9 MB (1902682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b1b9496e2dc80ca7becaf53e31756d19236f8765a75971a63493cfa058b33`  
		Last Modified: Sat, 17 Aug 2024 03:08:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.23` - unknown; unknown

```console
$ docker pull logstash@sha256:8d240a52adc04d30b4345e03c3b97337580e26fd500b2f1a2b732f459d38fcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60867c66fb098ded28055ae47cf264a63bc763671aba8c2d743edf1da03c82c0`

```dockerfile
```

-	Layers:
	-	`sha256:16849a3e2e9013dd68c62f65aede0351a641d983e42e8d6d31756c4cfd6f3dd7`  
		Last Modified: Sat, 17 Aug 2024 03:08:39 GMT  
		Size: 3.1 MB (3068971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fd3fcfb8d306b5e4bd7bebacdf193611fc44817a35003b9f5aaa5735128c52`  
		Last Modified: Sat, 17 Aug 2024 03:08:38 GMT  
		Size: 32.2 KB (32197 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.0`

```console
$ docker pull logstash@sha256:b15236b441aabf9418f32022ca5b047c3f0b26acff7e1e2dfd664307c6ca09b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.0` - linux; amd64

```console
$ docker pull logstash@sha256:cb8913653069e7e0c0bdfa9100c9982fd89b0d706100285f554e1865df9bb186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.3 MB (504348813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b658c48349a097ecc5960a1658c7bd7a8c7bae0cc6705abfd467179cff13ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 08 Aug 2024 13:05:51 GMT
ARG RELEASE
# Thu, 08 Aug 2024 13:05:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 08 Aug 2024 13:05:51 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/logstash
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 13:05:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.0 org.opencontainers.image.version=8.15.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-24T10:13:18+00:00 org.opencontainers.image.created=2024-07-24T10:13:18+00:00
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9f96b55dcb272ab685ac6bcabc4a8c39daee425021e4aa2bfbc018cf5ac41`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 49.3 MB (49311985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c9d3b5a4031cfd35eb6a26864b1d710f117dd8bc0ac3f37077311fe50d03f`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6641590284a8bb74b521bc4c497758aa3354b4f2442ea781abad26990c6981`  
		Last Modified: Sat, 17 Aug 2024 02:02:01 GMT  
		Size: 421.9 MB (421925905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cdc127830e8958337ad4398501833633b3aad4a106f3cafafd1106faac0422`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f30dc7b8e7cf57413c88e5cc09bfc023db998ad27a91669224076ffc6b584f8`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04274e815ad155e891cc97bc7b8dacb2153750767cb13cba0ff3d2d16eb6fa2`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee22730ee950e52ffe20f880abb465b66c975c96a0b1ceedf22727124a6e313d`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321b4de3ecfa33fec81ae0dc8584c1fde2bc19a4a2b7c0ea4632787e9aca98fc`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 3.7 MB (3690581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e28732563693ac271be0d600e67234223f9984b46be61f9bc3ee13f8fd37e`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 1.9 MB (1902097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c237b0c1647625eefa629bac6091a85dea9cfaaac6b93eff47d08e07e07355`  
		Last Modified: Sat, 17 Aug 2024 02:01:58 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.0` - unknown; unknown

```console
$ docker pull logstash@sha256:746bb205d45de376952e68a70cd672bdfa4887c939b17a11e0569dfa995973e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f9c68e7d787e9594181eef25a2d97dcc59c0f1e4aa4db760e9081c877c0681`

```dockerfile
```

-	Layers:
	-	`sha256:564d4a44bc3677d8d5fa9073e21e1107173be8dccd8cdffa61835b9597a7081e`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 3.2 MB (3238794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cb7e12cb4e4cb9ae44176fbaca5fcb122d47d1e7b310095cb9f85ea1e82f26`  
		Last Modified: Sat, 17 Aug 2024 02:01:56 GMT  
		Size: 34.3 KB (34317 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f8d597456ffaa1193f8219a93c25b55b4716b21a26404df082f0a62b5ac76fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.6 MB (489594336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2197181730f675e176792e4b304c005181de4f55e0c8e22f1460209e38cc46a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 08 Aug 2024 13:05:51 GMT
ARG RELEASE
# Thu, 08 Aug 2024 13:05:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 08 Aug 2024 13:05:51 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/logstash
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 13:05:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.0 org.opencontainers.image.version=8.15.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-24T10:13:18+00:00 org.opencontainers.image.created=2024-07-24T10:13:18+00:00
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2664964c9665a54df6a105494b1078f790d0014d3fae1269b982310300cecd66`  
		Last Modified: Sat, 17 Aug 2024 03:07:02 GMT  
		Size: 38.0 MB (38036370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1daf002207d63c5b53c5faaaea31dcde78b569ada6176326e42f184e780b49`  
		Last Modified: Sat, 17 Aug 2024 03:07:01 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a4a4577a86498a42fcfe4c193bf420880a4be118b12e0c583e8285f72246f2`  
		Last Modified: Sat, 17 Aug 2024 03:07:09 GMT  
		Size: 420.1 MB (420099163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c877f4242256b0e7ca1e102df8cbac09a6f61b39fa5eea16e4762fd2fb9b10`  
		Last Modified: Sat, 17 Aug 2024 03:07:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c6b6b2a80715a78079ca76ab269771d01a2a4d81d1a9872c8fb58e49707c7`  
		Last Modified: Sat, 17 Aug 2024 03:07:02 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45140419970ff48ffb09e6703a3f94b9affb4aeca74b16f95fbc0a5bb55614a3`  
		Last Modified: Sat, 17 Aug 2024 03:07:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e0e4a2ffc135bd17a3da8b2a207dccda7b9b43ff57c1ab7c9da402ecda1378`  
		Last Modified: Sat, 17 Aug 2024 03:07:03 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314bb056a51cd8e7632e05b8ac88c56dc06eb9cae2b6d23db33afae559ef0afb`  
		Last Modified: Sat, 17 Aug 2024 03:07:04 GMT  
		Size: 3.7 MB (3690577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771e1ccec8d42fe9ded54d6df818751103a31fbbabc6234b68a2719fa0fc2bb`  
		Last Modified: Sat, 17 Aug 2024 03:07:04 GMT  
		Size: 1.8 MB (1787527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea993262c82656d46788cbe888344bdb1a462aed7396ff494fb4dd88d7560acc`  
		Last Modified: Sat, 17 Aug 2024 03:07:04 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.0` - unknown; unknown

```console
$ docker pull logstash@sha256:2dd823c6897006ce72cbada8a56ce9c223257a3acfb54a06f51f8d33a62446f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d8321ff0b61bcae4a0dcd002452e64703c40effaf0f154b199bdd96de8e2c`

```dockerfile
```

-	Layers:
	-	`sha256:f76c3515640174874fa97d5b1e1209b3e11dfad5b61f71d7e58f397d59ef1c9a`  
		Last Modified: Sat, 17 Aug 2024 03:07:02 GMT  
		Size: 3.2 MB (3239029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f67d4878747d8a67d9c7ba0f4342c4c341e05897cde52097af2a7171d3c490f`  
		Last Modified: Sat, 17 Aug 2024 03:07:01 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json
