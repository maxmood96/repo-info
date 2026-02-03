<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.11`](#logstash81911)
-	[`logstash:9.1.10`](#logstash9110)
-	[`logstash:9.2.5`](#logstash925)
-	[`logstash:9.3.0`](#logstash930)

## `logstash:8.19.11`

```console
$ docker pull logstash@sha256:f30f146a82c7eee5abb98e2ad63bd39b228a3fa2f2881cab1c8d60577b091e14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.11` - linux; amd64

```console
$ docker pull logstash@sha256:7e7c3a91455b61c641a8a94315456c0ee72e198cca60c50d5dcd11e08a38acae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.8 MB (532751023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1016543f8ad19f89f971fe48bc1bd510dc05d455021a32576c1eaa25b23fb5a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 03 Feb 2026 18:59:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 03 Feb 2026 18:59:17 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.11-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.11 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:00:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:00:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:00:00 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 19:00:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:00:00 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:00:01 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 03 Feb 2026 19:00:01 GMT
USER 1000
# Tue, 03 Feb 2026 19:00:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:00:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.11 org.opencontainers.image.version=8.19.11 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-27T22:28:08+00:00 org.opencontainers.image.created=2026-01-27T22:28:08+00:00
# Tue, 03 Feb 2026 19:00:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d10823a9ceb0c0b9d0389e00cd6141333752b6ec7a9f34a0c1d3431c712bbe`  
		Last Modified: Tue, 03 Feb 2026 19:00:40 GMT  
		Size: 58.7 MB (58686464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d685d166f4307b433d8be0b3b0bd757a0b022557f5102091d04b28df6d40d0`  
		Last Modified: Tue, 03 Feb 2026 19:00:37 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b0cb4d12ed63cc38d16f2b34f20af3087a2f586333999766f411fba9220f3`  
		Last Modified: Tue, 03 Feb 2026 19:00:48 GMT  
		Size: 444.1 MB (444070806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c41cb6a663c6a1dbafd7eeaf3b0c3a6477989c1ab955df3ea5b1e130208d6`  
		Last Modified: Tue, 03 Feb 2026 19:00:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732f499c3b72efb8478d4644f7b8a212dbbb5ad3ea4652c36ef3ef647139c505`  
		Last Modified: Tue, 03 Feb 2026 19:00:39 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788433f5b397b4b89273f9f81dcdcd190412d37f7ff4dc21cc832a7f7717a4d`  
		Last Modified: Tue, 03 Feb 2026 19:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21491d85fa6ea0b12c64566ed4a55a762046284de8e020ed4277820f524eb74`  
		Last Modified: Tue, 03 Feb 2026 19:00:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f2ba390b9bbfdacb3486952f51579b5d38181e8cbc6115df142bebe2f44bdf`  
		Last Modified: Tue, 03 Feb 2026 19:00:43 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10fcb6f9fb9e3ec7e1e4fef22ccc7317c12ff3c4aef37522d2d552d48c3a69`  
		Last Modified: Tue, 03 Feb 2026 19:00:44 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d77764f7330f2c6dd1d28bb758d3076d2ea574ed57f791669e6537d24a8ffc`  
		Last Modified: Tue, 03 Feb 2026 19:00:44 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63e3134822cbb655bdc5cfe3851688f70e25c0ccd2a1927840f3509866e59cf`  
		Last Modified: Tue, 03 Feb 2026 19:00:47 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.11` - unknown; unknown

```console
$ docker pull logstash@sha256:52b06994b51e6d751a4c16a7ec2c86f63b6ae59ad8c9a5409c6d0dcaa51c8a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74db9553c91ed1978f49d50c1090d32f071da084fccfbb2f56b7c3e334f28931`

```dockerfile
```

-	Layers:
	-	`sha256:fbdfe597739ef32289305615ef35ff8df2db4cb0c7e0ab1766bf4772855849e1`  
		Last Modified: Tue, 03 Feb 2026 19:00:37 GMT  
		Size: 3.7 MB (3657088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90334dee7e9d74cd4ab477249c4be434329dde8f189085e9e965899273439f00`  
		Last Modified: Tue, 03 Feb 2026 19:00:38 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.11` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d60ee3e1796020c950e54ddc58dc53d5269fac2fc0d68e4654d9e17ca6e24c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533869881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f1d1a171c077818aff80a1b6c58cff8e93fb19c4f55364ed018b5f45c0461b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 03 Feb 2026 19:01:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 03 Feb 2026 19:01:48 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 03 Feb 2026 19:02:31 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.11-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.11 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:02:31 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:02:31 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:02:31 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:02:31 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:02:31 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 19:02:32 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 03 Feb 2026 19:02:32 GMT
USER 1000
# Tue, 03 Feb 2026 19:02:32 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:02:32 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.11 org.opencontainers.image.version=8.19.11 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-27T22:28:08+00:00 org.opencontainers.image.created=2026-01-27T22:28:08+00:00
# Tue, 03 Feb 2026 19:02:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840dcbe998448c6a23bd58d1761a21e183efe644b18288c066428fbdab373282`  
		Last Modified: Tue, 03 Feb 2026 19:03:13 GMT  
		Size: 60.7 MB (60666943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7904505e2526e1943057f1145019b619ce8c1b2350c2b1bcdff57eb9a0e1251f`  
		Last Modified: Tue, 03 Feb 2026 19:03:10 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a33a4ea6f102934b74f7615bc3d101c948bc52e0d9563952e7a08d14b84274d`  
		Last Modified: Tue, 03 Feb 2026 19:03:20 GMT  
		Size: 444.1 MB (444071379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427f8292b33b711e58e2b28eca30a9f97865961b348a0b7a95806b4687122f19`  
		Last Modified: Tue, 03 Feb 2026 19:03:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59abafd553a430a24364f2a6fda9b3a1207948108294eaf19437b651d0bb09`  
		Last Modified: Tue, 03 Feb 2026 19:03:12 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977e7f5f891fa6ce38b1380ffaa505f356b9e8c43ef685c73ef677e2febd45d`  
		Last Modified: Tue, 03 Feb 2026 19:03:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db1d26f0db22cfaac727d124fd7888a9f1dbd92a0cc466c8878c68365c6034`  
		Last Modified: Tue, 03 Feb 2026 19:03:13 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81c1c45f6185f85fa99a230ae8e76080b026e9e650c233d13ee13a8f90b7f83`  
		Last Modified: Tue, 03 Feb 2026 19:03:13 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2113431c81517a565991211a411384c244f92c03efd47cdd893e8963dc99464d`  
		Last Modified: Tue, 03 Feb 2026 19:03:14 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10ac7e6b87f28f779621756c8a6123b14d020ea33e05a2e76b05a98059d2e5`  
		Last Modified: Tue, 03 Feb 2026 19:03:14 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097affc80ffa6bfe651368f641443494f77dc2f83ecd27d416a3bc405c1f2389`  
		Last Modified: Tue, 03 Feb 2026 19:03:15 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.11` - unknown; unknown

```console
$ docker pull logstash@sha256:b41b18103c09ae57c6bdaaa1e5620c19ea5e96fecbd639b3ad87aa36bc5c329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3694108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618dc92925b7360393891284d87c4aa2404714e9304f8cdf65453d080dce6cc6`

```dockerfile
```

-	Layers:
	-	`sha256:424abe2005f6c7726d13fa440325a1abbbc52f3c717fd52cda9d5bc048bb7245`  
		Last Modified: Tue, 03 Feb 2026 19:03:11 GMT  
		Size: 3.7 MB (3658137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a291629fb8697656c5785c378fb7799e7fd87f61cc2d81966c3a8ab71bd026f`  
		Last Modified: Tue, 03 Feb 2026 19:03:10 GMT  
		Size: 36.0 KB (35971 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.10`

```console
$ docker pull logstash@sha256:c6c8d932806bb685ed60bd1309e77c8f66aa41c2ee6aeccd2113b7c74f2e2337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.10` - linux; amd64

```console
$ docker pull logstash@sha256:bf26ecc3ca6c1cec655589c97361be9e1db8fa542a893f1b9b8497b1d64e8ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (475999324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15391406e206d3f2ef245d5f252ad5f6f4ea53d575070841b5be7a43e8818c2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:08:25 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:08:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:08:25 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:08:25 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:08:27 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:09:00 GMT
USER 1000
# Mon, 26 Jan 2026 22:09:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:09:00 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:09:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f2014f0223687361cc12a7455f1058fdd0eedf18cae7bb514a09d3410e0692`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 5.2 MB (5157710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53de0a38b7b65bd5230bcf26f521bb9e202baaf8f358c11e1e2803d771cc8a4e`  
		Last Modified: Mon, 26 Jan 2026 22:09:41 GMT  
		Size: 430.6 MB (430571860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d22cd9bbcf7e8c0ac1a3262cbc835483f0be26c8b74a9ec3b156088ca2924a`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cc78e5b9eadac8bb1a5992a99e3d2038de133183d40f7f17f6f5589bc3ddb2`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7046d989e43b957a9f0297c413c47b5fd57dcee04ff77d6cbdfebb42b3be9e6`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe8eb55c57ee7ed56d186e50dd7b035f7d26088f91aa2015d2b127fdf6b961b`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb04f99cac0a2de36b3cca7b627c0832b13e8654dd11bdf531edfc6480962cf6`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7005ff28fafa6181f3190ae3bb94a2af2eee2bf77901f79af105829292b95`  
		Last Modified: Mon, 26 Jan 2026 22:09:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cfff653b1ac5b44f4d3a4f51e11207fe45cdbe2a55b1d3e711ede72e990a9`  
		Last Modified: Mon, 26 Jan 2026 22:09:36 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:bb32e5d36a31c201c507f6b545e90a2062ffcfc5513876493d57bc422c542c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4a89d8d1c96b1ff5a72ec6dd770e1bfcc2c65079b5f923ccb37ea19736f0a8`

```dockerfile
```

-	Layers:
	-	`sha256:a1250185d79340e5530a8ec9ebf383d51e5d5daf3ab17878c60da5f2a9df9f4d`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 2.1 MB (2088545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904a7d143426dc236d4b35454834071b4f84bc7e492fc29ba498a7989a61ca17`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 30.2 KB (30164 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5ef67eac7d2b2baa9c99e6a93fc1e1d9304ef9cf9e469bca909fd27bc6de0ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.5 MB (472493714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e212ffcb3ff49445acd07e89b5798f0b4655aec29a920f5f2f460b42fd7e29e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:07:35 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:07:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:35 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:07:35 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:07:37 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:08:25 GMT
USER 1000
# Mon, 26 Jan 2026 22:08:25 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:08:25 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:08:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adc5ed1a1becf097a6f22cd91cf266fb9cc3985a5805caba78518dffe1893c4`  
		Last Modified: Mon, 26 Jan 2026 22:09:01 GMT  
		Size: 5.2 MB (5155555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ac5fcb2e5372554e33c0519877f40cbe239aaa074b25b5c3a5bf6b2f3927d`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 428.8 MB (428849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58edc2b0049a542f7acb2574e41b18ccba5bd8d86e5f6e8f199a310d00417d0c`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e8b33e821e98bcea55269cc36c395cb4c837f6d85954388da85dae02423e0`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80234afe49e28bc2b0a6a16f2b32305516dc96741c99588643051a748499353f`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af078debe94f51318b4719124199557892e9289258258f3ac0aad1c00be3921d`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8ebb81b172309fec2f24211539d78e550845947c411bfd7a6bc599c8d9a95c`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d9a5666e7bf2712e0b4810c3c43e2b10c7e58f8c2cc3dbedc8c41caa94e39`  
		Last Modified: Mon, 26 Jan 2026 22:09:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27976b6f1397455da9032db32d9e7919400b0a47b16ad0eac4f14e7317f438eb`  
		Last Modified: Mon, 26 Jan 2026 22:09:03 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:7adceb11ee4334fc0e3e23c84d2954b40131b6fded58af0f45753eeda12b488b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44819da42498f2b42e49c1e57406ddab958fbc41ff0e2716a59c65b7016f4758`

```dockerfile
```

-	Layers:
	-	`sha256:7ec00180d2a0f1b50f9112a221f18b5b9b888b4944f439de156777f48028a7a5`  
		Last Modified: Mon, 26 Jan 2026 22:09:01 GMT  
		Size: 2.1 MB (2089115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1e57d8ff4a6d2931cd5824ec9b72ed24b1ee8cd9cf564bb81332ded41fd9d1`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 30.2 KB (30241 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.5`

```console
$ docker pull logstash@sha256:292e369d641941d378b5ca98fc98f9a84634cbaa813de8c016e86067156ef19a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.5` - linux; amd64

```console
$ docker pull logstash@sha256:fed608d6df08f2ace102d05af0999bc97d46dc2b976f0d1a5bebc5696f2e27a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.7 MB (491674433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e8c70ae8d19fd12859c4c36b2bb713abe4658cf46e6f1d90d28b0c63c3dbea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 18:59:32 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:59:32 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:59:32 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Feb 2026 18:59:32 GMT
WORKDIR /usr/share
# Tue, 03 Feb 2026 18:59:34 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:00:23 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:00:24 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:00:24 GMT
USER 1000
# Tue, 03 Feb 2026 19:00:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:00:24 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 03 Feb 2026 19:00:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c7d9987ba0acce0cfc286adf356e010c72e69b743f5e401583ed126b2f6485`  
		Last Modified: Tue, 03 Feb 2026 19:00:56 GMT  
		Size: 8.1 MB (8085534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2eec2944898ef37f17a04e5abfba7f050dd41f56e44677d9cd17029aa13ddb5`  
		Last Modified: Tue, 03 Feb 2026 19:01:05 GMT  
		Size: 443.3 MB (443319137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6839eee91b6e0738a24f5373eb17958833f6399506f036f4d7c0f65c60e58`  
		Last Modified: Tue, 03 Feb 2026 19:00:55 GMT  
		Size: 6.3 KB (6299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ef567eb71b44770ddf14522b9b964c02c324c8c3c33dfb57177e59f5459390`  
		Last Modified: Tue, 03 Feb 2026 19:00:58 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4dfaf1d87a1eb971524d84612d52c68da823006442614f4d41ae3df71740b6`  
		Last Modified: Tue, 03 Feb 2026 19:00:57 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca9a6d32a288bf4ac59eb531d153583a7809eafcb98647755ca9ce743a87b2b`  
		Last Modified: Tue, 03 Feb 2026 19:00:58 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d00e6eddd03fbe0242289fc080566399dcc187bf97f2830c96e347443622835`  
		Last Modified: Tue, 03 Feb 2026 19:00:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066259fc0aef7e460e98ce8d1e34ef4ba64d873ce35afc0485c945207b1b625c`  
		Last Modified: Tue, 03 Feb 2026 19:01:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f476412a156cdf4b5c09e1f7829c940b73a3238283aea257d145df87e1bdc4`  
		Last Modified: Tue, 03 Feb 2026 19:01:00 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:c22cc8a74b84084b6d51d08ea0547fddc9bbb0bf3ee593636c0d0eea4a5f98ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb97ab85202166db67ba93c49fb6d114ea0217bdde8045d286628ebfc71787a`

```dockerfile
```

-	Layers:
	-	`sha256:a09179b6409830ed2427fae15d5c5b078617e8695453a056a916858a009c26f9`  
		Last Modified: Tue, 03 Feb 2026 19:00:58 GMT  
		Size: 2.1 MB (2103690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97a6a964e4c14d72de05fd2b5f47fe87a7ef3f1341657dc089babf46358a7bc3`  
		Last Modified: Tue, 03 Feb 2026 19:00:56 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:21297e308c8cd6b42ab1253271f7770d0808ec852104cfc02525a971a1aa3327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489712258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ed5cc6450275cc4a77bf701c43f9e9f4bf473c8debc8e8ef7fe1bdd075dd23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 19:01:30 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:01:30 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:01:30 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Feb 2026 19:01:30 GMT
WORKDIR /usr/share
# Tue, 03 Feb 2026 19:01:32 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:02:21 GMT
USER 1000
# Tue, 03 Feb 2026 19:02:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:02:21 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 03 Feb 2026 19:02:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984bed9842f20413e3c3dc0d7e1e83578ff2255f8e24e365be5f445ec924b395`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 7.9 MB (7903343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4d1664eca8c46068a6cf55f06fcef3d77e48fadcf2e8332a85b3c3c36fdfc3`  
		Last Modified: Tue, 03 Feb 2026 19:03:06 GMT  
		Size: 443.3 MB (443320537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac46c0d951c856f397dbd26937d9cc311d222ff3cb8f606dfc6e0376a937738`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 6.3 KB (6299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67313730842d2fecef724bd18b9e9ed8eb25482f66707dbbf2ca91dfdef03de5`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fe422760d6796931b7c1896c0ad9422d3e72db84554402c0de30aa828010b`  
		Last Modified: Tue, 03 Feb 2026 19:02:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14234497101b9f3f1549247c8e266e54af7d4e02a7254d0db9140202063f7b48`  
		Last Modified: Tue, 03 Feb 2026 19:02:59 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09e6b740ff6b89e2feb671cc6c778f55305b8a5f9fb8dd6d495e47d3abadfb`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c3d8accf9bcda763363b1248892dee7fa58acefa8b8c9313aab5b4c76416a9`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d409935b2379312ffc7a040946222ae82b1f8a6bca9917b16899682a7b206`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:fbab9f632c259515e222e91269982e8ce6b0ab740e1cb9de2747801ab3f3c441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e34c4b3f42697b2f6dd8d628ed21bea7e93c15e451c43eda369a584517aef4`

```dockerfile
```

-	Layers:
	-	`sha256:70804aa734bcb64996873ddd6fd101228f14523ed07222958b0eace67d5ec6c3`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 2.1 MB (2104884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e1532a3ea2d46f3e083118b6db08a2929a81e35b8d0b6e05a95644f22e094ce`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.0`

```console
$ docker pull logstash@sha256:95c644a32b1429b6ee9eb389369dc427c55aac44e3040523e07d29e3f5a062ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.0` - linux; amd64

```console
$ docker pull logstash@sha256:8de2df60b9215435fab9f72d82f679c03979a3f52abc4e4b0bb078aa4b48da44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.1 MB (507093991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb4a1c7fac1b47fd0db44ecd23cb61c6e6ab20a47342d595caf23b4f8550c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 19:00:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:00:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:00:48 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Feb 2026 19:00:48 GMT
WORKDIR /usr/share
# Tue, 03 Feb 2026 19:00:50 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 03 Feb 2026 19:01:41 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:01:42 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:01:42 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:01:42 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:01:42 GMT
USER 1000
# Tue, 03 Feb 2026 19:01:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:01:42 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 03 Feb 2026 19:01:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f496cd090af514c3f6f018b6959016fe6d93657da53a4f7eba8196b9e9b2c8`  
		Last Modified: Tue, 03 Feb 2026 19:02:15 GMT  
		Size: 8.1 MB (8085528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4847ff20c21a2f28b385c7c86c9cba6cffca542a06911ab15aaac9dc772c5bc`  
		Last Modified: Tue, 03 Feb 2026 19:02:23 GMT  
		Size: 458.7 MB (458738700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4d33292837671d3f2efb39b327b447d71a97be73d17e2d86ea2243cc407f1`  
		Last Modified: Tue, 03 Feb 2026 19:02:14 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507e075ee5171d8f11a5312e6fb0d45b5e11184c5589ec54f15d872374aab5a4`  
		Last Modified: Tue, 03 Feb 2026 19:02:14 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd643a652dac86bedb52a9ac7a2ad4e758eb52ca3434c2f5685482cc9c0e310`  
		Last Modified: Tue, 03 Feb 2026 19:02:15 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8377e39f233fe87c6a69a690f287c6b6300c9ace2f3fce953d89a4149eb12f85`  
		Last Modified: Tue, 03 Feb 2026 19:02:16 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9eb7a8d96deba1df51fdeff25cfbdc91fe16bae9bd1b2d3b4da3b04629d014f`  
		Last Modified: Tue, 03 Feb 2026 19:02:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8811d89d36d6035f076ab82bda539b763f124d35529673a3f7091ae2517e9603`  
		Last Modified: Tue, 03 Feb 2026 19:02:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a155dbcab025e26b427bfb23a1f41569615494cc3a1186fc34e640ecd1b3e24`  
		Last Modified: Tue, 03 Feb 2026 19:02:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:13d66c0dadb231007159f82ac5b6240391eed4d0ea51a60f2f5ea99619e5efb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2114197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34df8fb9341624ba79c97f6f9ce0013813cc41474096eb4fd1abf17c2a0d2af`

```dockerfile
```

-	Layers:
	-	`sha256:89f138bb19c72c9889a3740a6893610680a578fe6aa03a2d7b8566dceaf0ae93`  
		Last Modified: Tue, 03 Feb 2026 19:02:14 GMT  
		Size: 2.1 MB (2083997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c58626ed7cf88fd74ea802cdc02183ad72e0fea2620aeb49c69bc9ed925da95`  
		Last Modified: Tue, 03 Feb 2026 19:02:14 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1b4a38347786d859853c06dd67d2a01f52af38de354287819dd9d60fa142d660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 MB (505129507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0cc34e4598e674fba5af3dda9403ea84d2ad50fe307f6f184e14adc0b0386d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 19:01:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:01:27 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:01:27 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Feb 2026 19:01:27 GMT
WORKDIR /usr/share
# Tue, 03 Feb 2026 19:01:29 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Feb 2026 19:02:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:02:21 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Feb 2026 19:02:21 GMT
USER 1000
# Tue, 03 Feb 2026 19:02:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Feb 2026 19:02:21 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 03 Feb 2026 19:02:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2c3686820e7749f4748cc20d868b2a8800f28b417dc2aaa52c6f7d875f873e`  
		Last Modified: Tue, 03 Feb 2026 19:02:59 GMT  
		Size: 7.9 MB (7903316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dc096eef5849bb92f06256081078ed107a537a82cc9988ca73133e7cdf35fb`  
		Last Modified: Tue, 03 Feb 2026 19:03:09 GMT  
		Size: 458.7 MB (458737806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97d35d62797c10b97cc518d8f9b77f912f1f247ad62e161c290a4fb2b85890`  
		Last Modified: Tue, 03 Feb 2026 19:02:59 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8bc8edd5a890a008afcc0285da258cc45288b49663379a3d1b2eff1b087243`  
		Last Modified: Tue, 03 Feb 2026 19:02:59 GMT  
		Size: 255.2 KB (255190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322b6899dc04371a76b7bf2b26c602d94336d54bab86feacfcde660d9b4efcf`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a0f98a51978ad05bffadcc651ffc056fe6751ae3675ccfb355e903bcb6e3e4`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302dfb64bb4d4d3f9324a9c531584823f92a810989249a92b54e8f905b51360e`  
		Last Modified: Tue, 03 Feb 2026 19:03:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ffb9ad95f740c614b88b585d40e200359f6d596c87fafddec6aae706a57b30`  
		Last Modified: Tue, 03 Feb 2026 19:03:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910c1044a05f12f242655fccf55c7405f387d0e32969dd428dfdc9ebf65ba27`  
		Last Modified: Tue, 03 Feb 2026 19:03:01 GMT  
		Size: 715.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:8b826b3b1664f1b513721a28096af81ce88eb8521a5b6a88f076536c38ba4e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc80f89ff4224782d0b88cf62d085022d96843f7467b7ba928bc9f44cc087bd`

```dockerfile
```

-	Layers:
	-	`sha256:f1cdb0d8567e4eee8589920b218d54e41928234ab4f83a46fd97f5e656bf3a77`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 2.1 MB (2085191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e345d74b2918bcb54a1a5d0085ed083cedaee6c2bdf7779ad2edbf68b5e0718`  
		Last Modified: Tue, 03 Feb 2026 19:02:58 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json
