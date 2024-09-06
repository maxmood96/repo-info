<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.23`](#logstash71723)
-	[`logstash:8.15.1`](#logstash8151)

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

## `logstash:8.15.1`

```console
$ docker pull logstash@sha256:8441647ce0abfc94f1ef93abcf2bfc7be220ce9a485608f84483fc30c7f0a7be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.1` - linux; amd64

```console
$ docker pull logstash@sha256:8f0a7473c31341aab78cac43bb6004192c806cf3799d1d1d46e2c712946a5070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 MB (505074787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43bf9243567ae5192cfba7aa6cec6737c96cd0c3584fa89ed33b23ab804fbb0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 05 Sep 2024 16:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.1 org.opencontainers.image.version=8.15.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-08-27T11:22:51+00:00 org.opencontainers.image.created=2024-08-27T11:22:51+00:00
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d3964864a8a755ba1d20688172476c54b810d6d46deb8d666d36f25a11f49b`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 49.6 MB (49569249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b4af60cc5ba8c40111d54cd8b1b5dd74ba591f8b61b59bf88c4d249ed8311c`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f95e883db8d0019de1cd75cbc2f17905d10ccbff80c9401c4fb6fd109a20fd`  
		Last Modified: Thu, 05 Sep 2024 22:04:03 GMT  
		Size: 421.9 MB (421929826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88c8cb15e0a587bc7e25b2aab041b6e4140c42540df52ca834f15fd9b2ab54`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac626b2c2a6ab81c24dea47da04cca1d42419983c36a3e523d0466f6fb7e2c`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236776d6d73a7693a48a5b501f1cc254ef4cf26544e295d3f701008dd680b80`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d26797fc2c046466f7f52e1927799536e3b332b3486d07c263650e6140d92`  
		Last Modified: Thu, 05 Sep 2024 22:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc49abbfa60dabe26a7f208d350bfbc71d1ad0f1cc598aff44397ffc150e30`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 4.0 MB (3996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e048852c7186b4402ae01a9d8470a142d76af961e3c3e5db9d6610e9871a1c0`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 2.1 MB (2061205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21d9a6cc95d2d4764ac8f7ee2653168942620d5777565e11c2d40c35a51eac`  
		Last Modified: Thu, 05 Sep 2024 22:03:59 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.1` - unknown; unknown

```console
$ docker pull logstash@sha256:26639e0279894f026b57c038ac752f4ee0334a1257db7ebd026cca5a45942717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371aca4113f997fc41faa0da0f9576d59c4bda7af78c6a30115474877f1648b2`

```dockerfile
```

-	Layers:
	-	`sha256:d274f1203f6ab60fd59531f05ca3ababdade3970cea92deb39db6d52de7875a4`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 3.2 MB (3238794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f041eab31b6989a9290386290074a4e52f1d21b16a4994fe1d1c3594878af4`  
		Last Modified: Thu, 05 Sep 2024 22:03:57 GMT  
		Size: 34.3 KB (34316 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3b16149c83377c0785eaaffd90175a04dfb1a9bd51095f69fbd6fa94c9cfda7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490048139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d045529c42f6a6a31260d9859a682821d1381cfd9043651255cd52ea15fb5d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 05 Sep 2024 16:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.1 org.opencontainers.image.version=8.15.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-08-27T11:22:51+00:00 org.opencontainers.image.created=2024-08-27T11:22:51+00:00
# Thu, 05 Sep 2024 16:37:13 GMT
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
	-	`sha256:5f89da44ca73a5a5252f89b19251df709a6ee274a4bee182e4a0c76ced70a1a5`  
		Last Modified: Thu, 05 Sep 2024 22:21:22 GMT  
		Size: 420.1 MB (420101771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a90c423044da8a865688f044fc7f10157aaa6979b7582ce57c6b5c769da6ab`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9843e4fa3be4fa1d5479e4caa3212e5a96ca7535693c7890440802ab94e702d1`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290fbb4bf3a4e70a05928439be48fe05caea232fadf5e4abc4c1d9b7f0e0102`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a58f9daa156317d55bfbcf884a4c9c8df9f491c68b5a9711094189cd4624d`  
		Last Modified: Thu, 05 Sep 2024 22:21:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383dd3c264aec39d030fc547091b48e0c3007b010996f0e5297d84ac84520793`  
		Last Modified: Thu, 05 Sep 2024 22:21:16 GMT  
		Size: 4.0 MB (3996251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb8baf7b7eeb5970af1da49e71e07a32a51064f4449e8beb7aa3edbde57d708`  
		Last Modified: Thu, 05 Sep 2024 22:21:15 GMT  
		Size: 1.9 MB (1933040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7f642fc48eccd14c9f2ac0383b4e39a0b23e52529572d803a665818b36ee11`  
		Last Modified: Thu, 05 Sep 2024 22:21:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.1` - unknown; unknown

```console
$ docker pull logstash@sha256:a1fb3bad9e5682ecd61eacca2d6f3d8140134ce071061a27d155cfb6e12950fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029f42a08374d117f5185efa67dd3ee0ec8c4cd4fd8836c5466d39bcec2c95b0`

```dockerfile
```

-	Layers:
	-	`sha256:164fc588f27d0d578d45a0c24450ae29daf1bbc3ee544a8a15218cc476124b82`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 3.2 MB (3239029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e23e2659c028d4cf21ea949286739823d27b62bd48b384fdc798b2d201b9657`  
		Last Modified: Thu, 05 Sep 2024 22:21:14 GMT  
		Size: 34.6 KB (34581 bytes)  
		MIME: application/vnd.in-toto+json
