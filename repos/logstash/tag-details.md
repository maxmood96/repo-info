<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.14`](#logstash81914)
-	[`logstash:9.2.8`](#logstash928)
-	[`logstash:9.3.3`](#logstash933)

## `logstash:8.19.14`

```console
$ docker pull logstash@sha256:37492d224102047ab95507abfbf28eaf4b41cb5bffb5f1c53382b10d96c5d617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.14` - linux; amd64

```console
$ docker pull logstash@sha256:2276f4865ac1bc7e67330d4cf6b1800312b974e946bbf6417bd57802f3fb2d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.8 MB (541778357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5174cb126ba275a7ef602423ca2c3e7b79eaead74052c02fa02580e9e73457`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:12:55 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 08 Apr 2026 17:12:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 08 Apr 2026 17:13:40 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.14-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.14 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:13:40 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:13:40 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:13:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:13:40 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:13:40 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 08 Apr 2026 17:13:40 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:13:41 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 08 Apr 2026 17:13:41 GMT
USER 1000
# Wed, 08 Apr 2026 17:13:41 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:13:41 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.14 org.opencontainers.image.version=8.19.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-01T10:06:20+00:00 org.opencontainers.image.created=2026-04-01T10:06:20+00:00
# Wed, 08 Apr 2026 17:13:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270e3d5ce91549e6a739573c42468f5eb0c06b6bcddd12acc3557b452464643`  
		Last Modified: Wed, 08 Apr 2026 17:14:20 GMT  
		Size: 55.3 MB (55311859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2097ac7c0f44f861832996bac68e8f07005f25a2e3a0884ff429eff6e3b8d73a`  
		Last Modified: Wed, 08 Apr 2026 17:14:17 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336bb33680d0e35606e892dabac341b7f577fd302e769a7624432a52d795a70`  
		Last Modified: Wed, 08 Apr 2026 17:14:35 GMT  
		Size: 456.5 MB (456465315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf57e023919b7477684e62676e190c8f3a150f641ac2cfa6dc99d966a762913b`  
		Last Modified: Wed, 08 Apr 2026 17:14:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e9642a1b5d44abd5753e8215765c4110e5c38fd674d2e7eecf9eae9fb1bc6f`  
		Last Modified: Wed, 08 Apr 2026 17:14:19 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497d77ac56d1959255c5db4610861d60d84b0ff3850c2a1a57cc0c3780b64ed1`  
		Last Modified: Wed, 08 Apr 2026 17:14:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20db049bc16270935b9dc45fbb3e7559abf78cf6ad710ce418effbba57d54d35`  
		Last Modified: Wed, 08 Apr 2026 17:14:20 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe3d0ef2e2f5c9e9ef77a4fb5a234d8000e7110354dbb98a3ede70179e2fa0`  
		Last Modified: Wed, 08 Apr 2026 17:14:21 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd80b04f1eabac79ff1fb75125066f74480eb435aa08589afe24ba749195367`  
		Last Modified: Wed, 08 Apr 2026 17:14:22 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ccc21f33bc2ffccfc7532727a54dbdae9deb1cc4cfa1942656485cda732dd4`  
		Last Modified: Wed, 08 Apr 2026 17:14:22 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5250ae70b829e0e9e524546818bd93c2c2fed3f1ba5680b9154476e0acb96744`  
		Last Modified: Wed, 08 Apr 2026 17:14:22 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.14` - unknown; unknown

```console
$ docker pull logstash@sha256:df52df252f31f24a069de8b31ad73e5ffc9d1d75a1a64f976f30c96d45d57fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0cd7175085ec11df3387e3ffbdca0333af1fc5392b81306533556e6a88d981`

```dockerfile
```

-	Layers:
	-	`sha256:4a6d0dd99ea836a68e881cd24c37addc322f98c2638846a5e8d420ae1fb4935a`  
		Last Modified: Wed, 08 Apr 2026 17:14:18 GMT  
		Size: 3.7 MB (3695661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aad5e094ebdc0fed436c78a05b55aac5ca477dc482571f54b84a0627d1834ca`  
		Last Modified: Wed, 08 Apr 2026 17:14:17 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.14` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:25d7b3398bae2ea51dea383803d57db94d6a5ba809cbffe1ae81f2aeea44a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (542048338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c7cce00b02831e74c3b57a7e941bfa44a463b68f440f764cadb39212739c79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:11:21 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 08 Apr 2026 17:11:21 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.14-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.14 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:11:52 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:11:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:11:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 08 Apr 2026 17:11:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:11:52 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:11:53 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:11:53 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:11:53 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:11:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 08 Apr 2026 17:11:53 GMT
USER 1000
# Wed, 08 Apr 2026 17:11:53 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:11:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.14 org.opencontainers.image.version=8.19.14 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-01T10:06:20+00:00 org.opencontainers.image.created=2026-04-01T10:06:20+00:00
# Wed, 08 Apr 2026 17:11:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e045f18a1b145263149ce9daea0777a6b25de43da17daf3c5e65c25adf3f886`  
		Last Modified: Wed, 08 Apr 2026 17:12:38 GMT  
		Size: 58.2 MB (58162580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd98bf01b82be65a572542e9349cdcb43d2d93a87953fb7ebb5c58f9c359543d`  
		Last Modified: Wed, 08 Apr 2026 17:12:34 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bf009e624f0d94b7670b104f3066ee32f043ec0f0944d55ba9ff3dcde3efee`  
		Last Modified: Wed, 08 Apr 2026 17:12:46 GMT  
		Size: 454.7 MB (454743965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef65c81cddd4a3992b909240e7d608eca47a8ddcad2913a445e239a061161f7`  
		Last Modified: Wed, 08 Apr 2026 17:12:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5cf0f33d8e13a21755d8f742ec1b1b0bc6da32c8d82c28657a160d8cbe4df`  
		Last Modified: Wed, 08 Apr 2026 17:12:36 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e55fac12b7cdf3c70d1612645744168d3acbea8c3477a9efe9d1e8bc377a40`  
		Last Modified: Wed, 08 Apr 2026 17:12:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acfd2ffeadafce5e7baab95399896db56f1e7fb66ffe0f23e077e6edfd70c09`  
		Last Modified: Wed, 08 Apr 2026 17:12:37 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cba68445d0e22d1abdfe5d9ff77ef54c3334cf5267afaa11bab5a65f3a1675`  
		Last Modified: Wed, 08 Apr 2026 17:12:38 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba1876ad27c972208e3bf94f3252248f29ff94d3e58fdf73b9833333f306d3a`  
		Last Modified: Wed, 08 Apr 2026 17:12:39 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb8c5c3f05f6044404acf9451d19d16d7f15955532bfbd43f2d04a75cd6ce6`  
		Last Modified: Wed, 08 Apr 2026 17:12:39 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdcf2992f62c630d5efe6ad0b1cc009448ef2005b5470141e32b2cf9ac45bf`  
		Last Modified: Wed, 08 Apr 2026 17:12:40 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.14` - unknown; unknown

```console
$ docker pull logstash@sha256:86e0bc550dd2d299bb40ee0452361c9fcefbf8a782ea9bda6c67ecd70008c08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e0f17e137be4f4ee00e4cde71cf492f51f57102b53abee422e1b62a96dadd`

```dockerfile
```

-	Layers:
	-	`sha256:db79320af7aad296e0ce92844ace0dd848a9452d6a3e8653b4083f6660ab0848`  
		Last Modified: Wed, 08 Apr 2026 17:12:35 GMT  
		Size: 3.7 MB (3696086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da5e5b65e026f4c3c08e341e551c96e78125853881bc3d3af0c0acafc64e1d5`  
		Last Modified: Wed, 08 Apr 2026 17:12:34 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.8`

```console
$ docker pull logstash@sha256:96109934f0a4ee952c347a4d73e5bc66ebc890054f6feb1f35e1e4c0627ca900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.8` - linux; amd64

```console
$ docker pull logstash@sha256:c50cb46dc650ee4a174598104ad122f19f9309d83c94b9c42b6a91c1e02358d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 MB (502174724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a1da6a8f76a1d0589c67cf211425515c8b791aeb5db81cef416721409b249f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:49 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:29:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:29:49 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Apr 2026 17:29:49 GMT
WORKDIR /usr/share
# Wed, 08 Apr 2026 17:29:51 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:30:43 GMT
USER 1000
# Wed, 08 Apr 2026 17:30:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:30:43 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 08 Apr 2026 17:30:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661b5256a2c19404391089166e392bb76e2b85393b03b57c9a2fc42f8ef0344`  
		Last Modified: Wed, 08 Apr 2026 17:31:24 GMT  
		Size: 5.1 MB (5148707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c8c40065637ec01be82ce0b2854f9ab6f643e4e0e2fda086375436ade3980f`  
		Last Modified: Wed, 08 Apr 2026 17:31:34 GMT  
		Size: 456.8 MB (456778636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf290227fb35498eaa75d15f729b94a8b7735a502ba7ca9a0c5824e37adbf0a`  
		Last Modified: Wed, 08 Apr 2026 17:31:23 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42ea1158b075fb49929a9430449db1c529bfff5ef27c4eb7ed6f2c354f7f45`  
		Last Modified: Wed, 08 Apr 2026 17:31:23 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2671908f233ac076d337a6ffb6e8ee18c3e9f59afd2a7ebc19f70470df1e56`  
		Last Modified: Wed, 08 Apr 2026 17:31:25 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e039e5ec8833fa62543465c8131a269ffc8644912bf9334304364a7e0818aa`  
		Last Modified: Wed, 08 Apr 2026 17:31:25 GMT  
		Size: 1.6 KB (1573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cef26fc216ccd83a5b3c035b977274d189784e7a9f786cdfb0b6b6d6f324`  
		Last Modified: Wed, 08 Apr 2026 17:31:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86473892a02070d9642b1d651506dc1f316410a07ec72bae5c18871b11fb7d8c`  
		Last Modified: Wed, 08 Apr 2026 17:31:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d810b61a10a6de0c028a48e92c604db765de44c5d8d9621d0a93e780481cdd`  
		Last Modified: Wed, 08 Apr 2026 17:31:26 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:35bf68c04094d2eec782e9c084672f8fbb1469bd6300e97dd6b8ff064deddf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca98a662f3bdaed02c1ba72fc499a5eac1544fb5ec84ad93568c7224fad0409b`

```dockerfile
```

-	Layers:
	-	`sha256:3faf561e063b1c76408fbb44919591405dd32d0ca34648a9e166293808a11e12`  
		Last Modified: Wed, 08 Apr 2026 17:31:24 GMT  
		Size: 2.1 MB (2139768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f1885a136f2a226f8b6bbb1a05e95f6cc2245f4e3806dc15a7bd46b181c39`  
		Last Modified: Wed, 08 Apr 2026 17:31:23 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:4e51ba9ed13949e6c1fb738e0a033510fce5d2439542bfccf220c21604539d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 MB (498676205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43e21bcd326241f55947f64cb35c067d94c83d4604df1ee86b56192b5606bda`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:28:54 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:28:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:54 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Apr 2026 17:28:54 GMT
WORKDIR /usr/share
# Wed, 08 Apr 2026 17:28:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:29:45 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:29:45 GMT
USER 1000
# Wed, 08 Apr 2026 17:29:45 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:29:45 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:47+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-01T10:02:47+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 08 Apr 2026 17:29:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27c19030d7d3ad3bd3ed893cd957545f0372fe505c729b3efdd998d2647af85`  
		Last Modified: Wed, 08 Apr 2026 17:30:23 GMT  
		Size: 5.1 MB (5147260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22509daf99fdeed5e86c4d5a351cacc421508c845307d261f23cd23eca503eac`  
		Last Modified: Wed, 08 Apr 2026 17:30:34 GMT  
		Size: 455.1 MB (455063932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027a9b570f22170ad23f8cca1f13b91ec011ecaed7c3d6caf07d7ab1498ed18`  
		Last Modified: Wed, 08 Apr 2026 17:30:22 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56a11f742f61a66065ab060046ce63d00d9574efd7edf81543884ed41eb75b`  
		Last Modified: Wed, 08 Apr 2026 17:30:22 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc156ab82a0b7eabf4e6de0668d88dcb10cb35d9a9b1c805a7f6d0f770098655`  
		Last Modified: Wed, 08 Apr 2026 17:30:24 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832714c6a6ae913883bf0317367602c7600d1c36acea223b46e4bf1682e9f683`  
		Last Modified: Wed, 08 Apr 2026 17:30:24 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6feb10179af0ce3a5738f183eb7a6e6f0e0cdc9c8cc10015b08033a37e3c57`  
		Last Modified: Wed, 08 Apr 2026 17:30:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288508891259ec7def834490887e77012264284e1342d1fb8b09f5f2b8d678b`  
		Last Modified: Wed, 08 Apr 2026 17:30:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc4fe0a79ece55101b742feb06c36e60a0d4d307ca96bc422755e93c33d4bf`  
		Last Modified: Wed, 08 Apr 2026 17:30:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.8` - unknown; unknown

```console
$ docker pull logstash@sha256:05c6e562c86d66ea60a1b846186f9232a9ebd555805b1a81fa029950e686d9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a8f93bd771ba39efc433f7b9a30d79bf57c078214e2a5d1fb19d2f2891d0c2`

```dockerfile
```

-	Layers:
	-	`sha256:7c102f0ce639c83ece0d5b40111af6176bfef2ab9108b1fdc093c28c23d1e7e1`  
		Last Modified: Wed, 08 Apr 2026 17:30:22 GMT  
		Size: 2.1 MB (2140338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5a37cea4f43534870cc9b35f3cc0f461eb41564e9cf644e13c5d2944940edd`  
		Last Modified: Wed, 08 Apr 2026 17:30:22 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.3`

```console
$ docker pull logstash@sha256:e280b2a20d04f5ad286465a3304c268b6ed81bc0fe40b9cf7e86ff4f4a404b8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.3` - linux; amd64

```console
$ docker pull logstash@sha256:b6979c802955bc2d4859cb28ff3ba9e60dc1664924af063421b13763d9b3b62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516479154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb4cdb294422546dd4a56080e34fc4c56d18e6efb1b67712462c0bf39881b68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:51 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:29:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:29:51 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Apr 2026 17:29:51 GMT
WORKDIR /usr/share
# Wed, 08 Apr 2026 17:29:53 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 08 Apr 2026 17:30:42 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:30:43 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:30:43 GMT
USER 1000
# Wed, 08 Apr 2026 17:30:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:30:43 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 08 Apr 2026 17:30:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb60fc19de02b34a1713c4516f3080d30bebeca616faa47edf87f68bbeb3650`  
		Last Modified: Wed, 08 Apr 2026 17:31:26 GMT  
		Size: 5.1 MB (5148746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8111ffb8cb4651bd01b2ad37a9ccdaf8d6f7ca2b6720a09f46885f2a0bde9031`  
		Last Modified: Wed, 08 Apr 2026 17:31:44 GMT  
		Size: 471.1 MB (471083024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95333502e62fcb536429d28a562bcf483b77d742041dd95c2774e22ac9946d02`  
		Last Modified: Wed, 08 Apr 2026 17:31:24 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a68bde937cb11d8b81bdd63e177752beff70a2044027b71362f2b8c4730fd7`  
		Last Modified: Wed, 08 Apr 2026 17:31:24 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e1f38bdcbc3a174cf7de0a245d378f3d232318470cdc9a7a5364d79c69780f`  
		Last Modified: Wed, 08 Apr 2026 17:31:27 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44644796a0d29e1936c05b0d70cc7a43596589671f1761bc70803997ab47dadb`  
		Last Modified: Wed, 08 Apr 2026 17:31:27 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8a99e0724f16f5a18bc606e51f236f4b569b1c28682bac60def7b50df65dff`  
		Last Modified: Wed, 08 Apr 2026 17:31:29 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87f0a1491c473b98856fa96ceece6f576f6670eb9d1cb37bb42af106e9b02ba`  
		Last Modified: Wed, 08 Apr 2026 17:31:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b826a7b84ab1741429b801737a2724e1720abaa93273c02c471ff882f9807c`  
		Last Modified: Wed, 08 Apr 2026 17:31:29 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:f76dcc2753c83e4ae4649d71a39c4d75ea90f93afc4641c5610725de37ec6bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18baf500f99bfaa154dce27f005f18f813de43b996809b65cac225c3d8c9da78`

```dockerfile
```

-	Layers:
	-	`sha256:f65133f61066e6e5b11469e892ae5f9dacfde469e83bd7b6be8e6fb93f663142`  
		Last Modified: Wed, 08 Apr 2026 17:31:25 GMT  
		Size: 2.1 MB (2119245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a8c1d47ce1bd83aa52bed15794e86384ccb5fcd30993c730fbc2607f1179e9`  
		Last Modified: Wed, 08 Apr 2026 17:31:23 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:141e1e5eae177a92a1b6baa7e8f14dac224031409b286d95ae0617b7c0d37223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512980834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93b5347f7374adf9960b5def5c0fec43acd5bd54de59e45b8fe91167308034`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:29:08 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:29:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:29:08 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Apr 2026 17:29:08 GMT
WORKDIR /usr/share
# Wed, 08 Apr 2026 17:29:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:29:58 GMT
WORKDIR /usr/share/logstash
# Wed, 08 Apr 2026 17:29:58 GMT
USER 1000
# Wed, 08 Apr 2026 17:29:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 08 Apr 2026 17:29:58 GMT
LABEL org.label-schema.build-date=2026-04-01T10:02:52+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T10:02:52+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 08 Apr 2026 17:29:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea3ed735ec938c23d5c644174aab62dd619287e07af159148341e0cccc463e1`  
		Last Modified: Wed, 08 Apr 2026 17:30:37 GMT  
		Size: 5.1 MB (5147323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a3b1b7e6d3d099fa3fade2190ac83621568b9091d69a8524bcdda8f6cf3a0`  
		Last Modified: Wed, 08 Apr 2026 17:30:46 GMT  
		Size: 469.4 MB (469368498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2e6a1c18e9499c044fee5013c5f8089e7c1c117b380f79fd574cda9d9ec7cf`  
		Last Modified: Wed, 08 Apr 2026 17:30:37 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0894e24a311bb78ec78e518c88dd9fc861a3b9cc6c6141261cbda75c2d63e4`  
		Last Modified: Wed, 08 Apr 2026 17:30:37 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c00bcf3401333ebcdcb73bb11737a2b2d17de721aa1155a933ee33ec0c1a8`  
		Last Modified: Wed, 08 Apr 2026 17:30:38 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b07c1ef51bd37d261067a8bd3631c9bc38938f77d11e4ed9d1df1986b6c14`  
		Last Modified: Wed, 08 Apr 2026 17:30:39 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1094fd769c3a1bf9a010e0eaa8d9fa64fd06df45435a3ac2d10e60db6bf898`  
		Last Modified: Wed, 08 Apr 2026 17:30:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565e90a8a49355f9df8f3224d2da981e44f7cb625007372b38c726c2d3c41d1`  
		Last Modified: Wed, 08 Apr 2026 17:30:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54c487777ef3c0364d4b68d484cbfb2e9740f62eca3ee8ee3f0e61c1d2b97f5`  
		Last Modified: Wed, 08 Apr 2026 17:30:40 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.3` - unknown; unknown

```console
$ docker pull logstash@sha256:e47ce2664217f167e0b931ca18d9501895a4a92aa92d7bebc461ecc0cfb91c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e054a1ff5de2f5b05f471551768257fbfc4c42a6ed122e068d82f85a2a8f30c`

```dockerfile
```

-	Layers:
	-	`sha256:68c4e9ea1151c58c42418683ba9f9ad75e40883c6df20e64e34ba1940874e2c3`  
		Last Modified: Wed, 08 Apr 2026 17:30:37 GMT  
		Size: 2.1 MB (2119815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2baf6713e070af21d2d2497c4bb1a5ccd1dba219ad4d0b923b445a90c070310c`  
		Last Modified: Wed, 08 Apr 2026 17:30:37 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json
