<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.6`](#logstash8196)
-	[`logstash:9.1.6`](#logstash916)
-	[`logstash:9.2.0`](#logstash920)

## `logstash:8.18.8`

```console
$ docker pull logstash@sha256:8c006abe9b1f9926222c07939abfbefc662ab65883a701a005fa6460d622f518
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.8` - linux; amd64

```console
$ docker pull logstash@sha256:377ad55bb0da79203fbea548719adc2c6d742198f72497574dc01e06227fee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525714530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5310b6b4be40ed72194f4fee098b39b8ca2e5a6e251df1a0840a344b65ff7354`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4b7d12085fad81ad7ec3163a7f3cc70a710841621da192e7697622e982f20`  
		Last Modified: Thu, 09 Oct 2025 21:20:06 GMT  
		Size: 48.9 MB (48922387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2801e6c15ff330e70b9332ab88f6639c91b1f3f0eae7d774db8526f6cbdc57`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba5ed7d944a1d29952ccfb3db307a04dbe527c911a0069691750bc5378d9f9`  
		Last Modified: Fri, 10 Oct 2025 01:34:38 GMT  
		Size: 441.0 MB (440980907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccae48fa8c35954d5933778e67a9082bbd63bc132b9b4374af7c1dd83453292a`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9340b991c583eee28ac3879ca3a55d7b265f81a2d422cfca371d0c4ba8b111`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f59104d8d1a6bf1554e5b7ceeb60f805fd0a2e1659bbd39d31cc70ea55046`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcea15f1ee09cf40b3da8cdda73c50ef50ca8cdaceba61b617f50aefaa8aa21`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53273aeb4bda01e98919eafef40fc74066aca799903202fc52667944989302cc`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 4.0 MB (4004183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7a8b0478e4a9ad3b607352cbde90f0dceb22b6ebc5f1257d64e99f02fa714`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 2.1 MB (2078019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60ff261aecaf304811f084aa2a492c33f6b25c45976cc547c4038f2ee2407c8`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:9f01ed0470443a0ec61e774d8bf316f80226724eb5a5e891cfdecfa816420f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148f4554e42b2812e060d34ce6c1ddac579773711bb79afe57c09c6001d172b6`

```dockerfile
```

-	Layers:
	-	`sha256:0980399329770b29b190e202748ee01270e1b804252036a729a74f02229bf16b`  
		Last Modified: Fri, 10 Oct 2025 00:53:35 GMT  
		Size: 3.7 MB (3657663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b5ea34633a16735d6cc449ed464af2cb65d494547aa648d87feeb90ef2f83b`  
		Last Modified: Fri, 10 Oct 2025 00:53:36 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d8126443d2fe9e8ef2a9dee7e7df25eeb721af2b36042877103410fc01fded1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.7 MB (524700374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4b09f60acb633b24f28272df1f67d82e349cf75b1fc594ebf6e3adc955c7f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63573c99495ce0d7e4663866b70688062419d2c6fab14fc48ee89d545d9e4fd`  
		Last Modified: Thu, 09 Oct 2025 21:22:08 GMT  
		Size: 50.7 MB (50654390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16040666ad5849dfac44240f0b9638ed221add0c480c1266be6793f01e14b7fb`  
		Last Modified: Thu, 09 Oct 2025 21:22:03 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de3f9d837667a5455efacb31c2f5634003662a7d2f84d9a81064331fa8d60a1`  
		Last Modified: Fri, 10 Oct 2025 01:34:48 GMT  
		Size: 439.2 MB (439248611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fe1f3fde0a2edceaa89fe2dfd6d28f1fb00ca1e732d34a62005008bc88a735`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb87b742c5b03aa23edbe6e2c3cc2575ae3fc29126340a98b6cf8705be3b94`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e50aeb11965eeee28d3ca308606108364c779a810047fdefbbebb8bf155af`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001e27e71c69416570e63c689913439b42ff5eda7eb344d8eba8d65980150f20`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66151e42d94dbf9b0e521d122eecc712cf59d6a59c4ceee8ce998c2e17bb4123`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 4.0 MB (4004183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639900a06964fadf7c7124ecbdbd057d5da77f7e3f8a1874cbfbbecace1c39c`  
		Last Modified: Thu, 09 Oct 2025 21:22:02 GMT  
		Size: 1.9 MB (1925572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5204c3975e93e59a2c18c1131dbd313c2d7d01cb8e996200453ce5f83585ec0`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:4b4a6c8d728e02817972442e7fbca761ca3f8343336bc511513166d46512398d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d499c7043e4183b4e4751ca3d009bc8c81c9eaa7a3ca2a78eb55bba399e206`

```dockerfile
```

-	Layers:
	-	`sha256:e73f29e0d0122230125d66c8977c3dc9091f4c3ccd9b41ab865d5cacfdad59a0`  
		Last Modified: Fri, 10 Oct 2025 00:53:41 GMT  
		Size: 3.7 MB (3658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84da2a7c3d55eb7a5470d8325d5e68d517d3755a71f99f1aacdf4199f2057e76`  
		Last Modified: Fri, 10 Oct 2025 00:53:42 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.6`

```console
$ docker pull logstash@sha256:fc8786f91f37493e537f384dafb35b0df0c05a59b956d6d2254d9eb7f898729c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.6` - linux; amd64

```console
$ docker pull logstash@sha256:9e6c73346622d5bd91d43152a220630d30f38bf9e78c3fe244c7c9b11569fdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526538873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3d1640b9c963f6f0753cdb05b4efd6dfc63f16e182d9a78fe2ec780d001cca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 13:48:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 13:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:48:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:48:53 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 23 Oct 2025 13:48:53 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
USER 1000
# Thu, 23 Oct 2025 13:48:53 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 13:48:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.6 org.opencontainers.image.version=8.19.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-10-22T00:57:39+00:00 org.opencontainers.image.created=2025-10-22T00:57:39+00:00
# Thu, 23 Oct 2025 13:48:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f23c8db13a45f445ce9af7976951866304aa797a21e703dfbed16e3f4efd2c`  
		Last Modified: Thu, 23 Oct 2025 23:31:34 GMT  
		Size: 49.4 MB (49357643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2d9bef9aa00430648eb476139476db67ab87fee51f0faf5392abfe379833b1`  
		Last Modified: Thu, 23 Oct 2025 23:31:31 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ed9bbdcc70cfc1a96d28ea628d9ff3851c3cab2c7da03c83589090cd538196`  
		Last Modified: Thu, 23 Oct 2025 23:33:09 GMT  
		Size: 441.4 MB (441368055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc02a7477e67f8fb1111ce7ed9251d3ddfaebd741682a93f0559a8228240a63`  
		Last Modified: Thu, 23 Oct 2025 23:31:31 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f409b27792cc39484f588fbd7c29ac540d8466298dda0b3eb73812a5e99bb28d`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc5c05cfe72d4d3f99169b1ffebd855f979a19af8b9fee5b3bbda382ab4b930`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505b4357589ed2fb144a1dcd042e34ff4bd45259ec9fb694b0746f9784a52fd9`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5265593bbed620f3fe7dca438b94418c145f74775737c993ee68fdec1d7d33a3`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 4.0 MB (4005475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d5c4e792ecaa3b8794d8764f4081cf83f2fae25227a67f74748243951f26bb`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 2.1 MB (2078664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6734c8827546c774fc9581c4f96fd3ca12bad575406f9342c3619982c289c6b`  
		Last Modified: Thu, 23 Oct 2025 23:31:32 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.6` - unknown; unknown

```console
$ docker pull logstash@sha256:fc7570d7065bdd0a8ceec08d368f5b7b32362170af339769c72a9933ab4a6b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbdea11a7a6652e3a11d3ad98ba98d2759558e93c5ba1eb72586e7b14cd9c4`

```dockerfile
```

-	Layers:
	-	`sha256:0bb0f3719377598fcc8249f71b23a3d557be9036fad171e6496ae48b452ee0b2`  
		Last Modified: Fri, 24 Oct 2025 00:53:19 GMT  
		Size: 3.7 MB (3653219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef19b3952e67baa3ea67b070e7c13849be7712fc83da6f13d5d8eeed17ab710b`  
		Last Modified: Fri, 24 Oct 2025 00:53:20 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7da0bb6851018460519171f1b554891347b207ccece35fa10db7283d398d463a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.6 MB (525563510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8566899257c2149b630253d18b0b903a494c408136abd0dc8d700f151979d22a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 13:48:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 13:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:48:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:48:53 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 23 Oct 2025 13:48:53 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
USER 1000
# Thu, 23 Oct 2025 13:48:53 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 13:48:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.6 org.opencontainers.image.version=8.19.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-10-22T00:57:39+00:00 org.opencontainers.image.created=2025-10-22T00:57:39+00:00
# Thu, 23 Oct 2025 13:48:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d27bcba5093ab1006680e7521f13f0e085af67f5ed934e120d3e4ba1983e1e`  
		Last Modified: Thu, 23 Oct 2025 21:05:51 GMT  
		Size: 51.1 MB (51133544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1304f7466440cbcf1428f270937c85c264c7bccc17b53a8ac0e9684e3599b01e`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d942d9f57ab308853a5d0480ac163d27cbc903d50eb875588d877c48c17309b7`  
		Last Modified: Thu, 23 Oct 2025 22:02:17 GMT  
		Size: 439.6 MB (439630383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faef26ef3915937508ebae579a859fa20930d50a7da97814ca634e79814bca9`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406962429e087eb83dcdefd6a40b2197ff0b09ebc85a6586c7aba6455f2f12f6`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23538735740bac356e5506c9c1d8edc3c1500086fb4a57addb4cbd9ee51794f2`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09b964bde549a0cba518600e036f1d6d8c462d39638b182c7790605bd7bfed0`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e302239cfdd04f5558b2478922d7e61b440e682430b888174a7551e8d28a63cc`  
		Last Modified: Thu, 23 Oct 2025 21:05:45 GMT  
		Size: 4.0 MB (4005465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8584debfc7caf2c31ab132963008102f64293b30f8ae0911bf4ddc74d05f6752`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 1.9 MB (1926503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd16be324341081e12ef4784ca01e6a3e8d53df382160d59c033d9bb74362b`  
		Last Modified: Thu, 23 Oct 2025 21:05:44 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.6` - unknown; unknown

```console
$ docker pull logstash@sha256:983e74331e5be0aff84de89be445c4f44d9a0140d616d29fca6f2e62c5a1e8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e768b37104380e5a59390812e823c4cfdd9529177595f7c49bc298348ebda8d`

```dockerfile
```

-	Layers:
	-	`sha256:33be84292d9d67361c016d0187e7682cfe1171b9b8a53307ec89e09454e3f75a`  
		Last Modified: Thu, 23 Oct 2025 21:53:22 GMT  
		Size: 3.7 MB (3653644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf5fa89464f927a85845d8f89465171006a0f3ff2421cb61e7307e242e07649`  
		Last Modified: Thu, 23 Oct 2025 21:53:23 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.6`

```console
$ docker pull logstash@sha256:6a52b754e263accc8f9467058e8c2359a881ae203eaffdcfe15066d831446341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.6` - linux; amd64

```console
$ docker pull logstash@sha256:c4c469bd6473cc26284c5fe911c8afab9b971b23330e9ebd9bfbe7160bc1eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477039624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f19314edba516e6f8762d22c5fb2a45a0bb57b30b9db834a687c860535ead18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 13:49:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:49:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:49:09 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share
# Thu, 23 Oct 2025 13:49:09 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 13:49:09 GMT
USER 1000
# Thu, 23 Oct 2025 13:49:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL org.label-schema.build-date=2025-10-22T00:49:24+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-22T00:49:24+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 23 Oct 2025 13:49:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3531c154156420c055e69d084b983062bdb5b36228ff1230cd3033dc4928897`  
		Last Modified: Thu, 23 Oct 2025 23:31:17 GMT  
		Size: 5.0 MB (5017252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06baca9695e0f7e241d3fc32555586762b9f43451c468951965ff2a9e094f81a`  
		Last Modified: Fri, 24 Oct 2025 07:23:00 GMT  
		Size: 430.3 MB (430287085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1a5cd405848c6b326a6a559fc90340d83d6dd0763a347450ef5fb2420003a`  
		Last Modified: Thu, 23 Oct 2025 23:31:17 GMT  
		Size: 2.1 MB (2078854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd35309b3b66ac73a35c3e195cbcc18f9e574e08da13c221b48bd4eaf110b7`  
		Last Modified: Thu, 23 Oct 2025 23:31:16 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db8912f03ce4c2b8a8100fe6a58cc2f18e6058c721f988e69c0eb8ece6cbe7`  
		Last Modified: Thu, 23 Oct 2025 23:31:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1ee310286d761d8dec1f127d1ff83f442cafec03d5832fc080e0a6615f935`  
		Last Modified: Thu, 23 Oct 2025 23:31:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a949f5b3bd05f0ae16cb0ab5360454c2eecadd6a460eed54659e7c0447c4516c`  
		Last Modified: Thu, 23 Oct 2025 23:31:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.6` - unknown; unknown

```console
$ docker pull logstash@sha256:82440076282290e3406f07670943d7246479f73ae20944c5e5280b6ab4bdd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfaf0f405c3cf10a95fe0d940b207531019e6c7787fce9c7915b72b13b59ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e71aea604b336543fe6946e87d7acaf1c7ffd61293641683c815681ab4f1a5e`  
		Last Modified: Fri, 24 Oct 2025 00:53:24 GMT  
		Size: 2.1 MB (2075955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47ed714bf0dceeb9bf14509192d5b181312be24294cf9ba39fcc0467821a68c`  
		Last Modified: Fri, 24 Oct 2025 00:53:25 GMT  
		Size: 29.6 KB (29597 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d6da5cec1ddf5348b94f564d0e1013eb22a8de0338a6b3d746d2386eb9694636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.4 MB (473419190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047d1750bd03fbcc2f4fd2d77a1ab1cb74cd86d4a917d51fb614465cafd2c25b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 13:49:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:49:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:49:09 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share
# Thu, 23 Oct 2025 13:49:09 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 13:49:09 GMT
USER 1000
# Thu, 23 Oct 2025 13:49:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL org.label-schema.build-date=2025-10-22T00:49:24+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-22T00:49:24+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 23 Oct 2025 13:49:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a980f42143433962912ba3f2385aa4c03dce19631c57e8d31a685288b900d9`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 5.0 MB (5022783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903463f7ce3e88d89ca3e348221dd30f8c65b7fc3b0d8675ba619dca2bc081c5`  
		Last Modified: Thu, 23 Oct 2025 21:07:07 GMT  
		Size: 428.6 MB (428570344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9c8a8e60a24cb60c58ca8d6ec57e7cffb6e4b3005e80e3220a40d2066fbb5d`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 1.9 MB (1926885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e09591f344910031a3aa0d40eaf7894533e952efd9381d77d03e4cf17ce77`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764176452d313ee6c63b7e00e8f0a2f9d5a526963936632c4ff93e56d269a198`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c8143f6e3f5bd98085f98df75b9d34fddedd4168ac2ba67fcce08f4c68c2aa`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767dc6d964b80f503a41f73c7de8530d64fe1f9db22ec6b84ceeeaaf5c70cf7f`  
		Last Modified: Thu, 23 Oct 2025 21:04:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.6` - unknown; unknown

```console
$ docker pull logstash@sha256:70271b471a1d1504cf11e03f17cc3fca258744cf1db241df5532f166c9fe994a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3564d4d9dce0c22d48bed0cf8746712867a034554b53fcc49ca19ca988322d3e`

```dockerfile
```

-	Layers:
	-	`sha256:2ab55a2a0cbfb4681baa879b441e45f3224c60a6ac61db6389cf9e5a9324d822`  
		Last Modified: Thu, 23 Oct 2025 21:53:26 GMT  
		Size: 2.1 MB (2076527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c6cde4dbb54c125c7517ac327b7f30a93d8b99d434dff127aabf07c5a36465`  
		Last Modified: Thu, 23 Oct 2025 21:53:27 GMT  
		Size: 29.7 KB (29713 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.0`

```console
$ docker pull logstash@sha256:f402cb2880924518d997f733e9f9d970a0b887bdb37679ed559c83dbc1c3334a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.0` - linux; amd64

```console
$ docker pull logstash@sha256:3731c776b76393d171ff110ac73e2e7dc7b691eb6388ec64c93ecd11943d5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 MB (487342373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0244e207aa846e2e2430dbad1905389095863b265124ab05656b0a840c5f35f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 08:40:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 08:40:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 08:40:15 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share
# Thu, 23 Oct 2025 08:40:15 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 08:40:15 GMT
USER 1000
# Thu, 23 Oct 2025 08:40:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL org.label-schema.build-date=2025-10-14T17:09:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-14T17:09:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 23 Oct 2025 08:40:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65c37ca4be5f77d7e17c0065a12b7a37c4b29b551b73cb96a715903c328741`  
		Last Modified: Thu, 23 Oct 2025 23:32:29 GMT  
		Size: 5.0 MB (5017232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327bb6258abeb34006b90838234935977e0725aad4ab6c26a3ba0a2b8d8b1d1`  
		Last Modified: Fri, 24 Oct 2025 01:12:18 GMT  
		Size: 440.6 MB (440589853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb50f65cb27374b2764869e2030a3887712af1ae22ef60a4d3546d43043dc6`  
		Last Modified: Thu, 23 Oct 2025 23:32:29 GMT  
		Size: 2.1 MB (2078856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527c80442825c7ded6558016967e617bd258703f16523e4c1690619311d5a2a`  
		Last Modified: Thu, 23 Oct 2025 23:32:28 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb38dfbb6d066ad948989e3ce7c19b90fb2f6fa4b51151a5af1d8d283a86608`  
		Last Modified: Thu, 23 Oct 2025 23:32:29 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aefc7300f4a3012a5779da6984a93f65330b230a0be7642b3c422bce4e5e68`  
		Last Modified: Thu, 23 Oct 2025 23:32:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3e68804465a4ac073b8a7b14c1aebf8a5fcc727aeeebe55a8de6dcda6ae49`  
		Last Modified: Thu, 23 Oct 2025 23:32:28 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.0` - unknown; unknown

```console
$ docker pull logstash@sha256:6317625832a03723b9c123dcca86a66e7be9724875dc5ac6919ead19120131ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6fe5ecb72e4469e5a0fffd5cbedfb741ea241725db23afcbd398040c2721c3`

```dockerfile
```

-	Layers:
	-	`sha256:5091287b5349dea745422d372c643d8d01d7bfb6b4b47dbdeda4be0c55c3bab8`  
		Last Modified: Fri, 24 Oct 2025 00:53:33 GMT  
		Size: 2.1 MB (2085775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2501879b55d8b6f9777dd526abf7dfa3c32a2bc8f515faa6faf6891b87ec3b6b`  
		Last Modified: Fri, 24 Oct 2025 00:53:34 GMT  
		Size: 29.6 KB (29645 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1b5a8038882de893528f999d09dc4e78c95e39eaeb3407dc910108cbb53987dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.7 MB (483723518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfcecff3bfb553797715634e6e19e5b46d2cfbc773494b26c05573c9c10127f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 08:40:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 08:40:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 08:40:15 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share
# Thu, 23 Oct 2025 08:40:15 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Oct 2025 08:40:15 GMT
USER 1000
# Thu, 23 Oct 2025 08:40:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL org.label-schema.build-date=2025-10-14T17:09:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-14T17:09:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 23 Oct 2025 08:40:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5dd667b4b81c850a9fad07574845d2514ac14750622a5fba42e5848f3ccd82`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 5.0 MB (5022736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917d41a1c1e186350660e42ec75ba4d214293ca1311703ee4e1ccdbc8b7ddfe`  
		Last Modified: Fri, 24 Oct 2025 03:36:00 GMT  
		Size: 438.9 MB (438874710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c36260d6699d2b59c8891b5f933e0208bc71ec06da7949b2cd321da8125e9`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 1.9 MB (1926881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca6e736ac7592866e2a3dc7fffa4a50d50bda3eb3794a321c92a6102746a7ca`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348a19ef18ea40ee0bff05e4898b1e989c3dca37f3a8dfbc470eace76bac839`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937019cfee9bbe6b7aa58009fb9a23d9ad177a869061105f16cc7deec2a9681a`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89522d43ae3f51c8f292c70165c0a64261958e6caa6303d89f462abb71e66f`  
		Last Modified: Thu, 23 Oct 2025 22:10:26 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.0` - unknown; unknown

```console
$ docker pull logstash@sha256:877d241fcb2b5fa0528aac0f10b241cd245841a52dddf357b25d017d4a1feff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2116109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d255928c65944b1a3cab178ad803ac66a647518d7b0e951b692cf76781cfdce`

```dockerfile
```

-	Layers:
	-	`sha256:4365162dbdcc270d04e6df8560720a5f7e1cba733ab76559b7240f49f467b5bc`  
		Last Modified: Fri, 24 Oct 2025 00:53:38 GMT  
		Size: 2.1 MB (2086347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7963d4cc09abbdb212d37501298f904dae470020082286cc9124eaa250d3e440`  
		Last Modified: Fri, 24 Oct 2025 00:53:39 GMT  
		Size: 29.8 KB (29762 bytes)  
		MIME: application/vnd.in-toto+json
