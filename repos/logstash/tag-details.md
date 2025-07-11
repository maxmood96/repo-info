<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.8`](#logstash8178)
-	[`logstash:8.18.3`](#logstash8183)
-	[`logstash:9.0.3`](#logstash903)

## `logstash:8.17.8`

```console
$ docker pull logstash@sha256:8d9f3633fa6eb98744b92009b8f34c7de242fac150b82717041497e7c8bcb27f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.8` - linux; amd64

```console
$ docker pull logstash@sha256:d6ef1320297d0d5ee67b7c9977273ffb365ec336028124430c41af9c801e4f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.5 MB (522481263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f941bac8e669338349280535efed9444c3be17c8f17c479adf6f380ee95e31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:09:38 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
WORKDIR /usr/share/logstash
# Wed, 09 Jul 2025 09:09:38 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:09:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:09:38 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 09:09:38 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
USER 1000
# Wed, 09 Jul 2025 09:09:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 09 Jul 2025 09:09:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.8 org.opencontainers.image.version=8.17.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-06-17T16:09:24+00:00 org.opencontainers.image.created=2025-06-17T16:09:24+00:00
# Wed, 09 Jul 2025 09:09:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557de47cfa9f7c6b29b0facb719e7a6bdb562e803893c96dda249bd5e4ba4b98`  
		Last Modified: Thu, 10 Jul 2025 21:46:46 GMT  
		Size: 47.0 MB (47049671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b71160c32298d2d4ea908961e8edbba67d0e970e960504336418ea148763e`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed9691436d875722f60b77b75125559aef6ac1c0bfe2afc83df4397d83b4715`  
		Last Modified: Thu, 10 Jul 2025 23:02:32 GMT  
		Size: 439.6 MB (439556614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96952b58cea54ca14783846b216cd5c1a373d4159040d8899927254d8bfe8bf4`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1563444329fb7526e53385903dc6b8bf10ea6da32e6ac9bb2ddad667d043f82e`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b059f0e28675522fbb83c1da68d6c417b7507b2e0e8d5fb888a5d250409fd`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec7ce0cd0fa31058700a688c65114e19b25cfbc38d9ad51804fe6396e3a375b`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf66a3bac1175c31c405553b5f659d86092933c2ea5157d27c8f8867bce8929f`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 4.1 MB (4056433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcc92e7f22ebe1f57f78b9a9fb90a5bbcfd9c1c200eb7755fb8d380af60ece6`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 2.1 MB (2094279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf994aafddddf760eacf55e51c15af1989495520fe0f67645098f83cc66baef`  
		Last Modified: Thu, 10 Jul 2025 21:46:44 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.8` - unknown; unknown

```console
$ docker pull logstash@sha256:74c39421428dc1a8a25fa104a57d94efaa956b39f7258ccb0aa7871812a40cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f731cafbb6c303b487b24ac03f807d6efdce653011102256994d4837629add84`

```dockerfile
```

-	Layers:
	-	`sha256:08ad3a73a6d5d96579226cdc9e660f3e3f2dc7a39913583fe26bacd6993f3cf5`  
		Last Modified: Thu, 10 Jul 2025 23:02:52 GMT  
		Size: 3.7 MB (3654598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbecc4882e7e6e63ff5da6eec8acf541b1810a0418afc721cf0d98a6ab4bebdd`  
		Last Modified: Thu, 10 Jul 2025 23:02:42 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7a3aa06cb07f01ef483f01ecafec5f0529bb72ebd9daad358f10e791d948a65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.4 MB (520354202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f4c54a861fc3712602fbe9aff78cc20cfbecad0801af61ccbe52e3fbd24b99`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:09:38 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
WORKDIR /usr/share/logstash
# Wed, 09 Jul 2025 09:09:38 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:09:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:09:38 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 09:09:38 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 09 Jul 2025 09:09:38 GMT
USER 1000
# Wed, 09 Jul 2025 09:09:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 09 Jul 2025 09:09:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.8 org.opencontainers.image.version=8.17.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-06-17T16:09:24+00:00 org.opencontainers.image.created=2025-06-17T16:09:24+00:00
# Wed, 09 Jul 2025 09:09:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941129add2844ded7ed685065061890c3582c568194d370aec48c22948f5bf89`  
		Last Modified: Fri, 11 Jul 2025 01:29:48 GMT  
		Size: 47.6 MB (47634312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3715108e98b64afbb61b374d31349adb4642c875c1ebaa2b28b0b69751737`  
		Last Modified: Thu, 10 Jul 2025 22:15:09 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deba0c0b737d107265a4fba86b2656bc7040da433ab4d871aa40b56d24a5742`  
		Last Modified: Fri, 11 Jul 2025 01:30:47 GMT  
		Size: 437.8 MB (437839849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f93cf2b57d111260492625beaba56dc6636c1f96e9e094c1a1e529183dcdc0f`  
		Last Modified: Thu, 10 Jul 2025 22:15:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1b858c5b1a1f6d68417b2325ba8a1731999fb54d882d73d622b469ce139bc`  
		Last Modified: Thu, 10 Jul 2025 22:15:13 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43781f0256fecb641e1970f7d0828452c1ca23ae9b606ab81b9190a7708793b1`  
		Last Modified: Thu, 10 Jul 2025 22:15:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c1134ca9c2ae98f1f2ce2fbc4558dd70feb32817b30c6fdc6f01304317910a`  
		Last Modified: Thu, 10 Jul 2025 22:15:16 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bfca5b49c9d7e2f56221921d96837a86f7222bce9fec851df1dc81ccf20a7c`  
		Last Modified: Thu, 10 Jul 2025 22:15:19 GMT  
		Size: 4.1 MB (4056440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eadc16e0f9de7ea16cc2da41602f77e4e9fee62b2a7d4e1c2a487e0d577b8e`  
		Last Modified: Thu, 10 Jul 2025 22:15:20 GMT  
		Size: 2.0 MB (1961677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457e0e05055865a073f2441d1546919a7c8b6f24e762986b238ba53ab54647e8`  
		Last Modified: Thu, 10 Jul 2025 22:15:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.8` - unknown; unknown

```console
$ docker pull logstash@sha256:35e4d6b8b07059306525d21aa06254a6e816fcec4eeae8f7e5d1cba3534b20ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda94f614d7a19f7d72d7f01aaf518d24b089cb8f8418cb3d9c44242fd6f22ee`

```dockerfile
```

-	Layers:
	-	`sha256:5da611944bd80ee8f2a81014f99c15b798184d29c741586be64ca8d8d0c1c3b7`  
		Last Modified: Fri, 11 Jul 2025 00:53:56 GMT  
		Size: 3.7 MB (3655023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527b036842108e3f90474616616c3b2547d4d17a37a0d9e6f868704045c94823`  
		Last Modified: Fri, 11 Jul 2025 00:53:57 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.3`

```console
$ docker pull logstash@sha256:004eba5e0ca87ec236b3db991b7b875542fc1bda5bf787dc86d5b3c932fd01ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.3` - linux; amd64

```console
$ docker pull logstash@sha256:4225d0b2433fab126a26e189a2751fc09f200bbc25acdb7abc158021745ae6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.5 MB (522521935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72d924f0d8e96391ec8df17825586826e9670889474c24a4d41191f12854dde`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:09:21 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
WORKDIR /usr/share/logstash
# Wed, 09 Jul 2025 09:09:21 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:09:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:09:21 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 09:09:21 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
USER 1000
# Wed, 09 Jul 2025 09:09:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 09 Jul 2025 09:09:21 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.3 org.opencontainers.image.version=8.18.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-06-17T14:04:51+00:00 org.opencontainers.image.created=2025-06-17T14:04:51+00:00
# Wed, 09 Jul 2025 09:09:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f086fc27d511c9edbea60e5f96f5949d34f13fd8f4ee1194e2ebb27489981`  
		Last Modified: Thu, 10 Jul 2025 21:46:37 GMT  
		Size: 47.0 MB (47049637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd4cd555c8db04c0e4a65b1549732c27d2cbe0271f001722e3b6cd33a094`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcda477d05cf14c72313a4f1c9a76f432569430b6834a657c48adb33071aa99`  
		Last Modified: Thu, 10 Jul 2025 23:03:20 GMT  
		Size: 439.6 MB (439597315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e208e245c65787bcaec1d3bf3fd48625eca3abae34bcd071118e7867fe130`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4944b67354d57c8b3e4e4d360a88df0277e0e0f92173aa5c197bae15a6ab89`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89f2bf85181afa0fbc3583703426d4c52834d0b8a4c24fe4c2f2d80e258ffc`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abcf238b5b06588847f469eb420388bab39c59af68e11495f127fce342ae89c`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f2250384e48be6d27ec931d0741f676ef2c3c67faa27bd2ae847697abb7529`  
		Last Modified: Thu, 10 Jul 2025 21:46:36 GMT  
		Size: 4.1 MB (4056436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cd9e174e864c7fe109ee38dbf4e5fc5d6c7f36a3db9bd27e8a54d0f98aa582`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 2.1 MB (2094280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c4351344d68a9bf937082857f3e01847830fafedc207fb1035b88ca60d34a`  
		Last Modified: Thu, 10 Jul 2025 21:46:35 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.3` - unknown; unknown

```console
$ docker pull logstash@sha256:19af6f7cb4a04d0c8fe69621483333cc43bb0012ea6939c5a93557ca81cddd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16b8f6e53b79dbf1473f5d955095c28dacd824373c1d7f06b018c5e7f34f112`

```dockerfile
```

-	Layers:
	-	`sha256:7af9102c32b2e7746b0fe174b03c28d01b4ebf74d73cd37aead3b9fed36543b7`  
		Last Modified: Thu, 10 Jul 2025 23:03:28 GMT  
		Size: 3.7 MB (3655159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff269fa5793e6db299366c7df6b18139038ce65e3fba84a70d1dbaedc9e5474`  
		Last Modified: Thu, 10 Jul 2025 23:03:27 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f3d93e9669f046190a9a0e3227adb069e9a9c6afe0d9a90b1053246c6c345622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.4 MB (520394396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4634090da461db5c690c4cfc19d7a5f1b73a9791468fd4f994c1d0bf3e1c201`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Wed, 09 Jul 2025 09:09:21 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
WORKDIR /usr/share/logstash
# Wed, 09 Jul 2025 09:09:21 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 09 Jul 2025 09:09:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Jul 2025 09:09:21 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 09 Jul 2025 09:09:21 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 09 Jul 2025 09:09:21 GMT
USER 1000
# Wed, 09 Jul 2025 09:09:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 09 Jul 2025 09:09:21 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.3 org.opencontainers.image.version=8.18.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-06-17T14:04:51+00:00 org.opencontainers.image.created=2025-06-17T14:04:51+00:00
# Wed, 09 Jul 2025 09:09:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941129add2844ded7ed685065061890c3582c568194d370aec48c22948f5bf89`  
		Last Modified: Fri, 11 Jul 2025 01:29:48 GMT  
		Size: 47.6 MB (47634312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3715108e98b64afbb61b374d31349adb4642c875c1ebaa2b28b0b69751737`  
		Last Modified: Thu, 10 Jul 2025 22:15:09 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d930fe01cfda250925dc9b361952f13e2764ac3e1f2a23424e512b8e274317`  
		Last Modified: Fri, 11 Jul 2025 01:31:19 GMT  
		Size: 437.9 MB (437880052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb46669d27136a21b73f815bc8642c1561959a45cd10b610462d26e11e826f5b`  
		Last Modified: Thu, 10 Jul 2025 22:16:37 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda716fb97abf94d863e264c45ecf55f38528cd832540530fd6cefa0468ba934`  
		Last Modified: Thu, 10 Jul 2025 22:16:37 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ce7dc7da819a384253cab1afcf4f167b8ea2847b4ed6e4be6fd5217b7362f`  
		Last Modified: Thu, 10 Jul 2025 22:16:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d07aa0a62eb0dfa3c9c5112998dde91bc9c39561d0ce9d075528b13b53dff`  
		Last Modified: Thu, 10 Jul 2025 22:16:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548566273757ac26e4ad8d6e70a825f6e38da5760b96b9b700b190a034749896`  
		Last Modified: Thu, 10 Jul 2025 22:16:39 GMT  
		Size: 4.1 MB (4056431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943cdd76dfbef5a2e43d5db6cca5a1a6fe2c5143580cc1a2c070e59b75524a4e`  
		Last Modified: Thu, 10 Jul 2025 22:16:39 GMT  
		Size: 2.0 MB (1961678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041468d0dd1b529a9a2414c04de60eb5bd92741ad837a0c5d4a1bb94e72a50e4`  
		Last Modified: Thu, 10 Jul 2025 22:16:39 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.3` - unknown; unknown

```console
$ docker pull logstash@sha256:8482301e80cf26ef44b33d397ea17ed1525c414838b7f5b23a3507b2c5a7a9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dee036e15fb64e62e6809029d5bab6c0576c7a7a7ddceae3f150fb949ed98`

```dockerfile
```

-	Layers:
	-	`sha256:56d1f71288ac3e318cc7212890b68f0f45022c9d9ba694f92884072383245731`  
		Last Modified: Fri, 11 Jul 2025 00:53:37 GMT  
		Size: 3.7 MB (3655584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57b667e82f4e5034804b1b3eea62c5a7d478a15e066183b8617d2ad07f8b0e9`  
		Last Modified: Fri, 11 Jul 2025 00:53:37 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.3`

```console
$ docker pull logstash@sha256:b4f13f8da86025ab609d1019fb308e8da35bdbda52f710e28cfe146bc8bb4c93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.3` - linux; amd64

```console
$ docker pull logstash@sha256:516fc8259cabd035eb960fd3d5b9e1fc5b68ee95830efdd7fbd5bddae03c21d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.1 MB (484132694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bfbaf22c0f72ba28508e94167d1e2878592f0880602086506b2920757ac701`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL url="https://www.redhat.com"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.openshift.expose-services=""
# Mon, 30 Jun 2025 12:32:22 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 30 Jun 2025 12:32:22 GMT
ENV container oci
# Mon, 30 Jun 2025 12:32:22 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 30 Jun 2025 12:32:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 30 Jun 2025 12:32:23 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 12:32:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 30 Jun 2025 12:32:24 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Thu, 10 Jul 2025 16:17:21 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Jul 2025 16:17:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 16:17:21 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 10 Jul 2025 16:17:21 GMT
WORKDIR /usr/share
# Thu, 10 Jul 2025 16:17:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.3-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
WORKDIR /usr/share/logstash
# Thu, 10 Jul 2025 16:17:21 GMT
USER 1000
# Thu, 10 Jul 2025 16:17:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 10 Jul 2025 16:17:21 GMT
LABEL org.label-schema.build-date=2025-06-17T14:27:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-17T14:27:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 10 Jul 2025 16:17:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c3a7d5880784993e5a05598addad7f8ae85f443983c1815ae46c8baadf155`  
		Last Modified: Thu, 10 Jul 2025 21:46:26 GMT  
		Size: 5.0 MB (5021965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b4736aa4f83589232f1923c2a54c6daf4ea2eb628e9fb370d4768b80b8125b`  
		Last Modified: Fri, 11 Jul 2025 01:03:01 GMT  
		Size: 437.4 MB (437391235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190256ba046f8deca2951602b6c1164aafd7a90f2b3059e47f75f4d3094904ad`  
		Last Modified: Thu, 10 Jul 2025 21:46:26 GMT  
		Size: 2.1 MB (2065769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d931c47490282a3b92ccf61ba86667f018933f08732d1d5ab4c04f3bdb492`  
		Last Modified: Thu, 10 Jul 2025 21:46:26 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17044c484264db9367ed062dd3e9fd8df9d5cd7d3fe97bcd7f2c0b7d3caf7f`  
		Last Modified: Thu, 10 Jul 2025 21:46:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159da32acf80a905f4d5a96065d4f9a96741ca775b1745a4c9309da97dc0df5c`  
		Last Modified: Thu, 10 Jul 2025 21:46:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a65ca839febd1747cfb0372c7313b27915327ef5aafebde0a56fd52cbc6e97`  
		Last Modified: Thu, 10 Jul 2025 21:46:25 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.3` - unknown; unknown

```console
$ docker pull logstash@sha256:016d9d93890125502e6afb5c364d7f2d657792120a9afc4d52b7b3afb62791fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb12cdec1033469e966d7722f2874c01e2adb9e64793ecd251e9708b518ef7a`

```dockerfile
```

-	Layers:
	-	`sha256:3361169699b2762cd8ec817dd88f428bf1ed485be19b2fd00671d70b3c450e77`  
		Last Modified: Fri, 11 Jul 2025 00:53:41 GMT  
		Size: 2.1 MB (2139887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151e555d2c2f0021bfa86bad338ec7e82e9d636f7fd95f2e05271ed45366b449`  
		Last Modified: Fri, 11 Jul 2025 00:53:41 GMT  
		Size: 29.5 KB (29541 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c24da4a3fae44d78c559f112765f6e78b90aa5d9223efd81b55afeb5f84473ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480502575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103844454756d7124ce180a7553df794d834e02a340906366418bb770526846d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 30 Jun 2025 12:37:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 30 Jun 2025 12:37:08 GMT
ENV container oci
# Mon, 30 Jun 2025 12:37:09 GMT
COPY dir:4a26990fc6a982252bab47a280479ef21eaa9fb0686b5810bf75da5fc5af7d4f in /    
# Mon, 30 Jun 2025 12:37:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 30 Jun 2025 12:37:09 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 12:37:09 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Mon, 30 Jun 2025 12:37:10 GMT
LABEL "build-date"="2025-06-30T12:36:52" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Thu, 10 Jul 2025 16:17:21 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Jul 2025 16:17:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 16:17:21 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 10 Jul 2025 16:17:21 GMT
WORKDIR /usr/share
# Thu, 10 Jul 2025 16:17:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.3-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 16:17:21 GMT
WORKDIR /usr/share/logstash
# Thu, 10 Jul 2025 16:17:21 GMT
USER 1000
# Thu, 10 Jul 2025 16:17:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 10 Jul 2025 16:17:21 GMT
LABEL org.label-schema.build-date=2025-06-17T14:27:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-17T14:27:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 10 Jul 2025 16:17:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ffb6dfc9a5fd85e709e0a3428084894621f9e001746e51a54875b13ff103e464`  
		Last Modified: Mon, 30 Jun 2025 14:20:11 GMT  
		Size: 37.9 MB (37864356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b5c2086442974f3fcde9e38c1ecc5ec8fea4714d20c1c90cc87cb364331cb5`  
		Last Modified: Wed, 02 Jul 2025 19:01:41 GMT  
		Size: 5.0 MB (5024658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b9c6227dcf403a4a1ddcb5dc6dee6673932b4815ded06050dbb42b92e3795f`  
		Last Modified: Fri, 11 Jul 2025 01:31:41 GMT  
		Size: 435.7 MB (435672881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c7b1fcdb245d46e353d907e76ce12a16337b98eb82e24628805f386b9eb0f`  
		Last Modified: Thu, 10 Jul 2025 22:17:54 GMT  
		Size: 1.9 MB (1937773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411589535fc52a6245e4c1462e4682fc1b98f3704a71c52e81d10fd4e8e85941`  
		Last Modified: Thu, 10 Jul 2025 22:17:54 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9c8cf709ea2e52509177fcd7ff787ddbdd09c7459d11e7970b43d8c4d185f6`  
		Last Modified: Thu, 10 Jul 2025 22:17:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f356c23e2dca0e5ce36ad136063b9510ee4d30b3ade298ddfca3e5aa7b536a`  
		Last Modified: Thu, 10 Jul 2025 22:17:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7212deded55c5ec1ad853fd62b9b09c33af4ce7fa36575a9dd9a5318932f99`  
		Last Modified: Thu, 10 Jul 2025 22:17:54 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.3` - unknown; unknown

```console
$ docker pull logstash@sha256:ef3eaa1ae4f13c241f7dc7ec42fca1eb9df78cd7a155eae9a7f301e39214b94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96c91c82289bbc348caf7dbd18b1eb52c73fe56a8368536955a73fb1a5cc030`

```dockerfile
```

-	Layers:
	-	`sha256:ef3265347a0dd0d4bf0ff50a0b05dcdc137c22b5362c3bc8f9165f100ae21a55`  
		Last Modified: Fri, 11 Jul 2025 00:53:45 GMT  
		Size: 2.1 MB (2140459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52062a9eb331360b09077a2f49d97c38a656b07568a416f4273975d7bd11dd00`  
		Last Modified: Fri, 11 Jul 2025 00:53:46 GMT  
		Size: 29.7 KB (29658 bytes)  
		MIME: application/vnd.in-toto+json
