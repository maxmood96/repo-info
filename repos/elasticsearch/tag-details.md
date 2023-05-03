<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.10`](#elasticsearch71710)
-	[`elasticsearch:8.7.1`](#elasticsearch871)

## `elasticsearch:7.17.10`

```console
$ docker pull elasticsearch@sha256:43b9e781ebb2bd731ea3966bb816edce947e34965676046b3c0f8c17318cee72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:81facec55eceeb7bebeed80af49eb9a05fce77709b231210f343ac8b9599098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355054430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a305059888ba801d416b5c586108895e4f650557856a19572d3f815b160e1d38`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Sun, 23 Apr 2023 05:37:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Sun, 23 Apr 2023 05:37:55 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Sun, 23 Apr 2023 05:37:55 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 23 Apr 2023 05:37:55 GMT
WORKDIR /usr/share/elasticsearch
# Sun, 23 Apr 2023 05:38:12 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Sun, 23 Apr 2023 05:38:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Sun, 23 Apr 2023 05:38:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 23 Apr 2023 05:38:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Sun, 23 Apr 2023 05:38:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Sun, 23 Apr 2023 05:38:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sun, 23 Apr 2023 05:38:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sun, 23 Apr 2023 05:38:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Sun, 23 Apr 2023 05:38:14 GMT
LABEL org.label-schema.build-date=2023-04-23T05:33:18.138275597Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fecd68e3150eda0c307ab9a9d7557f5d5fd71349 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.10 org.opencontainers.image.created=2023-04-23T05:33:18.138275597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fecd68e3150eda0c307ab9a9d7557f5d5fd71349 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.10
# Sun, 23 Apr 2023 05:38:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sun, 23 Apr 2023 05:38:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12bd77ba010a976d7845656c4f0cf9affa73cb9ad95aa165e7d799e422051ee`  
		Last Modified: Tue, 02 May 2023 23:55:47 GMT  
		Size: 7.5 MB (7488523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1301fe510917887796b5e67371d1ed9ef8e58e416aa142ac2de6f4bdf754bbd2`  
		Last Modified: Tue, 02 May 2023 23:55:46 GMT  
		Size: 4.3 KB (4341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b84f24899a89b9d0bc4a1bde480e2b09c7ddd4d6657906225c3358734cfef27`  
		Last Modified: Tue, 02 May 2023 23:56:08 GMT  
		Size: 318.7 MB (318678941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80def0a7fa7350415c940a42467e8591b2cbf41c5204802b78e1d1150d8f5ee6`  
		Last Modified: Tue, 02 May 2023 23:55:44 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b893bbb622cfc6c32cd4699db7907f835390ee9b308a3bb3ffa4460bd4a940`  
		Last Modified: Tue, 02 May 2023 23:55:44 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb7875ab0d20d1c37f3a1085dc1e27554a71f4912d32c1baf2b3f077054c533`  
		Last Modified: Tue, 02 May 2023 23:55:44 GMT  
		Size: 192.1 KB (192127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ed52a5c81982d65b4b0984ddb103751082a0ac40c34290d65c2cdcd62010f4`  
		Last Modified: Tue, 02 May 2023 23:55:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6942c0cf53a513a300fcd5bd7013634d1ddd1820c2fe5207d88da2682f5ef2`  
		Last Modified: Tue, 02 May 2023 23:55:44 GMT  
		Size: 100.0 KB (99988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9e3e732ae247a773ddb753abebbdf2094b2cccc74229761e270e47a9398afad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351588685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02ab30907c1ff1e1a46678a04e3986b0e0c1fed4069b9c0585e649562318ae1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Sun, 23 Apr 2023 05:38:58 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Sun, 23 Apr 2023 05:39:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Sun, 23 Apr 2023 05:39:00 GMT
ENV ELASTIC_CONTAINER=true
# Sun, 23 Apr 2023 05:39:00 GMT
WORKDIR /usr/share/elasticsearch
# Sun, 23 Apr 2023 05:39:04 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Sun, 23 Apr 2023 05:39:05 GMT
COPY /bin/tini /bin/tini # buildkit
# Sun, 23 Apr 2023 05:39:05 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 23 Apr 2023 05:39:05 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Sun, 23 Apr 2023 05:39:05 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Sun, 23 Apr 2023 05:39:05 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sun, 23 Apr 2023 05:39:06 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sun, 23 Apr 2023 05:39:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Sun, 23 Apr 2023 05:39:06 GMT
LABEL org.label-schema.build-date=2023-04-23T05:33:18.138275597Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fecd68e3150eda0c307ab9a9d7557f5d5fd71349 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.10 org.opencontainers.image.created=2023-04-23T05:33:18.138275597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fecd68e3150eda0c307ab9a9d7557f5d5fd71349 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.10
# Sun, 23 Apr 2023 05:39:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sun, 23 Apr 2023 05:39:06 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca59924f0d86cf80613044e81bb351de559728b0da8a28d2ca2955333ee540`  
		Last Modified: Wed, 03 May 2023 00:21:29 GMT  
		Size: 7.3 MB (7309587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8d3e68fe0c3228a2c728ef6416e688266d4ac9ef13c8e4c24067e2903013e7`  
		Last Modified: Wed, 03 May 2023 00:21:28 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046ebafbe7304d40fd0e6f552a9ee289fda050205f15f529fc06423fa0a1f7e2`  
		Last Modified: Wed, 03 May 2023 00:22:02 GMT  
		Size: 316.8 MB (316780680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf7ce3fa8665187fe0d08aa4e6511fd263eb0c23d633ae01315b714cd79098e`  
		Last Modified: Wed, 03 May 2023 00:21:26 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0625aa8000c2aab2dcc14e5ed7f2f09c8e046d91c0f93434673563de0d4564d`  
		Last Modified: Wed, 03 May 2023 00:21:26 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4048d8522fed75b092aff3b1d344939e073b97c33662ad9fb320830bfa1dc5e4`  
		Last Modified: Wed, 03 May 2023 00:21:26 GMT  
		Size: 186.2 KB (186162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03345f934121cb9b8051453128be9c8cbca5dd9b13dd4608424c221ebd6c3b9`  
		Last Modified: Wed, 03 May 2023 00:21:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffd0f00782dcf135cef9f641cf729c91315da45477bf364da5f0b0621446242`  
		Last Modified: Wed, 03 May 2023 00:21:26 GMT  
		Size: 100.0 KB (99985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.7.1`

```console
$ docker pull elasticsearch@sha256:160814e5972521291420c29edf4c0348b8591ac9235156f0dbf34befcf362825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.7.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9e6a585adeafc97a27c0aa300f62b6b95f12e5011030a52db26fec8a7f31fe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 MB (641465052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59075530be34d3a06866f894ae9735f6d739a7a751ad45efb86dec3c9bd16836`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Thu, 27 Apr 2023 04:40:39 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 27 Apr 2023 04:40:44 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 27 Apr 2023 04:40:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 27 Apr 2023 04:40:44 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 27 Apr 2023 04:41:23 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 27 Apr 2023 04:41:23 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 27 Apr 2023 04:41:23 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Apr 2023 04:41:23 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Apr 2023 04:41:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 27 Apr 2023 04:41:25 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 27 Apr 2023 04:41:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 27 Apr 2023 04:41:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 27 Apr 2023 04:41:27 GMT
LABEL org.label-schema.build-date=2023-04-27T04:33:42.127815583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f229ed3f893a515d590d0f39b05f68913e2d9b53 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.7.1 org.opencontainers.image.created=2023-04-27T04:33:42.127815583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f229ed3f893a515d590d0f39b05f68913e2d9b53 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.7.1
# Thu, 27 Apr 2023 04:41:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 04:41:27 GMT
CMD ["eswrapper"]
# Thu, 27 Apr 2023 04:41:27 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f96b513f07d2f86a9f4fb51144492836e5d32c905def556e3bea2fa3485ea31`  
		Last Modified: Tue, 02 May 2023 14:31:55 GMT  
		Size: 7.5 MB (7488347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df5d38d73b812a2364483e5aaab3d8b32fc2d4e8d1f96ff4434302984b1048f`  
		Last Modified: Tue, 02 May 2023 14:31:38 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404dcab8b481e7fa606cfbaf7a0c44e3d99b7f918ae90056d376f5f68b27aefe`  
		Last Modified: Tue, 02 May 2023 14:34:44 GMT  
		Size: 605.1 MB (605090257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3699ac88f4ec2bf827fec0f382b2cfd29e6b2b23236547d8c845dae78e16ce`  
		Last Modified: Tue, 02 May 2023 14:31:36 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440e18daf2ab63e12d463f3389662c341f961bb3960bc4e118dd0feba5469056`  
		Last Modified: Tue, 02 May 2023 14:31:36 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ffdd6503e3d743f375eb2154cc4402f2d604b7e784b2bb4904f1589096d8f4`  
		Last Modified: Tue, 02 May 2023 14:31:34 GMT  
		Size: 191.9 KB (191865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fa33f4ba5c24161a572a41a161710e043d070905047dabccbc4a028272474e`  
		Last Modified: Tue, 02 May 2023 14:31:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5ae6b8f17fad5b0d6d530e274d291058354afac911aa1d3a7854684ed47bb`  
		Last Modified: Tue, 02 May 2023 14:31:33 GMT  
		Size: 100.0 KB (99985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.7.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:cbc7950662b3f85f3b5910683990080dbb4973b0b81a98009e6905467e958566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434795107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c46ca52228b94f4e48414f01552c8764f63d5b8d3fc8ed241e0ffdda7155bdc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Thu, 27 Apr 2023 04:40:59 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 27 Apr 2023 04:41:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 27 Apr 2023 04:41:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 27 Apr 2023 04:41:02 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 27 Apr 2023 04:41:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 27 Apr 2023 04:41:23 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 27 Apr 2023 04:41:23 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Apr 2023 04:41:23 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Apr 2023 04:41:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 27 Apr 2023 04:41:25 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 27 Apr 2023 04:41:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 27 Apr 2023 04:41:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 27 Apr 2023 04:41:27 GMT
LABEL org.label-schema.build-date=2023-04-27T04:33:42.127815583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f229ed3f893a515d590d0f39b05f68913e2d9b53 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.7.1 org.opencontainers.image.created=2023-04-27T04:33:42.127815583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f229ed3f893a515d590d0f39b05f68913e2d9b53 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.7.1
# Thu, 27 Apr 2023 04:41:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 27 Apr 2023 04:41:27 GMT
CMD ["eswrapper"]
# Thu, 27 Apr 2023 04:41:27 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35c80ae7deefedac75b0a53c22a4ea9a399d36de868afed32b029b4015e4c2`  
		Last Modified: Wed, 03 May 2023 00:21:00 GMT  
		Size: 7.3 MB (7309434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c1252969cef75d072325c7dd7caa4565335576c4c766ee8c530ccfb50ec87f`  
		Last Modified: Wed, 03 May 2023 00:20:58 GMT  
		Size: 4.4 KB (4352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76867c6d7ff09276332cc399dd8bcd808dacbcf9c049583af30d64ba184b8b1e`  
		Last Modified: Wed, 03 May 2023 00:21:19 GMT  
		Size: 400.0 MB (399987781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598dc937986f26adda743aa4e2ba176b81d1be54bdd6983705c2f146157171a8`  
		Last Modified: Wed, 03 May 2023 00:20:56 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8989f93c7cccb33857654609c6e7b5fff75093657aeafa0a2f78fae04fcdcdd`  
		Last Modified: Wed, 03 May 2023 00:20:56 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397e9044fa2891cea503995f50a8cd90f61eed2e8fba252086812f8462ca6b7f`  
		Last Modified: Wed, 03 May 2023 00:20:57 GMT  
		Size: 185.9 KB (185893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d320088bb61f9cc32c6479e6c4fee9766796c5e41d125dfeccb91d0f66059a`  
		Last Modified: Wed, 03 May 2023 00:20:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05deba30ddeefdce3177da41081dc438aec70d08203b370b5d32fd8da096ebe4`  
		Last Modified: Wed, 03 May 2023 00:20:59 GMT  
		Size: 100.0 KB (99990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
