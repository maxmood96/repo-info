<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.7`](#logstash8187)
-	[`logstash:8.19.3`](#logstash8193)
-	[`logstash:9.0.7`](#logstash907)
-	[`logstash:9.1.3`](#logstash913)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:af1921a96e6b08ac40bab4c796cdfe42f7a4f0bbc4d9b25be639d6e76c31c11f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:905a165f6c87ba168364f6aafbdafce3b510c4487539786a08a772b0f7b00257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.0 MB (523979498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925a9d44457f4d8788f77592a32c132e6c506792eac38affea6aa45e4dd3d35e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579bcce4de643d530f781684978c4a68dac722b6a60828d036a4b9ce477857b8`  
		Last Modified: Mon, 15 Sep 2025 22:21:01 GMT  
		Size: 47.4 MB (47403277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba2c0a6caed177e2ec76fd814200dcecbc8a32574d1dbd848b5fd30d1c4f598`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8fd3abb625fa37009f7009ee6da7d321ec1c66368c4d16e205796f5f0ceaff`  
		Last Modified: Tue, 16 Sep 2025 02:29:27 GMT  
		Size: 440.7 MB (440696591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f415177e3d6977934337520b5f80338e5dc33fb448e32effba80538b714072`  
		Last Modified: Mon, 15 Sep 2025 22:20:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5d7e5e76f837474ac746c18cb575c620394f7bac30f385e5ff5b6d41642d5`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ad7b31d7c9d3ee063a98308a85ca92747f513417d7fdf50894e19c105bc6e9`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfcdc4c411a57cfb109aa039a7b22d2ae15c40aacffcfe6e6707c0000b9a8d`  
		Last Modified: Mon, 15 Sep 2025 22:20:56 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62d905567d916c8d1476c32c55261a638e8ed9e7f1e2fb36be8fae4865f4be7`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 4.1 MB (4056197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2860d77b3e4d5cf0142f2a6c713fb19bc5055d1e7943cf99b7c8cb14744ec086`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 2.1 MB (2094090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a25506f627bfd5936cc6e97e041245addf0ffaf72f8732170b173340f0f147`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:41afefff9e23d763515f0f530e56492bf39f9999dd86ef565e591b9493f5defb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0412088455f3be53298b01ad6c8ebc91ac946f3044babd3b6efa754c0af81a42`

```dockerfile
```

-	Layers:
	-	`sha256:e67b9a77cf2b48528219c055e8e0b9e02690d06bbc819c41c46102f9e7acd88d`  
		Last Modified: Tue, 16 Sep 2025 00:53:22 GMT  
		Size: 3.7 MB (3657090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0524551cff5670fa7b45aa6b49bc94f32787f863e6314a2315fe5709f2751e50`  
		Last Modified: Tue, 16 Sep 2025 00:53:23 GMT  
		Size: 34.7 KB (34664 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e0781cd6933364c9570b8384a1672c1071fcdb1af825dcf0453674da5d026490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.6 MB (522568245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79cb83a79df1855c3329d460a47a565b457de959eb8d4064bae17937faa49a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 12 Aug 2025 08:18:47 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc01600197852e39a8bb17591f2f36f4cab030b0d794af9ff4801ea719f982`  
		Last Modified: Mon, 15 Sep 2025 22:20:38 GMT  
		Size: 48.7 MB (48701611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae3c30d51737eeab8ef75e00d3f6fb1a8680fb954b7b88bbe3132357e79ca49`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcce7ee9a510c171e936db806242584c36f8e9d00ae7c14386299df9d87ea42`  
		Last Modified: Tue, 16 Sep 2025 00:54:34 GMT  
		Size: 439.0 MB (438981597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fab3060222aa631a8bccd344ab490008f2f36150686b6f37992f45b03b5283`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d570b227c41960baa24be8d12a0f73adfb8823a4dda2c9f6d988c23bb508f159`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aff25dbbb49b1b7fe6cd6b5b4e96e2b699102bfbe48b5286762f5e0c3d92b0d`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3fb3458e53d1f53a5e2aeb41d6dd3c9555e57ef896f3a1719361db6150f807`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad60a56f000b01043f2c69fc45f5def62c9429471b26f72a04870ab277d527bc`  
		Last Modified: Mon, 15 Sep 2025 22:20:36 GMT  
		Size: 4.1 MB (4056215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944ada5b0d12e0120762c64231dc3fdfe3eb0748b77ee48f58437cfc546cc9eb`  
		Last Modified: Mon, 15 Sep 2025 22:20:36 GMT  
		Size: 2.0 MB (1961620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31333ca0ca47031332554217346521a6dd0cb84be2c913d67c3369f51ef7b07`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:a328b53e38ce1dba860d97b6ce1576fcdd0c72a66a44f6d7b41f917eff64c95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f7d5489b2152295bc2eae6484e948f4080ee1fe4435e49fb287446bb3236c5`

```dockerfile
```

-	Layers:
	-	`sha256:701e69e2c008b603cef5ad91c1df79ee0cd67fdb2c4c7919db05e438d9204a86`  
		Last Modified: Tue, 16 Sep 2025 00:53:28 GMT  
		Size: 3.7 MB (3657515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5092a52308576b3e9ff0d5b17e5bbbfb70b817092771ee8632f2bf8544e9e8`  
		Last Modified: Tue, 16 Sep 2025 00:53:28 GMT  
		Size: 34.8 KB (34806 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.7`

**does not exist** (yet?)

## `logstash:8.19.3`

```console
$ docker pull logstash@sha256:aa415141e5ac82d75d8aa8c8e1796866bfe78177317a10243fd028095b2e6713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.3` - linux; amd64

```console
$ docker pull logstash@sha256:e374797cd6e53335066715012ed70cce618446ea86393710b62ed96003451ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.3 MB (524320552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d175dfd52b52309c931e6b7604e9f0e0c56244e408ea0034bc620b504ff6cdc0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/logstash
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 Aug 2025 08:37:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.3 org.opencontainers.image.version=8.19.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-25T16:49:49+00:00 org.opencontainers.image.created=2025-08-25T16:49:49+00:00
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eec9fa333b92724c6dbcec7c3f532e6d8b8117dc3c6e983e1cb1a1e3f1059bb`  
		Last Modified: Mon, 15 Sep 2025 22:21:41 GMT  
		Size: 47.4 MB (47403322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0f93e66ce9cd0d073ecc68b5b35b910f31c00cab005e5e4badbbe1caad39d9`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48920cb6539e118314fa132cff1e11a4a466b80a5d28b7f76e7fdf84e2c11e1`  
		Last Modified: Mon, 15 Sep 2025 23:23:50 GMT  
		Size: 441.1 MB (441105427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d59ff624e3a2c41e5a42ae5876057deff8f3c390ffd3ffa5e5966d9217470a`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a8b1b9d8fa5eeb5bdd3a148eccb042350a2fca294bc48691f5937ebae2837`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039c33e9b623985fbffa949964d05e77d2331edf699d12c8cbc077ea70391d7`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117bd1cd84a10368ae29f5fe661964a0df9b81542ecb862fe2b0954bab2ea643`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb3b12241c6a6c0542e5f41e2d66d37eb013334dd1cc50a6263595a87221f76`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 4.0 MB (4004276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde514f4161e60ce0e3f8de47b68ef0d81831a62cc6fdeee7939261566e8838`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 2.1 MB (2078193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253bc4df24243c32252bf35bd4679dd4afbb1334848f50c408d4eaf114342b2f`  
		Last Modified: Mon, 15 Sep 2025 22:21:38 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.3` - unknown; unknown

```console
$ docker pull logstash@sha256:fac668709c7bd101fd0cdca4f6eb77068d2cfe2140369bfac1d383dc6df61662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be8cdf1f38e3d6ae37f6a1080981d59326fd3280d525cd433e8c5a4911dc76`

```dockerfile
```

-	Layers:
	-	`sha256:645ab447d6733ce91cb34eac97bab1fa8093e47f5cfb2f9cf963f46a3a44b79b`  
		Last Modified: Tue, 16 Sep 2025 00:53:42 GMT  
		Size: 3.7 MB (3653202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed6748cfd6e0225cfb6d2714f5d29c6e205c96cad69ddba1c953a9132c6678c`  
		Last Modified: Tue, 16 Sep 2025 00:53:43 GMT  
		Size: 34.7 KB (34654 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f8a41c747afc65e1787fa1e59d7d600ba5beeb688b3ac90a2f6629ab01dec536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.9 MB (522884102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9400963ba9090942f0c4b2d88f7c8b7479854fba6ef4efe99b989e2c856041`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/logstash
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 Aug 2025 08:37:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.3 org.opencontainers.image.version=8.19.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-25T16:49:49+00:00 org.opencontainers.image.created=2025-08-25T16:49:49+00:00
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98030c31491111cb3e9f0b4729948ba57f62e52c7614ff6f6c65b18b6551f6af`  
		Last Modified: Mon, 15 Sep 2025 22:20:46 GMT  
		Size: 48.7 MB (48701371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc3421e304a0f99837bffd38eb8026f7c1be57eb2020d3edad3a01a2c05543`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a8f09f119d0aaa15c020492529aeb9741aab6121e850965ca6674f2535f7c1`  
		Last Modified: Mon, 15 Sep 2025 23:21:15 GMT  
		Size: 439.4 MB (439385818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45409a47b8f53656fcb58e8a7c58cd7d5c07f19f41c6c9fe5083b8c3beb0a3cd`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49a67eb5d6e43802991f88418b4475b90240642709418ac882e6aa449ed16d`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506363920205d7082d7fb9f0688275c969af879c7aa49dd9a59925dd7ffb466a`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23c14269a574b172019ace457141ac88f26094c90c70b6eda2205e5e6f19fbd`  
		Last Modified: Mon, 15 Sep 2025 22:20:40 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e743aad55f9fe100ca6610a03f83a236829c512f46106bd153c0bd7c92d67e8b`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 4.0 MB (4004281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2514a235f037327ca7b13275837ba9d78e56a0cb904bda8336e152b644b8735a`  
		Last Modified: Mon, 15 Sep 2025 22:20:41 GMT  
		Size: 1.9 MB (1925420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c58fe7d48f53ecac73abb45751c29a1a6b3f2dc2e5fe02a7f65ba4e96d2cf0`  
		Last Modified: Mon, 15 Sep 2025 22:20:39 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.3` - unknown; unknown

```console
$ docker pull logstash@sha256:62911ff2a9ea5fdf5017fe0ab875de401ea1241205c48a3180e4ad7529732386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646088b7d44080bc0b4f2bf2281313960926d1872d1819ddffddfb9be44e06af`

```dockerfile
```

-	Layers:
	-	`sha256:40b0118ea1a269e6697f22c4fb14d7425b8dbf3375f225437aa952a2e43ae5e9`  
		Last Modified: Tue, 16 Sep 2025 00:53:49 GMT  
		Size: 3.7 MB (3653627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9372cd15867ca568914b2cebf60ccbb45b92c4eb9a39e792bbb0715a65ae672`  
		Last Modified: Tue, 16 Sep 2025 00:53:50 GMT  
		Size: 34.8 KB (34798 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.7`

**does not exist** (yet?)

## `logstash:9.1.3`

```console
$ docker pull logstash@sha256:434e4955a8a205cdf13305c59841666fe0d2722eb67d851adec8599a48bd1ede
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.3` - linux; amd64

```console
$ docker pull logstash@sha256:2ba1992da2e1787e036a0dfb7bc7c4b2e5ffd8676b5cd28f562bd0b91b8c975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476783183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45e95440776895f141b07b4fa5b1da440d4188ef8bd1a7278465ff748870a5f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-20T01:20:45+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-20T01:20:45+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a563a108f97a5ca4b28564420a0feac16cb91fc56e727a2ff31eecb7b4e616`  
		Last Modified: Mon, 08 Sep 2025 23:30:09 GMT  
		Size: 5.0 MB (5018682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7224deedaf3e3de2293b490f9fb30ad8efae40962b547f822373083e27e3ef4d`  
		Last Modified: Mon, 08 Sep 2025 23:30:24 GMT  
		Size: 430.0 MB (430036122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e3867f56c1c6b1311cbfc7dc8da0c60b288c9f7daea034aaef4cd21921c45b`  
		Last Modified: Mon, 08 Sep 2025 23:21:54 GMT  
		Size: 2.1 MB (2078182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31ee4bb135fececb776f3871556ae880506abd76a141a81200279dc24845ffc`  
		Last Modified: Mon, 08 Sep 2025 23:17:48 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3053ede0ed94644852a6455cc6ff317fd5360f3b8f5f843726980844a7719bc`  
		Last Modified: Mon, 08 Sep 2025 23:17:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8b84a22d15bacff27e42ab2970a6227a62d14e056201a48773ed60f23c945`  
		Last Modified: Mon, 08 Sep 2025 23:17:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c620550e8216a7295f2a05bc6b6567a088cfe29bb3df43903e5606b443bf6`  
		Last Modified: Mon, 08 Sep 2025 23:17:49 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.3` - unknown; unknown

```console
$ docker pull logstash@sha256:1732021342391ba072fe299a55239fc2efb80c9dd470e1dee5a87e28f6979714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec38a932b01b393c890fa21e0fa116c92130d3e478cce42d007cf46b8299cfd4`

```dockerfile
```

-	Layers:
	-	`sha256:8db7102accdb4782a07d82cb67c9c610901d8d67942a25d1d38e6d71faf39e94`  
		Last Modified: Tue, 09 Sep 2025 00:53:25 GMT  
		Size: 2.1 MB (2075930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e071aa8f00aede4fc6156ec4b0ff7eae2ace37a755297e76aff3fc50099d59`  
		Last Modified: Tue, 09 Sep 2025 00:53:26 GMT  
		Size: 29.5 KB (29537 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3e91d28438f6513ee5cd83f732cbe6e2a0ab35cdd540a52b49387ff8533e18a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473142559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e964fc9cac82731a261b7b19a30f81d659c06bf96d52b0a8af835c1467a6bc71`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-20T01:20:45+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-20T01:20:45+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af6d43f622e7d0754ce9e9e31f01892e18723489d0025941757047a1784bcdd`  
		Last Modified: Tue, 09 Sep 2025 08:32:49 GMT  
		Size: 5.0 MB (5023649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9869b6530162d679efd22b719ea897267e440a22b0f26e971a8ad7185960300`  
		Last Modified: Tue, 09 Sep 2025 08:33:22 GMT  
		Size: 428.3 MB (428330017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e8dbd92136d69ff3847b483f17783a1460d47ae4a7a297291397501d0e108`  
		Last Modified: Tue, 09 Sep 2025 03:55:27 GMT  
		Size: 1.9 MB (1926413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da9b45fa9a70278c392af7fcbafb426de144a6ed282f147bb84323fe0521611`  
		Last Modified: Tue, 09 Sep 2025 03:55:25 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2917c01f5bad51843a3c4884e4ab21f8860586bcc3f6c98f121a3df0bd448b74`  
		Last Modified: Tue, 09 Sep 2025 03:55:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0489508b73e29b519bf0b330d57d9f52e9b924405125e34582ebb06c27831c71`  
		Last Modified: Tue, 09 Sep 2025 03:55:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da5e5d9e01c36b718faab81a1a0e56fd01033c0c66e1b24b3c7dcf4e4a648da`  
		Last Modified: Tue, 09 Sep 2025 03:55:27 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.3` - unknown; unknown

```console
$ docker pull logstash@sha256:d89b1eb18e305bc57f28bca69e8e08770eca3a96690fea913ac303e62b84fbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1af10d23c1574daeffdf3c7823c12479857659e2cec3ea4ead4bebc0cd6a04`

```dockerfile
```

-	Layers:
	-	`sha256:6a2bc1c0654d6d4a9ea35da81fdc1bfcaf0d266fe8e00b120f193c528ee068f2`  
		Last Modified: Tue, 09 Sep 2025 06:53:27 GMT  
		Size: 2.1 MB (2076502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d249ad44def538d874b2510e5bd246759d6ff67bf364f7e496bfbd464596ca`  
		Last Modified: Tue, 09 Sep 2025 06:53:27 GMT  
		Size: 29.7 KB (29654 bytes)  
		MIME: application/vnd.in-toto+json
