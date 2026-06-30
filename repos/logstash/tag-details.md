<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.17`](#logstash81917)
-	[`logstash:9.3.6`](#logstash936)
-	[`logstash:9.4.2`](#logstash942)

## `logstash:8.19.17`

```console
$ docker pull logstash@sha256:b92e83c51ade92313bc35a0a300df258593b432585f90579081f8d30b4dc0db7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.17` - linux; amd64

```console
$ docker pull logstash@sha256:969dab6353f08ec7ed2e87c15d7eeab99068394e259d995a2e02073a8bea92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.1 MB (538060693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2863389df4b27ee63f58e6fd82e1b6cf70a59d06ef1883f905aede7c91e188`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 18:50:15 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 23 Jun 2026 18:50:15 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.17-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.17 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jun 2026 18:50:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:50:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:50:39 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 23 Jun 2026 18:50:39 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 23 Jun 2026 18:50:39 GMT
USER 1000
# Tue, 23 Jun 2026 18:50:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jun 2026 18:50:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.17 org.opencontainers.image.version=8.19.17 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-06-16T22:44:47+00:00 org.opencontainers.image.created=2026-06-16T22:44:47+00:00
# Tue, 23 Jun 2026 18:50:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d57e49ea1c89a495677db8b073e6dcdaa382cbc3b73dc44487972d123839f21`  
		Last Modified: Tue, 23 Jun 2026 18:51:16 GMT  
		Size: 50.1 MB (50058205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f04bd36440124ba4e9ac497cc220648e76a5dd2c1079fc3d90cd6310b92ec6e`  
		Last Modified: Tue, 23 Jun 2026 18:51:13 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227e52dcdc8030d915b19ae901559e1d70a72bcd56858b7df6caa0cf54abac3`  
		Last Modified: Tue, 23 Jun 2026 18:51:26 GMT  
		Size: 458.0 MB (458001946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab7c631979fc5d255ba11c3359f1741488cf02ed1124130c4066b6fef947555`  
		Last Modified: Tue, 23 Jun 2026 18:51:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2a26929b597af196fca4a04bc2b6ef28e36ec8cb87a3077ce34dcb54e537d`  
		Last Modified: Tue, 23 Jun 2026 18:51:15 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bf37f4ae9fa09b965fef013161e6940d0c0ba5c4400b5315f62f49feb1cb46`  
		Last Modified: Tue, 23 Jun 2026 18:51:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a6842ca2892b405eabce1a91787fb9ead5f03de1235dd9d472ca497324d5e4`  
		Last Modified: Tue, 23 Jun 2026 18:51:17 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ed3395d0410115ea66ab41985d3b67ea3703dafd8241c6404f7677edbfba1`  
		Last Modified: Tue, 23 Jun 2026 18:51:17 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89eecc8410d841ec7dc5fa1260ef4cc000a32d12017efe40a2c0578c3bb1ff`  
		Last Modified: Tue, 23 Jun 2026 18:51:18 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825e1ef73b4bff3ebe559a2c1dd1a46f0ad5e71d272d88653284d3cc3c021ae1`  
		Last Modified: Tue, 23 Jun 2026 18:51:18 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba3fb7a0b01944aab181985626c1acaae43c585fa114fdd9564a294c389279`  
		Last Modified: Tue, 23 Jun 2026 18:51:18 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.17` - unknown; unknown

```console
$ docker pull logstash@sha256:3bf274ab2cfcc90d337d3df76fcc1b5be6bf59604d7c6ad6024186772d7c3588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371a597411987b6b43670a35785ab23154517a2e2dfc73ce3acaa68cea13c01a`

```dockerfile
```

-	Layers:
	-	`sha256:43d5be70aa45a51f20f31db058fdc15e349a7eeef58d07a1783fb0dd9f60e484`  
		Last Modified: Tue, 23 Jun 2026 18:51:14 GMT  
		Size: 3.7 MB (3678254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf4d2950bbb679d94a2045f1a0649b78f3f7e37df1b4116ad02ac83ae692eab`  
		Last Modified: Tue, 23 Jun 2026 18:51:13 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.17` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:b0608b3fdf881b4bb65174c2b51bcc575a8b174ad71b4d756b98c98e16370bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.3 MB (536317077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bce373b548fe09f6866a373b137e94b9ad21cb8ff7d8a5f331578f8dc77f97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 18:49:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 23 Jun 2026 18:49:20 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 23 Jun 2026 18:49:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.17-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.17 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jun 2026 18:49:47 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jun 2026 18:49:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:49:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:49:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 23 Jun 2026 18:49:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 23 Jun 2026 18:49:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 23 Jun 2026 18:49:48 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 23 Jun 2026 18:49:48 GMT
USER 1000
# Tue, 23 Jun 2026 18:49:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jun 2026 18:49:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.17 org.opencontainers.image.version=8.19.17 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-06-16T22:44:47+00:00 org.opencontainers.image.created=2026-06-16T22:44:47+00:00
# Tue, 23 Jun 2026 18:49:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2718ee952508675555e86bb4257be16ebcad1c3a596f5c9fcc198b9032e344e`  
		Last Modified: Tue, 23 Jun 2026 18:50:29 GMT  
		Size: 50.9 MB (50872037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676d595f039c81dbb58b92fbfcded154def34dee30c37f66fd0448ba0840343`  
		Last Modified: Tue, 23 Jun 2026 18:50:26 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a8c9aac4e775d4160d78f2eff9f21d1e16d6e8297eb6ae5eeaf9f67c3e0fd`  
		Last Modified: Tue, 23 Jun 2026 18:50:39 GMT  
		Size: 456.3 MB (456300885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5cc3df7b0079abcf9edb63d98b2abcb634ce72f37eb1c96dbd3c0043f50da5`  
		Last Modified: Tue, 23 Jun 2026 18:50:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2571352312e3a5f5a668b1f2259af86380889c2199cc2998bf667a337542bcf`  
		Last Modified: Tue, 23 Jun 2026 18:50:28 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3820c0228c4ff79b23b54697784c57d2db65191fe60a364a267010ba416f6d69`  
		Last Modified: Tue, 23 Jun 2026 18:50:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6342bf2689c0432655b1b2945217cb620f0e6fc929cb36ac3102f386e513d3c1`  
		Last Modified: Tue, 23 Jun 2026 18:50:29 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde6c4f7848b3c1eb97e3d8528fa284803747b7ff39cd3ba177f9f52a9ebdfe0`  
		Last Modified: Tue, 23 Jun 2026 18:50:29 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ef80c6e6a87d8c3899c94c8450148a19ed5dbffe1553609269ef0b46a604c`  
		Last Modified: Tue, 23 Jun 2026 18:50:31 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b030905afdab731de38e93ee8c539d54288f7f096e9e45eb55c8f4ab239d29`  
		Last Modified: Tue, 23 Jun 2026 18:50:31 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1541f5d8ce0909d4a674013403b1ad057d03d0bd79da3cbb32a7172d691b409`  
		Last Modified: Tue, 23 Jun 2026 18:50:31 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.17` - unknown; unknown

```console
$ docker pull logstash@sha256:4ecd54c8579d0c2fc2f883e3597fed994ccac0a6539972201bd1d4d47cce6d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d3bec8abf2a4eeebe1c95049598073ade5de475ff337a944fe71a915f1561c`

```dockerfile
```

-	Layers:
	-	`sha256:d409d2053a6b5773f66944dd5d36caeab04d7d7fa342ce8cf269dccbe0e1c754`  
		Last Modified: Tue, 23 Jun 2026 18:50:27 GMT  
		Size: 3.7 MB (3678679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01444a825806ce7c119d228a2c0376c491343c8e5d8a7c9155f0096321c853b9`  
		Last Modified: Tue, 23 Jun 2026 18:50:26 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.6`

```console
$ docker pull logstash@sha256:6d45247f67fcffae3af55806ebd500362737be3cb34ff35e74f4cf6b0cbb3302
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.6` - linux; amd64

```console
$ docker pull logstash@sha256:17fa7f14a0baae5561ce5bbf97535ee301c84dac9822ee110c29a2ec7d601197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518156069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcaf1c68d42309b19be14fa099cc4473b8b7024500a4fb0e5a5a8fe21047a64a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:14:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:14:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:14:25 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 00:14:25 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 00:14:27 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:15:25 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 00:15:25 GMT
USER 1000
# Tue, 30 Jun 2026 00:15:25 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 00:15:25 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 00:15:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232c81f04c249259d96bb17601f33aba2b17a892c4bfc2c9ab8955cfb2b7d7d7`  
		Last Modified: Tue, 30 Jun 2026 00:16:02 GMT  
		Size: 4.8 MB (4774934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7316a09552534dedf520318d3e3901de48728a575794fe6d6fbcdd32a8465b2e`  
		Last Modified: Tue, 30 Jun 2026 00:16:13 GMT  
		Size: 472.4 MB (472429585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1f3b52df85c7b737e33378d2071ee92abd52abec12e31cb575869ab2432202`  
		Last Modified: Tue, 30 Jun 2026 00:16:01 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae8de5e1e41bdbac638ba826679728bc37e8009451a10e0f6f5d61d186fdc79`  
		Last Modified: Tue, 30 Jun 2026 00:16:01 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8fe2d4473e5f477917f2868fd97e853a1025c62b0a9dc564375df935d839a8`  
		Last Modified: Tue, 30 Jun 2026 00:16:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47405ab25f90580292c05839cf2fbe21da362d5ccb66d58eb515fe4a9f1b8fac`  
		Last Modified: Tue, 30 Jun 2026 00:16:03 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79316ff5a55ba3feb57493cb829cb8eb5cdbc0c20eeb2893ba9a0ecf91a7b7c2`  
		Last Modified: Tue, 30 Jun 2026 00:16:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903bf3c070b2e7d81ade453230f74cf06d3b69634cab417699e9bfb76cbd686`  
		Last Modified: Tue, 30 Jun 2026 00:16:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e606fdd702f64cea84fbfe4228908c7107edc8837cff871194436aa6f26e3`  
		Last Modified: Tue, 30 Jun 2026 00:16:04 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:85c1c05e08936c02b13c061eae1c78bb4bf5a2682f73c39eb61f2d443b7c49a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b38b8452670aad0c1e92576ff3936543fa18916e366c1db1d3474d94573734`

```dockerfile
```

-	Layers:
	-	`sha256:1489721b7c0d8bf6ed4328e0bac054ddaa62bd77794c6e04e63ef2ecc84bebe3`  
		Last Modified: Tue, 30 Jun 2026 00:16:01 GMT  
		Size: 2.1 MB (2109708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e65e9b5ef990752c6769c155a328caf7fc170995b04994231d05b0d81813a7`  
		Last Modified: Tue, 30 Jun 2026 00:16:01 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:fad873e91dbab599cc11ecf0d915f5a4d2e6284e6ad416fc47e86a7fe0824268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514561559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044e53edf09d8d34b68b77acaf70a9d2204e7280cd8c0e0f23c9eca7126bbd7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:12:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:12:58 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 00:12:58 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 00:13:00 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:13:57 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 00:13:57 GMT
USER 1000
# Tue, 30 Jun 2026 00:13:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 00:13:57 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 00:13:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47373fd3e0102f2f90343424da31465e24d97f3d4064544b9dd1d888d5d511b8`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 4.8 MB (4759842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60cb813c44cf8ccb2baf2e5db5e3c346ac7b7629a9850951f1936b63822525`  
		Last Modified: Tue, 30 Jun 2026 00:14:47 GMT  
		Size: 470.7 MB (470717534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72051e264161da24738fd82782297d332e41876b4cb99758ce362cdd974ef7ff`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3bd122e13bb14fad536c0ad1a943e8c62f23a7d7fd68143bf110d8d9ef584d`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa135a56398c31d70538cbf9af2af2286129fb892ab12ff0e0d933b69ee49153`  
		Last Modified: Tue, 30 Jun 2026 00:14:36 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7543269d6c5f9a3e00010d25f6841c82733d0b01298bbbb6de3f78dab05f8e91`  
		Last Modified: Tue, 30 Jun 2026 00:14:36 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43af72d6546760afa830ec745ca7ead1f2038f84fc62f24b0337300ef0f79ab5`  
		Last Modified: Tue, 30 Jun 2026 00:14:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1179e3167a195227197d5c756fe35e37cf50b99dd041ce8871ccfa55f953c8fa`  
		Last Modified: Tue, 30 Jun 2026 00:14:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8475553239fcfc0fe75228994c20fe6e1ef45e192b51fc182ce8699b1b043`  
		Last Modified: Tue, 30 Jun 2026 00:14:38 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:d8916b0f0626022bed81bf993053a6b94b906bdd420d355e129770d7769c837f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96ce98f69eda2f0dbb27d43976e2458ba118def20ffb5dad59f2a07d1461a45`

```dockerfile
```

-	Layers:
	-	`sha256:6e8a214d0e65e9a8510ccd7a47da34c594ab5490e54d9b1b3f0485ed0142597a`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 2.1 MB (2108496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b234a254a7923785264e1d8c16732b1e8d717f4c963b8ab5ea949bb212a4c33`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:bf13a8d0fc344604d3f8c458a7beeb23be987e6a62956439c72673632645d029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:511e619707a3117caf4e1fa07af72cc27aecf6c1e1a8f4e391ca50a251b3f23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524441358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83058fd82fb3e4a7c28b9d61e224222d88c23a4451a1036ee84ede3a85f82142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:15:59 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:15:59 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:15:59 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 00:15:59 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 00:16:01 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:16:52 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:16:53 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 00:16:53 GMT
USER 1000
# Tue, 30 Jun 2026 00:16:53 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 00:16:53 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 00:16:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdffa0d4d6fea0aedb3b86ca2fd1370cbec71f2fa975f33ee6bf8b6549bc8e3`  
		Last Modified: Tue, 30 Jun 2026 00:17:32 GMT  
		Size: 4.8 MB (4774898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8fa7dc84e6aabb64efafd36b4624bde86a77abd38aba1a5299bef5831e0d03`  
		Last Modified: Tue, 30 Jun 2026 00:17:42 GMT  
		Size: 478.7 MB (478714835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91622ab7565977fa9a9345b9fada8918c3f125062fed6960fb51f9e060e32fc7`  
		Last Modified: Tue, 30 Jun 2026 00:17:32 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8241d64c9f16fea9ebf45e4d73986cebcf300eade92c1345524c7d8cb2484`  
		Last Modified: Tue, 30 Jun 2026 00:17:32 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24d0083d95fe35f5605ce9dd2cbfb0306fa0307b58a8bc670373b44a0fcf845`  
		Last Modified: Tue, 30 Jun 2026 00:17:33 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc15daf5788eff1165a9673018172d889d49ab5d484c9e88fec3ea8dd05801b`  
		Last Modified: Tue, 30 Jun 2026 00:17:33 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea84eb51461dcdc6fb0d8bd27c1f343007b0b52577eadba4eacbb52ff882bd3`  
		Last Modified: Tue, 30 Jun 2026 00:17:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a9ed97e32d1081093a2cd9ce74dbe35ffcaedeb31200fdaca556e7743fae81`  
		Last Modified: Tue, 30 Jun 2026 00:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c377f01f6698dcf40376d3b4235fe95dcffed9a2ca3fc34dd94579ccdfe72ca2`  
		Last Modified: Tue, 30 Jun 2026 00:17:35 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:5a23db07e9f77554003d970cc7874a6a52cb5a77dbe67e23bf97f8f6880b9670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a3bb733fa6f8cb446a9a8c08f25e67741bde458864c2d5cdc769afbb0d4c88`

```dockerfile
```

-	Layers:
	-	`sha256:40b29cdd5f64150ae2ab026d930acceed0eb7136ec398e02a88347f35ad72638`  
		Last Modified: Tue, 30 Jun 2026 00:17:31 GMT  
		Size: 2.1 MB (2117931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0593c4c1b44a820e5407f7d6bd10f92afbe859eb4d25ad18bc1ac330ae7a22dc`  
		Last Modified: Tue, 30 Jun 2026 00:17:31 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c9ece513df1f7bc722e918a4db96b6359e3b4a6dff1cc4a8f62db90fc57e2d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520855089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31c2cd72fdde1192c1cba750073ccd6e39117273a9616e783c5752dee49ab9c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:12:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:12:58 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 00:12:58 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 00:13:00 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:17:00 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 00:17:00 GMT
USER 1000
# Tue, 30 Jun 2026 00:17:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 00:17:00 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 00:17:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47373fd3e0102f2f90343424da31465e24d97f3d4064544b9dd1d888d5d511b8`  
		Last Modified: Tue, 30 Jun 2026 00:14:35 GMT  
		Size: 4.8 MB (4759842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072f4fd6f16ab2dda24bc75fba34d01979c46e9e34148a0333ce8cef2b4f183`  
		Last Modified: Tue, 30 Jun 2026 00:17:49 GMT  
		Size: 477.0 MB (477010989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add4c2455839da60032e8c1d686892ae70cc7ac3bced8718bf07ae0cbcd61c88`  
		Last Modified: Tue, 30 Jun 2026 00:17:39 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503b8c0c8497c1bbd2dd00dd85b4c8856a9a02350c85e4ab1a1f8b8420fd4af6`  
		Last Modified: Tue, 30 Jun 2026 00:17:39 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ccc7efcfaede1c426b79f0f83c2fbafe88a98b6c80bad1613985bca0e497c7`  
		Last Modified: Tue, 30 Jun 2026 00:17:39 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568c880dc7c8d282e1aed9d15c15b66217411359a6ec23d80b11e2ab29228ee`  
		Last Modified: Tue, 30 Jun 2026 00:17:40 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734d0b9febcf86696600480555789fb01486bf114e9557053bfc27eb7d8a18c`  
		Last Modified: Tue, 30 Jun 2026 00:17:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358bbd888313f1ed96681b6200aa8f67efc21af33a3ebd41851c341d0241c03e`  
		Last Modified: Tue, 30 Jun 2026 00:17:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be29a7f475cd79f781e63f6ff17f5e1344ebc7913d570a3646a57017025e75`  
		Last Modified: Tue, 30 Jun 2026 00:17:42 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:882562f99d33ec8da4ad0bb6b0c7f5904fe928f9560681218d7a6cc8ec1bc371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aade6780c18cfbe898c13575916a63103ff56199974033d9d2f919874cd02950`

```dockerfile
```

-	Layers:
	-	`sha256:5884e1616a23d552ff2bbe7cb69d8637d0641760ce07f5aa8922930772b1bb3d`  
		Last Modified: Tue, 30 Jun 2026 00:17:39 GMT  
		Size: 2.1 MB (2116719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12765b5cc913f182a25132cf28a0ede7a1c430617919c0f49e471bdb343b1af0`  
		Last Modified: Tue, 30 Jun 2026 00:17:39 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
