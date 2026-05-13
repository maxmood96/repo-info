<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.15`](#logstash81915)
-	[`logstash:9.3.4`](#logstash934)
-	[`logstash:9.4.1`](#logstash941)

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
$ docker pull logstash@sha256:55d6ef57b3218de182783c4baf5a6e198730a170be793690f409cc547c7ce27a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.4` - linux; amd64

```console
$ docker pull logstash@sha256:0439cc1d56fede28176541dfc0f18cbda0ba73c5501c5057620cebba2b5bdf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516533284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ab37f26be95a02867b79b415f429eb8ec1879f1ed85d4d98c071b085e53628`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:34:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:34:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:43 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 May 2026 23:34:43 GMT
WORKDIR /usr/share
# Tue, 12 May 2026 23:34:45 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 May 2026 23:35:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 May 2026 23:35:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 May 2026 23:35:03 GMT
WORKDIR /usr/share/logstash
# Tue, 12 May 2026 23:35:03 GMT
USER 1000
# Tue, 12 May 2026 23:35:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 May 2026 23:35:03 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 May 2026 23:35:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51c59b97c6cb96d35cc7309eb3c7f1c05cb60b1e2b84d4f150864f701e607ab`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 5.1 MB (5149165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f723e077daf4230a9fb65764e08f7f2031839ebcb2281df2bc215984d97b1000`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 471.1 MB (471096759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e502e107f340fb5df1278bd40b3f2cd4ec919dd94c132d9b79cf71c0e292712e`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe2173072fe70fe0addab361b01f4113495ca6979c3cd3482fc4431752b000`  
		Last Modified: Tue, 12 May 2026 23:35:36 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3727427820e365e0491f62615eb7947e2da933db8d5f77213a46375b8edf1133`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e52f56daa3e82c266bcf1e920446478d22f789c92cec588908f097443af8f03`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025ee4bb9d52506dae80e08e485e47b04b3521ce5e4ceb5b76a67caf51af84e`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15342d103329282b30857183e592accc7f36f1dd1e84b9873fb08185e8b68b3`  
		Last Modified: Tue, 12 May 2026 23:35:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f7690b7515bcb7b94427a6a987ee36c17c9ef823198c167e7a62c37abc378f`  
		Last Modified: Tue, 12 May 2026 23:35:39 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:e6ee835039a15195a3a589fda575dd97285eafd1b3bb283cabc48da068108c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44d96a957385928589e87010b48ca50fb2a13e8b7a1235d4fd305faadecf237`

```dockerfile
```

-	Layers:
	-	`sha256:c3f80f75ed4089da3eba1e527ec74a10249a21c0ad8c2123f2f6231b0b28e4ed`  
		Last Modified: Tue, 12 May 2026 23:35:36 GMT  
		Size: 2.1 MB (2119274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00f7349d90aa9af33693e399fec9eb3e3fcbc63cccf62333759a47784ebceb7`  
		Last Modified: Tue, 12 May 2026 23:35:36 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f054b2e53caad5cc1b0aab570176a2c7b06e06f5fb188e46c9ece33e6c980364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512977022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd8b68dba80307adfdc428f2e64d9053be391e22e26f8b2e5ad54d2acfa80bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:34:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:17 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 May 2026 23:34:17 GMT
WORKDIR /usr/share
# Tue, 12 May 2026 23:34:19 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 May 2026 23:35:07 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 May 2026 23:35:07 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 12 May 2026 23:35:07 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 12 May 2026 23:35:07 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 May 2026 23:35:07 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 May 2026 23:35:07 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 May 2026 23:35:08 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 May 2026 23:35:08 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 May 2026 23:35:08 GMT
WORKDIR /usr/share/logstash
# Tue, 12 May 2026 23:35:08 GMT
USER 1000
# Tue, 12 May 2026 23:35:08 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 May 2026 23:35:08 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 May 2026 23:35:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a1350113a2acaceeefd4086b6f1c641af2033cc9b04974ecf770ea65731bc1`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 5.1 MB (5146044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24bba115382400e38984f4061e54204aea79e92d1b96367bd303f77b511f9f6`  
		Last Modified: Tue, 12 May 2026 23:35:53 GMT  
		Size: 469.4 MB (469361219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534cb72eb6a482ca81573b7b310a0f242a00721c6353cf50ccf26923a477672`  
		Last Modified: Tue, 12 May 2026 23:35:44 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dafd8b58b20ff24b83253ee9b3d0df29f96e69c53285a62bf892e52d6c4164`  
		Last Modified: Tue, 12 May 2026 23:35:44 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5af03b77c596bced2ac16843e214acecd04ef7bd9f2e0530183846585c27460`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f741d8d39d216610d69bd326c194963dab38cf8ce1ef3a3c169cbe0d140425`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e50854c2ac596f2782ae57135e2b0ba6bee589770ab989aedacec4a4671b2a`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f851e30ebf6822547e795eea3caf739206bc23a0f745cf3ca94420adb0268c`  
		Last Modified: Tue, 12 May 2026 23:35:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1542f3e469e7c13f144359ede431c00b78846b3dcf51d159fa8c08a7ae8cc55`  
		Last Modified: Tue, 12 May 2026 23:35:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:a81588c8052185129bdb340124c7ea97e58ecb5def5a963cc7f3502da35dd905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd4c2c29177e3ce2bd6b63fc642f01f4880bf261ab65ca769da07dd679f68ab`

```dockerfile
```

-	Layers:
	-	`sha256:fb154c139823a79febe237e7aedec25bb7c78b7fdc2879230def47cb7b5096bd`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 2.1 MB (2119844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f3efa272bd38dc88c60f779eeba2a6445e3bc6e8f3379c1abfe268d58eb67b`  
		Last Modified: Tue, 12 May 2026 23:35:44 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.1`

```console
$ docker pull logstash@sha256:19ca09d34ae5739807ec6731d183b33725b0995adbeba1ad19892b129b588679
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.1` - linux; amd64

```console
$ docker pull logstash@sha256:ae455a02c6649fa65ddc2c8344f5e8b5eec59bda6273b398d2c875a629db931b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.6 MB (523595815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f5739d81cb5935ee53820ad2bb86ef24ab4035bce340c29942da1dfacfe667`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:34:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:34:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:43 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 May 2026 23:34:43 GMT
WORKDIR /usr/share
# Tue, 12 May 2026 23:34:45 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 May 2026 23:35:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 May 2026 23:35:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 12 May 2026 23:35:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 12 May 2026 23:35:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 May 2026 23:35:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 May 2026 23:35:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 May 2026 23:35:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 May 2026 23:35:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 May 2026 23:35:10 GMT
WORKDIR /usr/share/logstash
# Tue, 12 May 2026 23:35:10 GMT
USER 1000
# Tue, 12 May 2026 23:35:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 May 2026 23:35:10 GMT
LABEL org.label-schema.build-date=2026-05-08T14:31:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T14:31:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 May 2026 23:35:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1a6015fa2a3bd09a937fc80c6387a3435bdbd782706c0f79cc78406148881`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 5.1 MB (5149252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023b1a9421e8c25c4d001998281fce52d0e7df95bd14fc4f164c1bfa9d21bb25`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 478.2 MB (478159137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b2d1bcda623a53e480b521e1cdf652b0d36c2f183af667543c4fba4f40f3f`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 6.4 KB (6363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3532fa3f7245f13583c41e01d371b0f2e5b50e38f14242851f20e78a353de78`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caf1751af647e7e523b597e38f12dd6606d611eaefdc1709f9b15e31f35b186`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69efffbc624e1fa3d41d94277dba2c17807654c20ca3a27a6b66f3d3f2ad511`  
		Last Modified: Tue, 12 May 2026 23:35:46 GMT  
		Size: 1.6 KB (1573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5866dcc99cda8699f047fcec7cf3706b1b6ece7e0c55017e8fbda8338e98a956`  
		Last Modified: Tue, 12 May 2026 23:35:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b873a6053b7a7883ccc928c01a1f56865281dd5fa4d59cbc35addf00282533d`  
		Last Modified: Tue, 12 May 2026 23:35:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca40ce40acbc9cf5017ad92499c8282921142ea28d2bcc9e93e5f54627e5c83e`  
		Last Modified: Tue, 12 May 2026 23:35:48 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.1` - unknown; unknown

```console
$ docker pull logstash@sha256:7675b5b61abb7a30019f23abe15cbefcaecc06a49af76c2ef344ebeff6301c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2154654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15c49cac4ce1ab65733367cb34128b988f5d213389116e9370a245f66c87b7b`

```dockerfile
```

-	Layers:
	-	`sha256:75d2fd0a64eee18c66bb5dac11fc42d03475c7b70774bf49fc9248daa8f963c9`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 2.1 MB (2124454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780ea9a51af077c96aa4a982bb8a577564774a0328bcf4cc315e82d650494264`  
		Last Modified: Tue, 12 May 2026 23:35:45 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2799082f38c1511919cd6f208d86fe54b961a864c507ae1d0ea1564e61a234ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.1 MB (520066425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3986eecf2e44bf27a4ab026d4cf88d5a5353f6139bed702f3dbd137c5ece1ba4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:34:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:34:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:20 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 12 May 2026 23:34:20 GMT
WORKDIR /usr/share
# Tue, 12 May 2026 23:34:22 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 12 May 2026 23:35:14 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 May 2026 23:35:14 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 12 May 2026 23:35:14 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 12 May 2026 23:35:15 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 12 May 2026 23:35:15 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 12 May 2026 23:35:15 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 12 May 2026 23:35:15 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 12 May 2026 23:35:15 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 May 2026 23:35:15 GMT
WORKDIR /usr/share/logstash
# Tue, 12 May 2026 23:35:15 GMT
USER 1000
# Tue, 12 May 2026 23:35:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 May 2026 23:35:15 GMT
LABEL org.label-schema.build-date=2026-05-08T14:31:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T14:31:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 12 May 2026 23:35:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbcd5014a639dfb6d2c2d3b9086b9a4724f4c3619286c1b7c3b559e859db61`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 5.1 MB (5146035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698011aaa830911565a6cbea75dcda1788fe28e62774177f33efab18b576759e`  
		Last Modified: Tue, 12 May 2026 23:36:03 GMT  
		Size: 476.5 MB (476450553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92933be4058b17226ed79f215594ae8c408534334b3e550fd68bf575cff35f6`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c701189e72d861f417cdaef83a930617afb129025aeade4adf64a8810d69ca`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba532052d9eb4c9f11561fab8db52a6aad663d12545631f7e386198f7000201`  
		Last Modified: Tue, 12 May 2026 23:35:55 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb918831a30334ff6682270105c5850113a2873726450c95cc2d9feeb95a850`  
		Last Modified: Tue, 12 May 2026 23:35:55 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241a4b79de7785c652ec2f0eecd65ab6e49dcf226cc3b9bf313fb215ed93f0b`  
		Last Modified: Tue, 12 May 2026 23:35:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f5758ac2b79c3cd76d0e0be7ae20ff76fe595e322eacade176334d6d0f9fbc`  
		Last Modified: Tue, 12 May 2026 23:35:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c7144121bf8da8ae818dc828adab5973223aa630b4feb17069360fc395661`  
		Last Modified: Tue, 12 May 2026 23:35:57 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.1` - unknown; unknown

```console
$ docker pull logstash@sha256:50970300196eb450265efbc86573d4621fa33f6008a858161f4e084f7071077b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1767c1a75ebaf10fe232e0f2e1c7e744f1424da2cb75da0b80e2fc543a5e325b`

```dockerfile
```

-	Layers:
	-	`sha256:020bb2e89137f05bd31d20ecba6cd6a81a142c36994ddf16b2e66840e1981335`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 2.1 MB (2125024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec5bf41ec767c8b12d4b65a8d26b2098d158d4c15ea1cd04e5315c8ef34e116`  
		Last Modified: Tue, 12 May 2026 23:35:54 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
