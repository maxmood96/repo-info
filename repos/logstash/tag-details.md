<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.5`](#logstash8185)
-	[`logstash:8.19.2`](#logstash8192)
-	[`logstash:9.0.5`](#logstash905)
-	[`logstash:9.1.2`](#logstash912)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:9220c09b68ec05850a3d30f92210f3f5eb9df6a91a1e9279bf4e0168674a9b78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:c1e71f88104d7f42019ff1e06c685539cd44d68b9473ebac128772648b45be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.7 MB (523720786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a6a010e3ff8c0f68b970cb905a5fb897c2114d5ac0813cb767b703cdb639d3`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6be6cd7cb47b69220bac933d5243e7756704af2b2955e9ceb8765b0e5e167`  
		Last Modified: Tue, 02 Sep 2025 00:28:12 GMT  
		Size: 47.1 MB (47145152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab034a4b19052699f44dd6414bceb2296c3399687045b61904574d961c978490`  
		Last Modified: Tue, 02 Sep 2025 00:28:08 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e975114f9edd779332d9bf31512ad443321bc36977a4bc007a5908201e5052f`  
		Last Modified: Tue, 02 Sep 2025 00:29:36 GMT  
		Size: 440.7 MB (440696363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d065116f006854464e6f707abbaf3ef2e16505e7daae4a8c104041519db2ef5`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd4231d24be059d34d7106c5fc4b98177fd27537d349c9d55122adeaba16119`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c4b62881286cbd524e411ef9400cfa5b51b6267b8b6f6e3858dde6980d2f`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10360c17a2afd327dc87bc7fb5e7a04b7431c5118673e4192f6dd3b5e3b91c4c`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771145a5c7721a968b056eb1592a04e7dc99e424f7b0b9f924d6e3f017535e23`  
		Last Modified: Tue, 02 Sep 2025 00:28:10 GMT  
		Size: 4.1 MB (4056207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e5973d33e5c2c0c0baa8eb47234388bee28c72fc486e3e728955acea61fc23`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 2.1 MB (2094102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615fc0fdaf9a8762374056aef23b942c6f6cd51c9f4b882f0fbdce7ae74edeaf`  
		Last Modified: Tue, 02 Sep 2025 00:28:09 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:b109dd282f7529742aadbd4db241832631209d358995013a5637d1f744af7998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228071b016d154fe1f265350b1e6397ae7f0b29f96baf914d9f39acd3406d0dd`

```dockerfile
```

-	Layers:
	-	`sha256:b30978a9435fdf389ded33e583e4d98993344cd7e98cc6bb5e0732466d8e283a`  
		Last Modified: Tue, 02 Sep 2025 00:53:19 GMT  
		Size: 3.7 MB (3657086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541aee585edf9042a2f6829a11716ce64e2c249dae84ca452fa3d346a959be38`  
		Last Modified: Tue, 02 Sep 2025 00:53:20 GMT  
		Size: 34.7 KB (34664 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bba7d7484adbe5d2520cfa5b2991c8e31cc479fcc278c6d6d127c01b3bc05c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.2 MB (522162856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66b9c38c6b2b70d6b0b18066cc19148e4c5e7024e1c668ebf7243d4e081b5b0`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6949fe861eda4b6c181435ae9de035109adfa17335435de30387fda0d887819`  
		Last Modified: Tue, 02 Sep 2025 02:18:54 GMT  
		Size: 48.3 MB (48297631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6e76fe45a68fb01fc3a97bfc9b127a4bb84c49741c5ccf85d319a907ce3bbb`  
		Last Modified: Tue, 02 Sep 2025 02:18:47 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e34266707e3cb512d37b1a860149b2dfd551820d09d0f6604922e3c7dbca06`  
		Last Modified: Tue, 02 Sep 2025 03:26:15 GMT  
		Size: 439.0 MB (438981254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8782f67ce86d82a9a9b34a66364177e0ce926341a1f77b8d4dd9d35ef70882af`  
		Last Modified: Tue, 02 Sep 2025 02:18:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7cc01222542a9f577df4e458f485a7af6edc2542a0c2eff6d10a44527ed9ba`  
		Last Modified: Tue, 02 Sep 2025 02:18:49 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61eb8d2559e883dd9d749c754fd41cc443e4f1b3163fcb03e985cfd89e2422a`  
		Last Modified: Tue, 02 Sep 2025 02:18:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a428a93d3d2672194e06a833252c07b3f197eb13892ab61cc3e79ef71eb61cd`  
		Last Modified: Tue, 02 Sep 2025 02:18:48 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f24afc0dc34b6862dd4c5db0bc9c58c779875cf01cd0683df1d0cdb312e05d1`  
		Last Modified: Tue, 02 Sep 2025 02:18:50 GMT  
		Size: 4.1 MB (4056208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d67606805585b395576ecde227db5d6f0ed119772aab24b08f01a95a48a97e2`  
		Last Modified: Tue, 02 Sep 2025 02:18:50 GMT  
		Size: 2.0 MB (1961623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9344fc676224902374312dd4253982cb1064a13f9626557b4c6fe2162d9a9f1`  
		Last Modified: Tue, 02 Sep 2025 02:18:50 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:be8cad653b2eb47d9f7bb16f44269cf0389808d96b42b61d58b7573ed18be49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba4cd2ce1b70faf1f527bd44999384076ec71cfeacfca3b1c7d6430237846b`

```dockerfile
```

-	Layers:
	-	`sha256:e965f6413abfcb4b000fd744d6dc26c17150ddb7b86195b1814f61c04b03c3e1`  
		Last Modified: Tue, 02 Sep 2025 03:53:20 GMT  
		Size: 3.7 MB (3657511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9b92ab82cd211d5ae8c8e79aacffb4fbfae9604ee3dd8c4597fbeec2c3dd96`  
		Last Modified: Tue, 02 Sep 2025 03:53:21 GMT  
		Size: 34.8 KB (34807 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.5`

```console
$ docker pull logstash@sha256:8b0184f4cab227fdff3fe07e5d0ef17455e1dbcec33c5bf861864c132aad3bea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.5` - linux; amd64

```console
$ docker pull logstash@sha256:7e56828cd9f5c231a40fedb9b30fe84a297e7b644531c3f687d7aa015a009ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.8 MB (523769772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6922cd9e61105c7414aed4bfaa1e5003855e2008171ee2f8f80d327cf09ede1c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:42:34 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.5 org.opencontainers.image.version=8.18.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:39:19+00:00 org.opencontainers.image.created=2025-08-06T09:39:19+00:00
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b62c5539cd8991fed94e261221a3ca899bb624db93736342ddff5727eea92d2`  
		Last Modified: Tue, 02 Sep 2025 00:56:05 GMT  
		Size: 47.1 MB (47145038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e874c1db79403347be55620f613213815eedca23bcc47d95f48e11bb25be4334`  
		Last Modified: Tue, 02 Sep 2025 00:56:06 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8c9593c96eb79bd27d4b76d26963b7928c78ba46fa9e97891fc8190f0b4f0`  
		Last Modified: Tue, 02 Sep 2025 00:56:42 GMT  
		Size: 440.7 MB (440745477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cf357aa8c6e69126a404f79611ae81d562ea3008208c8d1f80dd09d75449de`  
		Last Modified: Tue, 02 Sep 2025 00:56:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c49e6f725da78bd02eb2531eba7f0254b0824e97041131e225c771afbb49f0`  
		Last Modified: Tue, 02 Sep 2025 00:56:16 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b0527b8fef2778d1a934601e100cce27fc34bd9431990133e3aa368c821bd`  
		Last Modified: Tue, 02 Sep 2025 00:56:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a693287f7cd4b8e042f644736f8a2e8b285c96ced7a7b674ac93c9bd9df79`  
		Last Modified: Tue, 02 Sep 2025 00:56:17 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fbfd5bb05c56539668be3fe60e62257fd1055e650d8bb9e6d4ab9bfd3593e`  
		Last Modified: Tue, 02 Sep 2025 00:56:17 GMT  
		Size: 4.1 MB (4056203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5c98221dd72b74c7c6f7915e8154d78243c656a37496a9ff9eb272d954c23`  
		Last Modified: Tue, 02 Sep 2025 00:56:17 GMT  
		Size: 2.1 MB (2094099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5984cb65b910e1bb208f8085dd010be6577cf13002f09c6bbb07c23a58894a05`  
		Last Modified: Tue, 02 Sep 2025 00:56:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.5` - unknown; unknown

```console
$ docker pull logstash@sha256:661c162c3946f70e6f95b1aba186b9a8e6a46af3279c4cde8f12668843e8b93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b39579390540f0052e9451bcdba8abf2b423903b7696e17b9bd493e1355b6de`

```dockerfile
```

-	Layers:
	-	`sha256:ff7381a53dc857647e03736237c13e13af621a69755625b69115d67734b8f0f2`  
		Last Modified: Tue, 02 Sep 2025 00:53:24 GMT  
		Size: 3.7 MB (3657642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4224b23b605b54649d43f4ae25c8b9d3491548db570966aa56c20272a9b8db`  
		Last Modified: Tue, 02 Sep 2025 00:53:25 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:9e6e18843a2b11b23131333aa32509128c583182913e4d16d15177559e1f58f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.2 MB (522208423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880df45ed7fb88ed338a2e98f19c4c1ec5dab16bed28b0aa3cd5d96d0ad5328`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:42:34 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.5 org.opencontainers.image.version=8.18.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:39:19+00:00 org.opencontainers.image.created=2025-08-06T09:39:19+00:00
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6949fe861eda4b6c181435ae9de035109adfa17335435de30387fda0d887819`  
		Last Modified: Tue, 02 Sep 2025 02:18:54 GMT  
		Size: 48.3 MB (48297631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6e76fe45a68fb01fc3a97bfc9b127a4bb84c49741c5ccf85d319a907ce3bbb`  
		Last Modified: Tue, 02 Sep 2025 02:18:47 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891f4dc0e403437cca5d3c9c89c55eacf0011baf4e4bfbf8aaaa434263ea08ac`  
		Last Modified: Tue, 02 Sep 2025 04:02:50 GMT  
		Size: 439.0 MB (439026812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8ef6a76931457ea5bb5418676adbb219fc9b0fcb02f64f7bc6e1f0c04c8ad`  
		Last Modified: Tue, 02 Sep 2025 02:20:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6a51be04f9640171657a62eb51318a84baac2e187ba33b6587d26fc7a8f870`  
		Last Modified: Tue, 02 Sep 2025 02:20:06 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f581a3c98d7166bb9ad08fe9c25dc07148bd5df30448ecdae93a4e3f0f7c9b`  
		Last Modified: Tue, 02 Sep 2025 02:20:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cc18d748f6faad95a802e21fbbc3b59ad330b119f59571ee0322060054b569`  
		Last Modified: Tue, 02 Sep 2025 02:20:06 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0edcee0cb316f19800a754eb3ce6815b4789d59f5a32b31df1674b4e3b89ed`  
		Last Modified: Tue, 02 Sep 2025 02:20:07 GMT  
		Size: 4.1 MB (4056209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26677f7d407d197d84a5bad53f4e8ba0d4e3c352fb96d67edca4a9da2b2eb9b5`  
		Last Modified: Tue, 02 Sep 2025 02:20:08 GMT  
		Size: 2.0 MB (1961626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77647f887503e946855f74f91fdbd2be9348e33ecd5ecf817e6b8582115bb82b`  
		Last Modified: Tue, 02 Sep 2025 02:20:07 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.5` - unknown; unknown

```console
$ docker pull logstash@sha256:ddad3df4c73eff65d9e6c717b776a4a6b60b97fdb3f03ac83a1150b065990983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9b4c8887e2ee19bebff5ad04e2a7b4bfdad4157c84063ad2bf9e4bbf2e6791`

```dockerfile
```

-	Layers:
	-	`sha256:3429c1c4ffdce6b28cc84e0b6adb4a7a902e3e249221b3a38055c24b111743a5`  
		Last Modified: Tue, 02 Sep 2025 03:53:25 GMT  
		Size: 3.7 MB (3658067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3d9c96868f1f8d5d3399d101e13ea1d984e6d3e1f41fce4de2465aff6d9b1e`  
		Last Modified: Tue, 02 Sep 2025 03:53:26 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.2`

```console
$ docker pull logstash@sha256:be0837d9740b582a9f04eae78846759f5ded5aa67e037a6c9359ba733e8bfacd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.2` - linux; amd64

```console
$ docker pull logstash@sha256:a90b612700ebe10f5a339a9eb14761a49ef64b0aa09a4893fe73fd3a3d8e6f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.1 MB (524126073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356f424e504e2ec270bef2648dcc2d5ea90a7720268ab005db22a705c12ed1b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 11:48:35 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.2 org.opencontainers.image.version=8.19.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-07T09:55:51+00:00 org.opencontainers.image.created=2025-08-07T09:55:51+00:00
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975c50cae56cc49052bf5e4c1627219dcb67787909d56b411e7c9be5430e8c9`  
		Last Modified: Tue, 02 Sep 2025 00:29:18 GMT  
		Size: 47.1 MB (47145149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1392faa80aa551abee3689040cf1e60b01cdff08bef5d00a152df22b69985395`  
		Last Modified: Tue, 02 Sep 2025 00:29:09 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbe1b103acb5bab358bfc15e9c13adfa87293ed7c0f77bf99de9bd0949d6145`  
		Last Modified: Tue, 02 Sep 2025 02:08:31 GMT  
		Size: 441.1 MB (441101657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b77ed129e029f8a008af98f10d082715a8b7d3b92bc544c7fea70bc8bdbc410`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00da7366f42e35f98c84f9b06f432d4a205b19f18d95b688cf124fba2aa0fe65`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40fb9f68150d420d245b9b0c59acc177a47e01c56ca8d3fa380ee0cf5120f82`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f9037cd1766a7c2c1f38cdea70159d97fbf828b16df0f4cb6dca06d6c3a03`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea5770e0efd420455fed1caeafba414b9eaf19e79dfc304d1fe9e2dc5f0431d`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 4.1 MB (4056205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b144c10ae539f2658fa37f6ee970d76cb63ab2ffb686392c7b2333817ef5b0`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 2.1 MB (2094103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baaf1d6e0a9b7d137fe9fb92ad4042bfd640e34d8b686ddc575eea682dbee21`  
		Last Modified: Tue, 02 Sep 2025 00:29:10 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b08b11ca1156b3b6df5c1acc3846b816c45240014078509f35dfcdbf7c1a130d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60786dc31eb846346741c0817f19858528470b01c347a931c198e59bcb36e5b`

```dockerfile
```

-	Layers:
	-	`sha256:87eabf60f316ddbaf62a66c71cd3a6ea70f9166ed63c1c718d0b178e5672b4fe`  
		Last Modified: Tue, 02 Sep 2025 00:53:30 GMT  
		Size: 3.7 MB (3653198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738d20e732b10f8f18b1cbfa693f86081fd3f9ddb3de84347a899bc834783204`  
		Last Modified: Tue, 02 Sep 2025 00:53:31 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:74dae010f752c8c5d6dbf690723bfd1e9a5aaa8715c931d3401bf2df299566f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.6 MB (522565933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaaeeb7338de3963e3398cea0fa256bb4f0c15670ba0f114e5091e3ff659a498`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 11:48:35 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.2 org.opencontainers.image.version=8.19.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-07T09:55:51+00:00 org.opencontainers.image.created=2025-08-07T09:55:51+00:00
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6949fe861eda4b6c181435ae9de035109adfa17335435de30387fda0d887819`  
		Last Modified: Tue, 02 Sep 2025 02:18:54 GMT  
		Size: 48.3 MB (48297631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6e76fe45a68fb01fc3a97bfc9b127a4bb84c49741c5ccf85d319a907ce3bbb`  
		Last Modified: Tue, 02 Sep 2025 02:18:47 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee988f46efd17f58e33af34af314c4d68ddc1c96184faa23ed1840f2b9be82b3`  
		Last Modified: Tue, 02 Sep 2025 04:01:50 GMT  
		Size: 439.4 MB (439384329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b5fcced0cf3eccc56a293e2bb6cf7d881039ad4421b3c89fc44a261c0e8d1f`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672715ff14c166c081f87c8401c756a2832bcbf8f2748f7f19383a960aa0ace1`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739d4e02e17c9c683624db6790b07c5ed126aa826337333df9e003dcca904839`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b2a224a20f37e0ab79527ed65b4983b6d8e236940e807513ac7a94cabdc13`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc322ea1fd9da519df3cb147ce7eb7e80f3f43a70d4890749969807aabe8dd8`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 4.1 MB (4056209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06c6b13635acc321438dd66cea6a0e25696a83dee20eb9b4f99f8356bcce2dd`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 2.0 MB (1961626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3159b97c954d7a4f1ba036655d84f674f0d12f3820ae046374fe794a274d13b`  
		Last Modified: Tue, 02 Sep 2025 02:21:38 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.2` - unknown; unknown

```console
$ docker pull logstash@sha256:38684d1373ff69b484c8df72f590cf2b149120842513e499d664ca9e39629a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26514fc7a9e7bc57a6b2656cc6336c55ddf3e096eb4b3f4cfd58f450e85d07c6`

```dockerfile
```

-	Layers:
	-	`sha256:0d35e8e6cc394b780c7c5a54b82d3ea44418b43407978e59304fed01914db954`  
		Last Modified: Tue, 02 Sep 2025 03:53:31 GMT  
		Size: 3.7 MB (3653623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca50ffd405cd35d6d59fa6c1b190c3df29aaf0542eabdcd7fc9ff44a5455d92`  
		Last Modified: Tue, 02 Sep 2025 03:53:32 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.5`

```console
$ docker pull logstash@sha256:cd25e74fbbf50261efd63c2843d21bc96630a83102f6459681a2140d5d8294c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.5` - linux; amd64

```console
$ docker pull logstash@sha256:ee366ddbeba93b3b6d911eb0c5b32ce97092bcaf14dad62da18c828ec0ce27c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484705985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15259721136a658e6e414bc3ea231dffbf0c3d2fe6275aed0a04f610e4a3b1fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T10:22:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T10:22:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 08:42:57 GMT
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
	-	`sha256:d3a33b99528d66c4423958cff5c8fbc2e34df06814b68eb2ca76c5bba90ef01f`  
		Last Modified: Thu, 21 Aug 2025 18:57:52 GMT  
		Size: 5.0 MB (5018698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39509f3b75786c4cf757c0eca02ca58750bf28a514505f04eca43e5540f8a375`  
		Last Modified: Fri, 22 Aug 2025 02:48:04 GMT  
		Size: 438.0 MB (437971029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccc46fbf7f0d8bae89a67bf52f01aa3c0f96ea5ab93365cf34e83957d8e9f9`  
		Last Modified: Thu, 21 Aug 2025 18:57:46 GMT  
		Size: 2.1 MB (2066060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57af7edcdb55e7eb1acafa11933c3a5e55bbd03f7c047a882869542fd758ccb9`  
		Last Modified: Thu, 21 Aug 2025 18:57:51 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c8ec3a8ab8329471eabdceb8a17981efc7d334d239196fb4998ddcd90f6df9`  
		Last Modified: Thu, 21 Aug 2025 18:57:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c32fae70a7f2f205014314f4ee0edb05babe281f6121dc4e35c14b7058dfc`  
		Last Modified: Thu, 21 Aug 2025 18:57:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e5ef8336a6382cfefcd2fbf9d69b514c6e6e497156cd55bf78faf6df6a256a`  
		Last Modified: Thu, 21 Aug 2025 18:57:53 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.5` - unknown; unknown

```console
$ docker pull logstash@sha256:27bc4a266989ca51fa452b99ce5921828221308e543b7ad3a5dc5a401d5798ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74f9dfa313a6ade4b99f38d6529fc95d2aeb1f42fc8f306804dc05ef02f2c5`

```dockerfile
```

-	Layers:
	-	`sha256:c0aa5505517408967c73ab91558b23a420f2eb8f1a694e678842325c774f5a53`  
		Last Modified: Thu, 21 Aug 2025 22:02:16 GMT  
		Size: 2.1 MB (2142409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5826b6a3da8a03bd7941bd4a8e5b32ee5fc9df9a672ad006aa3780c84d977c`  
		Last Modified: Thu, 21 Aug 2025 22:02:17 GMT  
		Size: 29.3 KB (29314 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2e6415b9b913ecaf5cb1177bb9f57d3ec609d6af1d83ccaf7a9d3af80e3f6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.1 MB (481079623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e7824304c7790e820114347665b9f5de7f7abcfad476d078e3312f0dee29f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T10:22:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T10:22:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 08:42:57 GMT
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
	-	`sha256:1da2c2a1254adb658a53c42c7feda5c2cc238dbc04c4ed19139b1cd573483c30`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 5.0 MB (5023624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3fa2a50693889f9057eae63eaa3aff4447b787f186d782a4144fe5ee5f8599`  
		Last Modified: Fri, 22 Aug 2025 08:10:02 GMT  
		Size: 436.3 MB (436255875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5044148a7ff6298df09356b99e907a19f1203d158788e7db8445b1cdbf8cc39a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.9 MB (1937642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b860b458f67f936bf13ce98ba9733166e2b3b7e2c8eabd2db84e6991f09beba5`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcc18f7bef5f8d4c3f4822d5c2ec59e7d5615d386ad933b7ea302c0202d3d3a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f708f0505e7fa94f99d3426fb2a32f147f40fdaf866e86b93b2b37e759f53`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287fa818df8491fb60d3c143ad2bd9ebf3abcfa653c195e9ff67f5875419dddd`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.5` - unknown; unknown

```console
$ docker pull logstash@sha256:fb385c18687864c307c61a91fc3c51dbc044dab250a0b638f61d57caa776be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1897d1eefc57890f9b844dd7992cf95eac06479735fb34040eaa13fde9cb1dc7`

```dockerfile
```

-	Layers:
	-	`sha256:72fa51bd18261a2a727f528562fa032c161250fb266ceb263ff71e40aa60dc06`  
		Last Modified: Thu, 21 Aug 2025 22:02:22 GMT  
		Size: 2.1 MB (2142981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144d21b8043cd7e8595cc108edee23f520e4714cf5b2f1d89a214e1c7fef4c54`  
		Last Modified: Thu, 21 Aug 2025 22:02:23 GMT  
		Size: 29.4 KB (29425 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.2`

```console
$ docker pull logstash@sha256:33eae14f0867ad20d6e4b615027f3ca41c74fdf58aef41fc67c9ccda9670794f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.2` - linux; amd64

```console
$ docker pull logstash@sha256:d019f567db5939953a4dffc47bde8f2337bd479c7ab8cfd4bb0997229de0a32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476770924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed419197c884f8b72f84744e10cb8f502e966acd09f111b1f14841474436f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-07T09:34:04+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-07T09:34:04+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 11:49:08 GMT
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
	-	`sha256:e480078bffc6f59514041812029dd7a013d7e474cc5ac6f6fc2cff7b7e5498ba`  
		Last Modified: Thu, 21 Aug 2025 18:57:47 GMT  
		Size: 5.0 MB (5018753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57bccc655f8167ea6209a69716095bd9507e30e256e12fefd18045e7411730f`  
		Last Modified: Thu, 21 Aug 2025 22:18:12 GMT  
		Size: 430.0 MB (430035922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62796d04558dba7c22926b460745aab2ed01dfc96a1ecd980b859c6ae2c2a65a`  
		Last Modified: Thu, 21 Aug 2025 18:57:46 GMT  
		Size: 2.1 MB (2066061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d397328904440b5cfb3c9068c957e3b8b00975531849250dea9a9e55037079e9`  
		Last Modified: Thu, 21 Aug 2025 18:57:49 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c252008e23ee51a298e4e50e8eb9cd700839d0f4c681791094105c9c9f97ce1`  
		Last Modified: Thu, 21 Aug 2025 18:57:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860105d5ef3ee98067174a1d8339f860a96572995630b70aab681ecd23251b3f`  
		Last Modified: Thu, 21 Aug 2025 18:57:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa40c56ac1120dd9781d2cec38ce362afdfe0e54475c234cbb753c64d5128cf`  
		Last Modified: Thu, 21 Aug 2025 18:57:44 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.2` - unknown; unknown

```console
$ docker pull logstash@sha256:4bebf1ca37387313a36e4f9672a70d0204555b47a203ea17daefcb0fb73793bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2890ca415b9c295d2edc9b8a5d478ce9b85d5bf1e22214fa63c3cd16f09dc32a`

```dockerfile
```

-	Layers:
	-	`sha256:2b4d3fbb87e955c52fdf6e6c7af86ba6301831acd90df6204c1d0fb0135b8811`  
		Last Modified: Thu, 21 Aug 2025 22:02:36 GMT  
		Size: 2.1 MB (2075932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f4db275b71b60a3aca6bbb639ac710160a1b9d8a14212022e26d1340d3fe9a`  
		Last Modified: Thu, 21 Aug 2025 22:02:37 GMT  
		Size: 29.3 KB (29314 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e3350ed24fcc93bd02803b39fe92e7b16547121b9456b8668c881abf8826fd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.2 MB (473153613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ded9e6ff70877fbe822c6dcae4d7a74abe55c3a212b0887907d106213a52d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-07T09:34:04+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-07T09:34:04+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 Aug 2025 11:49:08 GMT
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
	-	`sha256:1da2c2a1254adb658a53c42c7feda5c2cc238dbc04c4ed19139b1cd573483c30`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 5.0 MB (5023624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c40f6acafd05f448f81897163954c7a03f7aa3dff88c8b39b27b295eabfd3c`  
		Last Modified: Fri, 22 Aug 2025 02:33:26 GMT  
		Size: 428.3 MB (428329881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1aa71cecc8c01e7aa1ee9e899caa9e4756c7d704cb3782ee35f47cec71aa6e`  
		Last Modified: Thu, 21 Aug 2025 19:31:10 GMT  
		Size: 1.9 MB (1937628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c9ae81c6b85ae58b9903f13ea2ae45369183762f45be916d5b1196a828197`  
		Last Modified: Thu, 21 Aug 2025 19:31:11 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3476f1b4c4d97e05599ebc32950b65eb0c12de15ad93ffa5d588efeafc7522`  
		Last Modified: Thu, 21 Aug 2025 19:31:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dccb625a129b0d4d4fc373a1b67daaa7d9efd802c0f330b77d30fea3bdc502`  
		Last Modified: Thu, 21 Aug 2025 19:31:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2a7ac76d40355b6904cd0dc57c27968928c45e56fac8a127d7cf083458487f`  
		Last Modified: Thu, 21 Aug 2025 19:31:03 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.2` - unknown; unknown

```console
$ docker pull logstash@sha256:879ddb488ddee1fceaaab6814682f9c318786e4d2a482f200588a7b14588883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0912996f0068c9021138f8179a86e6d0818a3d3a5c8078f1b3f41569efc3d586`

```dockerfile
```

-	Layers:
	-	`sha256:1d7b3de91e18d61533dfe2c0b945ea8651ad212ea28753de10bd4e2370857edd`  
		Last Modified: Thu, 21 Aug 2025 22:02:42 GMT  
		Size: 2.1 MB (2076504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5195a2f01d30b5f508f1cd6717af3ce1593b4d3cb10dd40392a1cbf638bb248c`  
		Last Modified: Thu, 21 Aug 2025 22:02:43 GMT  
		Size: 29.4 KB (29426 bytes)  
		MIME: application/vnd.in-toto+json
