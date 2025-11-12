<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.7`](#logstash8197)
-	[`logstash:9.1.7`](#logstash917)
-	[`logstash:9.2.1`](#logstash921)

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

## `logstash:8.19.7`

```console
$ docker pull logstash@sha256:4559e674753e8e0c981bd40f8aec1aa72785cf5b067e85ee712fa3d11d322a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.7` - linux; amd64

```console
$ docker pull logstash@sha256:4733264957d10ddb540feccc0dd6c32c7f88a8adecff862749d26b268fcf8d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.9 MB (526906789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40241fc7ee33ff5166b1d3d3a46c714c3877cffd87e411995b5cabc5d4b6ad98`
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
# Tue, 11 Nov 2025 18:09:21 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Nov 2025 18:09:21 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:09:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:36 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Nov 2025 18:09:36 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Nov 2025 18:09:36 GMT
USER 1000
# Tue, 11 Nov 2025 18:09:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:09:36 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Tue, 11 Nov 2025 18:09:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef12c45ab074d6fed0a7733358f4343a5edb8a27263536f523f5430435f8514`  
		Last Modified: Tue, 11 Nov 2025 18:10:29 GMT  
		Size: 49.7 MB (49695396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cdf32fd32c6c0e7ba2b12f4cc3f8e3a8f4dde682404f50bd6a247da6be42e9`  
		Last Modified: Tue, 11 Nov 2025 18:10:26 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2848a18d188ced8e8cae20536e53211dfc566b3869da57a2369921bf8f70e88`  
		Last Modified: Tue, 11 Nov 2025 20:38:30 GMT  
		Size: 441.4 MB (441398221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707f297f5a0a7fbcf10b34cb0c2e806d44e2d021d9795d817d066ff586dbc89`  
		Last Modified: Tue, 11 Nov 2025 18:10:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f735a0a1551fbc0e1a702e88ba1747fd8286cda4ba4d780c4960d0f4036ca`  
		Last Modified: Tue, 11 Nov 2025 18:10:27 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763d8323e925fab6501bd6aef335e69e4ede73f771b93eedd3842a32f958249`  
		Last Modified: Tue, 11 Nov 2025 18:10:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649be092846005536a64d616fdb821cd2c05d924a5997680adde65de79fe665`  
		Last Modified: Tue, 11 Nov 2025 18:10:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fd6651985957dd32b9eb52e3a158d6e43904737e242ff4ec2fd8493b52c58f`  
		Last Modified: Tue, 11 Nov 2025 18:10:28 GMT  
		Size: 4.0 MB (4005474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8bec964867714846cc011558d050b56799f6094ce94df67776e8fdc4a9beb`  
		Last Modified: Tue, 11 Nov 2025 18:10:29 GMT  
		Size: 2.1 MB (2078660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656a995a3f251e76b9d055940ff924d31d57fd7e17f23601582e9b940dce06ed`  
		Last Modified: Tue, 11 Nov 2025 18:10:29 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:52364ee122c36ab704ef995d32645cab028b5c23947daf41bcbebd4fc13802af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3a74bec3d9d01a7d5f6f0fe34d64f8b6820f170c28430ad95914a693f657f1`

```dockerfile
```

-	Layers:
	-	`sha256:08b49c51d4734ab0838b9dbbfc139b0da2b487fc5d028ab9d89cc0070d322027`  
		Last Modified: Tue, 11 Nov 2025 19:53:21 GMT  
		Size: 3.7 MB (3653221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a081c8be6f45e6cc9ec88c33151e02f8d7c3654e247ed391e749621e8f449c`  
		Last Modified: Tue, 11 Nov 2025 19:53:22 GMT  
		Size: 34.6 KB (34612 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0ab5d285a80b94b11489361c5aa994a0447de4dd26a41db733be0aa4aced1e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.1 MB (526052245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64026c6a5c86fab10530c6693b83f14b5497eaead015587cf367838dc3d9cbc5`
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
# Tue, 11 Nov 2025 18:09:05 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Nov 2025 18:09:05 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Nov 2025 18:09:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:09:26 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:09:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Nov 2025 18:09:27 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Nov 2025 18:09:27 GMT
USER 1000
# Tue, 11 Nov 2025 18:09:27 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:09:27 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Tue, 11 Nov 2025 18:09:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a0aa4137ea383e239dcecd801b76dd0e0a1d4fd2f4487234bbdf31b82ebcc`  
		Last Modified: Tue, 11 Nov 2025 18:10:27 GMT  
		Size: 51.6 MB (51569754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e1f1148c19c9ada0925d13f107c152d20501b90d2f856b169dfe1f6c797ed2`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d53d3fb972eef02dd5ee6f9d8075f3ade0e6c84c4225252e8cf87ebe6557c4`  
		Last Modified: Tue, 11 Nov 2025 22:15:20 GMT  
		Size: 439.7 MB (439682903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa51cd0e33ad3225d9119b882b3759156edae06f3362b238e2a56bb03ccd51`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748b5f71d9eec832605dd7b50de577238b40ca6914741f170dbc2ab9da1ed0ac`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5932f6e22c54dc2e8a253407525e09ef07f0ba9235d39ad95fdf79537610888d`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99042a27f64e39f5d744031f96d6c37278dd8422bcac7741b4e324f0fc0c04aa`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8d3c01d9009fd6452df94699bab059cc9904324ff30a4cd2f7ec7c3f5df09e`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 4.0 MB (4005469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0354ebaa64e9c93bc96d061c898090c63f1dd7a1730486c9f0da469d9404bfe`  
		Last Modified: Tue, 11 Nov 2025 18:10:23 GMT  
		Size: 1.9 MB (1926503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6218ce4af086a7082fb52db838a016ca26a099db48c49941a66a00fb07a2e5f5`  
		Last Modified: Tue, 11 Nov 2025 18:10:25 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:b099d77c4263f31131e82ef23e62c555fc417b0197ba47b20a1fe103c4c2dd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd83c82db5fa9d85a4b9dc9dcb21da558cc86934710e17efbd6367e21f0617f`

```dockerfile
```

-	Layers:
	-	`sha256:bebe550aa39d8c621f3f0bbcbc0c5e52a1a9e0b28fa5993e70c291011489dbfa`  
		Last Modified: Tue, 11 Nov 2025 19:53:26 GMT  
		Size: 3.7 MB (3653646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da7630eb78a5b91dbcf78b85982538be7ec406c0ed6c43a3b8e88a15b5b8ec5`  
		Last Modified: Tue, 11 Nov 2025 19:53:27 GMT  
		Size: 34.8 KB (34756 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.7`

```console
$ docker pull logstash@sha256:1282352c8c8aed501b03d67a1729ea14e782b90e35b568962eb837d28b5b51e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.7` - linux; amd64

```console
$ docker pull logstash@sha256:e004b73b7048319ea8f0bec7491a85089dac61b61bbd0333a9f69290fa3a5750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.6 MB (477558809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb79fb999a63a5aef6da3905369f3d19270be57161d5c48ba7e411d30a9fca3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:03 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:28:03 GMT
USER 1000
# Wed, 12 Nov 2025 00:28:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:28:03 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:28:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08ffa2fc6588f8cfb8ee84071bf573d0941e8759083a6f14b5c578d504c816`  
		Last Modified: Wed, 12 Nov 2025 00:28:51 GMT  
		Size: 5.1 MB (5147817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e5a90d5cfdbcec07a48ea0d47b6b726340489b3bb63b9eda8e0f4959fb914e`  
		Last Modified: Wed, 12 Nov 2025 03:57:24 GMT  
		Size: 430.3 MB (430328501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4145e9627d74996067e05f5daba468e5c8950a39525fe4b07bbb8458395de9c`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 2.1 MB (2078842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc110383dac8a31a21e671d5d2be5ce6e1229a7ed8df5a8c65877f62713c582e`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e77c4a61dff62eea99ce2f9782574a36707435e44da66b724cdbdd16a8828d`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815ff428d47931db349a477168f19978f6b1c4aa84da204d4fcb3fa9e8ae83d`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9173feb053dc15a039ee3ef321fff16e283b081d70fc48cb64acf1e8d7f8c9c`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:cb8d8ed667b5d722b79ddc5d1a9d66f21adc3cdd051d7f5339d9f7d3c6f86b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2129b42c35ef3fbf2b16af012560eb6ef21e84deaa770a51d85b4cc61f6f953a`

```dockerfile
```

-	Layers:
	-	`sha256:1729df2508444f7574e03c9459a5e135b33ad9d6158c1788088cb7b4134ad8cc`  
		Last Modified: Wed, 12 Nov 2025 01:53:20 GMT  
		Size: 2.1 MB (2090542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e60429724087a4668585cf45306d362727566adffb018a156c60e0bd5b3061`  
		Last Modified: Wed, 12 Nov 2025 01:53:21 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7446343e7c606bd0247c1e1a08b51d052b94cf6f3105beddad29dd496754c2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473889089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e23d61d14f8a3d159694e31614bf41271a893f285c4e05c58c71fb88300d007`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:47 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:47 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:28:48 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:28:48 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:28:48 GMT
USER 1000
# Wed, 12 Nov 2025 00:28:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:28:48 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:28:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5e300dc91d5bfeeb5cf4d5a19dc6ac25019695b33b871574ab571904330fa`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 5.1 MB (5146008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba5795ac88e10c36af818451049ef447d5b4d4ea79f63a5e4e37720bf925c7`  
		Last Modified: Wed, 12 Nov 2025 09:37:22 GMT  
		Size: 428.6 MB (428601843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada5ed8d4b716c793e1d9fc654bf155dd85f35850647d2710837ef164949c524`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.9 MB (1926865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59946ad42512d5539203225831945f1206025834c2955d7305938faaad98643`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96a9a874ba2d15cefcee8637b656583a5a7b9b98596cf0721fc07bd5711ce0`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb98927cdcaf7ab06495f1139a227208f9bab9da29db5507b9bd02379928b7`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2709ff6f5a7713057b87c5bdc79ba322f8046b0beae226b91520b334500b19e`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:40198e71762bcf1f23266d1c3f8f327e6f8be0a3a5c7f4503aa0cc4b4fec45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412e91c4e1d0b4098b801e9f35d067509c470ce2981a68093f739b3d7c78ce7`

```dockerfile
```

-	Layers:
	-	`sha256:9c2ea2193f5da041dd02659d351def8150bcdaafabdf896beae5db8c8611369d`  
		Last Modified: Wed, 12 Nov 2025 01:53:24 GMT  
		Size: 2.1 MB (2091112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be87fbc662ea7353bf088d104208397abfaccd1658efcbcd8d8368565124f2e`  
		Last Modified: Wed, 12 Nov 2025 01:53:25 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.1`

```console
$ docker pull logstash@sha256:782d55660ff0539ca757d56deec0789ac17728bf509c2e72ddf0958e861c2c47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.1` - linux; amd64

```console
$ docker pull logstash@sha256:838e4196851770c712953dc599b761d4544316aebdc2f9b79c2d4b2c5b2aaf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487862141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1689deab253065b9ee98089de1d7bc7f7c007b3a8f4c55ed4ecb4f2293018534`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:03 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:29:37 GMT
USER 1000
# Wed, 12 Nov 2025 00:29:37 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:29:37 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:29:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08ffa2fc6588f8cfb8ee84071bf573d0941e8759083a6f14b5c578d504c816`  
		Last Modified: Wed, 12 Nov 2025 00:28:51 GMT  
		Size: 5.1 MB (5147817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e86bcf970f8e0f65cb30024c9d03958476f82cf22fecf96c5f86fa2f263be`  
		Last Modified: Wed, 12 Nov 2025 02:33:21 GMT  
		Size: 440.6 MB (440631845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a349297bf9f6039497587783ef7c3d75bf4c39c752195f7609a4f176ae54cbe8`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 2.1 MB (2078833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af0aad64cef5655ceb8fc1b625421e29f350eb14e188bf272476b0ab13a4d3`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4589ea598d3872511f70908a19cfd957ba70088159e21902bd73d06a26b59a`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0401be97e0334c2cdb9dd611cf6145a8a07acce6318b2f9ac50441c76ec650`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3b21ac1b8555f7ffe251b4ab39282d4c575549751e421c59a4f3857ef6a14f`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:3e87ce19c4e77504e1d0682ee041942de055e724ae54aea4249c74b63ee73aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd389027b9941ff33e47f26ce06facac1659210d2db8313394a29168bb847a44`

```dockerfile
```

-	Layers:
	-	`sha256:b44d9863d7846416c296b28afbeeef327e1d804970178989f9ef601197ceea0b`  
		Last Modified: Wed, 12 Nov 2025 01:53:29 GMT  
		Size: 2.1 MB (2100362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ba1e5cacb4de7171880aa1477beb651817f7ff57c344154596e108a93ca5ec`  
		Last Modified: Wed, 12 Nov 2025 01:53:30 GMT  
		Size: 29.6 KB (29601 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f5b4ea7128b9c7400b5f85147696cd9f1bc3cb22662501b6fb1f6e617be57773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484192729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac2e2fd9e93bb310c6f4f2fec4232f771879454aa63989e2897bcef3b2dc59e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:26:07 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:26:07 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:26:07 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:26:07 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:26:16 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:27:07 GMT
USER 1000
# Wed, 12 Nov 2025 00:27:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:27:07 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:27:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e8a4753d23ce5c4edb4cf20502bce845d035ecbd804614e6f7268bf721692`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 5.1 MB (5146000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdfe89646a6e9f15e3c553c17c9003fc14f66b4f4a0085578521532f8dc09f`  
		Last Modified: Wed, 12 Nov 2025 03:45:53 GMT  
		Size: 438.9 MB (438905507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a66c53a9834d2f7229e0f47b440d89b7ba5ec48fe8f86f865fcfc53abbf2f`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 1.9 MB (1926841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d17e33434912de0ef9c93f2d55cecd0d16e2709675e350eaaa0820f18f8b`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a64375614f691df0a2b3a78bb0ce9943dc1d8295572386544b93961e3d1b7b`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2735a09509afdffa27e70b2121a3093d85adf24acc577e166e5d21050ee48805`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6daedee833f79500e54efa9ffe98c90ab667f263c0f2d9406415bb41945c45a`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:66afc028b57fa6b036098e91cd404a92ebba724ebff4613e3c394f4b129f9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a791a8c7edf9b0d91e847a98a82cb6d6836175f21545442062ea42be0f293c27`

```dockerfile
```

-	Layers:
	-	`sha256:4ae066810895bc322403d8f6c18b67188bc1753246a08c8ec916d34b66c7e408`  
		Last Modified: Wed, 12 Nov 2025 09:37:19 GMT  
		Size: 2.1 MB (2100932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62b29df92a64c940a23f95d2b4997d33d636bba55cae436318e1d84bdf034a9`  
		Last Modified: Wed, 12 Nov 2025 09:37:18 GMT  
		Size: 29.7 KB (29717 bytes)  
		MIME: application/vnd.in-toto+json
