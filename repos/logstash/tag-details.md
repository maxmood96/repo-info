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
$ docker pull logstash@sha256:1d341e47353f31c1c34bd95f19436668e46072ec9747ccee12928f23e769ae40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.6` - linux; amd64

```console
$ docker pull logstash@sha256:783af23f965d7a0b8a8d1aac75dd1d2199b29bf78578cf836ba8095ca96c2a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477039665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05438be69b5d24baec5a901781b9a716c5b32d465c4e080738095a8b063905dd`
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
# Wed, 05 Nov 2025 21:11:40 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Nov 2025 21:11:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:11:40 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 05 Nov 2025 21:11:40 GMT
WORKDIR /usr/share
# Wed, 05 Nov 2025 21:11:49 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 21:12:36 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Nov 2025 21:12:36 GMT
USER 1000
# Wed, 05 Nov 2025 21:12:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Nov 2025 21:12:36 GMT
LABEL org.label-schema.build-date=2025-10-22T00:49:24+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-22T00:49:24+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 05 Nov 2025 21:12:36 GMT
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
	-	`sha256:f7cd4857b353dd3bd3e78c690609f973cb661d8ef465495dfe96dcbbf1fe141e`  
		Last Modified: Wed, 05 Nov 2025 21:13:27 GMT  
		Size: 5.0 MB (5017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ca605dbe19d35d2f1de4e28a1284f575cb6cfadde2cb8323ba75e2277f6eb5`  
		Last Modified: Thu, 06 Nov 2025 06:05:31 GMT  
		Size: 430.3 MB (430287058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e69cfee5d395d2d2899d92c7fa985bcf51362ad0179fcd8ef91ecf6bde672d`  
		Last Modified: Wed, 05 Nov 2025 21:13:26 GMT  
		Size: 2.1 MB (2078846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493ea202d252cebc70274e7bfab55fafe62137a443dd6e8f49864df4fcae2ae1`  
		Last Modified: Wed, 05 Nov 2025 21:13:26 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc18694dc3c773aced2c9ec8a8d0914cea380d3568640eccad15a2d060daa08`  
		Last Modified: Wed, 05 Nov 2025 21:13:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab961820a9827508e227ec9dc4e51a7f41b557512f19240fe4f10ba576e4aa81`  
		Last Modified: Wed, 05 Nov 2025 21:13:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e01d9f572e12e959f870092857fcec441860d602f1e81614026840539eb3e09`  
		Last Modified: Wed, 05 Nov 2025 21:13:26 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.6` - unknown; unknown

```console
$ docker pull logstash@sha256:e55598e50ce62a7334120340d89dd2f9d37f5f7d907f94ab533ad6e8ed536682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1236358b7c3100d0bf50636223a41c4213ac9d14fb72048c4406c8e44bc9ebf`

```dockerfile
```

-	Layers:
	-	`sha256:8a7cafd7bda2d6be6225cba58a1964c5993cdfc901afa03d991e288964df6a3c`  
		Last Modified: Wed, 05 Nov 2025 22:53:48 GMT  
		Size: 2.1 MB (2075955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3672e21665766fe738cf6d2f8c199668d8721f3f62f705773b4e00a0f757b2a8`  
		Last Modified: Wed, 05 Nov 2025 22:53:49 GMT  
		Size: 29.6 KB (29552 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1aec0f0189e9c7544e49cd70c300103ad64f31305c6f48d56876ba57024c6d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.4 MB (473419955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3e4472efaab1abb695246beccd2388f395caf5094c80e26aa77b9861c4751d`
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
# Wed, 05 Nov 2025 21:11:47 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Nov 2025 21:11:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:11:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 05 Nov 2025 21:11:47 GMT
WORKDIR /usr/share
# Wed, 05 Nov 2025 21:11:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 21:12:45 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Nov 2025 21:12:45 GMT
USER 1000
# Wed, 05 Nov 2025 21:12:45 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Nov 2025 21:12:45 GMT
LABEL org.label-schema.build-date=2025-10-22T00:49:24+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-22T00:49:24+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 05 Nov 2025 21:12:45 GMT
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
	-	`sha256:19640046e6bd232cc1b35866d11ea56294095461c7f213a1ea4ee5d5cee3f6ec`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 5.0 MB (5022750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536083bdc8d9e55b6de39dfc6b4b7c6aa724aa438daa834b9368571148ba3d5`  
		Last Modified: Thu, 06 Nov 2025 06:30:22 GMT  
		Size: 428.6 MB (428571144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b98705992efbcf6c7062d18d9db63931e3ac149764889061a2fa2efdc7fbd7`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 1.9 MB (1926869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4cbfeca28b41ede6d7c574f84915aa69a0ac92ca3acd9f51dcec869d87288`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7e62224932bafbf2c83474b3d45b830e216c3f38acb8ca4671b18f08b03d22`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ae9e50f19ed89af0cea711bd2ac553e466106bc43d8675d21312f19882bfff`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff67e105154b286d93745fb79f8d78a61ca4c7acf59afb07cbbb842d4f80a1`  
		Last Modified: Wed, 05 Nov 2025 21:13:45 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.6` - unknown; unknown

```console
$ docker pull logstash@sha256:5c3d52c19297aec667867fc9f5f497f4e1a8757801de60b3fcfa107f1f29e124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5a4cd167336d8cd72835e308e1ec9f6b836dfddbc974cbd1ca245dd40058ee`

```dockerfile
```

-	Layers:
	-	`sha256:f081c2f6109d9e7f28465345c3c63767d62a8614e16a6ec818a8572b29868684`  
		Last Modified: Wed, 05 Nov 2025 22:53:53 GMT  
		Size: 2.1 MB (2076527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa0d73b73b84927dafb870411f2d01c7ff20934aa1fb189e7770e8503f28d27`  
		Last Modified: Wed, 05 Nov 2025 22:53:54 GMT  
		Size: 29.7 KB (29670 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.0`

```console
$ docker pull logstash@sha256:e73333d13757fb744d45861011fec26410e1131ef4154d86e2b06092d2f0232c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.0` - linux; amd64

```console
$ docker pull logstash@sha256:5b5821125f5c20dee1fad76b1b8b99ba639214f3cbdba1b117670d9f04e207e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 MB (487343487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467f8c86e2bca69983ea5f83a5b007fde8cf0f63a995d4c93a46a38d0d25d2cb`
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
# Wed, 05 Nov 2025 21:12:39 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Nov 2025 21:12:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:39 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 05 Nov 2025 21:12:39 GMT
WORKDIR /usr/share
# Wed, 05 Nov 2025 21:12:47 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 21:13:36 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Nov 2025 21:13:36 GMT
USER 1000
# Wed, 05 Nov 2025 21:13:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Nov 2025 21:13:36 GMT
LABEL org.label-schema.build-date=2025-10-14T17:09:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-14T17:09:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 05 Nov 2025 21:13:36 GMT
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
	-	`sha256:e74ae943f4d9f5ef9d88af5ad69ca0f230a9371547e31a27b4de0bc06d6644d1`  
		Last Modified: Wed, 05 Nov 2025 21:14:32 GMT  
		Size: 5.0 MB (5017310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd7b8a0beacd5ff504e239e7c09f36c9c9abd9395780abcb1ed1848cdf2e71`  
		Last Modified: Wed, 05 Nov 2025 22:54:17 GMT  
		Size: 440.6 MB (440590902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6617c827905ad2b79989a7a365710cf766cfc732b4b8d396203ddc02f3d5ad62`  
		Last Modified: Wed, 05 Nov 2025 21:14:32 GMT  
		Size: 2.1 MB (2078840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c366c02d5c7fcfd40be2ea4caabf52c0318c9acb93bac5dc9230e78e9b10b8`  
		Last Modified: Wed, 05 Nov 2025 21:14:31 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7c483d6aa504f29808b5a1320d1f02bfb7f3085169885b069678f9dda63bf`  
		Last Modified: Wed, 05 Nov 2025 21:14:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1300845432389742fd748547e5a930e208caa75b52a22f3f1f07c441f3640f9d`  
		Last Modified: Wed, 05 Nov 2025 21:14:31 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06257b6fb277b1b44aceea233ca725950981eba11bb118af1f56379de2280ba4`  
		Last Modified: Wed, 05 Nov 2025 21:14:31 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.0` - unknown; unknown

```console
$ docker pull logstash@sha256:c567ca99fc78117f9445055cb6ed25446642aafc391e768110f6bfc1929e67c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf6f2f27ffc892da4e400a594c5b46bfda524a5597300d66ee91e3e241ca4dd`

```dockerfile
```

-	Layers:
	-	`sha256:4bb666cb3a79fc98870ab5b9437e38bc1cd2d1d6daecfbdaa8c0dea093836f63`  
		Last Modified: Wed, 05 Nov 2025 22:53:57 GMT  
		Size: 2.1 MB (2085775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acbd34ab317f3d55a5dca380ee776d82f1195a1c79a15aad13a9811724451ac`  
		Last Modified: Wed, 05 Nov 2025 22:53:58 GMT  
		Size: 29.6 KB (29602 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:216cab59a1c947064048606aa1a50ce2b68042cd00797487b00562c9a8d79529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.7 MB (483721979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e0425a32859dbd1d66212a53abb08fe98b266f74ddaf3f20770d48680efcd`
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
# Wed, 05 Nov 2025 21:12:42 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Nov 2025 21:12:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:42 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 05 Nov 2025 21:12:42 GMT
WORKDIR /usr/share
# Wed, 05 Nov 2025 21:12:44 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 21:13:33 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Nov 2025 21:13:33 GMT
USER 1000
# Wed, 05 Nov 2025 21:13:33 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Nov 2025 21:13:33 GMT
LABEL org.label-schema.build-date=2025-10-14T17:09:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-14T17:09:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 05 Nov 2025 21:13:33 GMT
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
	-	`sha256:bb09c2129a5ce37427a35fd1fa7d9eaa2afdba8f567ccc4191b93fe4452f5bbb`  
		Last Modified: Wed, 05 Nov 2025 21:14:29 GMT  
		Size: 5.0 MB (5022742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a8d65ee75eeb231ea062d742c23a44853a0a46f365bcbd94202015e12eb50c`  
		Last Modified: Thu, 06 Nov 2025 01:13:40 GMT  
		Size: 438.9 MB (438873200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704cc6e755b60696ecb83685b8330b68a29715f31854b73f0c1820f0b7298755`  
		Last Modified: Wed, 05 Nov 2025 21:14:29 GMT  
		Size: 1.9 MB (1926850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b1025b11530623a0672e79f3c767120c2cb68d443ed95261cb0cfd4b31dae`  
		Last Modified: Wed, 05 Nov 2025 21:14:28 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00b3f750a1521fa5bfe77be9913be299cb597f651fb633d3652398d9372254`  
		Last Modified: Wed, 05 Nov 2025 21:14:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bda2a661efc5e12e6d04343c2eefbdfb74512fd20f47aa1dcde20f6c70cb7e`  
		Last Modified: Wed, 05 Nov 2025 21:14:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97e6df17256ae62d44872e8a75d658726402dfce95c654c35a5162da969ef0`  
		Last Modified: Wed, 05 Nov 2025 21:14:28 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.0` - unknown; unknown

```console
$ docker pull logstash@sha256:ffdf5da43dc473350dcf64b6776205efd9b11cd395dda8aea107cda9403d1b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2116066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c2572b5ff4992908d136dc74686ce8e7d7d64895f38139470a84d524246ce7`

```dockerfile
```

-	Layers:
	-	`sha256:8e79ffcf06ed286e084fa9a1ce77d2b34a8ca0262db93eec7ebe67a774338355`  
		Last Modified: Wed, 05 Nov 2025 22:54:02 GMT  
		Size: 2.1 MB (2086347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a9eade8d7ea05b4522520374557f320ff98a1c1f6205c3d1bf474d811ddfef`  
		Last Modified: Wed, 05 Nov 2025 22:54:04 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json
