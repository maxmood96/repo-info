<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.18`](#logstash81918)
-	[`logstash:9.3.7`](#logstash937)
-	[`logstash:9.4.3`](#logstash943)

## `logstash:8.19.18`

```console
$ docker pull logstash@sha256:d38b3758fd6a3ded520e641ad2339fccf5061e08e681e654765608dae23fbffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.18` - linux; amd64

```console
$ docker pull logstash@sha256:c157f36f7accbe27e241052b428010f95eec60ed54c4f2194ee5bce8c65d0c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 MB (540898087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751af4e6aef6728bcc03392c91743bc80cd882372760593abbc6a74e4b2991c5`
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
# Tue, 30 Jun 2026 23:26:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.18-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.18 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:27:16 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:27:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:27:16 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 23:27:16 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jun 2026 23:27:16 GMT
USER 1000
# Tue, 30 Jun 2026 23:27:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:27:16 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.18 org.opencontainers.image.version=8.19.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-06-24T20:36:37+00:00 org.opencontainers.image.created=2026-06-24T20:36:37+00:00
# Tue, 30 Jun 2026 23:27:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633fd10fb757524022e1233bbd3b03acc62e3baada9a963fc72f42a62fefe2f`  
		Last Modified: Tue, 30 Jun 2026 23:27:57 GMT  
		Size: 52.9 MB (52852117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fc69995895f6777e43162332f32622a3e8a58382426ec3d975069963d19797`  
		Last Modified: Tue, 30 Jun 2026 23:27:54 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112857d800b143c7d4ca37fec1494eae693b60a451b19c26dc1a53991f69300d`  
		Last Modified: Tue, 30 Jun 2026 23:28:08 GMT  
		Size: 458.0 MB (458045426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a036a48c56d55986fec5bb930eb6b2b52097313c4739f9cafecc93a74994fec`  
		Last Modified: Tue, 30 Jun 2026 23:27:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21994aa11891fb22ac3f649d2d5de16cd60791f9a0c1161df841f72747186164`  
		Last Modified: Tue, 30 Jun 2026 23:27:56 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23d661e4ef87d203041e2a53fe712ce04a0935b68b7f89bb5384c75593c400c`  
		Last Modified: Tue, 30 Jun 2026 23:27:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9814ac2c54a4d030478c233cb0affc93fb271e3023017842f7f1fa77d7d41e7`  
		Last Modified: Tue, 30 Jun 2026 23:27:57 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5454117059650536b10b9ce115d976362f0f50c81c64d21cf7a9945b95a6c23`  
		Last Modified: Tue, 30 Jun 2026 23:27:58 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a031df7f157982a190f31cb804bb322982d06fbac42b223dcf4b18b0929e5ff`  
		Last Modified: Tue, 30 Jun 2026 23:27:59 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3243066a69c4eb2acc5d6aea43d9554916844ae957698decbf9ebd2644c3ed44`  
		Last Modified: Tue, 30 Jun 2026 23:27:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbc67dc90794c707269e3435fe865bffd7a981ba9f4f1b72c978279905772e`  
		Last Modified: Tue, 30 Jun 2026 23:27:59 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.18` - unknown; unknown

```console
$ docker pull logstash@sha256:bb701a23f4e94821021fc1ff8f49666025ec07bc80689444e948d57de2085430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1b68eca5dcedc3680129ef091ec0a0bee44ffcdb273a8e4390c80605f1a26d`

```dockerfile
```

-	Layers:
	-	`sha256:f7f94cb343baf83549f8c1b6c54e4311628f4e4d5e5992fd3df405c5e67920b2`  
		Last Modified: Tue, 30 Jun 2026 23:27:55 GMT  
		Size: 3.7 MB (3678260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc42b3f8024caf434ea89a640c10dcce9f6b484b549f010f8da88af9792a7914`  
		Last Modified: Tue, 30 Jun 2026 23:27:54 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.18` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a9d3c1cca8c84aaed6b4bd2bfb727c4bfc32a132646b2a42f1705e4ca605f0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539194133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae101def25f733a98e75229836dd5377bf9de64a4fee80cbe462209a02c5883`
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
# Tue, 30 Jun 2026 23:26:15 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 30 Jun 2026 23:26:15 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.18-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.18 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:26:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:26:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:26:35 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 23:26:35 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:26:35 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:26:36 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jun 2026 23:26:36 GMT
USER 1000
# Tue, 30 Jun 2026 23:26:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:26:36 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.18 org.opencontainers.image.version=8.19.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-06-24T20:36:37+00:00 org.opencontainers.image.created=2026-06-24T20:36:37+00:00
# Tue, 30 Jun 2026 23:26:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c785aeaf419dbb7913fb1b49c412377fb5767ff686c90e1460163571b607a`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 53.7 MB (53701363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285e4b9c797dbaf2ee856b715a3a6bb1ffc3920290962060f5ed752156bccf38`  
		Last Modified: Tue, 30 Jun 2026 23:27:15 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fea4ea0d9aaafe6b7dc60e07b784da6bb4679fd97580020b660c348f6043d2`  
		Last Modified: Tue, 30 Jun 2026 23:27:25 GMT  
		Size: 456.3 MB (456348622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9750c65570475079967680ead39a892b8b97793c3a03ed98ed0e3cd37726164`  
		Last Modified: Tue, 30 Jun 2026 23:27:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f84f513d80452208b99f9894381e145bc04a37628ffc2e7c5c0126ac2b4e99`  
		Last Modified: Tue, 30 Jun 2026 23:27:16 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3061b68fd46fe2f04c5e78b8afb29dafc45208b21b9a4bc437120c60d97323e4`  
		Last Modified: Tue, 30 Jun 2026 23:27:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451bcea8a2b00ab3868eba7126be93c425139eed60f871a0d936303d1bbd2aed`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d3237288954aa60f5393a44d13619a51aabadc783c8518418d6b721acd764d`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb6649877d0e109389321689200d4125b21a6eded4c7c6f2c2acb7224ccdaf`  
		Last Modified: Tue, 30 Jun 2026 23:27:19 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b0084fc256b15282768040de61adf8a7f3c72f45b5e84e5a78e0142282729`  
		Last Modified: Tue, 30 Jun 2026 23:27:19 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977726725e9ce4abeedd9324af5367170ea2b917082d82aa0ac2e2f1d8e63a73`  
		Last Modified: Tue, 30 Jun 2026 23:27:19 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.18` - unknown; unknown

```console
$ docker pull logstash@sha256:f5245261a23bd0fed4d3f213ff4958d7f2655c0f30b00030a980bc7178a9d170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e505fdcbe8370c7be70f3f3dbc60112ea7850b5cb458c533f1f352ecc7acbd`

```dockerfile
```

-	Layers:
	-	`sha256:85dcb3bd6b6a45237a898ae715555b9db3d5e9c641a90c3c5af4b96907f4eafc`  
		Last Modified: Tue, 30 Jun 2026 23:27:15 GMT  
		Size: 3.7 MB (3678685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31862801d180672e8f7f2d1be09250db8a9772e22f3d957ac80c31a7f4c4ea9b`  
		Last Modified: Tue, 30 Jun 2026 23:27:15 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.7`

```console
$ docker pull logstash@sha256:c8f0bdf27f5549453d7ad470e9af3461356a1351e7863abfa56c0d0e46afd8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.7` - linux; amd64

```console
$ docker pull logstash@sha256:276ebf78adaba357878cbf25da17daf1d210054eb72777287f12fc4c55a63b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518199231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8a5bf4a51155a3ce6868144737b269ea25c734beb3e349e64e92bbacfc831c`
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
# Tue, 30 Jun 2026 23:26:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:26:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:26:52 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 23:26:52 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 23:26:53 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:27:48 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:27:48 GMT
USER 1000
# Tue, 30 Jun 2026 23:27:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:27:48 GMT
LABEL org.label-schema.build-date=2026-06-24T18:18:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.7 org.opencontainers.image.created=2026-06-24T18:18:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 23:27:48 GMT
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
	-	`sha256:45329f7bd9d6f3fd595c282b0344e581745468fa1ffb9dcedefdc110cf572639`  
		Last Modified: Tue, 30 Jun 2026 23:28:23 GMT  
		Size: 4.8 MB (4774921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9327184ac0a1aea9881895a73d6e71d66d4186f1229f292e73e1652b958ce2c7`  
		Last Modified: Tue, 30 Jun 2026 23:28:34 GMT  
		Size: 472.5 MB (472472745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67eff0304fd79f8c5037a8c85a0425bb8e87bb788ea89147581cc462ea84593`  
		Last Modified: Tue, 30 Jun 2026 23:28:23 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6700149a3f1a4338a22d9268f6158d8f22db793a69e8ec162ed371143147ceab`  
		Last Modified: Tue, 30 Jun 2026 23:28:23 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087ccc0c54b21c3bb62a27f8f05a5db23f3e5ebe7aa054f94a4734f260e20e39`  
		Last Modified: Tue, 30 Jun 2026 23:28:24 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a1062eed693648ffe569b633cb830d9fcb89c88e0a4f1f64db974d0353153`  
		Last Modified: Tue, 30 Jun 2026 23:28:24 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0a00b0c718d07065bcb72501ba00d6df03a118114cabe8b514fe657ea28a3e`  
		Last Modified: Tue, 30 Jun 2026 23:28:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af48071549ef47750e23dfe90b8375a89567ff26fd21f961744c0bd316eda9b`  
		Last Modified: Tue, 30 Jun 2026 23:28:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f055d12ff0bcc7d2a0558acb124d0c20b6c52243e29fce54330a5c4033116c89`  
		Last Modified: Tue, 30 Jun 2026 23:28:25 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.7` - unknown; unknown

```console
$ docker pull logstash@sha256:5cf1385d9bfed8762a2194d030c8fb9170f8c29526b2fa277c2c7a0d60ac8913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35518391d9fa39448efeaa507e9d8ecdafac186cc2d4023bbf019552a5e84d07`

```dockerfile
```

-	Layers:
	-	`sha256:c2527b56b6498517e6e23586f409ee36eb35f1d44325d3dedac042fda5153022`  
		Last Modified: Tue, 30 Jun 2026 23:28:23 GMT  
		Size: 2.1 MB (2109708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541cb3f26ff5a384da8e59280062b759f34b808e4a5cf9b45002253b3bbb6068`  
		Last Modified: Tue, 30 Jun 2026 23:28:23 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0680e133562cb7d63b8a47f2205198c2b8308dc0fea8ac697583051f95fee99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.6 MB (514606878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c716b53fd3f514fe1392ebf27c309f08fd8230a03e212ef4c4f9fbd4ef5ec`
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
# Tue, 30 Jun 2026 23:26:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:26:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:26:00 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 23:26:00 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 23:26:02 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:26:28 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:26:28 GMT
USER 1000
# Tue, 30 Jun 2026 23:26:28 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:26:28 GMT
LABEL org.label-schema.build-date=2026-06-24T18:18:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.7 org.opencontainers.image.created=2026-06-24T18:18:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 23:26:28 GMT
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
	-	`sha256:1b85d4373354aa434b9842797ff81b372e511db94349642a28d80271eac5e6a3`  
		Last Modified: Tue, 30 Jun 2026 23:27:07 GMT  
		Size: 4.8 MB (4759844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db3610458b916505606f81064831cec05f4f307856b4d18430e0ee7320941a`  
		Last Modified: Tue, 30 Jun 2026 23:27:15 GMT  
		Size: 470.8 MB (470762848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14a244fed2a9fa0807dff828664d65bfae0379b4fa487379465069aef7d8b58`  
		Last Modified: Tue, 30 Jun 2026 23:27:06 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccbf9ffa199001356486de58b8e6d8ee0eba9580a8a68e4d94e2404034693eb`  
		Last Modified: Tue, 30 Jun 2026 23:27:06 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db30e0670fb277fa7129e131fa3ff67acb11c451a306f7967b6dbbb62242bf3`  
		Last Modified: Tue, 30 Jun 2026 23:27:07 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fdea76fa1d56eb950e72a0692791625513cc2da2aae810f8c7d27fc71a1b33`  
		Last Modified: Tue, 30 Jun 2026 23:27:08 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e78afa4e7c81388c176f059dd53983d57ff178e5e0287cc190096deb2a359a`  
		Last Modified: Tue, 30 Jun 2026 23:27:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bbf7fd73ffc0c798693e1ad11282d4c538f53744e3e827920fa9c071375cfb`  
		Last Modified: Tue, 30 Jun 2026 23:27:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2428f67a7f6f44e2419cc9b20b2980451a9acc8cc6f5f6690ffb97162d5ca`  
		Last Modified: Tue, 30 Jun 2026 23:27:09 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.7` - unknown; unknown

```console
$ docker pull logstash@sha256:3bb4aa9db426d4fa9833f51ad613cfb88da133e3d721e2ce7d170879a028366e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199b52db0daaa710a8c95906a8894783feb00f7601232d9e914f8a576b5779d6`

```dockerfile
```

-	Layers:
	-	`sha256:adf3ee0618956a1462c723c86e34d856a773648b821ae213521e4bffb91727b6`  
		Last Modified: Tue, 30 Jun 2026 23:27:06 GMT  
		Size: 2.1 MB (2108496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fe239c761f3de09a6e9796567d8397d3634373e720c0c8a20d81829bae2d8f`  
		Last Modified: Tue, 30 Jun 2026 23:27:06 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.3`

```console
$ docker pull logstash@sha256:150ecc881e0507be6e32e6d4f1271ebef95a8354a4344516d017301bc67a98d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.3` - linux; amd64

```console
$ docker pull logstash@sha256:64992a5ed02e5a0f5c9accfae994905a8d5af497b7c784ddb19db0c4871a598c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.6 MB (524555588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88926200840cd50bad2abebe491143d7410c5c956c8e24f1d8de47874d792704`
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
# Tue, 30 Jun 2026 23:27:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:27:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:27:13 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 23:27:13 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 23:27:14 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:28:09 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:28:09 GMT
USER 1000
# Tue, 30 Jun 2026 23:28:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:28:09 GMT
LABEL org.label-schema.build-date=2026-06-16T22:44:15+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.3 org.opencontainers.image.created=2026-06-16T22:44:15+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 23:28:09 GMT
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
	-	`sha256:351d29f80999650a393cfee53ba64b9a2c862490c75289c3cdd7c9470a1ecbfa`  
		Last Modified: Tue, 30 Jun 2026 23:28:47 GMT  
		Size: 4.8 MB (4774901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540a51abb5313d41b27a3c93fa4dd4e5dee983b7de0d1cf3aa9778ffb2d7680`  
		Last Modified: Tue, 30 Jun 2026 23:28:57 GMT  
		Size: 478.8 MB (478829057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288be073a1f1c513a293a6b328f8daf8c14bfa5c08a5e59a1b70bb7b5885a3b5`  
		Last Modified: Tue, 30 Jun 2026 23:28:47 GMT  
		Size: 6.4 KB (6368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a873950f43e0f8ac5f9ef0cc8888aa2be78d213ff32e4b07b0ec89729c5b4434`  
		Last Modified: Tue, 30 Jun 2026 23:28:47 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e01f0525a89ed54f5d888511d3808270c740fdbc389e22ff30ba5fac28f8d3`  
		Last Modified: Tue, 30 Jun 2026 23:28:48 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0667925d622f8874bfbf581a6e81acc6f31af3eecf078895bca0d11fe6f7fc3`  
		Last Modified: Tue, 30 Jun 2026 23:28:49 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f9cf0b385ac5668ae07239cb099906eead927637b1dd8057e56327c2fab229`  
		Last Modified: Tue, 30 Jun 2026 23:28:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84d321c30d59a7a8ba9a147b3e4e1cb8258392583a87dabd8b8e91d9482bff0`  
		Last Modified: Tue, 30 Jun 2026 23:28:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a9e98736d6d344a50beb1c52d0d3816883015578ffec0c4960456ad007525a`  
		Last Modified: Tue, 30 Jun 2026 23:28:50 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.3` - unknown; unknown

```console
$ docker pull logstash@sha256:32924e7caec9c35be3a318c07cfb92616ff49826030c2ddf5b010543cc1f4f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371cf2d20d89f3560f83dad022b50b5ed5fa1bcbd44a9b13ca9ebd1e04e3143e`

```dockerfile
```

-	Layers:
	-	`sha256:7b566b4537ad34e160be3e54315a6fe3db911229dc904c359986b0933e35861c`  
		Last Modified: Tue, 30 Jun 2026 23:28:47 GMT  
		Size: 2.1 MB (2116217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7357aa4e0b9d7189e1f3f4518635dd15423aa880d5da6468a4059165f5c0a6`  
		Last Modified: Tue, 30 Jun 2026 23:28:47 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5a71186ca0a64b07f5e3341ab485fe9475e23ba266086db22e2d716baf81c469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.0 MB (520956369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c252d0053f44a136f5b5d3ae1db7bd65fa6bdf5a5ea84c75a25ba8a9b49fc383`
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
# Tue, 30 Jun 2026 23:26:06 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:26:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:26:06 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 30 Jun 2026 23:26:06 GMT
WORKDIR /usr/share
# Tue, 30 Jun 2026 23:26:07 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:26:37 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jun 2026 23:26:37 GMT
USER 1000
# Tue, 30 Jun 2026 23:26:37 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jun 2026 23:26:37 GMT
LABEL org.label-schema.build-date=2026-06-16T22:44:15+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.3 org.opencontainers.image.created=2026-06-16T22:44:15+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 30 Jun 2026 23:26:37 GMT
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
	-	`sha256:00ba249bb11aa06b2c92599fe6bf279db451963116f1fd3b7b0b07f5a78b9256`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 4.8 MB (4759845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536e8e67ec19f4d38bc43fd9a89b3e581c1e00f4b2abf0c87bf66918a53bb18`  
		Last Modified: Tue, 30 Jun 2026 23:27:26 GMT  
		Size: 477.1 MB (477112276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358a37f6bfc8f7c47622914c62eabe534fbd9bdc32e7f1c673091c23e273bdd2`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 6.4 KB (6363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec01cdb2efd015f53fd7c24d81110d460319f9a63c84d5e086ed393c0a39b0c3`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a505c0d87b5023737b485a26290e716d09c84a58b9210654ef4d2eb6201948`  
		Last Modified: Tue, 30 Jun 2026 23:27:18 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286415912539deb6734705ab18a9df2f21684cd5be94b23d754bbe1bc8f8677`  
		Last Modified: Tue, 30 Jun 2026 23:27:18 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d983335ad635068af5e9922d3f6e1192f6b2c4e3e791e457dd76cf24fc9517a6`  
		Last Modified: Tue, 30 Jun 2026 23:27:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b56fcd85e6ba110497c391b84d4212182d3a8b506418739b4a3294aa9f6df81`  
		Last Modified: Tue, 30 Jun 2026 23:27:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7749ff2cf15c7de8885c80563720b3cda4f52bb1d40ff14b284afba43348041a`  
		Last Modified: Tue, 30 Jun 2026 23:27:20 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.3` - unknown; unknown

```console
$ docker pull logstash@sha256:10b5cc9eda8733619bb3de40f0f41953a93195a1ce4d8913621ef7ccc46d2034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a7d201de16292919d559296612c2488e77841fecb3b863d90d0e1afbf81083`

```dockerfile
```

-	Layers:
	-	`sha256:e71064934081ada5198892fd82d9a6003c5cad18c700ed2f43e7a0d270c988e1`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 2.1 MB (2115005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbeb294dc1dd778cf8bdb9acda3f9cc759f884bf629f61b337e019eeda5bd3f`  
		Last Modified: Tue, 30 Jun 2026 23:27:17 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
