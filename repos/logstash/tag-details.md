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
$ docker pull logstash@sha256:ad4cd2e7d62590201dac782275711ef12165eee10da9758e3dfb28ba554fa873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.6` - linux; amd64

```console
$ docker pull logstash@sha256:77bc8d33b44ae480d0795b646955bd13b7d6bf482cd8904c316ee6349c092063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518159617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1367430155d41f1171dc5968ac3deaa2677f0f7e148ab86f31fa2d56a1618a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:31 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:27:31 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:27:31 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 25 Jun 2026 23:27:31 GMT
WORKDIR /usr/share
# Thu, 25 Jun 2026 23:27:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:28:30 GMT
WORKDIR /usr/share/logstash
# Thu, 25 Jun 2026 23:28:30 GMT
USER 1000
# Thu, 25 Jun 2026 23:28:30 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 25 Jun 2026 23:28:30 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 25 Jun 2026 23:28:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd179466b6751d253690e6275fa11ed9fe4d496c1d132a646fb5feaf061ddf80`  
		Last Modified: Thu, 25 Jun 2026 23:29:04 GMT  
		Size: 4.8 MB (4775841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9024d78b552259592bf928a35bfdd0993fae90ca7f524d0df3edf7862ea594f2`  
		Last Modified: Thu, 25 Jun 2026 23:29:13 GMT  
		Size: 472.4 MB (472429759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbc83e1fd066e9c454615e6a2ba680f364b54ec7d027e46cb35425671dd290`  
		Last Modified: Thu, 25 Jun 2026 23:29:03 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cd923bba21c11dc72c7a0b224f672e7e845cb0c5b8de3fc95eaa10a05cd80`  
		Last Modified: Thu, 25 Jun 2026 23:29:03 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e2d7fe844f2bb46f23c4b57c2a1d73850eb7153b1c3613206b582ba86994e`  
		Last Modified: Thu, 25 Jun 2026 23:29:05 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e90527e89f41c8f6ea056c0869cccb4d87817ed9e290f116cab08d0308edfc`  
		Last Modified: Thu, 25 Jun 2026 23:29:05 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a70f2807efe85ff7e3a47c5a6644e3eb546d8656e142d5ee6fca27422daa5`  
		Last Modified: Thu, 25 Jun 2026 23:29:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b048c609df23d74b3259f00e26950e35fa89483303f3ba6315ffbf6b41eefc0`  
		Last Modified: Thu, 25 Jun 2026 23:29:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f03bc7e8525732092f782b92c522f0c3f9af933ee4fcd79ee43de33a48daae`  
		Last Modified: Thu, 25 Jun 2026 23:29:06 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:29968639c3fbf2318575643bcf25c39d8130154d35a92c443677284758fea5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd526f4fe52badc69987193a3944009cf1517d82534a956f1b86da122da353d`

```dockerfile
```

-	Layers:
	-	`sha256:9459818e2fb4277e189c49f2620d908a03486d09ff1714f7494868ada2ab9cb7`  
		Last Modified: Thu, 25 Jun 2026 23:29:03 GMT  
		Size: 2.1 MB (2109700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6824f54b0e3343cd4fac432d57441dc1581804c33b57b9572dbd88a457dadace`  
		Last Modified: Thu, 25 Jun 2026 23:29:03 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e257d62c1ce6c6e64b171651e586e2917cc936f3a8a8533396138cd44f7c8324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514560253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777a27eae2a09749b608732d518d0c6b67a5d8b407dfa8a0c97904adb142106d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:48 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:26:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:48 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 25 Jun 2026 23:26:48 GMT
WORKDIR /usr/share
# Thu, 25 Jun 2026 23:26:49 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 25 Jun 2026 23:27:17 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 25 Jun 2026 23:27:18 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:18 GMT
WORKDIR /usr/share/logstash
# Thu, 25 Jun 2026 23:27:18 GMT
USER 1000
# Thu, 25 Jun 2026 23:27:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 25 Jun 2026 23:27:18 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 25 Jun 2026 23:27:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197a86bf4854bc0d8dfb5d6d7192dbf9eb50a92c5fa93818a5d4b1898867dee`  
		Last Modified: Thu, 25 Jun 2026 23:27:55 GMT  
		Size: 4.8 MB (4760086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789ea02604b341a516d963644de9d4bd1413eb50f1921a8ce8b320eaf91fafa5`  
		Last Modified: Thu, 25 Jun 2026 23:28:04 GMT  
		Size: 470.7 MB (470717312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b7d878ebbbf812a76b4ac2a91108a593bfd488fd756d2615f68e37b61219`  
		Last Modified: Thu, 25 Jun 2026 23:27:55 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec8b388ea79be91115e20d45f0ebeb347dd9c97531210389d8b48911e49411`  
		Last Modified: Thu, 25 Jun 2026 23:27:55 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8831735de52b1fe58f4cd79113653480eebb0d404ec934208260bed7cc026b`  
		Last Modified: Thu, 25 Jun 2026 23:27:56 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ef9c3c7687743def768788c394af0c73e49e9eeb11fb12a05b665f059ded1b`  
		Last Modified: Thu, 25 Jun 2026 23:27:56 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5d8cba8e3263a4a85632af1d6b92e2e69463128d0f77bd05d7709612912d93`  
		Last Modified: Thu, 25 Jun 2026 23:27:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04c3cb6fa3d5e9e0eaeb2c203f2a8357ae2834143800140ef676f29ab2a5e9b`  
		Last Modified: Thu, 25 Jun 2026 23:27:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648aef47e59b962b53d12cf1e7c648470b9ed82980a81a0e33918e8ddd46bef6`  
		Last Modified: Thu, 25 Jun 2026 23:27:58 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:f0112b5fdc5b7a9190694041f05c3803fb4a112a0d9fedc0dd956a2deced1e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2da4553fd888164259682f9663190216d834b676c68c69dea3d2e98bedbed0`

```dockerfile
```

-	Layers:
	-	`sha256:1f185246774038b755fd27251f18e308badc295d4ffeb1656f4a6479319d1a16`  
		Last Modified: Thu, 25 Jun 2026 23:27:55 GMT  
		Size: 2.1 MB (2108488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66e98fdb2aa541a9577468ee7473d8bbe7d053fac0cbd0c4de8b6dfab88850c`  
		Last Modified: Thu, 25 Jun 2026 23:27:55 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:bcf269d134b058ea0ef8bf1cb9ea84450c495a1930813b07ccc211176c3f759e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:7576256605690085b3939095bcd97a52bceee7ad1f281517f0b579c006a3f13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524444753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257fd4d4b73a1de7ca3238f637afe0a43d4f489c6e8d529e74aef6333e2af6db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:33 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:27:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:27:33 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 25 Jun 2026 23:27:33 GMT
WORKDIR /usr/share
# Thu, 25 Jun 2026 23:27:35 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
WORKDIR /usr/share/logstash
# Thu, 25 Jun 2026 23:27:56 GMT
USER 1000
# Thu, 25 Jun 2026 23:27:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 25 Jun 2026 23:27:56 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 25 Jun 2026 23:27:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087e281bf1f450e78e3c0ccf0dfbbd534ad6f7c35fac98218e5cf26710f838e3`  
		Last Modified: Thu, 25 Jun 2026 23:28:33 GMT  
		Size: 4.8 MB (4775820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e654bcabb6583c71f02512e698a6dfce7efd61bf8db71d5280d328c4b9864940`  
		Last Modified: Thu, 25 Jun 2026 23:28:46 GMT  
		Size: 478.7 MB (478714864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177877df78a23def9f8961232158f6f1a9dafa7562fc70ca9cc813b386a7bd34`  
		Last Modified: Thu, 25 Jun 2026 23:28:33 GMT  
		Size: 6.4 KB (6362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86142672370c8e79da939b66052f9d5f231d8163554aae5ee31f5510c8227dc`  
		Last Modified: Thu, 25 Jun 2026 23:28:33 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac93450387536ddd4e0c7b3b89e1b05a68b5d8bab2fc90eaf33cbc1a7aaa262`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4756218b3754e4341601148883c0fc89c0a46c9f8443601a1f58f4aeb22eb`  
		Last Modified: Thu, 25 Jun 2026 23:28:35 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233abf7c3442c5fdd88460c4b8c536d0d5179e45d42b6ba348cad43bedfef91`  
		Last Modified: Thu, 25 Jun 2026 23:28:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4a335d45691a67b02bb621a78e4afe351de4797ae0f9b1fe458b6049c72e38`  
		Last Modified: Thu, 25 Jun 2026 23:28:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cf246f539b0485d224df46a05cc2ec545bb3f555231de1664344c2c647f9f1`  
		Last Modified: Thu, 25 Jun 2026 23:28:36 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:3a09628ad8d18b3a28311df103f1da21e851d2f97dfd9c8e74bb6c5deb6784bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dc42af9da9cac3c26a45b8cbe22a96d9561de0156c001b72de967c43ba7c74`

```dockerfile
```

-	Layers:
	-	`sha256:5ab1b97b07baf58a8d46ba14d78f7312b00983cde586dd1f0e347ba601ef6dba`  
		Last Modified: Thu, 25 Jun 2026 23:28:33 GMT  
		Size: 2.1 MB (2117923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f337ed49b5d8289fb3dd97f358a0918cae83db693819009f0e8558f2419e23`  
		Last Modified: Thu, 25 Jun 2026 23:28:33 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:44a7fde34c4f6e3fc7e55913dab778e22cb0d2f2e4a8de4d3b0a0bfcb4f105e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520854336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdb0a5d05dfc1a101400795a14e2f4be3e9d24a7d562b8253184a1eb7d9d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:26:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:56 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 25 Jun 2026 23:26:56 GMT
WORKDIR /usr/share
# Thu, 25 Jun 2026 23:26:58 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:27:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 25 Jun 2026 23:27:54 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 25 Jun 2026 23:27:54 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 25 Jun 2026 23:27:54 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
WORKDIR /usr/share/logstash
# Thu, 25 Jun 2026 23:27:55 GMT
USER 1000
# Thu, 25 Jun 2026 23:27:55 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 25 Jun 2026 23:27:55 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 25 Jun 2026 23:27:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e9467fbaa031d3cd94eec204c74758800331531452d17708e0bf330719e`  
		Last Modified: Thu, 25 Jun 2026 23:28:35 GMT  
		Size: 4.8 MB (4760159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03d6ffdb9cbd4a63326cda6297424766efa3b48fa91abb2d5eb8ea68e9964e9`  
		Last Modified: Thu, 25 Jun 2026 23:28:49 GMT  
		Size: 477.0 MB (477011249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba5e83a12e2812ab3ca6c8e1618ecc8798b523b0020bd48626c45f5182313a9`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6550eaace7174671e6520cd37a44fe7dde9a1a589b89f73159d0fb92c83575`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c59f820dd2ae5cf0c27dbe27c97862893b8ee16580cff427c83a094d99cb75`  
		Last Modified: Thu, 25 Jun 2026 23:28:36 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecff5d96990b0c135da2bc596702d3ffe804a97dcad00f3f1d7b37ce3265f02`  
		Last Modified: Thu, 25 Jun 2026 23:28:36 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adbffb598489f6ca9741595e831c4dcd849bd70df58817f88dd533ea22db26e`  
		Last Modified: Thu, 25 Jun 2026 23:28:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac4e80c3b9f49b0f2afc69f4a956232ac851cddecd47304db840e31899d750`  
		Last Modified: Thu, 25 Jun 2026 23:28:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad3fc93a8f2e8d7728ba35d8a7009360439b5e8064260943e151316843ebc6`  
		Last Modified: Thu, 25 Jun 2026 23:28:37 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:375012264fb1f028152b1d1ae362b45629b937144c9052f076ac8e9af88d94ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbeab9b98874aff770e4cabca606ddca50adb7e74668bc90026aa16453f301c`

```dockerfile
```

-	Layers:
	-	`sha256:7dc5ab050be36c6e672434070d3f4ed25f895cd0a00b812dfb09a6d9e293d0cd`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 2.1 MB (2116711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ea3f8b05467e33b6b9ce2dd88594cddcc3ff951fe26633891d1008c3830f4c`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
