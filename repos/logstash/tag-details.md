<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.10`](#logstash71710)
-	[`logstash:8.7.1`](#logstash871)

## `logstash:7.17.10`

```console
$ docker pull logstash@sha256:b1290fe8dc61956a79a0f0c9a3b40eb228b966385667045bb82facecca54de8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:7.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c5fddc691f01644abb2458d947dda15670c0bc7eb3dcecd76929164e63035a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 MB (428108876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aca257c77c5816e7ac4ecaf50ffae3cda57f348dac8f7a4c97c0dee97953a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 15:56:47 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 20 Apr 2023 15:56:47 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.10-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.10 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
WORKDIR /usr/share/logstash
# Thu, 20 Apr 2023 15:57:00 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Apr 2023 15:57:00 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 20 Apr 2023 15:57:00 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 20 Apr 2023 15:57:00 GMT
USER 1000
# Thu, 20 Apr 2023 15:57:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 20 Apr 2023 15:57:00 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.10 org.opencontainers.image.version=7.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-20T15:43:51+00:00 org.opencontainers.image.created=2023-04-20T15:43:51+00:00
# Thu, 20 Apr 2023 15:57:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df146c1c3fdeefbf2c8499aba2e532c39356e14630bc4d0800c704c8ae9c239`  
		Last Modified: Wed, 03 May 2023 03:45:51 GMT  
		Size: 35.2 MB (35192502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3e2d4e6e72b4be71db7399fd03ec4846eaf96070eb4ee12b7d585ec32484e6`  
		Last Modified: Wed, 03 May 2023 03:45:48 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda4e20a465e10b98ca6f2051b81363fb407484af53012181f80e5ee515568b`  
		Last Modified: Wed, 03 May 2023 03:46:08 GMT  
		Size: 364.0 MB (364023654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95c90cfa68731e409f58cf9413cd14d352c799691c4e3350932b48a1728de8e`  
		Last Modified: Wed, 03 May 2023 03:45:47 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27628d91aa2602189ff17407206d2deb1ff8000c9c96cbbde0d363a2c3ff7`  
		Last Modified: Wed, 03 May 2023 03:45:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75024a673d419b30010aa065f9cf7a394e6a6bc41c69e4c64d66499be68a741`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6e12f434639053c3e159dcd1969589f973158963e08ca610e7aadfd7794d72`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124287526a1bf4df21260945ea7007f4f8a79dc5e9e00241230ea5a87d3c0262`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 2.9 KB (2851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea4b9ceb2ccb6eee733f6df7d88df3e300facfc1e4a2c21944ac73e77244ea2`  
		Last Modified: Wed, 03 May 2023 03:45:46 GMT  
		Size: 1.7 MB (1689166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ceb4ffb8e47010f2205563ab97aeb34220207f6f3d523d2b0e8810d556d0d0`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ceb4ffb8e47010f2205563ab97aeb34220207f6f3d523d2b0e8810d556d0d0`  
		Last Modified: Wed, 03 May 2023 03:45:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.7.1`

```console
$ docker pull logstash@sha256:42153466d02f45965e7334e33895907665c7dc38cd9eea739e801212bf8b8a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:8.7.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:cb994b8cf3d20cd89fdeb9e8a4c0c09fd8b232384087a8687641d28522123903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 MB (390523193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b51d8266ff19a0eb95e478b9d2109e5ac4cc306ee0a6e22237481399392d02`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 11:08:00 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 20 Apr 2023 11:08:01 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 20 Apr 2023 11:08:11 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.7.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.7.1 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 20 Apr 2023 11:08:11 GMT
WORKDIR /usr/share/logstash
# Thu, 20 Apr 2023 11:08:12 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Apr 2023 11:08:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Apr 2023 11:08:12 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 20 Apr 2023 11:08:12 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 20 Apr 2023 11:08:12 GMT
USER 1000
# Thu, 20 Apr 2023 11:08:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 20 Apr 2023 11:08:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.7.1 org.opencontainers.image.version=8.7.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-04-20T10:53:40+00:00 org.opencontainers.image.created=2023-04-20T10:53:40+00:00
# Thu, 20 Apr 2023 11:08:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8d59d49481743a7bb1a40b4db9f49011978857d4fc0416eef266bbb02f3062`  
		Last Modified: Wed, 03 May 2023 03:45:23 GMT  
		Size: 35.2 MB (35192458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0bd36011283b6348d4da22f4c7e78eca5f9a292746a235f02b8d76e9618ad5`  
		Last Modified: Wed, 03 May 2023 03:45:19 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23712106d21e473d88ce18673544b89a72bea3f470afbaa77404fceefdddb8cd`  
		Last Modified: Wed, 03 May 2023 03:45:39 GMT  
		Size: 326.4 MB (326435068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0510e81a54602eed92adbb294b76e380485500d58c97b47cb0b845af6fb7644f`  
		Last Modified: Wed, 03 May 2023 03:45:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a509ab883b17015e1c65a9436cd2459c6c8f7a013af655679972c2626cf43dd3`  
		Last Modified: Wed, 03 May 2023 03:45:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edf50ff612ca3120615bd2c8570e8e2d366e7de78b67edbcd725cb1108e80c5`  
		Last Modified: Wed, 03 May 2023 03:45:18 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35911fa894ffcaed80a61d1d1d319c352fd6021bd5056da67041ac6f49c33bd9`  
		Last Modified: Wed, 03 May 2023 03:45:16 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570261b8be8109d0d37b2ed44208851995a7683435dc0fbcdd032e30a89ca673`  
		Last Modified: Wed, 03 May 2023 03:45:16 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6584fd971211a4febbaf1f66cf39f5e3e4b857cda01fec00f65eb94e572f12`  
		Last Modified: Wed, 03 May 2023 03:45:16 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576d2cfa12c8bd947f1785d37969e1632216b0db0048bee596ba531ebecf56d0`  
		Last Modified: Wed, 03 May 2023 03:45:17 GMT  
		Size: 1.7 MB (1689520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd63d93c485968b9cc30c0db8f22914dd530550a644728c5562fe91f26148c`  
		Last Modified: Wed, 03 May 2023 03:45:16 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd63d93c485968b9cc30c0db8f22914dd530550a644728c5562fe91f26148c`  
		Last Modified: Wed, 03 May 2023 03:45:16 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
