<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.7`](#logstash8187)
-	[`logstash:8.19.4`](#logstash8194)
-	[`logstash:9.0.7`](#logstash907)
-	[`logstash:9.1.4`](#logstash914)

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

```console
$ docker pull logstash@sha256:4cff5e648622e2007d3d09bf4f54701a629f0c42d54155a22aad038d164b8c1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.7` - linux; amd64

```console
$ docker pull logstash@sha256:3dd480d92d8d45684bc18ab2f7925632b5b8da48fae230512ac8f77a4f47b200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524202572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d93301a9b1dfae633ad2e33a43872a8831b1568f991da67765ce1dde77608b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.7 org.opencontainers.image.version=8.18.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:32:30+00:00 org.opencontainers.image.created=2025-09-09T20:32:30+00:00
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683daac8f55b8c39c6efac24271b3d9ad3e26f8572a533493441d51add3235e2`  
		Last Modified: Tue, 16 Sep 2025 18:02:43 GMT  
		Size: 47.4 MB (47410876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fa495453266cc5b135f688e8ce62639de93fccf6cc30e37903223a0a56a4a9`  
		Last Modified: Tue, 16 Sep 2025 18:02:35 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34b613f9b0ab7e553db9cdcf85fc1f22d3f2c0dd0dd50c3e4b02b13d7d660fc`  
		Last Modified: Tue, 16 Sep 2025 18:09:30 GMT  
		Size: 441.0 MB (440980153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e1f8411d0ac0e85b91edf10067200cc018f6579858009bdc1609dd7e1bc3f1`  
		Last Modified: Tue, 16 Sep 2025 18:02:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ebe138b4dac794e0d310062f9ce26338f42b0d7023320c313324921c4f6cf`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0df81189cd3cdf52297fdf08962ddba3300ef56a41d288362e143299388685`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7ca17a9f239146a1c1bb3ba02a7c9601bbd027f8b2a6a91fc08873437f942d`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a954c93c3b8dd327d2832bc9bb1a15e4f52bc0a81ee9f50cf2dde9ea9d5cc54c`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 4.0 MB (4004187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba3adbf5489c03b1bcacafc6d94205b6da7c5130c61fb23f427871699ec1e02`  
		Last Modified: Tue, 16 Sep 2025 18:02:37 GMT  
		Size: 2.1 MB (2078012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae963b11313e5f5f67219f6b57e5f45efe8aeb303e774e48483bdcb5b13f66`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.7` - unknown; unknown

```console
$ docker pull logstash@sha256:f0d6adf780755aee565bf4d23d776d05755df3f377372904e1e096e08f4393f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0a46c6f2076521677680f87a169de4f3715c8445c985cdd579b6053aded75c`

```dockerfile
```

-	Layers:
	-	`sha256:5f95b14583b757118dede6b9768b899994f19d51b1f12ce11876a56522863420`  
		Last Modified: Tue, 16 Sep 2025 18:53:24 GMT  
		Size: 3.7 MB (3657649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c255529988e4546a307a3989ef079a4aafad76ee2f380916498d0b1753c44e`  
		Last Modified: Tue, 16 Sep 2025 18:53:25 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1c4ba85a5ce0067c0525bff060d0639e1c47b8a7534383bfef9487a38bdbfc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.7 MB (522747367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901da7b542968cd645cfaf4c72641862e7e558ffd9f94e247d080c8a962ef2fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.7 org.opencontainers.image.version=8.18.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:32:30+00:00 org.opencontainers.image.created=2025-09-09T20:32:30+00:00
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b1805703c37759a4938f935402fde116c1955d7da9fcda6156b98fb62def02`  
		Last Modified: Tue, 16 Sep 2025 17:56:41 GMT  
		Size: 48.7 MB (48702336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c042b4e73ea0d89249862836214dadd9fda94c4914521203fa78243ad839392`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5419478cd706f583a610216d348f19d658aad7c2417aaed2eff15ef5d20d7bda`  
		Last Modified: Tue, 16 Sep 2025 18:10:18 GMT  
		Size: 439.2 MB (439248072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8322dcb8989db83804b3a194d52d6db006ef325b6764b10c08df6f23fdf51`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb4776cd52f8fd1d41c31603bdaee568cf8a756e24f69963417a6d78a19d2a`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dde569527a175ede3a45f3e3161ef41174061a5bb95f7c03e61d7a10bbfb07e`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27add514b2115e0f7cf225a95cc1dab9a52d78e3dce14ea941fc281e0a33206c`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34107bd6e0d259b5042da8df8e56dbd7c12479164de05957e150c8846bd3ad50`  
		Last Modified: Tue, 16 Sep 2025 17:56:39 GMT  
		Size: 4.0 MB (4004181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cce590839bb38369140443c392c8d209abcc4173a8de686dd914d52f8bcf527`  
		Last Modified: Tue, 16 Sep 2025 17:56:39 GMT  
		Size: 1.9 MB (1925563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30d62192ca8abec5b88f6add2aec9fd8b8a07a9e3f8abfc9d18ebe7194a31f`  
		Last Modified: Tue, 16 Sep 2025 17:56:38 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.7` - unknown; unknown

```console
$ docker pull logstash@sha256:36c2acd87f066a2b77c6767b41df6f196870a32b0ade042e7e2e4ed3f9cf9c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3d637a946a2586956e7d5cb1f76275ad8f5a6d968f21ada6b8d97f2829da26`

```dockerfile
```

-	Layers:
	-	`sha256:e17d041920abbe4aa9523499817e153118d31b45284603b4c913d889896a95f2`  
		Last Modified: Tue, 16 Sep 2025 18:53:29 GMT  
		Size: 3.7 MB (3658074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ec43d9ab72eb7b8005ad1f12d98ff405a076494bf68bd7377052f881772692`  
		Last Modified: Tue, 16 Sep 2025 18:53:30 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.4`

```console
$ docker pull logstash@sha256:2fced8628bd13873de39c99d58e53f465c004a8c1648a9ab4cf3e05468f1d1a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.4` - linux; amd64

```console
$ docker pull logstash@sha256:758e9cb5457bc8a2d4a130112a4dda506192215f9c053042bf3224f500d8eaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525261419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e8db18f84d40ba3df3318dcd6c46ebb4ae1981f38c6baafa4e652e0d1e11c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Sep 2025 08:07:26 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.4 org.opencontainers.image.version=8.19.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:37:29+00:00 org.opencontainers.image.created=2025-09-09T20:37:29+00:00
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8a09bcc55010a9f249521ddcaf490a2453ff601376b25589371e31078960f`  
		Last Modified: Thu, 18 Sep 2025 18:52:15 GMT  
		Size: 48.1 MB (48085685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83746b49af5bd8320110899d6c30b3884e966f6b9b40f68e97be0dd9d5470c4e`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdd74ad860bd1f50c637bafcedb6f1f666cba9a2e8f939d61cc6ea02dce2e50`  
		Last Modified: Thu, 18 Sep 2025 21:54:08 GMT  
		Size: 441.4 MB (441364191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fbd91a6301af2f4dfafc42533ae12f2589085e0fb4405552916835df38cde`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2030f244d06962c6b1f3c9f724c6706fab10a0a552f91bb737d97252086c530`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b0fc397b45fef4aac6f5fb34dd44559557e2bf8c249d5dcfdac43f2404b6`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf86639004c7d50ce0a3e345b68464006c55a27aa1b62dabbf497f411fdbe61`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd1f2ff29ca527a5bacab5041651be6c11c511c1be843308145eda4f013b07d`  
		Last Modified: Thu, 18 Sep 2025 18:52:11 GMT  
		Size: 4.0 MB (4004190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d1c7bcd066daac2e15caf683f410828fa405d4484deafe90184096ed793fb5`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 2.1 MB (2078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59130aaaf38d62800b4cbd923c6215523be6fd8885b28209075e23fd28de9d8b`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.4` - unknown; unknown

```console
$ docker pull logstash@sha256:e1416e01637752f109ef469d2268af85895a0f92a9a1118352259977247f4753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb06035c0f5a68d767aab371fb964b6cdb87de2b5408ea9fd03ac66a1fec726`

```dockerfile
```

-	Layers:
	-	`sha256:e53af1484e7ae8f52bdbacec4eba1e9e952f0a2fc842768653e858711d5bf259`  
		Last Modified: Thu, 18 Sep 2025 21:53:18 GMT  
		Size: 3.7 MB (3653205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f300551e9002dbd7937d90a6465dbea9d4a69434113e32eecbbb2f311c7fe7b9`  
		Last Modified: Thu, 18 Sep 2025 21:53:19 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:9b905bc97dafab68b8fba09be2866a748efc76784b4cff44dec679b26b773da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.9 MB (523932172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9f70af42c2fd8524e509abb1cb96fb9e8f92f648347c4fafc3a930ecf24e6f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Sep 2025 08:07:26 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.4 org.opencontainers.image.version=8.19.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:37:29+00:00 org.opencontainers.image.created=2025-09-09T20:37:29+00:00
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09748050e7703ffc65ef119f061bb301ec4e8534dbaf31ae8461980b1f661a7a`  
		Last Modified: Thu, 18 Sep 2025 18:52:54 GMT  
		Size: 49.5 MB (49507305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4841211c7a791ba5ec03ec309c78089c18e16c4e1d5793f915e12010b28c8473`  
		Last Modified: Thu, 18 Sep 2025 18:52:41 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef06319a9e70b0471ef7b8cb0dd294157fc848d1995092eb24539eb59d5390e`  
		Last Modified: Thu, 18 Sep 2025 18:53:19 GMT  
		Size: 439.6 MB (439627909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d3816b6f8508df37fd4a92fcde44759ae834505d3d92fada9fd704cc4cccab`  
		Last Modified: Thu, 18 Sep 2025 18:52:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d368b8ac0b43fa43f0680063fdaf03fc2602265fd972990cfa7b2ef0ba261d9a`  
		Last Modified: Thu, 18 Sep 2025 18:52:44 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b03bb07219acc91feee251f431e02ae5258dd6bde896e0b40ea84bd02462b5`  
		Last Modified: Thu, 18 Sep 2025 18:52:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fef1a1ee3625e7e77d61f0a05c0bd5815c5c0e33e7bd2e0184d3f7cd34c32f`  
		Last Modified: Thu, 18 Sep 2025 18:52:42 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c378d47402d0c7b18946f60fbd0a3861c86ece663cc43605b4da6e24b54c5c0`  
		Last Modified: Thu, 18 Sep 2025 18:52:42 GMT  
		Size: 4.0 MB (4004181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a835c8c857d8ec419686bfdc21112bd3bfd7563eed192ff167734009437f9de`  
		Last Modified: Thu, 18 Sep 2025 18:52:43 GMT  
		Size: 1.9 MB (1925568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bd3648790edf1ba830651788a59b7cc4bbb1f99e042ce4b6f0426404bdf922`  
		Last Modified: Thu, 18 Sep 2025 18:52:41 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.4` - unknown; unknown

```console
$ docker pull logstash@sha256:01fd3c9a8ae02354c136c446f19abadd269de7770a44f35c61e44aa053071cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5298545a2a9fc1b893b85b455cb13b3835d8184a99f95755710b9aef284ae513`

```dockerfile
```

-	Layers:
	-	`sha256:44c2020141c04afdf57314909f403bf44681a38b152d19470422a71479f7deca`  
		Last Modified: Thu, 18 Sep 2025 18:53:21 GMT  
		Size: 3.7 MB (3653630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94195dcf247d7f405269f24450ac8368f0ac6bef37a7a3fd324f04d0d0771e4c`  
		Last Modified: Thu, 18 Sep 2025 18:53:22 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.7`

```console
$ docker pull logstash@sha256:09ce8f97402593d4a2c35fb1010a54c67b47ae4c250b374dfa105a74284de9c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.7` - linux; amd64

```console
$ docker pull logstash@sha256:5af6b7e90498d795e7a13464af8004a075faed9b1f8052cd655d1f47f74e7fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484967026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951875a64fdc1a95a2fecfd716b229599492b6ab071f41cc9533df8e84f120d`
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
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-09T20:25:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 16 Sep 2025 08:32:12 GMT
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
	-	`sha256:64655f97cbab2d06feef6c5d5faf8dea79031e1eda1a79721465372b9652ca0a`  
		Last Modified: Tue, 16 Sep 2025 18:02:03 GMT  
		Size: 5.0 MB (5018755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66909ed008b6c53d6628904b8655cff93e8a76a2f08c2a4b599d4252de7b69e9`  
		Last Modified: Tue, 16 Sep 2025 19:00:55 GMT  
		Size: 438.2 MB (438219893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a1f249c80a71f212fb90f0fc0e2ad435b7f999bc56e91f1a250a518209e9d`  
		Last Modified: Tue, 16 Sep 2025 18:02:03 GMT  
		Size: 2.1 MB (2078179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb731bd00bd5ff0caf154b7ac11fd7bdfa4acdac4039fc5b4c92832c4af9117`  
		Last Modified: Tue, 16 Sep 2025 18:02:02 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23ee72d1470a3845137e9c05476bff7ff544ce25bb5c1d640841ad7db7588eb`  
		Last Modified: Tue, 16 Sep 2025 18:02:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385e295920d6833799bf0f50548f330516e3aca79159e116b72a8ab88dc57897`  
		Last Modified: Tue, 16 Sep 2025 18:02:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b3bbf8619b4746b4223c786594c3be9accf24e93d9bdb36fd0f53fc12303e`  
		Last Modified: Tue, 16 Sep 2025 18:02:03 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.7` - unknown; unknown

```console
$ docker pull logstash@sha256:a7aedf016e276f369fb9a4b2269f651fe68d4dc3efb5af3dd59a142edf3e9d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89032c7e2979e37c747560ed574bbf396569a9cb9f2855cf8ca3791209c646`

```dockerfile
```

-	Layers:
	-	`sha256:011200baf29d66b37141e635a9d14f5482d3424fb77f5008700d537042f2c975`  
		Last Modified: Tue, 16 Sep 2025 18:53:32 GMT  
		Size: 2.1 MB (2142410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e7afd4e1c68729448597ca9315ffeb99a7c29f3d4e9ee7d0b90bb1a3732b98`  
		Last Modified: Tue, 16 Sep 2025 18:53:33 GMT  
		Size: 29.5 KB (29536 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:6776a295b21eed6e5cb4c1d8757a0e1fa614dcb566b506cb1e0a48e41fc72f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.3 MB (481295812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200240e31f3891c9ec76b8bad843bb7998977d822e1f20154b33507c4b062967`
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
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-09T20:25:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 16 Sep 2025 08:32:12 GMT
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
	-	`sha256:6826552dd24e13fd656768516c4b45ccf6b0050f6fdd7cc055631718c3ac98a0`  
		Last Modified: Tue, 16 Sep 2025 17:56:59 GMT  
		Size: 5.0 MB (5023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf6b7de3dd809efbf1d562079c536be9bea8a4175a1f578ed93ead2c58c7a8e`  
		Last Modified: Tue, 16 Sep 2025 18:53:52 GMT  
		Size: 436.5 MB (436483295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfa27241a3236e454e378ca8599fa9ff95c99f3bd14880f34c653902aa61aac`  
		Last Modified: Tue, 16 Sep 2025 17:56:58 GMT  
		Size: 1.9 MB (1926417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc3f9ba7faad62a22558654e42f476a64e8767d075edef62d9965b2a640310`  
		Last Modified: Tue, 16 Sep 2025 17:56:59 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fa1f8510efa0222ab083bf7d43bd8c1847d3103e992d2ce265ac81e530b1f8`  
		Last Modified: Tue, 16 Sep 2025 17:56:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fde07fbbf362181278ac6175e5b19e5a5e372d8f90da1f095677d741b4f4d6b`  
		Last Modified: Tue, 16 Sep 2025 17:56:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca21402935e5aa467d3680ed21fd6a391f18a4bada70929b24c7fb846e8f30eb`  
		Last Modified: Tue, 16 Sep 2025 17:56:58 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.7` - unknown; unknown

```console
$ docker pull logstash@sha256:bdc7ff16b52774ef75bc06c3c018d25209f0cbec4d0370eb67c6839fb1df2db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbfabdf8b67a2ebec915cae9126e52742b469a486434f24dc8e5275edc1df35`

```dockerfile
```

-	Layers:
	-	`sha256:e57dbcc17b657413fd49636a1270971cb6ac315f4f1d7c7984e627131fe7d1ba`  
		Last Modified: Tue, 16 Sep 2025 18:53:37 GMT  
		Size: 2.1 MB (2142982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f635ae5db38427546d2c526454ecd11958353b559d9fed8b866d6e8265dce`  
		Last Modified: Tue, 16 Sep 2025 18:53:38 GMT  
		Size: 29.7 KB (29654 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.4`

```console
$ docker pull logstash@sha256:16b00989a83ece71462f9f18b4914875d77bc40388453e93140b02aed7acd921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.4` - linux; amd64

```console
$ docker pull logstash@sha256:1f52d2df13149eb4ac355e6aff6f4a49543b36a94d20b575dc761cc2335cb6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477030582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b478a920f1a50a8c84dc3b28ccb61f107b8fd1f42da63e3b6d681928e9d8243`
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
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-09T20:25:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Sep 2025 08:05:18 GMT
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
	-	`sha256:ae4dba34329df27c9b513fd1db0e5aff51bd702bd6ce3d943895f0ce1ab4b249`  
		Last Modified: Thu, 18 Sep 2025 18:52:59 GMT  
		Size: 5.0 MB (5018693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72b4e0bbf0319acc224012994e353a7e2107b09ded8d77e0cb7f95b3f15a0e`  
		Last Modified: Thu, 18 Sep 2025 19:12:51 GMT  
		Size: 430.3 MB (430283513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd601c3356e57d6b1f58128a6aa195812b0050ec80b71133220459dc94fcdc8c`  
		Last Modified: Thu, 18 Sep 2025 18:52:59 GMT  
		Size: 2.1 MB (2078181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952483ae472a5daa56f7b7c3da07c15624d29315e6933ca2c1dacdc0d49d0904`  
		Last Modified: Thu, 18 Sep 2025 18:52:58 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b2e9214fd522eaed9bd5adf55cf4653e256ae3a87ed217e907841d91e1ec0`  
		Last Modified: Thu, 18 Sep 2025 18:52:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b690231b7d883e51c008b3c91dff76f5112dc3eb6587e9de66d8a5f6dbca6d62`  
		Last Modified: Thu, 18 Sep 2025 18:52:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67eefdba5efcbabe403eb2890b1c1d5ebbd0bfa319fd0c9223927355a27a43b`  
		Last Modified: Thu, 18 Sep 2025 18:52:59 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.4` - unknown; unknown

```console
$ docker pull logstash@sha256:3471658cc6beeac57650fd04a53ecfd7d9ae35935f6e9e1183407934a47ba9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab69b00ba3eada22ff5bfbe27f8074d7e817997919bda965f87e3fc41aeb4dec`

```dockerfile
```

-	Layers:
	-	`sha256:c851d493edd21b627db26d8b7faeba2e3be7f0a785bb0011c79766f9c4faa551`  
		Last Modified: Thu, 18 Sep 2025 21:53:24 GMT  
		Size: 2.1 MB (2075933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7574952505a14027251187f32ed41d83206e17785f3cb3cff6e7120426e40f96`  
		Last Modified: Thu, 18 Sep 2025 21:53:25 GMT  
		Size: 29.5 KB (29537 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ed56cbffd5e8398931ec95b67acf03aad3583eb76285ace3dc15dcc05e5f321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.4 MB (473379914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565d078eac8a0d4fea0dfde5071b7b0cc770ce6fcefbc072f78dfe58e65ea17f`
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
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-09T20:25:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Sep 2025 08:05:18 GMT
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
	-	`sha256:e13bae584497092e5ca29a14307dc89269e2fbd62627239737b0628ecbbe0522`  
		Last Modified: Thu, 18 Sep 2025 18:51:47 GMT  
		Size: 5.0 MB (5023607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22975224748e8a7a2de4d0bbde92b0dd193257eb4f5f16c412b552b1924cd3d9`  
		Last Modified: Thu, 18 Sep 2025 19:02:14 GMT  
		Size: 428.6 MB (428567405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01f8b961968267530a5acea858ed4769af405e8a386b645f53f793f129ee792`  
		Last Modified: Thu, 18 Sep 2025 18:51:47 GMT  
		Size: 1.9 MB (1926411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f89de1bfcc9b59bdc20b552c24f0ee93570f4fc0d9395b412ccd4330151839`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb0995e5103283ddf239a244345955b234093e0a56a508e4c1843c72d499522`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cc57ae98d9b27e816f9060cece3d4ca8580e16d00ba7877fa47574d51a2828`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d52aca21b4f35120d8a7e2c6cff1961145124c9dd5e67762a585963cc7b415`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.4` - unknown; unknown

```console
$ docker pull logstash@sha256:1a64911b70d4d53288d9a636a6f5b21f9cf7fd0fdd8a5fa976ccb36c03398b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fac0058719a3fb6cb713c1214c18a86320f4aae7a0a867c6e6b4bb8221ac5e`

```dockerfile
```

-	Layers:
	-	`sha256:034dc0480be4d1142f27693312b6869c1949f3f67ff5b02ba300f8aed20d06bb`  
		Last Modified: Thu, 18 Sep 2025 18:53:27 GMT  
		Size: 2.1 MB (2076505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee30e4193a14e1d326bb5107d4c3a5a801ee1e7ee9c27e1c612bf5f1c834ec`  
		Last Modified: Thu, 18 Sep 2025 18:53:28 GMT  
		Size: 29.7 KB (29654 bytes)  
		MIME: application/vnd.in-toto+json
