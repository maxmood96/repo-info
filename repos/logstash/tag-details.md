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
$ docker pull logstash@sha256:bf2273fc0924e1d26540b7bf82e2c61aabf626e94510d20b1aed786955021e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.6` - linux; amd64

```console
$ docker pull logstash@sha256:bf9047a916e307be9f27aaf527b859875f3e6b5df014be0e888fca4cecbe3da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f04bd5e4ba73f032d5ae36f02fc2fab9cad9394c98f58921b4947ffb32e7b4d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Tue, 23 Jun 2026 18:50:15 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:50:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:50:15 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 23 Jun 2026 18:50:15 GMT
WORKDIR /usr/share
# Tue, 23 Jun 2026 18:50:17 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:50:47 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jun 2026 18:50:47 GMT
USER 1000
# Tue, 23 Jun 2026 18:50:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jun 2026 18:50:47 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 23 Jun 2026 18:50:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c7ac8096ae3d30d90610825f957215126959c5585d5aaf5daa75fa7f067ad`  
		Last Modified: Tue, 23 Jun 2026 18:51:24 GMT  
		Size: 4.8 MB (4775121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99865ac4676a85617e9f759d1ab5f61057959da6bd88081168ff3f8c225e8b8`  
		Last Modified: Tue, 23 Jun 2026 18:51:36 GMT  
		Size: 472.4 MB (472430161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ea899fbbc75eff760aa24511afb83924e7eee548cbea1cac1fb888a7908dc`  
		Last Modified: Tue, 23 Jun 2026 18:51:24 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9c90ba2aced0fc679b844b7bf03d637fa649cf28c50dfcca34deaa4b8aa49c`  
		Last Modified: Tue, 23 Jun 2026 18:51:24 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989ac445ec4e1e3004cc77d8b4afd42ff46ab1976540f456e1793c218890a95`  
		Last Modified: Tue, 23 Jun 2026 18:51:25 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67301ffe5877b919c5b1a731cbcdf86522b4e99cd29e4c28c5288137b5ee8e4c`  
		Last Modified: Tue, 23 Jun 2026 18:51:25 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56608fd6336c87010ff96101d5b7c87b3b051045ab8500c60de79bfb67944d8`  
		Last Modified: Tue, 23 Jun 2026 18:51:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2d295c3a513f7e94915ec719c364c0ef6d5789bc858de7bff44d9d024b8bcc`  
		Last Modified: Tue, 23 Jun 2026 18:51:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453c2d07552ebafb1d690b96a43d3b4d80004c25b1bb035f20fb71e7df66c590`  
		Last Modified: Tue, 23 Jun 2026 18:51:26 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:0a1d720a47a22b9faa3264e198ead5f30d9c41be74865361ddbbd27bb9584eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e319537c620ac3206e305b1857b184d623186de6e3a7c667a30a931267beac09`

```dockerfile
```

-	Layers:
	-	`sha256:38588eacba89cf70da6b47b3d337f8ce0792ea829201b2aa07be8560e644f3c7`  
		Last Modified: Tue, 23 Jun 2026 18:51:24 GMT  
		Size: 2.1 MB (2109674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331cc67f35c2de04bd57759ef89db0e07705b61b46ec9271f6076bfc0d24e25a`  
		Last Modified: Tue, 23 Jun 2026 18:51:24 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eb25c33ea69d5685f7d1f2f4613eb4277d0a9272d74dadd133c9f403bd34b4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514624442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803c71aff39c8e87a8092cbec682c11703e9b2e7b4393968b2f4c855f7c03e30`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Tue, 23 Jun 2026 18:49:21 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:49:21 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:49:21 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 23 Jun 2026 18:49:21 GMT
WORKDIR /usr/share
# Tue, 23 Jun 2026 18:49:23 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 23 Jun 2026 18:49:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 23 Jun 2026 18:49:56 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 23 Jun 2026 18:49:56 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 23 Jun 2026 18:49:56 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 23 Jun 2026 18:49:56 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 23 Jun 2026 18:49:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 23 Jun 2026 18:49:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 23 Jun 2026 18:49:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:49:57 GMT
WORKDIR /usr/share/logstash
# Tue, 23 Jun 2026 18:49:57 GMT
USER 1000
# Tue, 23 Jun 2026 18:49:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 23 Jun 2026 18:49:57 GMT
LABEL org.label-schema.build-date=2026-06-16T22:41:23+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-16T22:41:23+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 23 Jun 2026 18:49:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2cf8fbe47b75d3aa645884059a7dfe670abeecc67df407e503873d5b719f16`  
		Last Modified: Tue, 23 Jun 2026 18:50:35 GMT  
		Size: 4.8 MB (4769185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2e7f8eca31db7b5c74b4a2d82b3bc3a59f176ad6d363d26e0afe653c64910e`  
		Last Modified: Tue, 23 Jun 2026 18:50:46 GMT  
		Size: 470.7 MB (470717492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5b26874f88208900f116c80a8142efc35f5cdf5b2f8c86125f1c34050a15bf`  
		Last Modified: Tue, 23 Jun 2026 18:50:34 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7099874df8908fc79b7b8cfebdeab3c84d49bcb87c246ac25f0e5fc847147bb2`  
		Last Modified: Tue, 23 Jun 2026 18:50:35 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cb7a1a79ab9e94a996185b33b8b036adb0903670f6f6dbe1326b243683c272`  
		Last Modified: Tue, 23 Jun 2026 18:50:36 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfaeb19290dd928939d4c03a4218c91349999e6f547e07e089812242e9e7862`  
		Last Modified: Tue, 23 Jun 2026 18:50:36 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921c5e6e31138968d4c0e467adb82a2bacf8c7419735baa3233564f5e6198307`  
		Last Modified: Tue, 23 Jun 2026 18:50:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ade8f4214d40eda584b66a76efcbe8840b9c6efb47c00780a9b5780b446f3`  
		Last Modified: Tue, 23 Jun 2026 18:50:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917928d3295f1df911959da2046672eeb9a0204a1839cb94a13d76242df8235`  
		Last Modified: Tue, 23 Jun 2026 18:50:37 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.6` - unknown; unknown

```console
$ docker pull logstash@sha256:887def7ff6c2533b70efda4f2cc09431a3f274fdd9ca922275a06438077a6a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62c349343ac9099de0fde89e75c3d7ba0513b1b384b4786f9bbd1e67f28fab2`

```dockerfile
```

-	Layers:
	-	`sha256:e1b6b6d9b04093a30bf347d9bdb45b0731999899f96bdacef1fe1ce53000421e`  
		Last Modified: Tue, 23 Jun 2026 18:50:35 GMT  
		Size: 2.1 MB (2110244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056224a1286e449cd18e716a0451d1b5523faa59e022cbedf7ccbdd64df6db84`  
		Last Modified: Tue, 23 Jun 2026 18:50:34 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:648a781b7360736754a9f583f7819d166be9dcee42d272bbce7d67278f529398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:757cbff166ca2e68887ca89c60ff8082c1f6fcfa920efb80db931c8a51a0ea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524435028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f798eb45116e783bac26177364cf2f39d48492075d1e0c45053d160e0e68a2a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:15:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:10 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:15:10 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:15:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:16:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:16:05 GMT
USER 1000
# Mon, 15 Jun 2026 23:16:05 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:16:05 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:16:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d3afa2da55aebe1433c4e560b1e3190d53420e1185a6fb24dbd147ced548e`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 4.8 MB (4775109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4eefa873493c008faa123f0343a5d298310c0c0e3c5e01f8a9b531867594db`  
		Last Modified: Mon, 15 Jun 2026 23:16:54 GMT  
		Size: 478.7 MB (478714901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5bdb6058a800ae9b083ef950ebacd167dff4b3817d774634d039bd96554b8b`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993c936a52c2113b66d15fcba049cb80e5c26785a5133a2bc5132935d453470`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 255.2 KB (255191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0105efd551d3f43e5655b08921d0eb2df2a4339ab7f0662046061b15ee00feb3`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118e4f4a5f36a0743ddb3aab006d0044ec1a4912851728acd871d899e64e430`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f330cca4c8365005afebf7e87e762b34871dbd9a5f918534f9844fb13f001ed`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9368e0d0772fa36a4d43240280333213eeab0acf21dfeb03ebbef67ddb0fe`  
		Last Modified: Mon, 15 Jun 2026 23:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7178dda110a6f8dc24e7178ba8e6b2f81e3ae508f363b6170520c4cc6f042d`  
		Last Modified: Mon, 15 Jun 2026 23:16:44 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b45c2106aad26bb65843cce45404dad7e01def23323bf9c9b9b3391cacbd1cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e58da10d20376f80c9454e4e7a6687bebd427057ed370050455428b18f82f5`

```dockerfile
```

-	Layers:
	-	`sha256:9a3d51a453084c5a61de746fdaac073e266aaf600f3390a1de397a77ce47bc7d`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 2.1 MB (2117897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e790a31c51dc1f75ac8058bf18d00bf95060534558a7f27b58b29cd36f62fc2`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:12fa0622b470f87267310eb3881f543336d19daead5bae58047f2c71001c89ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520917841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0145bd4e28433030a02f4196340b2774aadde8c73810e27597dea87bd1f0c90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:31 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:14:31 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:31 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:14:31 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:14:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:15:31 GMT
USER 1000
# Mon, 15 Jun 2026 23:15:31 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:15:31 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:15:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fd8f1e7ce7cbb741ef49b9bc9fdb148993453ba881f04614af92f5e83a59fb`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 4.8 MB (4769159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32581674843d054565b7213a821949a4df2e0493cd4dba407b50ec832b96136c`  
		Last Modified: Mon, 15 Jun 2026 23:16:21 GMT  
		Size: 477.0 MB (477010847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cac5f5f25088452c06d856becd206d110cb7e3cfce691211a051e24eb51cb7`  
		Last Modified: Mon, 15 Jun 2026 23:16:10 GMT  
		Size: 6.4 KB (6364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e67b1ff21af1237c58dcce1649a1d960ba49fcceb9224be5b4dc515425d58a`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe8542a67266909d942641983fa45bc1deb5ef5a203473adddfbdbee9f7097`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e8a22dd39224a492ca9357a3caa10522c06f5fecc42dfbb2301f591fed0f4e`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74425dc94b44c678381611bdcc27be0990636d5bd2dc2e88781d581d06273f00`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529fc3d3e0abadc067571d95bac95534c17bee2174468cb8fd27d3c9cba8389a`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d66d2c19d56b7b71e1ab014ddff9f424b3afb8573de330e74d57607746a85`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:7b060c670a0d88ff0e8656529f4891ed49fa92f504b67ee8fcfd19331901d228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c045d60409e09b3fd414a541ae035e68142421a65cc63a71ad2d470a25e2324`

```dockerfile
```

-	Layers:
	-	`sha256:22838af172254b3fec2e43209e78ff20358dd37cc698fef9f4b3fee66a72f932`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 2.1 MB (2118467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9139f2547203d2600d2eb07717c6a3d59f481af0b808ff61d46cb2054646df`  
		Last Modified: Mon, 15 Jun 2026 23:16:10 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
