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
		Last Modified: Tue, 11 Nov 2025 18:10:16 GMT  
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
$ docker pull logstash@sha256:6aaf64181c257fac5968cca8e0420bd3ec9173f2537a1eca48f7cbcc2897156c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.7` - linux; amd64

```console
$ docker pull logstash@sha256:2c35dae974feac3b1c2c72f9bef39243b86894112931a351ac665733b8f22cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.6 MB (481602313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a54850342cde61a111e1685da0d6e30f7598f71b70b2d972ad3eac839dabd11`
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
# Tue, 11 Nov 2025 18:09:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:35 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Nov 2025 18:09:35 GMT
WORKDIR /usr/share
# Tue, 11 Nov 2025 18:09:43 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:10:10 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:10:10 GMT
USER 1000
# Tue, 11 Nov 2025 18:10:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:10:10 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 11 Nov 2025 18:10:10 GMT
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
	-	`sha256:27699cf22a5ab90bb4836797e49b1fd52c57505402ec1de7d004ff74b70f8b27`  
		Last Modified: Tue, 11 Nov 2025 18:11:02 GMT  
		Size: 9.5 MB (9538552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf44e121af119f052a49ca689a14668ffafccaa4c37afaa755cb373389d2a520`  
		Last Modified: Tue, 11 Nov 2025 20:12:14 GMT  
		Size: 430.3 MB (430328477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a5cc7ab8d35442ea1fd5708baa260b5c068e6f1c8f00c2b7393e0798406dec`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 2.1 MB (2078845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca8f35fd5a68e0c47716081cd5d5e9b4d9fd4469614918cfe10d4a63545a7f8`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b03e5699fc5df314dce13250da9d3c62e032de9624d4baaf3c480bad4f9b2ad`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9215fa4132cc717b432e723690b01a124ba11e69226aee97052348611a5a770`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af14fecd0c42564a4589ba91bb0015b45cad309f2c0507c05ab2f1390d300f1d`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:f50fbe1f8ab6ec6f09d9d3d5f9b9ee429f43c9950742cc48d6c5fc939806f9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21d7c26fb51fdd964ba7eccb2b4cf56e30d811fd705a9c21d7dc56f19cfae15`

```dockerfile
```

-	Layers:
	-	`sha256:78815dd40241cf3be59ba636634489ab4de0f07ce78ca2ff9aac2e88f8f2425f`  
		Last Modified: Tue, 11 Nov 2025 19:53:30 GMT  
		Size: 2.1 MB (2105837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f290e02a8d1bcd29c3bf41a5e9653b227214de6854d1360f8c9726bdc87b10b`  
		Last Modified: Tue, 11 Nov 2025 19:53:31 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:03e37f614af0f79671433d7b35037ddba606bb3ca9f566d04d9b7ccc69fd76d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.7 MB (477708262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1355f01ce0da6a34cd483c7f4cd7a4268ce93560061742c33de62cfa406a705`
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
# Tue, 11 Nov 2025 18:09:07 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:07 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:07 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Nov 2025 18:09:07 GMT
WORKDIR /usr/share
# Tue, 11 Nov 2025 18:09:16 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:09:42 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:09:42 GMT
USER 1000
# Tue, 11 Nov 2025 18:09:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:09:42 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 11 Nov 2025 18:09:42 GMT
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
	-	`sha256:02f1daab0bb90cd0541729f39d262857371fbd95c5eb6bbfa8d9319b046c9316`  
		Last Modified: Tue, 11 Nov 2025 18:10:33 GMT  
		Size: 9.3 MB (9280369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db0d44e116e27c4f346094804590f99e861cdc380c87a89e70cc7af01282a68`  
		Last Modified: Tue, 11 Nov 2025 18:10:28 GMT  
		Size: 428.6 MB (428601833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fcff754e9cf0a60090a909d5af46b776e22fc7a105ce9bfb9ffac84fcea047`  
		Last Modified: Tue, 11 Nov 2025 18:10:32 GMT  
		Size: 1.9 MB (1926865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65d3311ced43e0b54eb754fe4a682d7b9603b48f192e16c25bc5d75ad7d04c2`  
		Last Modified: Tue, 11 Nov 2025 18:10:32 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0c644c77eb6da3ab03499fdbc32e909dd2fa499714fcc5eae4f4b48eb2769d`  
		Last Modified: Tue, 11 Nov 2025 18:10:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f847315fd655bed65ff490d43c23461b3445c1a896932c957d5c2808ef1c214a`  
		Last Modified: Tue, 11 Nov 2025 18:10:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c594bdeb335d14545609a40f2702032f97c58549bf151ec73eadf34d635a7cb`  
		Last Modified: Tue, 11 Nov 2025 18:10:32 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:864835d5c43519004ac88001332046643b6ef45264957447ef42de5f17d3a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5a1d0c25733afe50cdb3c0392937612e15392b6bf5d10c47bf8638318ef678`

```dockerfile
```

-	Layers:
	-	`sha256:00c5b463b8a93f853e89ce727640d8d91806166e3e867e1455a9b8ae9852e4f3`  
		Last Modified: Tue, 11 Nov 2025 19:53:34 GMT  
		Size: 2.1 MB (2106409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c35ba85e20da95c373e40c1a50afe3be9d4f94d637b7dc181a4e63f3347d89`  
		Last Modified: Tue, 11 Nov 2025 19:53:35 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.1`

```console
$ docker pull logstash@sha256:981b80d3b6fbf484480563e590a82b772d4de7f98a59306d1130e07345978d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.1` - linux; amd64

```console
$ docker pull logstash@sha256:8778cfd8d157cecc71447141be4c70917779f9b8414a4a49419cfc118c9880cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.9 MB (491905438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ef51c47a914d6282e18fca67b4bfab59a45a6bc3d9411212256dff02f07ef`
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
# Tue, 11 Nov 2025 18:09:41 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:41 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:41 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Nov 2025 18:09:41 GMT
WORKDIR /usr/share
# Tue, 11 Nov 2025 18:09:50 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:10:15 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:10:15 GMT
USER 1000
# Tue, 11 Nov 2025 18:10:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:10:15 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 11 Nov 2025 18:10:15 GMT
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
	-	`sha256:ba584fd4f240d31a745babdb21064da2c2e3dff323467f26d5cf04cd86441e91`  
		Last Modified: Tue, 11 Nov 2025 18:11:03 GMT  
		Size: 9.5 MB (9538456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbe94a3773a725768867bf55de238989ced5d5665e9ac8097985ffd3c8ed75`  
		Last Modified: Tue, 11 Nov 2025 20:09:09 GMT  
		Size: 440.6 MB (440631703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e44fad8c859942797ac39451505320504a5f15e355672cf57324131e2364542`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 2.1 MB (2078843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52661b5b155931037f7572b4b157f864f305a498636f77bb24cf19de25a61be7`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a68547aa659e577dde667e9c33f9aaa275a1ba7eb9cb1d360550ea24489c013`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29465b312fcd59ab17512c4ddec8fe304881dea01afebf97eba5843d10e1af87`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6762963c9fd83edda48da9e06730736a7a3adf22a261a049c0fa174f4fc99a40`  
		Last Modified: Tue, 11 Nov 2025 18:11:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:f1b44181afe8414d3b0f9377e438305c6fc4f300a60c4b01230d50f8b2fdd6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbee1dcb0237c215e9ea1f8c941eb4158e9fd726bd586ca743c814c29d2a6ca`

```dockerfile
```

-	Layers:
	-	`sha256:1b68ba8ca612ee2dcf532991ca42b026732608872a7234a596039c096c3ffa13`  
		Last Modified: Tue, 11 Nov 2025 19:53:39 GMT  
		Size: 2.1 MB (2115657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819cda6de0d33945ff4dce29d54568374d8139009227f2454531058c4e29761a`  
		Last Modified: Tue, 11 Nov 2025 19:53:40 GMT  
		Size: 29.6 KB (29602 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:4f161a488aa5c59d9a914e44ffb94c1f05e7e2524badfc250ba8284032f66750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488011682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cb25974a5d91222a175290a00c341844e4d984b786e03684d541eb5d35aa5c`
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
# Tue, 11 Nov 2025 18:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:09:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:09:04 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 11 Nov 2025 18:09:04 GMT
WORKDIR /usr/share
# Tue, 11 Nov 2025 18:09:14 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 11 Nov 2025 18:10:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:10:13 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Nov 2025 18:10:13 GMT
USER 1000
# Tue, 11 Nov 2025 18:10:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Nov 2025 18:10:13 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 11 Nov 2025 18:10:13 GMT
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
	-	`sha256:521cb4281f314e3685cb7a63bf49ffa88cea57f771a9ef52db95877c9dbfb0f7`  
		Last Modified: Tue, 11 Nov 2025 18:11:05 GMT  
		Size: 9.3 MB (9280383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cddd7e9dabb34a68e3eb3e65337e55a344b4249799ea263b2508dd9d971b72`  
		Last Modified: Tue, 11 Nov 2025 18:10:58 GMT  
		Size: 438.9 MB (438905252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a7c8450b377d6ea14518931d01e9aa24b5883ea176acc1b61721cf6b4138ce`  
		Last Modified: Tue, 11 Nov 2025 18:11:06 GMT  
		Size: 1.9 MB (1926852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f7020461ff2aafc5d7060114d1323b1914579316801cf02b29ce61745bf98c`  
		Last Modified: Tue, 11 Nov 2025 18:11:05 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6400920d6228069ca6b7a591aa1ab536ed4d5d1601b5f88b4a74f10c42281db`  
		Last Modified: Tue, 11 Nov 2025 18:11:06 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e0cafe9672261dfe992a1aa24bc82c93e7384254624813a424a37d6a302f66`  
		Last Modified: Tue, 11 Nov 2025 18:11:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c567c5744a11395632a3877cfac07868b6ac7274efb06f8c63f7ec96cdbab978`  
		Last Modified: Tue, 11 Nov 2025 18:11:07 GMT  
		Size: 715.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:c58303a0ce69def21ab86fdf583042e7d77953d6af8c3fa6da7ce60f32c1f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641063bc00470e797baa3d1df48a724982f54ba21c4efa2820e62a34ad2830d7`

```dockerfile
```

-	Layers:
	-	`sha256:996c71dc9b6982ff17d996f5a1131ce16ac11e32172fca03d24c09ceff4053a8`  
		Last Modified: Tue, 11 Nov 2025 19:53:44 GMT  
		Size: 2.1 MB (2116229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980cdc8ef63534c4f1edd0307446063a5edf12bd309e2b3c589810fabfc6d4a5`  
		Last Modified: Tue, 11 Nov 2025 19:53:45 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json
