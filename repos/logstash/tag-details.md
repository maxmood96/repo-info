<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.19`](#logstash71719)
-	[`logstash:8.13.0`](#logstash8130)

## `logstash:7.17.19`

```console
$ docker pull logstash@sha256:0724e5b6be1d55623c8ac653d3712b03a12a56afb55fadf586e5829a97b500e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.19` - linux; amd64

```console
$ docker pull logstash@sha256:958b7e197f7278f427ada6a06dc392f69d5d69525547b75a0e5e3eea86a29ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.2 MB (444182453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00f280da8031991f56c44cd2468ebefb39e5d4fcab2a4e353a3f24c4e59cb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 11:00:18 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.19-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.19 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 11:00:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 11:00:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 11:00:18 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
USER 1000
# Tue, 26 Mar 2024 11:00:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 11:00:18 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.19 org.opencontainers.image.version=7.17.19 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-20T03:40:34+00:00 org.opencontainers.image.created=2024-03-20T03:40:34+00:00
# Tue, 26 Mar 2024 11:00:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401d267775752bcc2e5817c4b80711f5592b3d5b60ef9dffec0e7bf7e6c6547b`  
		Last Modified: Tue, 26 Mar 2024 18:50:42 GMT  
		Size: 47.4 MB (47426593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbb535cb4cad9205637fe7df55a9878859b0d1d999c8fc3b628f8558c43ebe6`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebe00f26c6f5aca51e58723fc902c2d0305487ea0092e97da20d993b52460da`  
		Last Modified: Tue, 26 Mar 2024 18:50:47 GMT  
		Size: 367.3 MB (367333949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a684d0bcd12e6d3c3bc59d369557bdee37c5bd651de5fbab57d53cde97c2123c`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70706f5ec88f2b011003860e8ba48c55cc0958bbf2950d32e660b06bc1dd86c8`  
		Last Modified: Tue, 26 Mar 2024 18:50:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22df1b47156f04be3c2f824e08dbe01a206ef30e500ebbd9326329cbed58164c`  
		Last Modified: Tue, 26 Mar 2024 18:50:42 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c35a63b482ffc269e5dd2f73dfb9a9db0a83afc25cecf7e62b077087dd865e3`  
		Last Modified: Tue, 26 Mar 2024 18:50:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a65b45359c0f97c9cfc5725317202b5cf692372a9dd19198bb17d9d3677b53a`  
		Last Modified: Tue, 26 Mar 2024 18:50:43 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbd5c4edf94b20961d7b11d3a0fc1598bef50a4b126c5f35b997f10acb5fd4`  
		Last Modified: Tue, 26 Mar 2024 18:50:43 GMT  
		Size: 1.9 MB (1902984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49953af235c07c7385d2fecdd03ee0d1e8e8b3096667ebc2b5185cfb0abea5a`  
		Last Modified: Tue, 26 Mar 2024 18:50:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.19` - unknown; unknown

```console
$ docker pull logstash@sha256:ae1be5ef8d08fdc8c8c7ed9a2cc37cd517c0d49a7781332c9a8fb00ec3e91b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3008969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277e046865e1f9ab8f59d0e4e0aedc5c26b30344094d27911358a4116d4165c8`

```dockerfile
```

-	Layers:
	-	`sha256:d956a40fec4770f68c017451594e9e108c3802c7096c145fb5865bcff0c33dcf`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 3.0 MB (2976801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446638d47f33534f92249523cbac844367d213edfe3181d2def1be8dbcaf96d6`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 32.2 KB (32168 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.19` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:974393f75098b27ce318a6e108428935e49623bcb4d1805dea70117ba9345c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429143738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef37a6e5ab96ba9147cf19897d3e54d4e0c35f4d2c370b1cc0c912d2f615e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 11:00:18 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.19-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.19 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 11:00:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 11:00:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 11:00:18 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 11:00:18 GMT
USER 1000
# Tue, 26 Mar 2024 11:00:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 11:00:18 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.19 org.opencontainers.image.version=7.17.19 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-20T03:40:34+00:00 org.opencontainers.image.created=2024-03-20T03:40:34+00:00
# Tue, 26 Mar 2024 11:00:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425fb225216dc969f3f10fa6812a6be467ea7c73fcdc1aa4c81534d48916720`  
		Last Modified: Tue, 26 Mar 2024 19:08:37 GMT  
		Size: 37.2 MB (37212876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b78517e16767316435e2ba9c047bbbc6d0af81f3c639bd7ee8f46fc542318d`  
		Last Modified: Tue, 26 Mar 2024 19:08:36 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094887473f6a1fdbcf71446e8d796e53e9d04a769c31ec677280dd5b947905b1`  
		Last Modified: Tue, 26 Mar 2024 19:08:44 GMT  
		Size: 364.0 MB (364048884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f340beeb10784e3afc88b2b6d3009f9c0e2ef957a7afa7d347a28ce7f32078e2`  
		Last Modified: Tue, 26 Mar 2024 19:08:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2088b57471bd627515d793ee2e32ee1e61195dfe143dc139b502cbccf09b5cb`  
		Last Modified: Tue, 26 Mar 2024 19:08:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51421ccf0571fa35469a779bfd47a24268547727cc66349b3133c6bac6a4aef`  
		Last Modified: Tue, 26 Mar 2024 19:08:38 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14022f0c552a6b0d513bf456890c135ab7486eb0afbd11c91e79e9a9d1e1c7e`  
		Last Modified: Tue, 26 Mar 2024 19:08:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12b97e92c53ef7d3d0df164a5c9256068009c64e249b189ec081d0fc426424c`  
		Last Modified: Tue, 26 Mar 2024 19:08:39 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899b0610e7bb0e40962b50d6a3380e59ca2e2f935462342fa68dfb51d6bb469b`  
		Last Modified: Tue, 26 Mar 2024 19:08:39 GMT  
		Size: 1.9 MB (1902983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff324ac5e34b38e41a610dd3d8c598ce21d804e811d395383f8101d2f939dd03`  
		Last Modified: Tue, 26 Mar 2024 19:08:40 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.19` - unknown; unknown

```console
$ docker pull logstash@sha256:3f99312c6685e01154d29bd89139f5dbe1d95c9e6c1c101a6de38d9a14965e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601bef5147303a7834a422371daae8f1574966bd8a3488fd7a1beed619241464`

```dockerfile
```

-	Layers:
	-	`sha256:0bd55dab618e3fdb7428875a9efce9b64e88057ade0958fe71e1fcf1d492d2f9`  
		Last Modified: Tue, 26 Mar 2024 19:08:37 GMT  
		Size: 3.0 MB (2977021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37b87ffd4cbe94a2399c81007b50d20224147f5a6f6640624f1c079da3726d1`  
		Last Modified: Tue, 26 Mar 2024 19:08:36 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.0`

```console
$ docker pull logstash@sha256:a5e35b86db3e0ef0659f83f42833cd23e5b5a6321d9b7d8406d4837d3bd427b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.13.0` - linux; amd64

```console
$ docker pull logstash@sha256:b5fd49e36194a24cace2bef49d41aa685e15ef5b6702b0ecdbeecd988c298487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.4 MB (490388804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ad97a2ce120d2bf93fd671b59ea4d6fe3d400b00bcc48f40db0cf4e18c09e8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8674d7cba002bd25c9485e9b15a6814a3a9ba0b1d4d268a1a25063fd636045ae`  
		Last Modified: Tue, 26 Mar 2024 18:50:38 GMT  
		Size: 47.4 MB (47426428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416696fe99421abed26854768fe2ca3c45a0530b9d5b08985d4ebb8eb9396cc7`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe51e0c800adeb5e586a454257bb79d373808518a3eaf913fba03902701d445`  
		Last Modified: Tue, 26 Mar 2024 18:50:46 GMT  
		Size: 413.5 MB (413537495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b0df39b12ecdab95bcb8a1af0b38d3e1e08c5f8b8211d17f4ebbfbfb55e7a2`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dbf5b1ac5195141c60333c2d6b8b71bcecb76c33717858af31ab96ed886722`  
		Last Modified: Tue, 26 Mar 2024 18:50:37 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1400e21b86f9c2b574e0164dcabce11258a50723136c71ec1a9ff9a7f717f7`  
		Last Modified: Tue, 26 Mar 2024 18:50:37 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3a033f6accb967a48801af5ca6dba5a235b5939ff8024a828bd1409f712b47`  
		Last Modified: Tue, 26 Mar 2024 18:50:38 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec1bd999b1f59733b482f0fd09181125c15e256fcaf667c709e21bdbf8d116a`  
		Last Modified: Tue, 26 Mar 2024 18:50:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0fbac536ed04493182520715b0ee6815c2e8c0e9d7ba572101bb474722f85`  
		Last Modified: Tue, 26 Mar 2024 18:50:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a4e130adc8f385924b007988f7a47389fd0a12f535f1951f63f382c3879f94`  
		Last Modified: Tue, 26 Mar 2024 18:50:41 GMT  
		Size: 1.9 MB (1903447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de83927b22492149387e94c6dbe43fae03e1137e02b770ae1805917690b6ee8a`  
		Last Modified: Tue, 26 Mar 2024 18:50:40 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:28651bfe74f16fe1d33143d686cd9c76ad54446f1afff0d20eaf8d2d04c35d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931cba84239092c2145258fc63ee129e6635fcf45998ea217299bc9731cd897`

```dockerfile
```

-	Layers:
	-	`sha256:1c88c3fc302118f8a8594be3d78df17b0de4f443535d534f3ac90161945b23b4`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 3.2 MB (3177191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41aca8e6521e78914434c04305cb2a9859b8c010130a57ff2389e70e96494c95`  
		Last Modified: Tue, 26 Mar 2024 18:50:36 GMT  
		Size: 34.7 KB (34690 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.13.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ade4c45b58c35477ef61874237331f3bc3205e47044db8bd6552702e4a33df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.4 MB (477443668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b37048aaa72ef6be711e16b5f29b7aca2837044a71bf313893980cb04b42e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e80fd83213efbe9caa80d6a019635678ee5cc95745f6acfa6f90c52f46df5`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 37.2 MB (37212801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c22d41b53528ed35fbeb2bfe0dd2d51fedef7886026b6c9af30f1386365cde`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7a1df18c719dd5312ecb83d38bdb2400349fbaf551bfb43aacbe1d123254c`  
		Last Modified: Tue, 26 Mar 2024 19:07:23 GMT  
		Size: 412.3 MB (412345902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc524d760a392f0ee217dc0a3bf114ea645902012b5e43c736a5b1be7e2456e`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08401652822e12af3c388e4e1c94ef641cb4b20444a859479223d5356fe2c809`  
		Last Modified: Tue, 26 Mar 2024 19:07:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695271c2dfebb37d215cc8f3f3386432bf3c5576de25061e56325dd8c6c558f2`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe93bd8ccad9167870793206184cc2b9db4741147e37371b4b355869ed665d3`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd6dfb1d001a06ea354e4f6f92aa4743699da41e3cdc3615b095e38185620e6`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5881ee79406147fb77c814643140b4ef3619668b3d36a123c1531f5be89c939`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d7ad580d97b6bb27e16e11d62fbece68772e3a9edf7c2168a7a0d2eb47cd8b`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.9 MB (1903443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34979c15a1233c67bd0ec46dadaeb9569227dc9d89d950fee2a65c338a094c1d`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:0f2bab4cb10e5f91f35a44a6be840eb663d099d578295d8e43956c8989e8f7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba68b61c5a236dab9c41021948429c3f3b4c8da03c703286afe903251cb3590`

```dockerfile
```

-	Layers:
	-	`sha256:562ca2a5070b8e2035df29e6c634bbd953ec6a8081b1808052ab752cff4abf2f`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 3.2 MB (3177418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aed4827ecf2de08bb7abf88eee3dea2fb807541ee82fe2502604e610ef7ef2`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 34.5 KB (34533 bytes)  
		MIME: application/vnd.in-toto+json
