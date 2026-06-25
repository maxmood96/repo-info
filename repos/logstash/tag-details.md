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
$ docker pull logstash@sha256:433ad5f85b8f50f8f1ea42e57e7c1cf2241dd7db7af273107d5bed993e112eec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.6` - linux; amd64

```console
$ docker pull logstash@sha256:331eebdea163e4b063982671108d4bbdec6a22c94c8c12281112ae681a586093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518140191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6d298f48eeed2f8ca27301a29fbcc3c174d0f49467e0eb7f5ed152e73233a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:05:00 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:05:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:05:00 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 24 Jun 2026 23:05:00 GMT
WORKDIR /usr/share
# Wed, 24 Jun 2026 23:05:02 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:05:30 GMT
WORKDIR /usr/share/logstash
# Wed, 24 Jun 2026 23:05:30 GMT
USER 1000
# Wed, 24 Jun 2026 23:05:30 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 24 Jun 2026 23:05:30 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 24 Jun 2026 23:05:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab2ea220a94063a1a8f330dcab27c8d11f9974ceb72cd6d3fb725c4b1fe2020`  
		Last Modified: Wed, 24 Jun 2026 23:06:03 GMT  
		Size: 4.8 MB (4774430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d3097225cfc6c11b4229d6747d948bfa7ab5289e1d620536efba5e6dcef5f5`  
		Last Modified: Wed, 24 Jun 2026 23:06:12 GMT  
		Size: 472.4 MB (472429897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70e95ea3ba9c7611b2b4c8bb761c4c40ec4d4a6978bdb43098529fdcd259c03`  
		Last Modified: Wed, 24 Jun 2026 23:06:03 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7816082a6aa6e715bbcbfb38808a12ec33a0087a2c4188b48bd98afe40bcdc`  
		Last Modified: Wed, 24 Jun 2026 23:06:03 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e213149ffe7abc305111e2a5f90f4aef16dd7fa2951a323dd83f4ef9eb7602`  
		Last Modified: Wed, 24 Jun 2026 23:06:04 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dad9d9d585454d20e3799d90925f82065d1e32633c11764bcf8d845300a589`  
		Last Modified: Wed, 24 Jun 2026 23:06:04 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceb32d2cd58b9afb7bcd4628e2925e95af9f838521455add55665b87431b6d`  
		Last Modified: Wed, 24 Jun 2026 23:06:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef919ff0f708300a820c640dc5391778c71f7e6958d52f5431f705d24d682b3e`  
		Last Modified: Wed, 24 Jun 2026 23:06:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2997de54569deea45332f1ed0310cd09aba11f76d2200c16bd5a6f24c42e783b`  
		Last Modified: Wed, 24 Jun 2026 23:06:06 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:23d9d3ee6feb5342aa8f5f2718c2fc0324d55477bea39ad949b5e2dd65e36f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23671624725f24832dbc898bd9028c0c3c24bf5bbfca33dbfc55b629e0872729`

```dockerfile
```

-	Layers:
	-	`sha256:12e9d9f47490ef1991b0740e66268ed8748233544040461fab50cf2eefc362f6`  
		Last Modified: Wed, 24 Jun 2026 23:06:03 GMT  
		Size: 2.1 MB (2109686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6f6a65a4ec962eb2ca4738f216eb00e8c974ade39219f686a89da78344be65`  
		Last Modified: Wed, 24 Jun 2026 23:06:03 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:56fbb9f162c1edfa9c68a64b045537a1bc068971a96a43bca4357a76b105f16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514556998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e5cc154811541acf916b345f4f7bb3e2f627d8df4336b193da81e4c35bc6d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:12 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:04:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 24 Jun 2026 23:04:12 GMT
WORKDIR /usr/share
# Wed, 24 Jun 2026 23:04:14 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:04:43 GMT
WORKDIR /usr/share/logstash
# Wed, 24 Jun 2026 23:04:43 GMT
USER 1000
# Wed, 24 Jun 2026 23:04:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 24 Jun 2026 23:04:43 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 24 Jun 2026 23:04:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221acf4c86c1fb29940d3e98619b6f0cd74cc8607736613116b1274330008f80`  
		Last Modified: Wed, 24 Jun 2026 23:05:21 GMT  
		Size: 4.8 MB (4768995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2a11e1e919c6767faccdad0c7e10d6764def8b5a2449827700e7adaa6c84ba`  
		Last Modified: Wed, 24 Jun 2026 23:05:31 GMT  
		Size: 470.7 MB (470717435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a609279d0e03a2735d2527036250b82dc69e0a395813cbd723e266cb1b733b4`  
		Last Modified: Wed, 24 Jun 2026 23:05:21 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69332173feaed82d0bab21b9b8c11ef85dbda7aa10d86355ef014672e288c0a`  
		Last Modified: Wed, 24 Jun 2026 23:05:21 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47739be8163051e6d38f645efa9d66bd010e1890e9b045aad9e34328aecd8fbe`  
		Last Modified: Wed, 24 Jun 2026 23:05:22 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc79f92c70c8c2391ad68c753d5d2e2529fc0b4893f0460cf5f27baafa1b8ef`  
		Last Modified: Wed, 24 Jun 2026 23:05:22 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af699a2f4f093b4d487d543265a8b2d884fb8a22e8142e6ba858b78fa7b5ebc9`  
		Last Modified: Wed, 24 Jun 2026 23:05:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21281005cc2ed1c722fa72322cf9b4d93234416168209ac0761bb6425c5ec9c3`  
		Last Modified: Wed, 24 Jun 2026 23:05:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e9b84ec6d6975f4808cc8c0969b215571854909c6ec7d8e5f3d644f9ba78e`  
		Last Modified: Wed, 24 Jun 2026 23:05:24 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:1a64f7477a15fe2cf354acf9f64acd1c469e0bbdf3b377889a71a0731e86e7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f91937ef38a0f5add5faa3c006f50c0d6a9d5528083566da745a0e1a2e23f1`

```dockerfile
```

-	Layers:
	-	`sha256:3fa2ab19d7493227fde7d90d250e7df341d5725536bce503dc243cca22a5e726`  
		Last Modified: Wed, 24 Jun 2026 23:05:21 GMT  
		Size: 2.1 MB (2110256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3d9dd51eabec574b5fad0c3d22b8d85c6a7bc1ad92c987b69497c7007e9ab7`  
		Last Modified: Wed, 24 Jun 2026 23:05:21 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:b41263fd1ddae8b7ff8bbf3f4eab600240092af5f72b18f656720d0551131b87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:48c2fcaaed7a9135a6fb97274c0ca8b07af12e151adc231fabe181cf2dbb8a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524424880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a605670f63ed0b69679597452be84e50f744d0c9dad725b4c5dc154be6513a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:05:02 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:05:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:05:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 24 Jun 2026 23:05:02 GMT
WORKDIR /usr/share
# Wed, 24 Jun 2026 23:05:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:06:14 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 24 Jun 2026 23:06:14 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:06:15 GMT
WORKDIR /usr/share/logstash
# Wed, 24 Jun 2026 23:06:15 GMT
USER 1000
# Wed, 24 Jun 2026 23:06:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 24 Jun 2026 23:06:15 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 24 Jun 2026 23:06:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bba6edca3353fcf29fbc745f231878d9bbf22fe39572a349aa7eaeefb6972c`  
		Last Modified: Wed, 24 Jun 2026 23:06:53 GMT  
		Size: 4.8 MB (4774431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732c718a438d32c5747d43884f3a2805bd3f482de13cb4662941e4372fbdee4`  
		Last Modified: Wed, 24 Jun 2026 23:07:04 GMT  
		Size: 478.7 MB (478714498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5461efecfbcca5452b2b51b7e3fd156b09f4a8db215212cc1bb061cfaee94f40`  
		Last Modified: Wed, 24 Jun 2026 23:06:53 GMT  
		Size: 6.4 KB (6364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2baaeb53ae1cc8cdc2e352be91eb48da59ef6b27571254a87bc154b5e6aee20`  
		Last Modified: Wed, 24 Jun 2026 23:06:53 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e647e7fd94e8f04d6723a929fab4d4a60368074fbeee7bc80e9365216505c3`  
		Last Modified: Wed, 24 Jun 2026 23:06:54 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6444206d0538d3336c2d5de40a4199257cee04b9dbc4c97d5d3c8b878b6562`  
		Last Modified: Wed, 24 Jun 2026 23:06:54 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee81cacadb9b0091cd6c30cf94c272da30ad8322ea89980a7e1feb9d8d52533`  
		Last Modified: Wed, 24 Jun 2026 23:06:55 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367219f9d6cafb0194f4752fd00cb18f6c89c53d7487c221a116226e7ccf5edd`  
		Last Modified: Wed, 24 Jun 2026 23:06:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24368ed3d80124c6be36fa885f0e5b8867f4903514985f8eb58b89d44d746561`  
		Last Modified: Wed, 24 Jun 2026 23:06:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:7d9f547449d67470b7baeb340991a5043cc2fa2a3eda64ef7a098b9b4311e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce64573a9e78ec77cb31d9139db46a67790eaaee32703766b5bced255cec54fd`

```dockerfile
```

-	Layers:
	-	`sha256:3e6fa650e2ee43ec964c55cae76bf2d77fb42b7a60878233538d3e2536c02733`  
		Last Modified: Wed, 24 Jun 2026 23:06:53 GMT  
		Size: 2.1 MB (2117909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a88ca8775a640f567b42ba8eb50f3d7f8b8a1e2aec993463938da27ca964f0`  
		Last Modified: Wed, 24 Jun 2026 23:06:53 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:91d6c445c8005a00a5a97c0d979fc56db6aa667ed3e6c3908c59663a6612d539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520850756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3488a0a1df1865f127a0fc1d92ecda02cb891ffad9351505c5ff8ae5a3bcb178`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:14 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:04:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:14 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 24 Jun 2026 23:04:14 GMT
WORKDIR /usr/share
# Wed, 24 Jun 2026 23:04:16 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:04:48 GMT
WORKDIR /usr/share/logstash
# Wed, 24 Jun 2026 23:04:48 GMT
USER 1000
# Wed, 24 Jun 2026 23:04:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 24 Jun 2026 23:04:48 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 24 Jun 2026 23:04:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaacf6d95561ec876afab6d2785317571e1f75eeb3ecec2a33a19db484ec610`  
		Last Modified: Wed, 24 Jun 2026 23:05:28 GMT  
		Size: 4.8 MB (4769003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7099a8143df955959b4f959a2ffd0c5f4bdb5c823250f21d6d3538be6524cf9`  
		Last Modified: Wed, 24 Jun 2026 23:05:38 GMT  
		Size: 477.0 MB (477011116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3926743eab82c90617ec259f9021ebdd1dc4940d9aff69884973c7ca65e60183`  
		Last Modified: Wed, 24 Jun 2026 23:05:27 GMT  
		Size: 6.4 KB (6364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae6aaf60176808e6f6b1f6253e10d89e309fc2670a29bdf70bf716feed07427`  
		Last Modified: Wed, 24 Jun 2026 23:05:28 GMT  
		Size: 255.2 KB (255189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950d69318d07f06357b0ace1fc2e6c8d2b86427763c2ddd94c05e1d015f4bad`  
		Last Modified: Wed, 24 Jun 2026 23:05:29 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47864cae48db1ea8ba78b85efa6395d5931243732cd02a04acf2a90111bcbb9`  
		Last Modified: Wed, 24 Jun 2026 23:05:29 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312dc83278af952ced3ea2329604b18a3577414b65837ec76efe5d5ec04b2223`  
		Last Modified: Wed, 24 Jun 2026 23:05:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa62a7bc3d32ac8d196890f6408a8e18f34d6125079a78afbef88a99cf7eca8`  
		Last Modified: Wed, 24 Jun 2026 23:05:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e7fc047bcf274a6dc0342c9b2269e32f6ce37f7b7335de6451d79c83cdd49e`  
		Last Modified: Wed, 24 Jun 2026 23:05:30 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:f0a385f012684715fb4d2a94c61a3e21bc2819690ede60fa708f85efdf43fa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a64eb130767097a79ac5365ea45854c16518fb6a6e9f9c7cc81bf182ce81ff`

```dockerfile
```

-	Layers:
	-	`sha256:92af06d2082b3a564b9a65d43200cc1bf28dc894b5f8637c618a16de2f967e39`  
		Last Modified: Wed, 24 Jun 2026 23:05:27 GMT  
		Size: 2.1 MB (2118479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2839f5252d07b9548ba2b1b5a35bde7d06e621a20854d3704eacee237a9bf0d5`  
		Last Modified: Wed, 24 Jun 2026 23:05:27 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
