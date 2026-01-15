<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.10`](#logstash81910)
-	[`logstash:9.1.10`](#logstash9110)
-	[`logstash:9.2.4`](#logstash924)

## `logstash:8.19.10`

```console
$ docker pull logstash@sha256:751bf522d88215c142ede46e3d063d9d57139e6a5bdc805f4e59780c4e1fafaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.10` - linux; amd64

```console
$ docker pull logstash@sha256:30a05cb1162cfbd23576900cdf53325291865ec9c835b5a5b801478c1a7657ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.8 MB (523785740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942d707529fd878b9dcaa6e5dcb4efc0f364e0baaf27e9aba0f2aa23fd3302c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Jan 2026 19:06:23 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 13 Jan 2026 19:06:23 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:07:06 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:07:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:07:06 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 13 Jan 2026 19:07:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 19:07:07 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:07:07 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:07:07 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:07:07 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:07:07 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 13 Jan 2026 19:07:07 GMT
USER 1000
# Tue, 13 Jan 2026 19:07:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:07:07 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Tue, 13 Jan 2026 19:07:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097298e658150b42caa97e9a010e81cdc276b4135592ae11d946dfae2a06ef19`  
		Last Modified: Tue, 13 Jan 2026 19:08:07 GMT  
		Size: 52.2 MB (52152978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22e7d0f49d5be2cd70c7b1c12c7508d748521183c27f901cc51e6fba0b73c0d`  
		Last Modified: Tue, 13 Jan 2026 19:08:01 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dc36229c9235142871afc43d48b94908635fe41fafb3919706a75c6f63e9a`  
		Last Modified: Tue, 13 Jan 2026 19:10:29 GMT  
		Size: 441.6 MB (441640335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db68930f1ad9ea1cf0702b246b22a9716fa39b250df075eb10e89014f48473d`  
		Last Modified: Tue, 13 Jan 2026 19:08:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea2981bb8b1a0295583a09093171f01a500266c90001f3ef947404ef073d5`  
		Last Modified: Tue, 13 Jan 2026 19:08:02 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9226116505a86273ebd45c821bdb0d61578537546f5fa5f6c2db6b1e15ae89a`  
		Last Modified: Tue, 13 Jan 2026 19:08:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19184b969d044e76c0e9c1771b342fca2c8d84fdd9af549f90ea8ad95857c254`  
		Last Modified: Tue, 13 Jan 2026 19:08:03 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41fb6efc1c330e8d8800f5f0459b9d472c04065275794a6e9afcdbe759efe8`  
		Last Modified: Tue, 13 Jan 2026 19:08:03 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd5c5085261067baf10a01c16e9ef0020b3d8e2b02d7d2eb9e21a66993256b2`  
		Last Modified: Tue, 13 Jan 2026 19:08:04 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a383c07d288cb53d720a57c4822f7c7ab14252d7aa8acd378014b11ac78f8eae`  
		Last Modified: Tue, 13 Jan 2026 19:08:04 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcd6720313f6b3ef77b1885a88e0859379332326c312cbdba57f1448257c141`  
		Last Modified: Tue, 13 Jan 2026 19:08:04 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:c3154d4ab46fd1793a997fc3247b2c1981436f9d38e007f3453152063775b2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dddcc121f2c8abaaf35ea7891ec54ed6a602fc4d5d5768ee384c5fa090ce64`

```dockerfile
```

-	Layers:
	-	`sha256:7b6a4a5ebf8dca094f2bcf4bb3a3f68df7e36191b18d29565e571c6b9adef7cf`  
		Last Modified: Tue, 13 Jan 2026 22:53:25 GMT  
		Size: 3.7 MB (3651746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d56b40bd9e43012fb3dfaf833d6a44c55ff9e2ca69618d1a305c67ea19e34a`  
		Last Modified: Tue, 13 Jan 2026 22:53:26 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:b80da7a707bb6422256d02a8f50d46871e97108d4fdfeabffaad76d0e752faf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523526039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68652484dd6c739f9b419f69737e22072e0a6943d8f7075c6cfdca207c61f4fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 13 Jan 2026 19:06:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 13 Jan 2026 19:06:20 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:06:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:06:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:43 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 19:06:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 13 Jan 2026 19:06:43 GMT
USER 1000
# Tue, 13 Jan 2026 19:06:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:06:43 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Tue, 13 Jan 2026 19:06:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d850ade28c11064c07b9b2727be0a42579654df6bd05f86cd61770cd573215`  
		Last Modified: Tue, 13 Jan 2026 19:07:51 GMT  
		Size: 54.5 MB (54471922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adbdd202e619eaeffa4167faf9d5e91bdb78f46a00f49dc87b1b75f5328b1e2`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5006ff765b7397b9839bd56609a5105ed7eb9f2329cc591d6780cdea7afa34bf`  
		Last Modified: Tue, 13 Jan 2026 19:10:10 GMT  
		Size: 439.9 MB (439924435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d28eeb5588d384f0ac539485a075f750303e06daf09ad164168f7a65f29e1`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff8aaf86f0260be67d7f1a9f666f687eb178d7c735047b6c45bc505bde9f21`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889c558c62b523f02bb8805acadac0d74696200b89d479eaf7115c1755c8daa`  
		Last Modified: Tue, 13 Jan 2026 19:07:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dfd9c7cfdbd7e0c4b6a1a5ae0cb32bf7c7983226720f48a1adecda3eeac7b`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9145eabaf8c0f7a9cd6ecd55e4dcfe9ebea09c0f808bd44a9925aba8afab0fba`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91f1f7f08a266cf40cac05cdb7bafd79759b515057a06eb3fcb5ae522bb1aad`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d0691d4019a96a4a66da381faaf09dfceffa596679dc4f93c21bb4ed958218`  
		Last Modified: Tue, 13 Jan 2026 19:07:45 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21378a5daa92551f2309bcbf82f0128d98e66fad8959eac8cb7598ca10b768cb`  
		Last Modified: Tue, 13 Jan 2026 19:07:28 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:183e598ea791ee4d7541039aedd51bce7fe148f50d6ab03be80ab2d4f6c25911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a56879978c4d39bd452690e1fda1c3a48e8886a2a471793711547eef46187`

```dockerfile
```

-	Layers:
	-	`sha256:61df6078ad663d9c8c78b2ca6f435614e6068ac008d99fb8ba478dee39dbf980`  
		Last Modified: Tue, 13 Jan 2026 22:53:30 GMT  
		Size: 3.7 MB (3652171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90e68ca598c0e2bd07c625a269874ee1c22fe02a44f609470d491bfd56f3d61`  
		Last Modified: Tue, 13 Jan 2026 22:53:31 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.10`

```console
$ docker pull logstash@sha256:8129c541317e01117bfa39dc71a5278914c53d9c19906c128f7f34c6d051029e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.10` - linux; amd64

```console
$ docker pull logstash@sha256:a46e9efd1dfb28a9203c8417c9a4977419d45b900fe7c58b14e14c4527daac87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478961284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56079015fab1beca47f126dece1b853c26cc9076decc53b19396ffeacd46471`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:06:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:06:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:38 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 13 Jan 2026 19:06:38 GMT
WORKDIR /usr/share
# Tue, 13 Jan 2026 19:06:40 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:07:27 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:07:27 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:07:27 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:07:28 GMT
USER 1000
# Tue, 13 Jan 2026 19:07:28 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:07:28 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 13 Jan 2026 19:07:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc87c24993cacb666c0aee4509ddfda9e8eb18b0f9896ef1801215d8ef18d469`  
		Last Modified: Tue, 13 Jan 2026 19:08:21 GMT  
		Size: 8.1 MB (8084838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779856d3d98da3fb99e76a9747140e01d6ba1e76020745407270ef4e395cc5f7`  
		Last Modified: Tue, 13 Jan 2026 19:11:40 GMT  
		Size: 430.6 MB (430570946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a36f8f88eaf568fa68b30017c84fce4af8e405b6746b9d3e7f24644458f9cc`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16b09084bbfdc0ed7c297c3c3b44ece0b4c1fbc28c70911e7a7f1e471fa2f2b`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3adf8abcb0e922845ed097f8206aa4b1e69d0b2d02fc2abff7e3f9e3f02b0`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7629a8e63dbcaf9c38926ad622a276672db551173b3e4a313f6cf8e33c32377f`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9398481419a9dac897eb5889933ccde656f689ac7ad825a8174cb363413e1246`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70bbea572bd0a4d78b4973cfb790cb1d67e443b92d036ca86e946371e1858e9`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca387b96dae4450368fa8cbb5dfe42a77159567dae635cca59a94d2fda877bf`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:c799ecce6beac80ddf90cde36ebee538e2c0902d7667a36e5d05561cd6361df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4941dca7683ac7fe76f8ebd260ef50427d5b16ecc90a5720882b3d10887095dd`

```dockerfile
```

-	Layers:
	-	`sha256:85336a55362cee643e31fcee1afaea2764af14e2cd56eaf05694b9d575564e32`  
		Last Modified: Tue, 13 Jan 2026 22:53:34 GMT  
		Size: 2.1 MB (2088537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d444da941c1af824dc84efbce1581528a43aaaebbb28e98808d290f71f303076`  
		Last Modified: Tue, 13 Jan 2026 22:53:35 GMT  
		Size: 30.2 KB (30164 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:301ee68126488738cdbe4a8df48ec5ef1a989b4b246515a75e4988d2b3f48313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.2 MB (475237648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5614cbd14d9c3dc3ad95600001edf609e8aef4e75a89f50a46fdfe9990ff79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:06:06 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:06:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:06 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 13 Jan 2026 19:06:06 GMT
WORKDIR /usr/share
# Tue, 13 Jan 2026 19:06:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:07:16 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:07:17 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:07:17 GMT
USER 1000
# Tue, 13 Jan 2026 19:07:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:07:17 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 13 Jan 2026 19:07:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2b51d60af8284f292a43a007edc45ab00ffc6f6aefe5806fbcd554aa9a993`  
		Last Modified: Tue, 13 Jan 2026 19:08:16 GMT  
		Size: 7.9 MB (7900534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1229e64ff249997d2605cdf25b2cce63fbfa297ca44d99268a379fc1ec826b2d`  
		Last Modified: Tue, 13 Jan 2026 19:10:41 GMT  
		Size: 428.8 MB (428849559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4505d3ec557209f01a51908e317ed4177dd657b66b14c383a47486b1ca760e`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 6.3 KB (6292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1f5712e2b8c936e67c9497449898632e676a58518c9fc01b01451e659b7a0`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 255.2 KB (255188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078bc50ad7a9fc7ce83899e7f18af1e11b4762c643676a17f4dd40d140fafe0`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d002a64fd7192161cc8e79a8bf09365311e863892a270371c44fcbde03fd403`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 1.6 KB (1573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd5793a876cd167378fd5d325a7c1f0844bd4cdb4b310a74c294bfdfa5e95c5`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfcbdda642ac93b902657db5230403862b0dc76990a4fdb5ffbaa2171ef0ef9`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c064a0c07b985773948ae6059fdd04442b0057ede5028e9e0ba8ad086750367`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:776bdaac89ffda39a60531bb744c326f6440bfce085e0856eb44c4ef02d883ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21be29e6fc7c08feef9fb617e0c6bd6c58fdff8a6efc082cd87e6a78432e004`

```dockerfile
```

-	Layers:
	-	`sha256:1e3fe2eb64cb7f67e7990a5c205133b7b1bdc2ac0a8ba4e1e0858483beccfe1f`  
		Last Modified: Tue, 13 Jan 2026 22:53:38 GMT  
		Size: 2.1 MB (2089107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f654b54be341947d4a08216e419f57217cd3396ba06c3ba8df5a6f5559e675a`  
		Last Modified: Tue, 13 Jan 2026 22:53:39 GMT  
		Size: 30.2 KB (30241 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.4`

```console
$ docker pull logstash@sha256:a54221a9d6c2d92f5d8f74beedcf9f21b964ac59dcd7f4285678e750b7f686ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.4` - linux; amd64

```console
$ docker pull logstash@sha256:23dd51076fdc32b248f078946ec7df5e53b650d37f23bad241d00891c3474d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 MB (489268666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d88a98df2356421fc66f0ab152f825be2be33fff04adeae96173eaa9e313889`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:06:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:06:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:35 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 13 Jan 2026 19:06:35 GMT
WORKDIR /usr/share
# Tue, 13 Jan 2026 19:06:38 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:07:28 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:07:29 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:07:29 GMT
USER 1000
# Tue, 13 Jan 2026 19:07:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:07:29 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 13 Jan 2026 19:07:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8631ad99cd185927720bb5bb6c0a7216d2d9b69417a79e90c1d3a72780988399`  
		Last Modified: Tue, 13 Jan 2026 19:08:20 GMT  
		Size: 8.1 MB (8084764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c856155b1b7bfeea8228af1af16ef9e740f9b2cf6952ee7d4ff44ce94ddc1`  
		Last Modified: Tue, 13 Jan 2026 19:09:57 GMT  
		Size: 440.9 MB (440878398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7058ad6c3551021f14837798ee1c764762367c45c3ed22fc3b685cb30a060ac7`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529696c893b2288c405623fa3d6e126d1fd1a9b7fd82f65096b5b2bc32c269`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b302f796d1537d31d18e036b97c7f2285995906d4cc3a9e6a6d62dbc3b02060`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f73397c45ce113628f36be16560d914fc7abe0edcbea53d9b1a6e13c2be27c8`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863a1de0eaabd485d98caddc602d3628e380bad63b2a3e450641a4679736facd`  
		Last Modified: Tue, 13 Jan 2026 19:14:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2059afebf752501e4de887fea23c39c9b1cf004b23119d0f7f736dcec49ec62`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6be5382dd678f33bae4b65e367ebb1f9c46eb0ca4065cff7d81351bf86d0b86`  
		Last Modified: Tue, 13 Jan 2026 19:08:19 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:85a979c92a08d24e455903d3a90c3510e66a34ea050c21ee8dc38c7607fb2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2128552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21238705c22ebc69f4177188990ff315c7fdcacf2ab0f809466b9e147a1681c0`

```dockerfile
```

-	Layers:
	-	`sha256:32869d3ebb6ef15a5c47a245f1a099d8043050bb64d332ff9fe91d6975e112fe`  
		Last Modified: Tue, 13 Jan 2026 22:53:46 GMT  
		Size: 2.1 MB (2098352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6452c3cd8e103e899214d73387332226b6adeb1be541d09f358ae4515972ceac`  
		Last Modified: Tue, 13 Jan 2026 22:53:47 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c438676c2c00939e2e9121483f43cb1dd4a14f10b38f203b541087129674cc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485543239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d40ba36b5d8667dea25e8bae734f3767f52b0727a549bfa4d6b9d408b3d083f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:04:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:04:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:04:36 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 13 Jan 2026 19:04:36 GMT
WORKDIR /usr/share
# Tue, 13 Jan 2026 19:04:39 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:05:28 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
WORKDIR /usr/share/logstash
# Tue, 13 Jan 2026 19:05:29 GMT
USER 1000
# Tue, 13 Jan 2026 19:05:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 13 Jan 2026 19:05:29 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 13 Jan 2026 19:05:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a5c32cfa83cabcff5d74d666f7b99ad8952c07ea094406bf9aa8a185807d0`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 7.9 MB (7900511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993ef861233b752e2e7a15fbab4ec248ea0a1207a4a9ef1cea8ca68f14fe6972`  
		Last Modified: Tue, 13 Jan 2026 19:09:31 GMT  
		Size: 439.2 MB (439155166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d060ebc3a44ab95810f2e7b1fdba284fbfdae2d1bf00fa562a3e469f25181c`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f6b998c6628efaff2a37363da7014cf3a9328afb463b842e5ea61f62a02d67`  
		Last Modified: Tue, 13 Jan 2026 19:06:36 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d4b55674d323c6aeb11a125b9873858b77e41751d736ec4de3d51cf0d43176`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4841bb8311e123b9f0c96f56089b219ac512fa47b545da5848e503eb4690ae`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094820a575ec8f6e12ca6e6a755c194ac55b00dc9372738718554cd74178d36b`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7890cb1809d6af4da94ae52aa97b139dd6c050de0fa4acf1f994e0849fd15102`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e43e3097005ee26fc824c7eaa8a6ef4ac919dcfdb158c8ae7f47f24e3d9622c`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:dcd78028bafe1e2ebd5995a2bb2f54f9b6ce63a25a04692008e6f435227803db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1e34d18e7ec35c0c8947f12addc63fe7c554f50caaf89666cc4589c8fb6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:63a9ccc5d44abdbff2ba3c55b78b7e5e04dbe063905c0caf90f7732ced35cb67`  
		Last Modified: Tue, 13 Jan 2026 22:53:51 GMT  
		Size: 2.1 MB (2098922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657cf5ea21d2f93cc8c9928ec30a93da01e28017255f3ad0c8be67bc22019d8`  
		Last Modified: Tue, 13 Jan 2026 22:53:52 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
