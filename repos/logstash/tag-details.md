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
$ docker pull logstash@sha256:a777d172adb4791b0329852c10a60aa3bb5d02f26622fecdfef56ca77d4e4d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `logstash:8.19.3`

```console
$ docker pull logstash@sha256:e0b12143ff6897f53764e51c55f14e68806da152904a38edd9a694ab35d66732
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `logstash:9.0.6`

```console
$ docker pull logstash@sha256:c42d073b50240d518e76209f5d43ea9f39987bc2b039bce0ed7fe5eb909c38f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:9.0.6` - linux; amd64

```console
$ docker pull logstash@sha256:688c829caf02a49e55778dd1b2f22d19a950a08fe133fb01fe974e734a8834f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484718683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1445bdf8ab483a9d8e75c6398d35a7cc76b58ed03143b41ca15963751cbb66`
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
	-	`sha256:00e19c0934433ff19029ca87ce96c94f091b98eb6bf6c27acffddc8e8b93a0e2`  
		Last Modified: Tue, 02 Sep 2025 17:27:41 GMT  
		Size: 5.0 MB (5018692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af3cd9ee677419791205f9ece0c69b560ab2616ffef50a71b4a379c79f4b15`  
		Last Modified: Tue, 02 Sep 2025 18:45:15 GMT  
		Size: 438.0 MB (437971679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9f88853c8875bd0c081bcca84727f84129464087c89c47fece6ede266cb933`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 2.1 MB (2078117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b029214538253c83ddf2a3c6f3efb8343c3f3856b13490156ff652a12ebc44fd`  
		Last Modified: Tue, 02 Sep 2025 17:27:42 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7247680873bf9f2beb95fade221d1f704f5b8e072bcb8d5aaebbc3696c46434`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae517ac813edd962e94a6768658a79510c7a3cf0ee4fd1dd3bdfb3d17d64d98`  
		Last Modified: Tue, 02 Sep 2025 17:27:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1959c92cfd6a33e7d901658d5312f8e3a409ad698090a41195003768cd2b67`  
		Last Modified: Tue, 02 Sep 2025 17:27:42 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.6` - unknown; unknown

```console
$ docker pull logstash@sha256:e48eab3e534cfcf392e57d8057f0bbe4a5e05655a9b5c4cd9793875f2a496cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b677b94d47028b186cbf49ea999af120a83c0989182ca418b077a9948cc889e`

```dockerfile
```

-	Layers:
	-	`sha256:fb335e8f1b3d2db37e5f9c48a757068943decf4745cfec64d31e7cda78d41978`  
		Last Modified: Tue, 02 Sep 2025 18:53:31 GMT  
		Size: 2.1 MB (2142407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67eec1376c2c383c6d25b642bd785b00de1c74c655a52480638ad6fa98dcf6e`  
		Last Modified: Tue, 02 Sep 2025 18:53:33 GMT  
		Size: 29.5 KB (29537 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.3`

```console
$ docker pull logstash@sha256:17bdbc370e616165bf2e8ab5ea0309643eb53f21645894fa253042430594cae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:9.1.3` - linux; amd64

```console
$ docker pull logstash@sha256:b3c579f342549542d2bec7d61dabcca66bd88c8cc8d9d054216a088b43e23c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476783155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf722608a012632e48e33ad1393f13ff6ad071f52a13b1d3eb959e9116e67155`
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
	-	`sha256:9f104cea9118ab28807891b743f06ad299715967fcda5ae0c6da6fea6f4c30aa`  
		Last Modified: Tue, 02 Sep 2025 17:27:15 GMT  
		Size: 5.0 MB (5018678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e7e28e214485104893767bb20939ca90497ccf309fc88ebda51eb7245e3843`  
		Last Modified: Tue, 02 Sep 2025 19:00:47 GMT  
		Size: 430.0 MB (430036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8520920a30ad1e18babf4faf911289146b978f2e22ff18b629538956038cb807`  
		Last Modified: Tue, 02 Sep 2025 17:27:16 GMT  
		Size: 2.1 MB (2078118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe81b6e3d94aecff53d9e51bba526a329b962d3f4d16b9a95cc5e664ac443d4a`  
		Last Modified: Tue, 02 Sep 2025 17:27:16 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf94e0078d1ebdb23777cea0f8336d1a86917af1d04b48132846bca70d29f01c`  
		Last Modified: Tue, 02 Sep 2025 17:27:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba65b2935b787a833b62d43ed69de18c48c7f6e685efa14881dc7e3ed3ea9d6a`  
		Last Modified: Tue, 02 Sep 2025 17:27:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911a6e7bbc5c89b2f4797ee0ec9d9adb5033fa2400233dbed76c3eaa02af0ef9`  
		Last Modified: Tue, 02 Sep 2025 17:27:18 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.3` - unknown; unknown

```console
$ docker pull logstash@sha256:c8621e6b82b01c2bed9d7b823c15d3438bf370a2030fab782b351c2ec0c49d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d5c3ad4d9bc79cbdaed11f947291639e1fecfd430cb4789fe93685d363efdd`

```dockerfile
```

-	Layers:
	-	`sha256:f93af9289d794f6f5741aa49986b0d60cbf90d9fb6c8ca343dce58a96e82dcb0`  
		Last Modified: Tue, 02 Sep 2025 18:53:33 GMT  
		Size: 2.1 MB (2075930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8fc195dfb61d180480a9f24d3d97e7a46c81d3780eb33274b59d30d182974e9`  
		Last Modified: Tue, 02 Sep 2025 18:53:34 GMT  
		Size: 29.5 KB (29536 bytes)  
		MIME: application/vnd.in-toto+json
