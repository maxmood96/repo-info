<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.6`](#logstash8186)
-	[`logstash:8.19.3`](#logstash8193)
-	[`logstash:9.0.6`](#logstash906)
-	[`logstash:9.1.3`](#logstash913)

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

## `logstash:8.18.6`

```console
$ docker pull logstash@sha256:66b775f6156685bdba0cb15466d2b1b07e20ba9b1c8306a9bb498b48365a0eba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.6` - linux; amd64

```console
$ docker pull logstash@sha256:baf10a159bb4aa4286b1201bbaaf80bf55ab8e4e3a50981d47d42ac4f05c1eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.8 MB (523751802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f066e11b4ba22642892f1fbcc31722633c7ce9569f55de16bcc983b4e59f275d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 Aug 2025 08:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.6 org.opencontainers.image.version=8.18.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-25T16:50:37+00:00 org.opencontainers.image.created=2025-08-25T16:50:37+00:00
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8223fce5cd3235ff9626e2db76c2a6ec312d09d9e5d64daefdd0757bd2889681`  
		Last Modified: Tue, 02 Sep 2025 17:27:54 GMT  
		Size: 47.2 MB (47193487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c17aba681d863256dee94e3c2714f3e39497a0df9732303e3fe466cd71e0d53`  
		Last Modified: Tue, 02 Sep 2025 17:27:46 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e174f3b425bf3fa61507660a838c0d1faab644b268427f18d423f38122d4e8d0`  
		Last Modified: Tue, 02 Sep 2025 19:07:13 GMT  
		Size: 440.7 MB (440746882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de46cc28033709a457102b8a91efe229254d54e25b50d74ea10a86ea65a72c20`  
		Last Modified: Tue, 02 Sep 2025 17:27:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945ec0a8da2f42704d85d6d8a2ae4d307731a69a6abe571dd8bc18c0eef629db`  
		Last Modified: Tue, 02 Sep 2025 17:27:42 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2825fc321f8707739f3e705a532c689c8378dec82dd9d358191bb4442aa08b`  
		Last Modified: Tue, 02 Sep 2025 17:27:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20b893c28134fc046bb9e2e99e33d5350dcc4c90bd9b9271460fb460ac1ca26`  
		Last Modified: Tue, 02 Sep 2025 17:27:42 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703f0eb37c8ffb2250e7b97c627b106b5d7296952ee8d0fc8c01e3e4b16aaed`  
		Last Modified: Tue, 02 Sep 2025 17:27:45 GMT  
		Size: 4.0 MB (4004277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e862dbf3c2572aa28657241ed126aaaef15b4fc28aaf60bf18fe52e4493d0`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 2.1 MB (2078192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed781e8a5ca239ae7fb47bca89fe66ffa218fb09120633889e7d015f4825f1a2`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.6` - unknown; unknown

```console
$ docker pull logstash@sha256:68b4580ff72272718872705b8e41d6ac55f99cf88a52a66f1862553483543d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36ed34f30142615ae94ab461fa540aa6e674131745d4f42ee3ca6d40972af11`

```dockerfile
```

-	Layers:
	-	`sha256:6e7674992b9e0f00af87ec2f1fe73b10ed7a91ba367dcfc8afbd458623d58ea9`  
		Last Modified: Tue, 02 Sep 2025 18:53:22 GMT  
		Size: 3.7 MB (3657642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dced39ee3b87c53da2b3b8ddfb676f8c14a585251a36d7941332dfecc4aa5b08`  
		Last Modified: Tue, 02 Sep 2025 18:53:23 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c1d2c8e90b1b0bf3e7c8695e7b7f587cb5dd89f247b98e7b9779d3b2d26772c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522120069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031572faf372c3a16f3853c38bec5eeb86490429ce7442c6b00703f36ff94203`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/logstash
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 Aug 2025 08:37:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.6 org.opencontainers.image.version=8.18.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-25T16:50:37+00:00 org.opencontainers.image.created=2025-08-25T16:50:37+00:00
# Thu, 28 Aug 2025 08:37:13 GMT
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
	-	`sha256:f897d3f9a92c248acd736be69aa8348d0db9d991f4a4ad10ffafea6727565cde`  
		Last Modified: Wed, 03 Sep 2025 02:28:41 GMT  
		Size: 439.0 MB (439026591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca7ac58707a8e977bc148127184d6844e36039ce8e7e6cd21d1c04c6f281e2`  
		Last Modified: Tue, 02 Sep 2025 18:14:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176dd07af0b82e4c23a8f6fd6e259ba3cf6ad243441b4beb0c03ed7e0309360`  
		Last Modified: Tue, 02 Sep 2025 18:14:52 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f4fafc979c987859f9705702067ac6c4614d4f79ad4258f00f9d7cd693f4c1`  
		Last Modified: Tue, 02 Sep 2025 18:14:52 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98237f358031c5ccd1f2e371a248274a9c9131fcb38d0febcba998d18391a32b`  
		Last Modified: Tue, 02 Sep 2025 18:14:52 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69c272d0c680a69506d20bef5ae397ecedec7c8fd7e58472449594f13c691`  
		Last Modified: Tue, 02 Sep 2025 18:14:55 GMT  
		Size: 4.0 MB (4004279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2217b882a017f9e10457954ef8757acf521f16f4412c9ca768836e4e236f13`  
		Last Modified: Tue, 02 Sep 2025 18:14:53 GMT  
		Size: 1.9 MB (1925426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f99f8fab98edf16b97b721a1ad3681fbc1a20837a44329491510b07380941`  
		Last Modified: Tue, 02 Sep 2025 18:14:52 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.6` - unknown; unknown

```console
$ docker pull logstash@sha256:118e2a7ece5995ae3e8de4c95eba405bd4896274c1853cca3a3a36ce275eef1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35523194b72d9bc7e55bc200302d5e8607090f2c13b5472478c056a00e0d0213`

```dockerfile
```

-	Layers:
	-	`sha256:55de1821bdb42fa6bacd85d5b85557b1f53f7a4c05e099fc1602dd7f591c8491`  
		Last Modified: Tue, 02 Sep 2025 21:53:22 GMT  
		Size: 3.7 MB (3658067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af802ce704b8b8081050db8c9af7ac6f0d8edd5a30715c33d302d7449e05a3df`  
		Last Modified: Tue, 02 Sep 2025 21:53:23 GMT  
		Size: 34.8 KB (34794 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.3`

```console
$ docker pull logstash@sha256:989cac34b302164ecc678a3090b2fa663161f709765c46cee05070caf3a9bb39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.3` - linux; amd64

```console
$ docker pull logstash@sha256:809a9b0d131c047a46470f246b1949f18e1bda530020653704e5236ef311cd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.1 MB (524109842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed58f89241876bec543314fa0435dd20c9b186069de4f26cf20767fbda31caa5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb755b0c9c36dd7d670c677e84e5256250e0b2597eb517cebde37e292834378`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 47.2 MB (47193513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1440ef870018ca3312122463d14383dcdc40ca713c7583cb43b3230c89e86317`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5234e0288d1037514d1f0b242401ed1c695bddf7a606faf2a7f16d7d142c6982`  
		Last Modified: Tue, 02 Sep 2025 18:57:43 GMT  
		Size: 441.1 MB (441104888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25c4b666e77994488cda7c0717096ad456860d77fa9f2d918ae7983e5b6e964`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568ef353123d76ac597d5e96e7da2c0404dfe294cf9dbb7b0a79efe5c3f0df6`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d91925ced8e2912afb3f533fd018e309f276c47f8bede34c553a543c287d2`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb4327c8052c7e079118db53bf276f29ebc938832ed29b6998b10ceb570abf2`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c91e5e65640c6b087b1212f1938c71f482e02963596d0126ab6ab9ce161be1`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 4.0 MB (4004278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b45a5e0e40e25aa150665a2136972e0b4d6da450c796dd8419354b417d8fc8`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 2.1 MB (2078192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28246ba0f9c914da51ab3747ab6bb56cfc6631ce38b597b7f00889ed8e345361`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.3` - unknown; unknown

```console
$ docker pull logstash@sha256:e213074fade6491178e8941ac24bf292284beba30963b26319e21e3da6e59824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057a2146cb0dbf2cd866d09bce9c97286da340005db84039ecf4ca54209bd0cb`

```dockerfile
```

-	Layers:
	-	`sha256:8bf5d504a60b567edcb8d38742cde3a2f2904f825df1c9d31957a911d1e025be`  
		Last Modified: Tue, 02 Sep 2025 18:53:25 GMT  
		Size: 3.7 MB (3653198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686a909231f9477e4f9eb7b3c8332f704eb11fa7ef810c3eff7a1a83024c7107`  
		Last Modified: Tue, 02 Sep 2025 18:53:26 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:36d1687b8feb5248880f9ca0d84fbb180b3d9467aa684cca4fb3980b6f66ab9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.5 MB (522479306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed08d21a0866cd5619c7086e49135924bcc5488cf890ea21f7c06775c25280ad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:a09b224f9fc5262fbcd1fd49644057ec4d40048c3874b57ff9e27dac8ec67ad9`  
		Last Modified: Wed, 03 Sep 2025 02:26:11 GMT  
		Size: 439.4 MB (439385829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e6b94012ba48a5f44f076fe764eeeac139aa7cb00a618e2976ff814b40dfa`  
		Last Modified: Tue, 02 Sep 2025 18:16:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c4f313590d069cc69905ee124608416f03d8f5fccc04bef6b12754b561bbdd`  
		Last Modified: Tue, 02 Sep 2025 18:16:47 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a8e30d7f5bdb10b2959fed9ce141e21d7671db786d9b22bf75629e2ab46d21`  
		Last Modified: Tue, 02 Sep 2025 18:16:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7960c3fa59ff8af15b5d0db7a62d43e26743b869a48a6f2ada3d9f3dd451c6f`  
		Last Modified: Tue, 02 Sep 2025 18:16:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c5ea92f2c653810aa17359bb2a3de7374f10a42576354c42aa628a485ab837`  
		Last Modified: Tue, 02 Sep 2025 18:16:49 GMT  
		Size: 4.0 MB (4004275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a887f386eb2eb6268432f1031ee0e16fcb973f1342c0aedbb6911415baa706a`  
		Last Modified: Tue, 02 Sep 2025 18:16:49 GMT  
		Size: 1.9 MB (1925427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694a2e6e8021f865804413d771cab70919642a5affa456f02a6382e77f9d343`  
		Last Modified: Tue, 02 Sep 2025 18:16:49 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.3` - unknown; unknown

```console
$ docker pull logstash@sha256:43939f91aabd59ab44a6cfa7f76ef9c0564a3de4099fa57125316731f26e0013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2207f49423400ce4df9b94cd673898e6c9a0ebb428e1531ddda73b22db3ecefe`

```dockerfile
```

-	Layers:
	-	`sha256:4fbffcd94a4062c3d721679075c9b8de1be3e46134604bc36de0c305de993dea`  
		Last Modified: Tue, 02 Sep 2025 21:53:27 GMT  
		Size: 3.7 MB (3653623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0bd5637ada3f1db0496e34f8e2227ed18a72a7c3f233dfb7419e0aa3faff9ed`  
		Last Modified: Tue, 02 Sep 2025 21:53:28 GMT  
		Size: 34.8 KB (34798 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.6`

```console
$ docker pull logstash@sha256:681c5420252b2d18458e972e25880fd9f2fbc8328ea0b4f7a443574806bd8df0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.6` - linux; amd64

```console
$ docker pull logstash@sha256:bbd8c7199358c06c5550a5002b4cc5b0299249cf7a822a3d51db18bdaac575a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484718524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac208fb29e40d9d4c36229d8cced05611e8cd6925a6f0c21981b75f1996a87b7`
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
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-20T01:17:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-20T01:17:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Sep 2025 11:31:20 GMT
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
	-	`sha256:e3f5a073c218ca9baf3314b68ea4e2080a9710a700693c017737146f4537ddd6`  
		Last Modified: Tue, 09 Sep 2025 01:02:28 GMT  
		Size: 5.0 MB (5018720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75bf9c0fefa29bd834af5d50a288c35f1519e2d7380b2ce68925a2e85153fe`  
		Last Modified: Tue, 09 Sep 2025 01:02:52 GMT  
		Size: 438.0 MB (437971428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0196086f8121ed5a7dffe1c26928a83f96244a3c65f3174fce2325e0da85ddc4`  
		Last Modified: Mon, 08 Sep 2025 23:27:54 GMT  
		Size: 2.1 MB (2078183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b8fe0f3eb02a2fd4cfa5f16e6357fb0d5b7d61d349a7093690061ef08b5f9c`  
		Last Modified: Mon, 08 Sep 2025 23:27:53 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c53cc488a70cc905c8a17446fdbbd51de226332531d33115347b27fd7635a`  
		Last Modified: Mon, 08 Sep 2025 23:27:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a393e3a9db245521a6b9cf56fb9383377dc9c3592ab59b6a11c9ea5bd0f3c7a`  
		Last Modified: Mon, 08 Sep 2025 23:27:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b856e1e11a1f48befca7779d9352708102e77e8d3a3ffb5da9621fb58250ed`  
		Last Modified: Mon, 08 Sep 2025 23:27:53 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.6` - unknown; unknown

```console
$ docker pull logstash@sha256:62227881e32fb4748ab50d3e8a4c1900a2cb7eff2eb42054373cf164eec1ba83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd24b5cb0926fe0646bf254b0bc7c2151df529f1bd2da20ed372eaed4e76e0ab`

```dockerfile
```

-	Layers:
	-	`sha256:198822694fa3095bda959178cfe0d36d8c9ff44cc897783003d428cc9988b340`  
		Last Modified: Tue, 09 Sep 2025 00:53:20 GMT  
		Size: 2.1 MB (2142407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9661db2fb3d3aa922dae505d31306df3264426bda5b0b31e1ac744a84f91f7e`  
		Last Modified: Tue, 09 Sep 2025 00:53:22 GMT  
		Size: 29.5 KB (29537 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:37d8b41540c62dbbff1795b9760bf62b0f59e2210205e2ce293076b012666e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.1 MB (481068558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449cec389cc3fb0aacb1ee89949a0dbf2e92640681d84aa554c78a28e8b9583f`
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
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-20T01:17:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-20T01:17:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Sep 2025 11:31:20 GMT
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
	-	`sha256:5ee7a736afa6eef6c43e8707a8e46b665e559825eda66a8ef89e175cde16702f`  
		Last Modified: Tue, 09 Sep 2025 04:38:20 GMT  
		Size: 5.0 MB (5023600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8470eee9bc9f382b66dcb0f9f2a97c8ae012dc074cedcf3300be8a33d32c0c`  
		Last Modified: Tue, 09 Sep 2025 04:39:21 GMT  
		Size: 436.3 MB (436256055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a882c1da46fd0dd48a6353122da9e9362b7cb6096567eedb79e4e5779af1a43`  
		Last Modified: Tue, 09 Sep 2025 03:57:53 GMT  
		Size: 1.9 MB (1926415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc28973a6ed14d558cc91e1def64ea56c11bd9b2c1b80a656869b1977dc8dbe0`  
		Last Modified: Tue, 09 Sep 2025 03:57:51 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c7bb2e0329ea0dc8c0ae76d0735a96c21a27b673a479e8d85d576a681e1b00`  
		Last Modified: Tue, 09 Sep 2025 03:57:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02834e19b1dd50dc15ada9ef4ff18e3dd5aa4e6ee40b0a53330ee64500899e0`  
		Last Modified: Tue, 09 Sep 2025 03:57:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d6be0fd4b177f0031dc328fa1506c610df4e7decdbf8d49d9dc8f92025c0db`  
		Last Modified: Tue, 09 Sep 2025 03:57:52 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.6` - unknown; unknown

```console
$ docker pull logstash@sha256:5d0a22226e1e2baef77a1c7fbd3f4f127a4e9f3fa5e565bffbe1ada339048966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655c3029929ab4315c54f866360b9ad996d5e58c8ba5661361e7157831df5af2`

```dockerfile
```

-	Layers:
	-	`sha256:6e0b98f0c511a1af2a51818842eaf8ba0b64561df931d705e34b271f6e8e77be`  
		Last Modified: Tue, 09 Sep 2025 06:53:22 GMT  
		Size: 2.1 MB (2142979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f239463693cc1e7240bc9bf3ad1bca53d5ce87872ec6a1c306ceede1d543bf`  
		Last Modified: Tue, 09 Sep 2025 06:53:23 GMT  
		Size: 29.7 KB (29653 bytes)  
		MIME: application/vnd.in-toto+json

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
