<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.15`](#logstash81915)
-	[`logstash:9.3.4`](#logstash934)
-	[`logstash:9.4.0`](#logstash940)

## `logstash:8.19.15`

```console
$ docker pull logstash@sha256:39bc2d4d321cbfc67e2747ff2e03b16d3246ffdd48464a7748bcfb44fee505cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.15` - linux; amd64

```console
$ docker pull logstash@sha256:8c654c7c64858216017478f33bdb2a14bcda8b63724b30d75b396613e125c11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539418949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13b09e0794560fe1c7117f84de7d4ebfee97df66575997386e35efc328fc68c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:10:06 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Fri, 01 May 2026 00:10:07 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Fri, 01 May 2026 00:10:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.15-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.15 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 01 May 2026 00:10:51 GMT
WORKDIR /usr/share/logstash
# Fri, 01 May 2026 00:10:51 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:10:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Fri, 01 May 2026 00:10:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Fri, 01 May 2026 00:10:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Fri, 01 May 2026 00:10:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Fri, 01 May 2026 00:10:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Fri, 01 May 2026 00:10:51 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 01 May 2026 00:10:52 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 01 May 2026 00:10:52 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 01 May 2026 00:10:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:10:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Fri, 01 May 2026 00:10:52 GMT
USER 1000
# Fri, 01 May 2026 00:10:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 01 May 2026 00:10:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.15 org.opencontainers.image.version=8.19.15 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-21T19:46:57+00:00 org.opencontainers.image.created=2026-04-21T19:46:57+00:00
# Fri, 01 May 2026 00:10:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd918eb76a319ee07e47764b25ed28eb98b86e0c04a55548dca2a76fc63da99c`  
		Last Modified: Fri, 01 May 2026 00:11:28 GMT  
		Size: 52.7 MB (52660873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14abfb8e8db7aac6334521e5c314f7c86c28a91069abb0614fcf44774ed54fa5`  
		Last Modified: Fri, 01 May 2026 00:11:25 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f053903820cfaa8594cd2a26d964613fd83c1cf6618f47b4d70641e1ef36d`  
		Last Modified: Fri, 01 May 2026 00:11:35 GMT  
		Size: 456.8 MB (456757353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf358597f63fb9761c2de066d4c45391b09e9af27a5bca7d4cf5549995b56ce`  
		Last Modified: Fri, 01 May 2026 00:11:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d9b6c216953fdf4cf428a242f2893e1e430c3f692a109f2491ca30270f9a1`  
		Last Modified: Fri, 01 May 2026 00:11:27 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4605537933df1cb02e323075cb58fc9da2fb30c79d37685f390b2ef18c1359`  
		Last Modified: Fri, 01 May 2026 00:11:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b561a1494869fa7265dc54866c6eea00b82115806dbd4081d80498faf5bc9`  
		Last Modified: Fri, 01 May 2026 00:11:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b71be81969f10f766b43f9bd91a2647b5510452a9d950af3fd1a14541e9047`  
		Last Modified: Fri, 01 May 2026 00:11:28 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4953489b9e0b7fb7a8ab9139eaba2693c0728f6cb94a9b41b2b40c693a4c8770`  
		Last Modified: Fri, 01 May 2026 00:11:29 GMT  
		Size: 255.2 KB (255189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332a908f90c565b8932ea0ce73b3f29cd3d354ade23a6593534142a273af7692`  
		Last Modified: Fri, 01 May 2026 00:11:29 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf2a617bd8bad1ea4822cd9cc45adac8b5066636eb96ba2992a4d84997ec655`  
		Last Modified: Fri, 01 May 2026 00:11:30 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.15` - unknown; unknown

```console
$ docker pull logstash@sha256:712df72859332df551babf0b41b724ab81899697b8e7d9949fecd9fb63df1957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758e02d372675a9eb1915ff2f65243e78e7ebf0e84f64ce8620fc387e212c5a3`

```dockerfile
```

-	Layers:
	-	`sha256:bb887c56e7878c6a1d84d5e0c1a72362f3989985b9bf9b6acdb2007ffac3d252`  
		Last Modified: Fri, 01 May 2026 00:11:26 GMT  
		Size: 3.7 MB (3695159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccd52ce34b03321285e06fe84a5aad7642b41155cf2a2d027150b04e7a09a8d`  
		Last Modified: Fri, 01 May 2026 00:11:25 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.15` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:769ae589d473471a58e04f84e3d89dbe3333e3a0d2696ec23b6fbfbed67eae8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540163848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe4fc6903bbc07f81c0dad70d36c8a7d8e5fb2fe06402c17db2a3a42bd4cc63`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:09:55 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Fri, 01 May 2026 00:09:55 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Fri, 01 May 2026 00:10:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.15-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.15 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 01 May 2026 00:10:20 GMT
WORKDIR /usr/share/logstash
# Fri, 01 May 2026 00:10:20 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:10:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Fri, 01 May 2026 00:10:20 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Fri, 01 May 2026 00:10:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Fri, 01 May 2026 00:10:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Fri, 01 May 2026 00:10:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Fri, 01 May 2026 00:10:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 01 May 2026 00:10:20 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 01 May 2026 00:10:20 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 01 May 2026 00:10:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:10:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Fri, 01 May 2026 00:10:20 GMT
USER 1000
# Fri, 01 May 2026 00:10:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 01 May 2026 00:10:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.15 org.opencontainers.image.version=8.19.15 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-04-21T19:46:57+00:00 org.opencontainers.image.created=2026-04-21T19:46:57+00:00
# Fri, 01 May 2026 00:10:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31721c67d9e7a6d14b8180bbe2466cf61e917e5b17f12654b00882e71c466e84`  
		Last Modified: Fri, 01 May 2026 00:11:03 GMT  
		Size: 56.0 MB (55976997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670667fde9b8b06e13931384a7f4c96cd95aa39c84731ecbcc494aa4f6f8e3df`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a245dd2c67d6c403a10377da13a235a9aedcd85037a0eded46a35f0f799d262`  
		Last Modified: Fri, 01 May 2026 00:11:11 GMT  
		Size: 455.0 MB (455043318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189a67397397ac661741742b83199fdaa7874c62012a45a9d0c46f805c902241`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6103e1dc0dfb235106787cf2fd6424b70e1c8d4487310f32dd2286f5f28f3`  
		Last Modified: Fri, 01 May 2026 00:11:01 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df15a2ee531affb104988be6f489d7db53c1706694f7a5262d31cf68b6bdae`  
		Last Modified: Fri, 01 May 2026 00:11:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf703a0ee727e23d9754b7852e1526e784ae62ddbcd6ae2942f41af09b2b3632`  
		Last Modified: Fri, 01 May 2026 00:11:03 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb973f2541917854a68a00cf5f449745157b9fb0863efcd0cf0fec101549827f`  
		Last Modified: Fri, 01 May 2026 00:11:03 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a248aaaf060f82f0de6a4857b1a59843313daa978f6f692602510aac01c894`  
		Last Modified: Fri, 01 May 2026 00:11:04 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1cc85838a36396de6d144c3abf55765c4b22f1e55991dae450f0d8241df7f8`  
		Last Modified: Fri, 01 May 2026 00:11:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a89bce13c3ab9e691a1c89d7eee2c9a249e65eef5f5d300c9e44acfd99dd63`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.15` - unknown; unknown

```console
$ docker pull logstash@sha256:38a1bafb55be938f1b5ba08bc1fde46169a43bb201691d83c2848b57895f88cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d2eaa8773ac605d1b38ce33a7bdf814d93ec046c982e56baebf556da0eecd`

```dockerfile
```

-	Layers:
	-	`sha256:a7a4038dd82e65806583c16707f79370e99ffa43f2cba9bca79f0f3d7775dc14`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 3.7 MB (3695584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bdf9fce978b78c857983fe8181382f70f53ce24ccde0440fb4acb48b7a77209`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.4`

```console
$ docker pull logstash@sha256:956096357725d470096c23b72eafc5ce0f76fb209c9d1beb0047c43303ebe346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.4` - linux; amd64

```console
$ docker pull logstash@sha256:e48bcc2f1b5353e1da00ecf5b1f9cf1b687c4ac39c918cd17c7eb27d7598bbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516506342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f340e0680186995890f92b776be1831c426d41ff14c233f82fc2eb1d2fef3dd8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 08 May 2026 16:21:47 GMT
WORKDIR /usr/share
# Fri, 08 May 2026 16:21:49 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 08 May 2026 16:22:08 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 08 May 2026 16:22:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:22:08 GMT
WORKDIR /usr/share/logstash
# Fri, 08 May 2026 16:22:08 GMT
USER 1000
# Fri, 08 May 2026 16:22:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 08 May 2026 16:22:08 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 08 May 2026 16:22:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36218eb223c61ac82ff82eb08675499c85556bffe25ebc85e44630c4283361fc`  
		Last Modified: Fri, 08 May 2026 16:22:45 GMT  
		Size: 5.1 MB (5149394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5324f464cb65857c8a0fa20ee5d6b1c742c65f49c9aa7d45367c25971ddc9c2`  
		Last Modified: Fri, 08 May 2026 16:22:54 GMT  
		Size: 471.1 MB (471097447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c910d8caeaf5de4ca7c05af246014d15576a6834dc4316b462add49557e3382`  
		Last Modified: Fri, 08 May 2026 16:22:44 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc01649071854e306c7a19221a9c87ed722b6f9781c24a5cfe012fb66c7c46b`  
		Last Modified: Fri, 08 May 2026 16:22:44 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45d55806b320c1099f0e37e3fd557f1fbab85caf8e7731f7696dd8bcbe51f5e`  
		Last Modified: Fri, 08 May 2026 16:22:46 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87fb2f28819d8291a5a010827fa2e77bfd46a7ff3daa37dd4df2284cf603215`  
		Last Modified: Fri, 08 May 2026 16:22:46 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3108a368009d9d23cb6c401e00ed03c88c5c29ed12f3d61577b501f7e516eeb1`  
		Last Modified: Fri, 08 May 2026 16:22:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7cabee91724d72b77095dab5354855aa8c2ba9d65c7599744ae67c321ae8e`  
		Last Modified: Fri, 08 May 2026 16:22:47 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc291c3d1b2e8f3edcaf9aa7935fe1763bd600872cff8dca44de416c4ffbd6`  
		Last Modified: Fri, 08 May 2026 16:22:47 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:e9a127bd42dafe3a76c38830765f39fc0abb7795c4fa1aca903004214715c1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c62d9875a17a0b24547b1f2188bb2dd6c48204f907bd8e3b01fc306c7a19b8`

```dockerfile
```

-	Layers:
	-	`sha256:8135b7a97ef8100e980ef9997d5a2764baaae08a3b76baf480eba3b9c79b0e39`  
		Last Modified: Fri, 08 May 2026 16:22:44 GMT  
		Size: 2.1 MB (2119272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6adc0d27db069bbad0154c343b319a4a2012a5f5eda094df078f37cca667b8`  
		Last Modified: Fri, 08 May 2026 16:22:44 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:aecd4079888b58187e33b491716b58ed996694dbce8cc939dbb3552aef877a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512975220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edfc1ddd708c8f81272f41ebaba65a11dcd74cc08cb2e85e18dc4936d9c1e6c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:28 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:21:28 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:28 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 08 May 2026 16:21:28 GMT
WORKDIR /usr/share
# Fri, 08 May 2026 16:21:30 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 08 May 2026 16:22:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 08 May 2026 16:22:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:22:00 GMT
WORKDIR /usr/share/logstash
# Fri, 08 May 2026 16:22:00 GMT
USER 1000
# Fri, 08 May 2026 16:22:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 08 May 2026 16:22:00 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 08 May 2026 16:22:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3a6f295a5102e8cf1b3ce31aebd17d7de769507a25814abcafb83ce08867b`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 5.1 MB (5145180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7967625a19111b3b6b21610363db6cf9962fd5c1c67f500a56944e538ef8b9`  
		Last Modified: Fri, 08 May 2026 16:22:47 GMT  
		Size: 469.4 MB (469359639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84de457aaf1dc4a735ea4d9eac012ef4b8429ae3fe277d5167d6ea871491164b`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4c5dc81176d808bc33dc3bab6b7d1fa113069e4be80c9c927a7d255bf69dcc`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71840d58c8392214a6d2f221f35c8fe22572e13bf108d52f3fdf86d42f3770`  
		Last Modified: Fri, 08 May 2026 16:22:39 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041443213cc9339a09b68f726bd000fe02203fbd240d861d4bbfe8cecad755d2`  
		Last Modified: Fri, 08 May 2026 16:22:39 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69cb2306cb9e95c12263d3bdf40bb0d55c582c23a6317edfd71368ec860ae08`  
		Last Modified: Fri, 08 May 2026 16:22:40 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555beaaefa0a7330a5d16d9f873f14997f885dcfacf3dcd5f952ecd5d0379c08`  
		Last Modified: Fri, 08 May 2026 16:22:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98247cbeca46700aa29d67297cd3689ccb88ba975e4f9737694f09fcb813d03`  
		Last Modified: Fri, 08 May 2026 16:22:41 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:1c87d87be8f31bab936fba360277025217caa92c63b4ffe61427cafdd0d77b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae86f1212c2fc884dc89d3832b9d9f6edd72ed860ec529b393e37e901821caa7`

```dockerfile
```

-	Layers:
	-	`sha256:ccba3cd86b0064983863500e5e259be2c0b632cb76d8c0ca3a7530c7243ccc04`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 2.1 MB (2119842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2bcc44978f4d751f93fd1087a2cb7a2f546820af413c19534a359f349d440e8`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.0`

```console
$ docker pull logstash@sha256:149638ad5446895a72d5f0a7780ce16b2808d1b414925c63f75520c31ab9b53a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.0` - linux; amd64

```console
$ docker pull logstash@sha256:2d2c299c45cf4cbe4b9b135e8188597e5a33fd1beee61ddb8ca811ba0ac3d68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.0 MB (523023113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68691fe50c220624687d331cc724d54653a5e1bf6412b31c37bca1a3bea7c91e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 08 May 2026 16:21:47 GMT
WORKDIR /usr/share
# Fri, 08 May 2026 16:21:49 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 08 May 2026 16:22:41 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 08 May 2026 16:22:41 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 08 May 2026 16:22:41 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 08 May 2026 16:22:41 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 08 May 2026 16:22:41 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 08 May 2026 16:22:42 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 08 May 2026 16:22:42 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 08 May 2026 16:22:42 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:22:42 GMT
WORKDIR /usr/share/logstash
# Fri, 08 May 2026 16:22:42 GMT
USER 1000
# Fri, 08 May 2026 16:22:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 08 May 2026 16:22:42 GMT
LABEL org.label-schema.build-date=2026-04-28T15:43:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-28T15:43:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 08 May 2026 16:22:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1b905f0c9c4d977e71657ccc18908380215b6d28baf4bb55cd1da2392f4e6`  
		Last Modified: Fri, 08 May 2026 16:23:20 GMT  
		Size: 5.1 MB (5149424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef404a6d2a3af537fc6f595f23a3dd1bad5f2c5a66f7a9ea4bb53421d59bb134`  
		Last Modified: Fri, 08 May 2026 16:23:32 GMT  
		Size: 477.6 MB (477614100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45ee14043499853619a48624bbc3c6f7d114658aef359bca084cd9dfb9dece6`  
		Last Modified: Fri, 08 May 2026 16:23:19 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de69823116722814b186e0f89d1cf3ed300804454106379a532779aacf57949`  
		Last Modified: Fri, 08 May 2026 16:23:19 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ae35a292d05e3a790411cba668c12eb25d1ffb3d5c4132543b666cca8e39b`  
		Last Modified: Fri, 08 May 2026 16:23:21 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6695d303f462f5f4d7ae917c4aaed5d1f1db136909f6587649d60c0ec9b21`  
		Last Modified: Fri, 08 May 2026 16:23:21 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b842c47c37423ab752b2863fc59aeef48ec44863ef0991501d48b23695c9a6`  
		Last Modified: Fri, 08 May 2026 16:23:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7cea1a6915cfda7d7d3c5ea037ee407b79efca6e7e94e9aed2e5209fe4a4a`  
		Last Modified: Fri, 08 May 2026 16:23:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c345fed6194304ef476ebe957f6b4604aeb9eb14c5540716d93e490c5fae5`  
		Last Modified: Fri, 08 May 2026 16:23:22 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.0` - unknown; unknown

```console
$ docker pull logstash@sha256:4b875df8d598797028adbd4bae37da67f71707489cf5eb77d2e4f85108486323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e370dfe42fb4a4d5ab0b63454bf9333ca4bd2dfc351349117e2f03c176aa28`

```dockerfile
```

-	Layers:
	-	`sha256:ade50f1210e5dd67f7fc896e2301764cfc528cc329d1be374d3dcf33bf553b44`  
		Last Modified: Fri, 08 May 2026 16:23:19 GMT  
		Size: 2.1 MB (2123790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0da79e569faad9520d25aca73145bc6bb88ff025e02596c4187e1e3d9bf90`  
		Last Modified: Fri, 08 May 2026 16:23:19 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7be12bcefb38cf1b5bd97cb7b2befee3367a6ffa0e96845909fdbd5e96b6797b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519514977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780c86b6cb75b38c86661a760d9be540251fe6f5114206e4275f367dbaed00d6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:34 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:21:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:34 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 08 May 2026 16:21:34 GMT
WORKDIR /usr/share
# Fri, 08 May 2026 16:21:36 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 08 May 2026 16:21:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:21:58 GMT
WORKDIR /usr/share/logstash
# Fri, 08 May 2026 16:21:58 GMT
USER 1000
# Fri, 08 May 2026 16:21:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 08 May 2026 16:21:58 GMT
LABEL org.label-schema.build-date=2026-04-28T15:43:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-28T15:43:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 08 May 2026 16:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152fa3077c39b2fa3a23653fbd9c859988e1411fd8f4a846c872bf62064878b6`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 5.1 MB (5145186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd403b0fc70d6b7c9cf326d1a83fab810c6ab050f747acfeab6979630d4e7fc6`  
		Last Modified: Fri, 08 May 2026 16:22:47 GMT  
		Size: 475.9 MB (475899316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6460309424c7138c82a2d9878f4f65cd681bb32ff2eb1d3b0131a53be99cd285`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370facb07539697eeccb7e18aec73606af30ce7c0132b7f2f943b9a4ab000970`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faedbe4e1655c7797aace87bb0077e069d6546fa6e742d71740565672f70cc`  
		Last Modified: Fri, 08 May 2026 16:22:39 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3758e24b9c536b9ec51df30e487ff428be6ee7e4b6982ab58c35411ec71ee4`  
		Last Modified: Fri, 08 May 2026 16:22:39 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8f06eef77a28017da2c8a7f175c524f40d4334c8a6d2fd34a38cdcd8cae234`  
		Last Modified: Fri, 08 May 2026 16:22:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797bc385c7a308f52b8914988936f842eaf064c5e492b27fb6b745c1e8e37f7`  
		Last Modified: Fri, 08 May 2026 16:22:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bbafab9cf2be4aa6baf98de55a114c19620e04a2e3f5d366040f9a88700fd3`  
		Last Modified: Fri, 08 May 2026 16:22:40 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.0` - unknown; unknown

```console
$ docker pull logstash@sha256:3a98342b96702ef770fad5c6820b9b862dce5de1ae2f205b9307e64cbadaa844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2154637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04562d94645c54fe08e3f64b6e79b4eaede54b5a8f0e66683f8bddd516fd0cbd`

```dockerfile
```

-	Layers:
	-	`sha256:fb8e22aa14f328d00375fc8c80073468b99db8e1238bc185718cdc5add98b0cf`  
		Last Modified: Fri, 08 May 2026 16:22:38 GMT  
		Size: 2.1 MB (2124360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ac24b05dc09dab9e0776f36c3d32ceac578ae606bac2fc1354d8e5ddf29d1a`  
		Last Modified: Fri, 08 May 2026 16:22:37 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
