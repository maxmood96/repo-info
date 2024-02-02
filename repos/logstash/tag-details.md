<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.17`](#logstash71717)
-	[`logstash:8.12.0`](#logstash8120)

## `logstash:7.17.17`

```console
$ docker pull logstash@sha256:df8493602d9a8ddf4830aa9bdeb64bb7b512533b45037197ef321a377c04de53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.17` - linux; amd64

```console
$ docker pull logstash@sha256:22e03d9f219c388fb7ced1867586f79aadf7154d8426061066e1a08c477de792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.8 MB (442756570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ab03965d060f08a665e2977b38b9cadbf6040ba0fb7fb9cd495a7ed82da2e4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 14:25:39 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.17-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.17 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 23 Jan 2024 14:25:39 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
USER 1000
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.17 org.opencontainers.image.version=7.17.17 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-17T20:23:37+00:00 org.opencontainers.image.created=2024-01-17T20:23:37+00:00
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb98151f1ab94576710562dfc53d26a0a47a25a7d93bbf643cc0226da0d06db`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 46.5 MB (46531755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d365f79fcef8bc6cb3ff7c3e8ae890821a2b930ffb057182084ffb6eff16e403`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879ab257f23066aef3b7b28ee8ecc78e1b6cf955c805bd2a8198cea1a9325cc`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 366.9 MB (366860395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e36de56e70f7917968e5c45fe3c56d82c2bdb692d2b794106fc0f58cca69460`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e34efe61932ee07709299f2fea5b663d26ab4fae412ad45807cb2e1a7e250bf`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff6bde4d4eb269fa85991644e52cc63afdc30f35a09e503859725b8f63834bf`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2b7297ccc420cab2c02583b28d92ec871731bf074d565ce05612109ed6abf4`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02987e507ace6ddc84629a9382eed8f67632e0048b710ebe28c3c285b5df196f`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f6a437b1741bf0581295706aa695935f825ea8586d89cee5562955f868468`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 1.8 MB (1844903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4275671fc28d882bd8ba4a90cde5923df354eeb5e443988022eeb98d8740f9`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.17` - unknown; unknown

```console
$ docker pull logstash@sha256:65ef8d58ace6ee22895566060e8af5e81bad40ea113339d6857577ad515b1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc91299487e1c90b5d42be2f2543d45ad288acc6678b7cef299b770e73b2b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8269a6db14f593dbd05ff3a30ce9bcf8df1c9e68ef4611787a375a2100323d05`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 2.7 MB (2673662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273f9eab4bf48ab9c579b8c8c1719564ca549b2cb7d16edbbf43b4c616cd59c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 32.2 KB (32168 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.17` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e505c0b8d95667b3d253dcba0f8c10a10085691f4d05b47b2a9e6053db254c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.2 MB (428155414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26e91cef7ac9472d4e97596b5853f9972fc590b858dd072b4e077ecbd12eb0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 14:25:39 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.17-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.17 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 23 Jan 2024 14:25:39 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
USER 1000
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.17 org.opencontainers.image.version=7.17.17 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-17T20:23:37+00:00 org.opencontainers.image.created=2024-01-17T20:23:37+00:00
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1e7d71d662fea3176db34f01e2afb22468596910909062e42889cb2be6766`  
		Last Modified: Mon, 18 Dec 2023 19:59:02 GMT  
		Size: 36.7 MB (36736504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fe55da162ade1eb87e2a8e5383c00e22edf99c2e9c1f861f35bb42281cdd2`  
		Last Modified: Mon, 18 Dec 2023 19:59:01 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f2424e2301175a15a894a53d3881569cea17cfc9aabdb940783e557d0ed5b`  
		Last Modified: Tue, 23 Jan 2024 21:45:16 GMT  
		Size: 363.6 MB (363594644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56daa6f56e18c5e002eb5a5481ccf011b54b54409a53f7dc84b96c809c26353`  
		Last Modified: Tue, 23 Jan 2024 21:45:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32daac92a5b0515f9958e6debc2e298c1d901060c4f63174d830f86b8c29f3d`  
		Last Modified: Tue, 23 Jan 2024 21:45:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d3ccb80e23403fc863947f1faf51e890985a7d4bd3c78fc1e15c610b7d0f1a`  
		Last Modified: Tue, 23 Jan 2024 21:45:06 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb827de92d909ed622666615c8abb39b3f7c907378753a6da781fbfc3e8f966`  
		Last Modified: Tue, 23 Jan 2024 21:45:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14091547a8028bfbf12aa2b10ef166ab5e7a3f223c89c5abf204e8f96573aa`  
		Last Modified: Tue, 23 Jan 2024 21:45:07 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d43785d1bccd24151f68492748d9760f341f1164bcbc5fffd34ab55a377983`  
		Last Modified: Tue, 23 Jan 2024 21:45:08 GMT  
		Size: 1.8 MB (1844905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2384e1d4e1f2e28c9fc457cfdd5b6f067e8f97ab29d42d83d308f85d8bec6f`  
		Last Modified: Tue, 23 Jan 2024 21:45:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.17` - unknown; unknown

```console
$ docker pull logstash@sha256:a99ea36add368df00b80da3e4b17fa2af70f1c8a816a591612378b090da3d7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92db14586b761fb97e20e42976077cf0865f2f43eab7ba5fd5a5ab8a4787598b`

```dockerfile
```

-	Layers:
	-	`sha256:26529d5a26436c9937ba91ec436f5029f69fd15db07d293b3f0828c1c4f2aa3b`  
		Last Modified: Tue, 23 Jan 2024 21:45:06 GMT  
		Size: 2.7 MB (2673972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f17666ebda34eb46974f2af3023ec7a3a60a733118adf218bbe7e3a00068ee74`  
		Last Modified: Tue, 23 Jan 2024 21:45:06 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.12.0`

```console
$ docker pull logstash@sha256:6f6796e5c380bbb80079ae0fae856d2e1963d9d18466894af6487d5f68650758
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.12.0` - linux; amd64

```console
$ docker pull logstash@sha256:64c4dc12d3852bc7bc775e434390c56bf834f969475e793b302fd7a668fc81fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428669276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78924a5f6d409a36dc38bc9cf1c0a4aec8a13d99d99dcee8ca923ffd4e39f14f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 17 Jan 2024 15:49:20 GMT
ARG RELEASE
# Wed, 17 Jan 2024 15:49:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Jan 2024 15:49:20 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/logstash
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 15:49:20 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.0 org.opencontainers.image.version=8.12.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-10T10:50:49+00:00 org.opencontainers.image.created=2024-01-10T10:50:49+00:00
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8718d36e461ca4e0c8cd65afe8d3cded662af2b6e11539cb51002e17ea1b8df`  
		Last Modified: Fri, 02 Feb 2024 00:55:57 GMT  
		Size: 46.5 MB (46531992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160ecfd46179b4fd63470f3381a8d0e986bd76d981f7769edc545922e8ddff1e`  
		Last Modified: Fri, 02 Feb 2024 00:55:57 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2771eb92b28ae26575b7413375a01ed06b72a1e062f82376ef15987e58500973`  
		Last Modified: Fri, 02 Feb 2024 00:56:29 GMT  
		Size: 352.8 MB (352770105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e11289728158fb7b0c86cbda95b4071cb2fab9d6c10706ee4fade108078ec8`  
		Last Modified: Fri, 02 Feb 2024 00:55:57 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba98b3354794c9c45b19f4bfd9db107b20f9d561aebe8bb738e57685870afd99`  
		Last Modified: Fri, 02 Feb 2024 00:55:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87950063e4adcdf6333a48dcd1c126000d93a339cb34ab1080b72bfa4753ce`  
		Last Modified: Fri, 02 Feb 2024 00:55:58 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9decdc1b8d0feb54b1326f6c4a27e9d47dfe17d1abb430e810c7fe884d25302`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d834e004727db19fa5d54d3cb2d27cc90c59c5102df3ba5a6a911f25fac74dfc`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688c96cc6413a4c8e4f4d37dc445d72b933bb385b67cee4d42cc05d427d80c44`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c76444475033df0187c9ac3466ded81627e5c971770441f856b9d30b0081e`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 1.8 MB (1845136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ed38944851a5103ffb5193db15486dbec27b33f375ec33590051783f4e1c2f`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.0` - unknown; unknown

```console
$ docker pull logstash@sha256:3e2211aaf085611be354834ede658cfa8dcb756e928e10c59b5e6b8e17b605ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6fef5a2cfe482b135fb9bb192254dfd15eea4856812da972cc2875b682164`

```dockerfile
```

-	Layers:
	-	`sha256:140b49f4e17287ab77a89666be36e1a6b9252350f9b735801ce7232ed11a06c6`  
		Last Modified: Fri, 02 Feb 2024 00:55:57 GMT  
		Size: 2.8 MB (2790555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1979ca88886a9cdad61facfc1384c966e378c45d541bf65a0659261bc92a37`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.12.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7a6ab3015c5b2b397ef7789e95ce89b5bbfb9bc47e4ce4b6156cfec66ea1dc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.1 MB (416147325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2392f7899b2e333139b3f051424eb8fbadf02fc5f9a11d3d8625a57fa32d35b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/logstash
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 15:49:20 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.0 org.opencontainers.image.version=8.12.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-10T10:50:49+00:00 org.opencontainers.image.created=2024-01-10T10:50:49+00:00
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1e7d71d662fea3176db34f01e2afb22468596910909062e42889cb2be6766`  
		Last Modified: Mon, 18 Dec 2023 19:59:02 GMT  
		Size: 36.7 MB (36736504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fe55da162ade1eb87e2a8e5383c00e22edf99c2e9c1f861f35bb42281cdd2`  
		Last Modified: Mon, 18 Dec 2023 19:59:01 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9240db9bf3ab6de1cb24342aa4b42df3aa0d718496e0c1507267360929659a`  
		Last Modified: Thu, 18 Jan 2024 22:20:23 GMT  
		Size: 351.6 MB (351583812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2bc5bc70f03789098968d7a5e0ca1044335d15b9e4b56102205d09aa6c6fc4`  
		Last Modified: Thu, 18 Jan 2024 22:20:16 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c26e305de11a02d21db24b9a3b04d9f9717622851860c3d4008393dc09ac3a8`  
		Last Modified: Thu, 18 Jan 2024 22:20:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e5c728f6ea0e9955fe8c9459aee3695c67fd60122de7f987eff72947cb06d7`  
		Last Modified: Thu, 18 Jan 2024 22:20:16 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8ea4e01a7974fee14d8f8d9ebc8fe6b3477b4dc85c519babf399885fd435f1`  
		Last Modified: Thu, 18 Jan 2024 22:20:17 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd068dc532137730b56f0ba36808dfa16bb66280caeb3cff14726c331c58a15`  
		Last Modified: Thu, 18 Jan 2024 22:20:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6871ffedeeb3fb5872feb8dbcfef82c81228424820e906268d081f9b578bbeb4`  
		Last Modified: Thu, 18 Jan 2024 22:20:17 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4111b01db4746215075baa4ec97663002920f1c4b08d8592564045ee7a80593d`  
		Last Modified: Thu, 18 Jan 2024 22:20:18 GMT  
		Size: 1.8 MB (1845128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963902c80a11a1e7fb35f5909f593a400ffe422f203b7db20eea35fa6b268284`  
		Last Modified: Thu, 18 Jan 2024 22:20:18 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.0` - unknown; unknown

```console
$ docker pull logstash@sha256:88a2c7f064ea6fde3c3674ce50bbbef9c8242a7c5607f3d687941562adac1560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5996428d60657a4a18746c2cd4d73957c4d4c118c11087886563f448c740684`

```dockerfile
```

-	Layers:
	-	`sha256:088d50bf09e29c21aaaf99700d0e51633204529b3a39c30c62e94d3ff5006175`  
		Last Modified: Thu, 18 Jan 2024 22:20:16 GMT  
		Size: 2.8 MB (2790878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b38bc48ea074f1b9c5673d6a38101fa601d289f44dbdca5440811be5a47a6`  
		Last Modified: Thu, 18 Jan 2024 22:20:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json
