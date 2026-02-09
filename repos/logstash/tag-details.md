<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.11`](#logstash81911)
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

## `logstash:9.2.5`

```console
$ docker pull logstash@sha256:bc2c92a2c127cbd37bfd46c68c6bed97675214abc5d82ae17b131bbfac2bb2f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.5` - linux; amd64

```console
$ docker pull logstash@sha256:f449e699739abca359cfb256b6bfd0ad0925b8ebe9374a54c5faa73cfc4abc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 MB (488799799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301d53b4defc2a52f52627b9f1c82bdab20ab2b8328ae6482f0ca1d50fafb30a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:16 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:16 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:51:04 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:51:04 GMT
USER 1000
# Thu, 05 Feb 2026 19:51:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:51:04 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:51:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc15a47de2ee719eecca0645d1aa0f7ce1013c8a44e00723938cd6d3580ea50`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 5.2 MB (5159975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc45e5b08a7a72d1a23e8ce47e047ddeae613a6628b51c1f8374bd72dd97343`  
		Last Modified: Thu, 05 Feb 2026 19:51:49 GMT  
		Size: 443.3 MB (443319199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6b3a3831a73abe84f75305ad66e280bac9b05e6ff5785a690e49dd3018f23b`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b3e6ea6a75512bf52e11612ba7ddd2ed0d2eeb4602fce67a1e74abcae9741`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9714590e469d7b75e04754f66318ea7cbd2b0ce6791932a526213dc0b7ee2ce0`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c38225e2f692ff02f7dbcccf220d000e6c30ce2ec52b3bdd3186afc0bf5abc`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46d6b1ea6436ed337b38fe61efcadb527a308e9cee4f9ba9d0963cdf29127e9`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847f3c6d5ccc3d1555e9ad0fe3ccf442b4a40ac916209d372ee581aa31bcd9a`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aeffc7ef03c787ab0534c11cb8e4f496e0b784d6aa7a2cbdbd999f260537d8`  
		Last Modified: Thu, 05 Feb 2026 19:51:42 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:ec59245a9ad91f937972607a65ea3c0958d8e7b76a3e4627ec1227b3e4db9a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c8613926e6cb474c9da073f928fc222db25385e0ca07d8085953f6f9fdb99`

```dockerfile
```

-	Layers:
	-	`sha256:6bce3a9f36536e8d16f07bc2fac9180933ce0b7476d0c24a17054856ff550b18`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 2.1 MB (2103734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3801c2c3b4b98188381172c76ccd0cf2721b4a70bad7068c11f9f3e860e690`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:934239a2ef67b1437a628b92d23548f03ce2c0739d50fde22450a99004a154d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486956679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d838f05b76a3bf6c735de2a70b9b87c9a17ef56f886cfc8cb7e683281e7b26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:01 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:01 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:01 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:03 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:50:50 GMT
USER 1000
# Thu, 05 Feb 2026 19:50:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:50:50 GMT
LABEL org.label-schema.build-date=2026-01-27T22:24:43+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-27T22:24:43+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:50:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a40b6d59de3ec92b630156b5cb394534adb05a60aa7bc1bc20f854580bd08f`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 5.2 MB (5155914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d7df42f84c27e0419769fc61f2958860ad2b4b6a7c81155c94b93e5befac`  
		Last Modified: Thu, 05 Feb 2026 19:51:45 GMT  
		Size: 443.3 MB (443320227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b651f6a06edb773b6a2649baf0ae564943c83ae3c9d9990bdd43f681ec5c618`  
		Last Modified: Thu, 05 Feb 2026 19:51:28 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09d3a2ba7ff6a04b1306be87ab0fa21b71dc284e027bddf698717e8db17f2d8`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b805f59ec599796ae2b80ab63a10b72316741b1ce4963ef44af5d64a3a57d13`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d196d0a2980a1739d93180a40f787922b4969e02a2b0079ae908b663d0318`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6dd0e3dad83410f811bc6df2168f5fc20d04bad901824567353592451fa123`  
		Last Modified: Thu, 05 Feb 2026 19:51:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab613139944f2809f5c9e1782f1f804d45b26a306f9a9685e1df38dcc74b3373`  
		Last Modified: Thu, 05 Feb 2026 19:51:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1bab64257e233dc79b1db714deff016b706eee49da0fb0243c7ca7092e4b47`  
		Last Modified: Thu, 05 Feb 2026 19:51:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.5` - unknown; unknown

```console
$ docker pull logstash@sha256:3c667bfa69adc2d2dad41e56b0ba2fc785a267ee2bed723ec34f1b30e34ac6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b1af19e969298e5e60fb43e02de93fcde8c40cb54ba93b46df9a5bd7c11adf`

```dockerfile
```

-	Layers:
	-	`sha256:05ce9f4ed79fe75f4a0ca087ee8a7fa03ea037057ac69ca5564fba9a925f3ca1`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 2.1 MB (2104928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa1e384088d733604b07c22983c3a7e7aa87b3bfeb932e8b2dd1af46c00802c`  
		Last Modified: Thu, 05 Feb 2026 19:51:27 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.0`

```console
$ docker pull logstash@sha256:6741e21f63dae474a677e5c4727e0b4f7008cbd585eed85f211219c9b107ee19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.0` - linux; amd64

```console
$ docker pull logstash@sha256:e8128b85679ba543248120c5b8d6cf116ff3f79de16f4e463dd08dd5647a8e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504219219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61b243620ef67c73e14594dbddc073b132f7ad7ec8ae72f14ce07cff4a26f5a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:17 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:17 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:17 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:19 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:51:05 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:51:06 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:51:06 GMT
USER 1000
# Thu, 05 Feb 2026 19:51:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:51:06 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:51:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b2689788ebfd5033405dad057f7f828959baefa46b40db565df6fc5928ab16`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 5.2 MB (5160008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb298610cacf5b9ccbb214fe20c1fd2b372821a880b2f298e7462b707fc8dd`  
		Last Modified: Thu, 05 Feb 2026 19:51:47 GMT  
		Size: 458.7 MB (458738586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9548a120e0e61e72f3426385f33e952cadc18835371fab7355ddffea2f382ce`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc07b8e6681b171d8a7ea1d33caaa818250d700897d9be91a65add3322ca000`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd13efb788f02be74845036d469e1e38e6b03c40ece1786898afe4d056faa5f`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a622c853b703330881b883f31cc3839d475fc1b099397a74c9adb59b5b3bc6`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aaea3b01583d175b7cc76b5eb9d709655bbcce1bc0ddbae35d5f730d766df5`  
		Last Modified: Thu, 05 Feb 2026 19:51:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4420e691c7c8cb17f44d3f1df06fa8abe632281bd888212526506285b360909`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50de45f97989054a16d1516fa7e2fd7a4346634d55b148c2573c850de6717fb`  
		Last Modified: Thu, 05 Feb 2026 19:51:41 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:5e500d44a15a2e3fb7f8f5a9e60d35e70c9e722fe027786c4387cdd86d8834d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2114241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb4527f25834e5d7115308668be42100a779b797b645d190a999b7c5e982eb0`

```dockerfile
```

-	Layers:
	-	`sha256:584f719dca0e3e123d69d1219b9da541dd2f4e365cf62139446795675ef774bb`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 2.1 MB (2084041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5695628b4b2648245a0bc05306e3d824e725211acbb64fc0eb3839364c1e52`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e968fcea8a0923abd564ad9623124b2b61836df5fddf219a1a01efa7542b88d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502374710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ef4931fc4da3da531624b49628c6d275e3aa52624d1208cfc868b55614cd20`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:08 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Feb 2026 19:50:08 GMT
WORKDIR /usr/share
# Thu, 05 Feb 2026 19:50:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:58 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Feb 2026 19:50:58 GMT
USER 1000
# Thu, 05 Feb 2026 19:50:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Feb 2026 19:50:58 GMT
LABEL org.label-schema.build-date=2026-01-22T01:49:14+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-22T01:49:14+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Feb 2026 19:50:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659990beb4076fb1c2255e471dc232922a40b125ee338a3addbf45e59c24072f`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 5.2 MB (5155898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c38274ccb2f2d29b80601d57a1bd06495a78f56f5bcb69042d0909ad8d5772d`  
		Last Modified: Thu, 05 Feb 2026 19:51:44 GMT  
		Size: 458.7 MB (458738265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0d452a8ae93dcd875db5adea9763f53ab7f90b7383ae396bd30bcbbe27f01d`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 6.3 KB (6292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a567133787ce2f900500f69c2a1e25011442e85d0a018691ffea4b51d1d453`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12111806aba0e8b018fb4c1be78b1bba4bd0698898bb9e7539f9d736179eb32f`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768604b9469e20096f8e9496f4c6c4cb8071667f79a788da7516e7a30658d89`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd3a4745e79a8dd0282c12330cd4859a9d077940118e8b4d6de0449465a927`  
		Last Modified: Thu, 05 Feb 2026 19:51:37 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118c00e5e26a6d18560b844e32f4e32686403e66931ed9213f22ac998d13f9f`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ae2e419a2a8c30309f90e0d927a239a49a76f61ea82c0094616fa71ac19bc`  
		Last Modified: Thu, 05 Feb 2026 19:51:38 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.0` - unknown; unknown

```console
$ docker pull logstash@sha256:e516a7e0ba11689715f4060034720480a31b5103b15988fefaca002d2b5aa8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b7417a8391c6fa9c274924842da7610aae9f8fd18c372f91d5dad3a48a1306`

```dockerfile
```

-	Layers:
	-	`sha256:3da0bdb537e9b6c4fc9f55ebc893a8ee45df7512aaad5a2e397c42769eb19840`  
		Last Modified: Thu, 05 Feb 2026 19:51:35 GMT  
		Size: 2.1 MB (2085235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa40faa93363455c6a7ef5663d1de1256f56a12eeb0d83dbbec7bec24a9a2ae`  
		Last Modified: Thu, 05 Feb 2026 19:51:36 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
