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
$ docker pull logstash@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `logstash:9.3.3`

```console
$ docker pull logstash@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
