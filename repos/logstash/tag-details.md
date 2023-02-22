<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.9`](#logstash7179)
-	[`logstash:8.6.2`](#logstash862)

## `logstash:7.17.9`

```console
$ docker pull logstash@sha256:48db6de65f1fde20b0dd0853446c1bedcb11d1213fb5a6332dfa9c692cc3ceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.9` - linux; amd64

```console
$ docker pull logstash@sha256:8a747338840cb6e49104a1562f33b570abcef33fc273101069a32b92a3291e9d
```

-	Docker Version: 20.10.22
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.8 MB (438827246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44725cae61eec71bd23e8631c176b918c121dcbf305702370270fe65001439ed`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Tue, 24 Jan 2023 22:17:31 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Tue, 24 Jan 2023 22:17:32 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Tue, 24 Jan 2023 22:17:55 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.9-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.9 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 24 Jan 2023 22:17:59 GMT
WORKDIR /usr/share/logstash
# Tue, 24 Jan 2023 22:17:59 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jan 2023 22:17:59 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 22:17:59 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 24 Jan 2023 22:17:59 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 24 Jan 2023 22:17:59 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 24 Jan 2023 22:18:00 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 24 Jan 2023 22:18:00 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 24 Jan 2023 22:18:00 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 24 Jan 2023 22:18:00 GMT
ADD file:ced67dbe23501a3719ed1c54ed9f2f87b1a48ab4ce16e5063914145d7cbed734 in /usr/local/bin/ 
# Tue, 24 Jan 2023 22:18:00 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 24 Jan 2023 22:18:01 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 24 Jan 2023 22:18:01 GMT
USER 1000
# Tue, 24 Jan 2023 22:18:01 GMT
EXPOSE 5044 9600
# Tue, 24 Jan 2023 22:18:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.9 org.opencontainers.image.version=7.17.9 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-01-24T22:01:46+00:00 org.opencontainers.image.created=2023-01-24T22:01:46+00:00
# Tue, 24 Jan 2023 22:18:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5f7ea055aea7fe08e8f7e798f6dc5bcbfa84121f413243918dc37fe1f90b91`  
		Last Modified: Thu, 02 Feb 2023 23:11:24 GMT  
		Size: 41.4 MB (41362862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fdc4e04fd512db3c86befe51ee955b3732e4b07149a3baf4e774aab2bf465c`  
		Last Modified: Thu, 02 Feb 2023 23:11:08 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea886dfdca899e749699cec9737455528542fdb68a39ab09146d309b8595499`  
		Last Modified: Thu, 02 Feb 2023 23:12:06 GMT  
		Size: 367.1 MB (367110311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc18e74b5812fd4f9acce5375f5b5d3e1268f05f9016b78e7bbfe501832cb4`  
		Last Modified: Thu, 02 Feb 2023 23:11:06 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110ad10a595ff40a6e7538ec3c905fdeaa843110d8eca7e57dd34bbda3f72c62`  
		Last Modified: Thu, 02 Feb 2023 23:11:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f069a2ebecdd13035537f2a0780a80c9997c1968184f2746019e707a5c3fedf`  
		Last Modified: Thu, 02 Feb 2023 23:11:06 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf535948a5f4e74303a1ad5cba184343f7d6f3f4fe17e3426586996f9a673113`  
		Last Modified: Thu, 02 Feb 2023 23:11:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d020f99453e9a58488f38b4269fb7303fcb1b16b2deb67dadd20794fb4306b09`  
		Last Modified: Thu, 02 Feb 2023 23:11:02 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809919f46c064cc9c4f4623ea15fe3da0daaf0a74e57b862132dbfe2265d40f4`  
		Last Modified: Thu, 02 Feb 2023 23:11:01 GMT  
		Size: 1.8 MB (1770100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e22311e0cf9b2e191427ecaf72446c894dc9811c2d4e31cac919643f072abb`  
		Last Modified: Thu, 02 Feb 2023 23:10:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e22311e0cf9b2e191427ecaf72446c894dc9811c2d4e31cac919643f072abb`  
		Last Modified: Thu, 02 Feb 2023 23:10:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.9` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0a83992e64519b85f040fc94bb20b5f611f707f885dde5c067f92b7185e84660
```

-	Docker Version: 20.10.22
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.5 MB (427451040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47f1c0ff51367ae955ae7c8f5cd9c77a4f274f019edbf2152bf4c80a8eb3155`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Tue, 24 Jan 2023 22:17:06 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Tue, 24 Jan 2023 22:17:06 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Tue, 24 Jan 2023 22:17:25 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.9-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.9 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 24 Jan 2023 22:17:28 GMT
WORKDIR /usr/share/logstash
# Tue, 24 Jan 2023 22:17:28 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jan 2023 22:17:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 22:17:29 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 24 Jan 2023 22:17:29 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 24 Jan 2023 22:17:29 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 24 Jan 2023 22:17:29 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 24 Jan 2023 22:17:30 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 24 Jan 2023 22:17:30 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 24 Jan 2023 22:17:30 GMT
ADD file:83f91a29fcb81019467f8bd1de10290c5d04ec23b929a6b8eef3fd6e3208404a in /usr/local/bin/ 
# Tue, 24 Jan 2023 22:17:30 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 24 Jan 2023 22:17:30 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 24 Jan 2023 22:17:31 GMT
USER 1000
# Tue, 24 Jan 2023 22:17:31 GMT
EXPOSE 5044 9600
# Tue, 24 Jan 2023 22:17:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.9 org.opencontainers.image.version=7.17.9 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-01-24T22:04:07+00:00 org.opencontainers.image.created=2023-01-24T22:04:07+00:00
# Tue, 24 Jan 2023 22:17:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdbdc9e3c4ca20d2def637003f01fbfee5e079461c2bf2afa2bae39a951da63`  
		Last Modified: Tue, 07 Feb 2023 22:58:30 GMT  
		Size: 34.7 MB (34728379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d22237706ea632948d69fa74a059182b4f043c3fbef4b821a67cf1c8c47cb2`  
		Last Modified: Tue, 07 Feb 2023 22:58:26 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4838229cd33f201b5395c4cb4a666c2e82d1fc9247f782190e56153a17656dd3`  
		Last Modified: Tue, 07 Feb 2023 22:58:48 GMT  
		Size: 363.9 MB (363873906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce10bfae58270d87e1b2f096e17646aeb92362ce63c8236e6c4d09c57b3a3f39`  
		Last Modified: Tue, 07 Feb 2023 22:58:26 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888ee304434cd86a1dde5858ec54f31e6f2922bdcf33838d78477121bbbac081`  
		Last Modified: Tue, 07 Feb 2023 22:58:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d5a146695eb8d6cdbf73af39a22e654ae46be97aa7445ccfa9ac36cccbf8f4`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a995c76ab5582895c18ae37084d06eb2bc12f8068f8258f6dc4afd6ecbce93`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c44745587e7af9750b7ccffbce7d9dc5e6e437cbf6a1d2845e805425afddc4`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd7254666423017892e872df8e289f44326ea905d8d8b212910d2df93d7d4f8`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 1.6 MB (1648477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7413ffca3e9aa329d54f3c9bf1359ce6171b90791359218ce54e9becda5a1cae`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7413ffca3e9aa329d54f3c9bf1359ce6171b90791359218ce54e9becda5a1cae`  
		Last Modified: Tue, 07 Feb 2023 22:58:24 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.6.2`

```console
$ docker pull logstash@sha256:e58b269c4f1436b6ff43b3b6fd8e5eed1251cf400b92635023d58f1c03241cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.6.2` - linux; amd64

```console
$ docker pull logstash@sha256:80ea11df02b7bd3f46758422417a177df154a50e843a731ca798558de09dca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399334871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc8356947724516b579c0d6a2e58a6c9b7c72a0e5ea8e2d27ba2a45a03f6e81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Sun, 12 Feb 2023 05:59:24 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Sun, 12 Feb 2023 05:59:24 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.6.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.6.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
WORKDIR /usr/share/logstash
# Sun, 12 Feb 2023 05:59:39 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 12 Feb 2023 05:59:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Feb 2023 05:59:39 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
COPY config/log4j2.properties config/ # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sun, 12 Feb 2023 05:59:39 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Sun, 12 Feb 2023 05:59:39 GMT
USER 1000
# Sun, 12 Feb 2023 05:59:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Sun, 12 Feb 2023 05:59:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.6.2 org.opencontainers.image.version=8.6.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-02-12T05:42:46+00:00 org.opencontainers.image.created=2023-02-12T05:42:46+00:00
# Sun, 12 Feb 2023 05:59:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e609e0d9b40ec4087767dc3ff219ab3b591586eccfcaab0afab26bccbb95518c`  
		Last Modified: Wed, 22 Feb 2023 01:30:55 GMT  
		Size: 42.0 MB (41965163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f012299a9644b3fae2cca1cf4eb1a3d316383c7b9982212dfb8548313b08aa7f`  
		Last Modified: Wed, 22 Feb 2023 01:30:50 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1010df88edbadeada7be005883929807d552e50fa26418f6ed6791f6618cd`  
		Last Modified: Wed, 22 Feb 2023 01:31:13 GMT  
		Size: 327.0 MB (326979119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c1374c48b05d0bc0520d3c8fc06ea42172d80b58845a710e3c554bbac1d4ea`  
		Last Modified: Wed, 22 Feb 2023 01:30:49 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eab925b24f966731713867644c4d274c616a1bc94196f9e8c81549cc9b7f51`  
		Last Modified: Wed, 22 Feb 2023 01:30:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f1e6a6e4631c3b8b0437ed68a04f2229f7032c13f3234717353bff16e0136`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f615c0e06970b27452a7c60dc8ee44a6a52b2a20c53c2b6c360296a6b912ce`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef7b6bc5936ab0dc3c8c11f63435f0f425be01da28d1f96a79bb3ac2dc32156`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 2.7 KB (2697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350f661e948ed8c8c3f6be44981cd2605221b618e3c39510650effb52f90f15f`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 1.8 MB (1805743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d840675da68fcaf66f11f72f57f47216d1321928bb731d44723c7e6a2e2f7`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d840675da68fcaf66f11f72f57f47216d1321928bb731d44723c7e6a2e2f7`  
		Last Modified: Wed, 22 Feb 2023 01:30:47 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.6.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:cb17934dac3119d8d7c61bf574b94ba6a53d47a6a3949eb6c920d189c24b1c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 MB (389910590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fca947a08072354eb7a55797d529f57f87d316d23938a168366b28283d6e21`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Sun, 12 Feb 2023 05:59:56 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Sun, 12 Feb 2023 05:59:56 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.6.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.6.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
WORKDIR /usr/share/logstash
# Sun, 12 Feb 2023 06:00:05 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 12 Feb 2023 06:00:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Feb 2023 06:00:05 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
COPY config/log4j2.properties config/ # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Sun, 12 Feb 2023 06:00:05 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sun, 12 Feb 2023 06:00:06 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Sun, 12 Feb 2023 06:00:06 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Sun, 12 Feb 2023 06:00:06 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Sun, 12 Feb 2023 06:00:06 GMT
USER 1000
# Sun, 12 Feb 2023 06:00:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Sun, 12 Feb 2023 06:00:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.6.2 org.opencontainers.image.version=8.6.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-02-12T05:44:59+00:00 org.opencontainers.image.created=2023-02-12T05:44:59+00:00
# Sun, 12 Feb 2023 06:00:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d156ae1f173bc4841346c3aaf1f9a4bebe97f282700722094c8dd3fa0844b365`  
		Last Modified: Wed, 22 Feb 2023 01:54:56 GMT  
		Size: 35.2 MB (35217249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5366b7b45485905b5962d9fdbaa22cdd8f68ad8c6bf7dce393fca9c262793697`  
		Last Modified: Wed, 22 Feb 2023 01:54:52 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a329aed5ac0629d366f91aee27af585b92ea22451459b4c615f19db347afd768`  
		Last Modified: Wed, 22 Feb 2023 01:55:12 GMT  
		Size: 325.8 MB (325807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1195878e2e417cf06a2dd506c5aefaa87eb54f94b2fbb1cfa109809ea3173db3`  
		Last Modified: Wed, 22 Feb 2023 01:54:51 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aab3f463200ecb680390a26fb2d79afd1e2c61c4f7002ea44ca61691988af9`  
		Last Modified: Wed, 22 Feb 2023 01:54:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacfeab1b6d2710989444c63660bcbf4f3b5ed95dfa6684d24dec451dbdcc7ba`  
		Last Modified: Wed, 22 Feb 2023 01:54:49 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834ceaff0fb39ad5c757a4fcf4788fe536806e6bd1465873ad4759a7a6b8f63`  
		Last Modified: Wed, 22 Feb 2023 01:54:49 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e031aa8f71a73150b4a860838ba85cdeb9dbdd294469c245185ba744daad9298`  
		Last Modified: Wed, 22 Feb 2023 01:54:49 GMT  
		Size: 2.7 KB (2701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf6c16a4450c586ab1fe38c21dc2fd2d87f7a43184be86cdc4fb2e4b07b4757`  
		Last Modified: Wed, 22 Feb 2023 01:54:50 GMT  
		Size: 1.7 MB (1684743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b7d7edcedc76ea2daeb5ac67b66d201ded4e680633e3d810fa2bde30a4d04b`  
		Last Modified: Wed, 22 Feb 2023 01:54:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b7d7edcedc76ea2daeb5ac67b66d201ded4e680633e3d810fa2bde30a4d04b`  
		Last Modified: Wed, 22 Feb 2023 01:54:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
