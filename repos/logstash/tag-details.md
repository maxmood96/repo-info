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
$ docker pull logstash@sha256:25337c852a6db27b952c3e2e630f19ce04eda19dbb85df2d3a03b5a291302e58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.4` - linux; amd64

```console
$ docker pull logstash@sha256:cd5cb4e6a8ca7153931b19716a710e1df149270a9a8e8a936b6f2b062cc17089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516843471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99431da0fc672294e3102299ff616c36f89ac53a9c07633dfd6222eb9b3f936c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:11:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:11:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:11:17 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 23:11:17 GMT
WORKDIR /usr/share
# Tue, 26 May 2026 23:11:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 26 May 2026 23:12:05 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 26 May 2026 23:12:06 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:12:06 GMT
WORKDIR /usr/share/logstash
# Tue, 26 May 2026 23:12:06 GMT
USER 1000
# Tue, 26 May 2026 23:12:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 May 2026 23:12:06 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 26 May 2026 23:12:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec67e6925d2b966ee90f38ad2e9488e474442ddcf6d0bc031ec50ea7a8d79c`  
		Last Modified: Tue, 26 May 2026 23:12:39 GMT  
		Size: 4.8 MB (4773486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a974ebfbfb12725d15382c515c72840f07dec25c1d64f2b2f4b41489eee99732`  
		Last Modified: Tue, 26 May 2026 23:12:48 GMT  
		Size: 471.1 MB (471096551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed3fc5f22d029438202aa4c1623b4f24c0bd948ba70e7043cc6ff5bd357114f`  
		Last Modified: Tue, 26 May 2026 23:12:39 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395703b790a64f55961a8de5764a2c8abc177b3fda66ab4f1e3786f408a5b7b6`  
		Last Modified: Tue, 26 May 2026 23:12:39 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70963d375e1ed2fcb265b395215d2fbd9414f78f8210f38b0329f1f24a09e5c`  
		Last Modified: Tue, 26 May 2026 23:12:40 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33fc8a27e4ddb4cc14b4959b8ee65a79cf9a18c8fec175b985507d06006891c`  
		Last Modified: Tue, 26 May 2026 23:12:40 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1943e0d9640626a89020d6d78cb037579f65db99d53e391a8885fb474409fb2`  
		Last Modified: Tue, 26 May 2026 23:12:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63da8799999b75457bfa59da11ec22b410ac73b7a6505b14b6a869abdaa2324`  
		Last Modified: Tue, 26 May 2026 23:12:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe7fd518341abf2ed652d9b1165e15e6ec5264425d60c63560aaa8a2e775fd1`  
		Last Modified: Tue, 26 May 2026 23:12:41 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:e014811113aebedcb01f3c92f081c99a45180fd3d866dea34ea5663aabaf49d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d82a4f510f48db30688dde00afc5ed864f1e3da110132a5bee5f66e987643`

```dockerfile
```

-	Layers:
	-	`sha256:ef952c821f4d2424a5708df8c3f2c0520e715b1a037da9df6e16ee4f2a0143c9`  
		Last Modified: Tue, 26 May 2026 23:12:39 GMT  
		Size: 2.1 MB (2112940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb139ea1e59493a729889b97b6acd4c88e0717fc548a16387f4ab0ebe4ae764`  
		Last Modified: Tue, 26 May 2026 23:12:39 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0acfce34748cc02da8b32e6980e588d6d8f7765948e38094087c81e864f8732b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.2 MB (513236819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ee52f93005f4761135290bb5249ac32f2ab75fcac87febe20c8c8efdbd77a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:52:51 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:52:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:52:51 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 23:52:51 GMT
WORKDIR /usr/share
# Tue, 26 May 2026 23:52:53 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 26 May 2026 23:53:16 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 26 May 2026 23:53:16 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:53:16 GMT
WORKDIR /usr/share/logstash
# Tue, 26 May 2026 23:53:16 GMT
USER 1000
# Tue, 26 May 2026 23:53:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 May 2026 23:53:16 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 26 May 2026 23:53:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fe267bb52509ce4510a5661cd9d40a69a43e8ea63589c0eb12ab5fc3d3bddd`  
		Last Modified: Tue, 26 May 2026 23:53:54 GMT  
		Size: 4.8 MB (4770775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fb1f8db4d4b0231d77d997670eb4cf4c0dd5d4e6a46072a9471bef4686fb6`  
		Last Modified: Tue, 26 May 2026 23:54:04 GMT  
		Size: 469.4 MB (469361151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ec439121f0637ee940e354670228e1fc0a5c9b5dfb9f897912ce00a4c13de`  
		Last Modified: Tue, 26 May 2026 23:53:54 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bad6ed466d9db45a288938fc0568352e5c483cb10d37aa16a61c1ebd37428`  
		Last Modified: Tue, 26 May 2026 23:53:54 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c06aef391f3f0f0995daa50bffa66defab4c27a27b8cfece66addc36528ab2`  
		Last Modified: Tue, 26 May 2026 23:53:55 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8f893df1d7eb863c7b6d8e834f5f31cfa4a86d97a476fb93e2d4491c73a045`  
		Last Modified: Tue, 26 May 2026 23:53:55 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467629b817a777d80e70bfd099c534cfbad617b89dc5ec3a79d65a8e1a8e43f5`  
		Last Modified: Tue, 26 May 2026 23:53:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcdc1309690982555061a92c5c4f030454e10b159023453e7dc3d49a15da8e4`  
		Last Modified: Tue, 26 May 2026 23:53:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4650774b21878eef5d92ed5429624172b6aaba01d081bcea98e3924bfa42e4f`  
		Last Modified: Tue, 26 May 2026 23:53:57 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:eee7c1f41b76d154fcbfa5a2d1aec8d23f79a76efecf2b486765975a2928df2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b1963632e7e8c5f28d1387651cb8a3aaa7ff5a7e012b0b11ff183e31f48176`

```dockerfile
```

-	Layers:
	-	`sha256:d2fab1c328c2c094fba999f4cdbbbad8be7943371ddf61b51ecfd356620ffdd2`  
		Last Modified: Tue, 26 May 2026 23:53:54 GMT  
		Size: 2.1 MB (2113510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d303fbde001334793d1d6eee2a9f26734a291daff2451400b55376c86e00b890`  
		Last Modified: Tue, 26 May 2026 23:53:54 GMT  
		Size: 30.3 KB (30275 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.1`

```console
$ docker pull logstash@sha256:85a4cc588f2ac8de2fafeddd5d8e8d873cfeb6a07fc36507d6364020e2cd8cdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.1` - linux; amd64

```console
$ docker pull logstash@sha256:746a4219a3789cb55a2715d938611d8aab1f5363fb1ac9953f62f499fdacbab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.9 MB (523905831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2974c4e35a371ddad1988f7f7dccafdb43ff6dc6682959ac81bacc201bf493b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:11:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:11:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:11:19 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 23:11:19 GMT
WORKDIR /usr/share
# Tue, 26 May 2026 23:11:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 26 May 2026 23:12:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 26 May 2026 23:12:14 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:12:14 GMT
WORKDIR /usr/share/logstash
# Tue, 26 May 2026 23:12:14 GMT
USER 1000
# Tue, 26 May 2026 23:12:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 May 2026 23:12:14 GMT
LABEL org.label-schema.build-date=2026-05-08T14:31:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T14:31:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 26 May 2026 23:12:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099eb27cf4b6d0bd52ed1b7bec45bd28d5e9be25ead3824f979d3b576bf7a737`  
		Last Modified: Tue, 26 May 2026 23:12:52 GMT  
		Size: 4.8 MB (4773497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4741a4652a9559bb9a431ef1082155d6f585798f724f966eda508b118d645d3a`  
		Last Modified: Tue, 26 May 2026 23:13:01 GMT  
		Size: 478.2 MB (478158832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7da8e23fe628ce5bb5c3553bfc1cd782c44f7a2078143de86d052d5d12948d`  
		Last Modified: Tue, 26 May 2026 23:12:52 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a40e827235f8e4c9b15180426d11b9410847c80419a3d744ff7a67287cfb23`  
		Last Modified: Tue, 26 May 2026 23:12:52 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32770dc6041c6f40016d2998a56680d4e59eabbc27580d0a45ccb06f6a973bcd`  
		Last Modified: Tue, 26 May 2026 23:12:53 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbeba1922afcf1ea346b5bdc866a16cc7cde24050de8c850c3077b7537f0675`  
		Last Modified: Tue, 26 May 2026 23:12:53 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371fcf6a87545f7d79ad72114fb9548b47c411d53e34125cbf2199f7efe63d9a`  
		Last Modified: Tue, 26 May 2026 23:12:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70ab99ddff383969fb46410cabd97427c48158bc2c7f62efa9627b68e7eda41`  
		Last Modified: Tue, 26 May 2026 23:12:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6a57f275983de2f9e4be158c444bf6a624a69468aad5eabee2b26ff2bfc19`  
		Last Modified: Tue, 26 May 2026 23:12:55 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.1` - unknown; unknown

```console
$ docker pull logstash@sha256:2a31ed9d219510415adde9b5a0be58230a218fd39c1e37a7cecc7c4875da3b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee65dceaccdb496def8efdb048f0b2ead33528542b4930303895a4655924e63`

```dockerfile
```

-	Layers:
	-	`sha256:ec88e72537c52c35ec166130e3650a1113e83d6e840121f9134084091f33f4a1`  
		Last Modified: Tue, 26 May 2026 23:12:52 GMT  
		Size: 2.1 MB (2118120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2196dcb0a25da7de55b5db2ee6866bf42450b31e4c14cb62631a2cf8ca220489`  
		Last Modified: Tue, 26 May 2026 23:12:52 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:32fc1d110a099dfb300d472f6e7fa3e2a1f72beed9dda46e4bca42bca9d03be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.3 MB (520325997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96326354c2178b799811d5040915c71858769f2b0a98fff73eabe68f0981ab52`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:10:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:10:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:10:43 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 26 May 2026 23:10:43 GMT
WORKDIR /usr/share
# Tue, 26 May 2026 23:10:45 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 26 May 2026 23:11:07 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 26 May 2026 23:11:07 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:11:07 GMT
WORKDIR /usr/share/logstash
# Tue, 26 May 2026 23:11:07 GMT
USER 1000
# Tue, 26 May 2026 23:11:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 May 2026 23:11:07 GMT
LABEL org.label-schema.build-date=2026-05-08T14:31:03+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T14:31:03+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 26 May 2026 23:11:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1630a00c56b885af1a2c3bc0d0b8081008e7f438780e48cf7d9108fe21e0553`  
		Last Modified: Tue, 26 May 2026 23:11:46 GMT  
		Size: 4.8 MB (4770805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f55fe4298e5852b86ef667fc482de99dcae77a8fe1b218120763f03ee1785`  
		Last Modified: Tue, 26 May 2026 23:11:56 GMT  
		Size: 476.5 MB (476450233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba13af23f5875cdff5263ba00228049326a11efea92e30b59ae9a4a5f83ac2`  
		Last Modified: Tue, 26 May 2026 23:11:46 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3970755b302849dc57937a7edcc5f0e4c9ba538f184a0c1436be4e852e9b87e`  
		Last Modified: Tue, 26 May 2026 23:11:46 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215003686c153b064d62e58f34876268906252d540510a7cddd5869ab10158a`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f96a4aa94fc1dcf73862f77df4bc941532e524c753e4f11e4b7c54c7877edb`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7064631b5698ca1bed6d6dd894c75a5a49c62e500c7ba133ba9e121c7b54de`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92b5374e8c335250f37dda1a19d21036530a806cf3d4c844ea9f28bd4ee853a`  
		Last Modified: Tue, 26 May 2026 23:11:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0464265b63f48873f254af841be0227f0dc6941ab22d85317f165eab3204336f`  
		Last Modified: Tue, 26 May 2026 23:11:48 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.1` - unknown; unknown

```console
$ docker pull logstash@sha256:57d5a12f502e004c91435832a238aab1769d792687fa2eeb622153c5dfb27a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ce7da569b46c0a9c62207459ad4f306518a282008904519ec0beba86ab9202`

```dockerfile
```

-	Layers:
	-	`sha256:7e3fae55ec86b5251176722a35662dad9431615d3459b6c19c1a7ceba798ed75`  
		Last Modified: Tue, 26 May 2026 23:11:46 GMT  
		Size: 2.1 MB (2118690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2761688be940fc40654d5121753ddb6aa9b4137120848ee778bbfd3f4811a4`  
		Last Modified: Tue, 26 May 2026 23:11:46 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
