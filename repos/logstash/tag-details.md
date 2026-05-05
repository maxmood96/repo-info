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
$ docker pull logstash@sha256:e0ec8861930464cf7e65ec77fe94e4f84ab621f742b59b829ad6fb6c1b17c9dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.4` - linux; amd64

```console
$ docker pull logstash@sha256:f2d55c6de43d922ebbd713aa9977b211958ce4498b19853e03c47e33d06efd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516536678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05e64d85fad94633644a0a8c3ba3fea7656d17407e2999bfe791905d5128a8b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Fri, 01 May 2026 00:09:58 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:09:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:09:58 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 May 2026 00:09:58 GMT
WORKDIR /usr/share
# Fri, 01 May 2026 00:10:00 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 01 May 2026 00:10:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 01 May 2026 00:10:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:10:21 GMT
WORKDIR /usr/share/logstash
# Fri, 01 May 2026 00:10:21 GMT
USER 1000
# Fri, 01 May 2026 00:10:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 01 May 2026 00:10:21 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 01 May 2026 00:10:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8013921dab50687f12fa0c34d7ef0515fd19279add7a635a54dfdc3d92b13b55`  
		Last Modified: Fri, 01 May 2026 00:10:59 GMT  
		Size: 5.2 MB (5150407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904edca78fbaf43e64caa3330d1a5a02da9fb2bbecb20d79a189cedfff7b6cbc`  
		Last Modified: Fri, 01 May 2026 00:11:08 GMT  
		Size: 471.1 MB (471096766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09892ee814fec80f1592fb4c6a0eeb5235e3ce48e5b8941730c5a18ec2aefb54`  
		Last Modified: Fri, 01 May 2026 00:10:59 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f13deff0648f6457da750e0f343f0591af5725da5408919337cdfa767d13d9f`  
		Last Modified: Fri, 01 May 2026 00:10:59 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11456e42183763b365ba4e960c5c21f57aaeb4f3f4cd10b02885431f93db134d`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1705520596fd2a27ac2f3c986ca94d126f526613305eb0259b9826106ee6a5fb`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099bda151142e6e587e5d787318878369a891ad79589490590971c09db18a904`  
		Last Modified: Fri, 01 May 2026 00:11:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0473087520802f50a3ca1bf11868c3b735c8efdbcefa119e619962678c8394da`  
		Last Modified: Fri, 01 May 2026 00:11:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13909932a93cb092cc19f0b423b775918f8a9a6a94ba0c3c64eeade733c6277`  
		Last Modified: Fri, 01 May 2026 00:11:01 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:deaf671d2e972186a28008bdf24198b901b74799ad0d0d1cbd2826ed754e2cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef18efd73ecc8ae1abbe818ce39fcf635623b60d91c97654bf195583659d8073`

```dockerfile
```

-	Layers:
	-	`sha256:1f896a93adef437f008591dac9412d3dbee6cc00b9282a238132e78fabea4b65`  
		Last Modified: Fri, 01 May 2026 00:10:59 GMT  
		Size: 2.1 MB (2119264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cca0ef7d43fca4771e2cf6db4cc046c98cda199cadacc76aa77082264c8aa4`  
		Last Modified: Fri, 01 May 2026 00:10:58 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bcfd6e2623f691a60240bdcd0e52afbc5537a645a5f96cf256583ff9cf8196e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842283ec8683f16fb219ae108d183da9176baa700ef76a231f5a5a072f874de1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Fri, 01 May 2026 00:09:26 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:09:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:09:26 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 01 May 2026 00:09:26 GMT
WORKDIR /usr/share
# Fri, 01 May 2026 00:09:28 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 01 May 2026 00:09:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 01 May 2026 00:09:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:09:58 GMT
WORKDIR /usr/share/logstash
# Fri, 01 May 2026 00:09:58 GMT
USER 1000
# Fri, 01 May 2026 00:09:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 01 May 2026 00:09:58 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 01 May 2026 00:09:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caa53f0813f90f3536dffd0b81c6ab9ad133f69e40480515021d681f01b88e`  
		Last Modified: Fri, 01 May 2026 00:10:36 GMT  
		Size: 5.1 MB (5146121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eeaf6f7d68701a56a094a7ca742d857eca3e48c1c825f59b830c8c6732f7cd`  
		Last Modified: Fri, 01 May 2026 00:10:47 GMT  
		Size: 469.4 MB (469359535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b47b47ee787180fabd260beac0300c69ed9b93220d4f25c501cffe064f8f578`  
		Last Modified: Fri, 01 May 2026 00:10:36 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496f46b57ca502e7fb03979612be32159717143915f481547efccfa37bef48dc`  
		Last Modified: Fri, 01 May 2026 00:10:36 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7c8491929468782173956ae10e2d96de700e3975d6c12f91fa0981e70ae29`  
		Last Modified: Fri, 01 May 2026 00:10:37 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281b832e035b2cffb7cd61e89f0f45fe6149b01b9db6107f6715f77351262172`  
		Last Modified: Fri, 01 May 2026 00:10:38 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19a9b42ab91eb4731fa9208dbbbfe925aeb9dee69546ebaa9e665124f02c5f0`  
		Last Modified: Fri, 01 May 2026 00:10:37 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bc75133cb6ba743b8e66a12b978cbf2a4a0bb8c24843301bf49b0ef93fca36`  
		Last Modified: Fri, 01 May 2026 00:10:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadfac1eafdbd33195a23f816ac2061ec047e93c5ad180ccd761315b54104fe0`  
		Last Modified: Fri, 01 May 2026 00:10:39 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:5581aff01c88e1d8b114def57dfc1cafffd6b28725c18d8322fd7485a8cda65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a369ee2da1c9766491d1112f01242880ce3d0b11394c091b9b66cafaac7abd4`

```dockerfile
```

-	Layers:
	-	`sha256:e7b55f023b8f26708f45e06fb0b2a793d7d3ff1aec99fc1c8d36e158a7b32527`  
		Last Modified: Fri, 01 May 2026 00:10:36 GMT  
		Size: 2.1 MB (2119834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648f916f5e4b2513b8f70497ded084485f9e8d36d4396f40a60ba881e9909f77`  
		Last Modified: Fri, 01 May 2026 00:10:36 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.0`

**does not exist** (yet?)
