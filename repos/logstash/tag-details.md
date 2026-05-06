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
$ docker pull logstash@sha256:28a143ed4e72dcda671adc4d8a8ff3be5a8f9ae4fb888a3f01255f6305fa2e71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.4` - linux; amd64

```console
$ docker pull logstash@sha256:55151a4ec1d02a20cc6b773f695bce21d65a9ad2acccf6f9b8cfdfa6e6ae84d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516529120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61618f00236576612892d4c07a82fddd27ceabe488c659a1a69c7caa2c468266`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:19 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 05 May 2026 23:09:19 GMT
WORKDIR /usr/share
# Tue, 05 May 2026 23:09:22 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 05 May 2026 23:09:43 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 05 May 2026 23:09:43 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 05 May 2026 23:09:44 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:09:44 GMT
WORKDIR /usr/share/logstash
# Tue, 05 May 2026 23:09:44 GMT
USER 1000
# Tue, 05 May 2026 23:09:44 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 05 May 2026 23:09:44 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 05 May 2026 23:09:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da59cc81d8e7f4b8082ba37de7d30dfcd0a9e919a99d2d181bd3f5470ca8d99`  
		Last Modified: Tue, 05 May 2026 23:10:20 GMT  
		Size: 5.1 MB (5148606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4202a0696d72c9fc9853b4f0c475b85092d3ddf94298bdf624fde783565e51`  
		Last Modified: Tue, 05 May 2026 23:10:34 GMT  
		Size: 471.1 MB (471096676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca66302b4e721a0ef2e32b2e2dac1635d8c2d4aaf3726ae147e187349f09792`  
		Last Modified: Tue, 05 May 2026 23:10:20 GMT  
		Size: 6.3 KB (6291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fd212a0cc8d6421374227431f8890eba95d3109932b012650651f9cf1f3aaf`  
		Last Modified: Tue, 05 May 2026 23:10:20 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e77980cfcdace6cb112cc2eb84d6de6e3c4626ca5b82c62a6c763a184652e`  
		Last Modified: Tue, 05 May 2026 23:10:21 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af78bf23951f955eb9ccb63517a587cf262b783a0512fcbc13dbc7d609570f2b`  
		Last Modified: Tue, 05 May 2026 23:10:21 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324527535fc0c99c73011834ce7ba1af527effd4373ad85c0b65a1a455ab8ff4`  
		Last Modified: Tue, 05 May 2026 23:10:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27abf208feffec3fb8ad04eaa41b15e7347a15e61b9d566862290a2b8218728e`  
		Last Modified: Tue, 05 May 2026 23:10:23 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d180cefaca3c089cc4d9e0931c20c5caaf01ab6de6756bf341e9e6d1d7b5143`  
		Last Modified: Tue, 05 May 2026 23:10:23 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:7894bd087b4d17e50dae1856385cb8e97087337e9fcfdc472ab873b1e54c3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feccbd5aeff1791089922f50102e306139673ab8bd242a1eb25d41530f8a082b`

```dockerfile
```

-	Layers:
	-	`sha256:58d4b37930d6ab4208b50a0c6d44c7ac70e4a9a9257139ca502d033fb8eef1fe`  
		Last Modified: Tue, 05 May 2026 23:10:20 GMT  
		Size: 2.1 MB (2119272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3de1603aa9950e01526151389a324664513bae17b92e0d3f491f477383942ce`  
		Last Modified: Tue, 05 May 2026 23:10:20 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:83c205b9e1b93a853d22b556b4c220130fab49ca1567f4bdccc654be609e0e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512977570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5988fd8c47722a1362012c1417fa2f787d50be0d837925f93c92c89435647878`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:09:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:00 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 05 May 2026 23:09:00 GMT
WORKDIR /usr/share
# Tue, 05 May 2026 23:09:02 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 05 May 2026 23:09:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 05 May 2026 23:09:55 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:09:55 GMT
WORKDIR /usr/share/logstash
# Tue, 05 May 2026 23:09:55 GMT
USER 1000
# Tue, 05 May 2026 23:09:55 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 05 May 2026 23:09:55 GMT
LABEL org.label-schema.build-date=2026-04-21T19:45:55+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-21T19:45:55+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 05 May 2026 23:09:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176b065554ef025ae11e6b5b642867d2d1be2033da3168605f2c6a3a91ec21b3`  
		Last Modified: Tue, 05 May 2026 23:10:33 GMT  
		Size: 5.1 MB (5147563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43af4e29ede8aaae31fd2845bfa54eda3abe67ab3279c092f8a637e8650ee775`  
		Last Modified: Tue, 05 May 2026 23:10:43 GMT  
		Size: 469.4 MB (469359449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87f7fa2e96e80391159707452bb8c500d0749b6058d8dcbc3d587c90586d47`  
		Last Modified: Tue, 05 May 2026 23:10:33 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7b14b5431c4c904334253ed1c2686b99a59a3df68da26cefd2501e0c76789d`  
		Last Modified: Tue, 05 May 2026 23:10:33 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7bba4e0c5d5ce95904c0035c13f2743cb8ae223794316d7de7dc86c448536c`  
		Last Modified: Tue, 05 May 2026 23:10:34 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9958d504c350c206fc14d1cba4816976125588e5661637fff62580939db94769`  
		Last Modified: Tue, 05 May 2026 23:10:34 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8579ec3c3d60d1ae4cf09160496fcc22fd01d3cc336ce1ba4f39ccdb2aa65b`  
		Last Modified: Tue, 05 May 2026 23:10:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7ac8a336f4548d9d98e4387f2f4500ec57f6c14a47600747650f1186397e8`  
		Last Modified: Tue, 05 May 2026 23:10:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091409dad7a7a46d0cd6eadd807dc076b47ecdf7e8fdf60a258336b3bc381fb`  
		Last Modified: Tue, 05 May 2026 23:10:35 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.4` - unknown; unknown

```console
$ docker pull logstash@sha256:3550e4d48987486085da130b8bacc1df44344b09dbaf3f68d050dc06e6733148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fd67f7a2194df3adc3b2b57c7ec6ccbc503fcc3c78a79e5ce5b15d8865bb85`

```dockerfile
```

-	Layers:
	-	`sha256:7026ef58ae850b4bcc0b3201672f137c19b98f2e88b47b6ea3073a897d047f40`  
		Last Modified: Tue, 05 May 2026 23:10:33 GMT  
		Size: 2.1 MB (2119842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09c1ba583ed2a4f4722962405f97d1ae0dab6e9d21942b0cfdca50491a7edc25`  
		Last Modified: Tue, 05 May 2026 23:10:33 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.0`

```console
$ docker pull logstash@sha256:0e038a2fadfdc38496c52b708a64b8989513dc521a8965d0a674403eb36b62a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.0` - linux; amd64

```console
$ docker pull logstash@sha256:bac72e3eafeb9cdeff5d626634ede87b918114a075d1dd587fa194a3b673b0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.0 MB (523047151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c577afacca5caf0892e9dd884187ebf83fe7718377af4487eb8e9d15825a7681`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:23 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:23 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:23 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 05 May 2026 23:09:23 GMT
WORKDIR /usr/share
# Tue, 05 May 2026 23:09:25 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 05 May 2026 23:10:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 05 May 2026 23:10:20 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:10:20 GMT
WORKDIR /usr/share/logstash
# Tue, 05 May 2026 23:10:20 GMT
USER 1000
# Tue, 05 May 2026 23:10:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 05 May 2026 23:10:20 GMT
LABEL org.label-schema.build-date=2026-04-28T15:43:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-28T15:43:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 05 May 2026 23:10:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d2270881f502145bd5a89b5332b1e5f2ec5dd0b93dfefc4d374bfdf0696f`  
		Last Modified: Tue, 05 May 2026 23:10:59 GMT  
		Size: 5.1 MB (5148533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4e04a95da2b88d168094aee6d383e74c05a11e46edafceb95084c23d0e98d`  
		Last Modified: Tue, 05 May 2026 23:11:09 GMT  
		Size: 477.6 MB (477614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ba9bd28092eb2301b605f976093b816b4d6bbed224afaaad9174f63fc64938`  
		Last Modified: Tue, 05 May 2026 23:10:59 GMT  
		Size: 6.4 KB (6364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51111dd92b160837c92c090a7457edd6e79a83124502c15f67fde3016e023801`  
		Last Modified: Tue, 05 May 2026 23:10:59 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9079fd4446a4debda7bed2f45105178922c3798df68df04a5dd6c1ceada158ee`  
		Last Modified: Tue, 05 May 2026 23:11:00 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6300503e615cece5658b688c9f65a45c0f58c5a63a1a2397222aa06e1d06a6a`  
		Last Modified: Tue, 05 May 2026 23:11:00 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126bb23054f75af17bc135eb1344ad487b7ee1eae0cd07fc043075cd21a1a6`  
		Last Modified: Tue, 05 May 2026 23:11:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf263a6fe1ead15e909356c1ba51519be877cf9ec8268ce86ed6c8427e6991`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591ad2438d6f9d160610eae6b991a8422c070a335f0fb7bd9dfe2ffc40c80af3`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.0` - unknown; unknown

```console
$ docker pull logstash@sha256:831573e615299ddd563773af5d1d89fd11a75da33294f50ac6d52b7e11e21b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c308806e1e226ed27f71df696914accc1256a1ff50070110503fa36af25f9fb2`

```dockerfile
```

-	Layers:
	-	`sha256:c8055507d4ec01ec71ca900aa618f66ca6b0b24b650307880537d48d9db091cd`  
		Last Modified: Tue, 05 May 2026 23:10:59 GMT  
		Size: 2.1 MB (2123790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec3bdb79799f9de4b5996f5bd268da7bd51c04a8db288e57547cd032615341c`  
		Last Modified: Tue, 05 May 2026 23:10:59 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5b83ffa0716252b60e2c0575229356a96d737a2792a4bcf87773424650bdf577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519517416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f623fd04070ec63f4d29c84057aa8edc7b125b9cb262c018d4c7da949a644e13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:09:06 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:06 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 05 May 2026 23:09:06 GMT
WORKDIR /usr/share
# Tue, 05 May 2026 23:09:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 05 May 2026 23:10:02 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.0-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.0 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 05 May 2026 23:10:02 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:10:02 GMT
WORKDIR /usr/share/logstash
# Tue, 05 May 2026 23:10:02 GMT
USER 1000
# Tue, 05 May 2026 23:10:02 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 05 May 2026 23:10:02 GMT
LABEL org.label-schema.build-date=2026-04-28T15:43:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-28T15:43:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 05 May 2026 23:10:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad64800f6d258ff13f849f0b303fbb682ceeaadc6c21edf03fb5665006dd6d0`  
		Last Modified: Tue, 05 May 2026 23:10:43 GMT  
		Size: 5.1 MB (5147539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad9aa91132dd944dd6e2b84bd8b425444991a3174349daf3ab0889f704b7bea`  
		Last Modified: Tue, 05 May 2026 23:10:52 GMT  
		Size: 475.9 MB (475899239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d2dbeab1b361f981bd1493e43afbae0e285b525587bf2d49979af494a46569`  
		Last Modified: Tue, 05 May 2026 23:10:43 GMT  
		Size: 6.4 KB (6369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77ab77ec3dfeb06d9e5805355b2549071b7f6507960edfd6e7f32ca702d8aac`  
		Last Modified: Tue, 05 May 2026 23:10:43 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b5f70666fb635e7830d70b97950bff2187fca96987f8ac5bd70f64ed5cd083`  
		Last Modified: Tue, 05 May 2026 23:10:44 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760052120e21e061a4132c34689972eb5aeb08503927d0465d2a119141ea0a9a`  
		Last Modified: Tue, 05 May 2026 23:10:44 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047919fd4849cb66b134864f010ed0cb1c3ee6da1daaea22e493ebb31bb51500`  
		Last Modified: Tue, 05 May 2026 23:10:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2f967ade452905805b0c277320b91d9825fecde28c786c254b43c3dd246a0b`  
		Last Modified: Tue, 05 May 2026 23:10:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c224841cc5406809ea33d3bda7bab6640441c6138e990673f41a32c5061af600`  
		Last Modified: Tue, 05 May 2026 23:10:46 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.0` - unknown; unknown

```console
$ docker pull logstash@sha256:ec5d26af294cabf726e70ae11ef1a9672766d30fc09932c89f99dff12d7ba863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2154637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa60fd5d72c6822b42f916e86a54107e608af3c777db0c62725a0f954c722de`

```dockerfile
```

-	Layers:
	-	`sha256:8eff9cb3f3c8622f1f3e86fb4a3da14f45af3c75bf10f00bd92c7eb0e8dc1792`  
		Last Modified: Tue, 05 May 2026 23:10:43 GMT  
		Size: 2.1 MB (2124360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad78cbfed8ec0dff0cf8673d8888a6802845802e16116516c80ecad6efcd921`  
		Last Modified: Tue, 05 May 2026 23:10:42 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
