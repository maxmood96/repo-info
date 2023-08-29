<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.11`](#elasticsearch71711)
-	[`elasticsearch:7.17.12`](#elasticsearch71712)
-	[`elasticsearch:8.8.2`](#elasticsearch882)
-	[`elasticsearch:8.9.0`](#elasticsearch890)
-	[`elasticsearch:8.9.1`](#elasticsearch891)

## `elasticsearch:7.17.11`

```console
$ docker pull elasticsearch@sha256:87216a9f0a1a5ff4acfc12dbdf3b2cc42f7bca073204011befefabca32666d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.11` - linux; amd64

```console
$ docker pull elasticsearch@sha256:11cfbdf081540efc0e3cf1a5ffd1cab3465189f4a01c7ef4db03a99fbe178172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358584320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f404e39b5e61d14bddf8b41fc04dc7d80b11e962e575e1c1101965b6cfcf5bd`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 05:37:36 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Fri, 23 Jun 2023 05:37:37 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 23 Jun 2023 05:37:37 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 23 Jun 2023 05:37:37 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 23 Jun 2023 05:37:47 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Fri, 23 Jun 2023 05:37:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 23 Jun 2023 05:37:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jun 2023 05:37:48 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 23 Jun 2023 05:37:48 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 23 Jun 2023 05:37:48 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 23 Jun 2023 05:37:49 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 23 Jun 2023 05:37:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 23 Jun 2023 05:37:49 GMT
LABEL org.label-schema.build-date=2023-06-23T05:33:12.261262042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=eeedb98c60326ea3d46caef960fb4c77958fb885 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.11 org.opencontainers.image.created=2023-06-23T05:33:12.261262042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=eeedb98c60326ea3d46caef960fb4c77958fb885 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.11
# Fri, 23 Jun 2023 05:37:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 05:37:49 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3db371e0d15ea94636813eebe0868d41bb405d00cf88886f39ac72d45f6d5`  
		Last Modified: Thu, 29 Jun 2023 16:14:39 GMT  
		Size: 10.4 MB (10443122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fca182724ded127c33eb687988feb75f4e97fe7b904750d8f2e110b4f2cd9b2`  
		Last Modified: Thu, 29 Jun 2023 16:14:37 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305e660de369ac58b20ccaebd61172cfab68642868d7e6f12c09f0ab30bf0f12`  
		Last Modified: Thu, 29 Jun 2023 16:15:09 GMT  
		Size: 319.2 MB (319243017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac16cfc30269f7e76d887f1eaeae5b11f6d1aea06ba3baef6e5c3daceb085db`  
		Last Modified: Thu, 29 Jun 2023 16:14:37 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d312feadd3a6c1d29644485a1d39d899ae50d2ff071e5d7b52f4234709619`  
		Last Modified: Thu, 29 Jun 2023 16:14:36 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b06a3f436bf2ad0ba6b8a160e2c4d66c039517798872b95456ce6821305b14f`  
		Last Modified: Thu, 29 Jun 2023 16:14:36 GMT  
		Size: 192.1 KB (192129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736bbcf13b1fc9f43d0207f7a382df3f54bcc879ea9ea0b39f2bdfaf48a9a10f`  
		Last Modified: Thu, 29 Jun 2023 16:14:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795bdaa6314b6e0e6206298e37719ef9925b097908a557c18bef74c756d2e5f3`  
		Last Modified: Thu, 29 Jun 2023 16:14:36 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.11` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1a7a957561e04e5307d5db0d3f85f8527009f60a559aa4c248650f28cba4f7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355075438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399cfbf7383e1ab737c4795e137c01309caeb7ffa8b7e341cdc0b62e23f41b3b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Fri, 23 Jun 2023 05:38:53 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Fri, 23 Jun 2023 05:38:55 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 23 Jun 2023 05:38:56 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 23 Jun 2023 05:38:56 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 23 Jun 2023 05:38:57 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Fri, 23 Jun 2023 05:38:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 23 Jun 2023 05:38:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jun 2023 05:38:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 23 Jun 2023 05:38:58 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 23 Jun 2023 05:38:58 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 23 Jun 2023 05:38:59 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 23 Jun 2023 05:38:59 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 23 Jun 2023 05:38:59 GMT
LABEL org.label-schema.build-date=2023-06-23T05:33:12.261262042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=eeedb98c60326ea3d46caef960fb4c77958fb885 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.11 org.opencontainers.image.created=2023-06-23T05:33:12.261262042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=eeedb98c60326ea3d46caef960fb4c77958fb885 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.11
# Fri, 23 Jun 2023 05:38:59 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 23 Jun 2023 05:38:59 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf2d4005d1d7acb50cdb433fcf63f02ff6784c98e9aabebcdd61d9b2fd19b3`  
		Last Modified: Mon, 28 Aug 2023 23:41:15 GMT  
		Size: 10.2 MB (10211478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f407a7076ebdb7e85ddf4419c4c0eff057043c0035716900de61b7a268e6c485`  
		Last Modified: Mon, 28 Aug 2023 23:41:14 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a402dc8985d4253420ff2f170c0232e5b138cf8a252f686a0b8548169dcb07`  
		Last Modified: Mon, 28 Aug 2023 23:41:32 GMT  
		Size: 317.4 MB (317352238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56069063a1233056a6f3f201e532816548ad3f08d9c38d3f16fe5105544649f`  
		Last Modified: Mon, 28 Aug 2023 23:41:12 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e81d9253972d451383f55254e3dab44539ea3826252fd978e973b38cbffd57b`  
		Last Modified: Mon, 28 Aug 2023 23:41:12 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acccdcfb380cbefc50c3a765d5f16665765c7d0af4603f844ef3ac054405f2ff`  
		Last Modified: Mon, 28 Aug 2023 23:41:12 GMT  
		Size: 186.2 KB (186162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ebffa29899e11b9f401789ff440f3fe8075c0b287b95fa0481d6cd23476873`  
		Last Modified: Mon, 28 Aug 2023 23:41:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015a7d148fbdbef67c464862b83342dd20983f0bb8692d43af667834901a0c75`  
		Last Modified: Mon, 28 Aug 2023 23:41:12 GMT  
		Size: 109.2 KB (109247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.17.12`

```console
$ docker pull elasticsearch@sha256:295a3f67e74f5d30d597d742b0d2387340543fd9ee4b090c822130f9b461bff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.12` - linux; amd64

```console
$ docker pull elasticsearch@sha256:09de980aef66b2c879c9f2bae02244aa9526d0ca15d3385ba88ee6d3b1c22557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356274906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12f24d547f7a416587396303fcae7f8228e75ebc3a5b970a79cedd91256fe1c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 05:37:59 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 20 Jul 2023 05:38:01 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 20 Jul 2023 05:38:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Jul 2023 05:38:02 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 20 Jul 2023 05:38:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 20 Jul 2023 05:38:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 20 Jul 2023 05:38:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jul 2023 05:38:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 20 Jul 2023 05:38:23 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 20 Jul 2023 05:38:23 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 20 Jul 2023 05:38:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 20 Jul 2023 05:38:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 20 Jul 2023 05:38:24 GMT
LABEL org.label-schema.build-date=2023-07-20T05:33:33.690180787Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e3b0c3d3c5c130e1dc6d567d6baef1c73eeb2059 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.12 org.opencontainers.image.created=2023-07-20T05:33:33.690180787Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e3b0c3d3c5c130e1dc6d567d6baef1c73eeb2059 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.12
# Thu, 20 Jul 2023 05:38:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Jul 2023 05:38:24 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f730e53da950f6ea7615ef96104ca2bee6e39f40923de90efc7fb6253c331d`  
		Last Modified: Wed, 02 Aug 2023 09:29:31 GMT  
		Size: 7.5 MB (7509902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00937b28d0ae005e91309a7e36c428adda3d0e8733063e101457dd45166682a4`  
		Last Modified: Wed, 02 Aug 2023 09:29:27 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31d9d48f767a2235bec564c378f53ac24e8b180ca436b213cbf0c9ccbca3bf`  
		Last Modified: Wed, 02 Aug 2023 09:30:58 GMT  
		Size: 319.9 MB (319867331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3302e7ae92d0fbcbda4f72b2920ebf046f58d4193033e0793110eed12633445c`  
		Last Modified: Wed, 02 Aug 2023 09:29:26 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39533148ce3716a5e8b954faa016fa4267ef73026f3f242af059ae22c28b09ed`  
		Last Modified: Wed, 02 Aug 2023 09:29:24 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873b68789259978b99abadf4fe9c2a714e589d0c600800a032475524d768410`  
		Last Modified: Wed, 02 Aug 2023 09:29:25 GMT  
		Size: 192.1 KB (192139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834621cdc73669366c4942ef04f5646054c5c41e846ebdebe6cf9a64a8bfb578`  
		Last Modified: Wed, 02 Aug 2023 09:29:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d765e9a19285f1e7deb1b963b605078e6fae9fd909297b4c30fd90b3f846965`  
		Last Modified: Wed, 02 Aug 2023 09:29:24 GMT  
		Size: 109.2 KB (109237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.12` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2e59a6dbd274364fcd6945312141f4648cbd4645463ae4281c46efd82975e6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352778423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed8ceb6348c4f73b902a2586aa0a5bfa1739d82407273ce7f136a7ae6eb225`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 05:39:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 20 Jul 2023 05:39:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 20 Jul 2023 05:39:17 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Jul 2023 05:39:17 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 20 Jul 2023 05:39:22 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 20 Jul 2023 05:39:22 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 20 Jul 2023 05:39:22 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jul 2023 05:39:22 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 20 Jul 2023 05:39:23 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 20 Jul 2023 05:39:23 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 20 Jul 2023 05:39:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 20 Jul 2023 05:39:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 20 Jul 2023 05:39:24 GMT
LABEL org.label-schema.build-date=2023-07-20T05:33:33.690180787Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e3b0c3d3c5c130e1dc6d567d6baef1c73eeb2059 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.12 org.opencontainers.image.created=2023-07-20T05:33:33.690180787Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e3b0c3d3c5c130e1dc6d567d6baef1c73eeb2059 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.12
# Thu, 20 Jul 2023 05:39:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Jul 2023 05:39:24 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8d2cecec7d4e8f9ce26b6a574f1031d908649763016604433586e4376ee9d`  
		Last Modified: Fri, 11 Aug 2023 19:12:58 GMT  
		Size: 7.3 MB (7330984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c45513239d3be0c22fdc0f75f705fc0af9d74afc459046dbe7b5320d24d30`  
		Last Modified: Fri, 11 Aug 2023 19:12:56 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ee9770d7627c968b35cfafd61a4daea728eef9ac053107d5d5c093ac6c49d`  
		Last Modified: Fri, 11 Aug 2023 19:13:15 GMT  
		Size: 317.9 MB (317937825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40158c56b2f278021639b5aea4e35c96709024daa9327c807343ab7a7194152`  
		Last Modified: Fri, 11 Aug 2023 19:12:56 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ef765ef9a494b1a9b2c133615628522c7ad6bc0bd842e512b7e69967043f7b`  
		Last Modified: Fri, 11 Aug 2023 19:12:56 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ee292f98e0d3c8fb3fe1adcef0175ca1fc3e4eee647e8cf5f788c7ef1ee894`  
		Last Modified: Fri, 11 Aug 2023 19:12:55 GMT  
		Size: 186.2 KB (186162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4ea39f4d4a8fc7e013276e2d62dac62dfa093e11e90341d599d768d63f3a64`  
		Last Modified: Fri, 11 Aug 2023 19:12:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c16b2b3cfdf718cb3f978dd395fa545c3f75ada989723405a04e0a99affd5e`  
		Last Modified: Fri, 11 Aug 2023 19:12:54 GMT  
		Size: 109.2 KB (109246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.8.2`

```console
$ docker pull elasticsearch@sha256:acb934176519afa01f195e06b6085a5159401be37cdd70c2fbcd04890581e41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.8.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d45ef71c0f2680bc38b1427f53ca294ebaef4a4ea88cb243cdefc96c3e44dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.6 MB (643649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673e6376a286fd839ecee644ccfb4951df6bda9a33532720b857eaca821ec5dc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Mon, 26 Jun 2023 05:23:45 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 26 Jun 2023 05:23:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jun 2023 05:23:46 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jun 2023 05:23:46 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jun 2023 05:24:12 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 26 Jun 2023 05:24:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jun 2023 05:24:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jun 2023 05:24:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 05:24:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jun 2023 05:24:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 26 Jun 2023 05:24:15 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 26 Jun 2023 05:24:15 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jun 2023 05:24:15 GMT
LABEL org.label-schema.build-date=2023-06-26T05:16:16.196344851Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=98e1271edf932a480e4262a471281f1ee295ce6b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.8.2 org.opencontainers.image.created=2023-06-26T05:16:16.196344851Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=98e1271edf932a480e4262a471281f1ee295ce6b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.8.2
# Mon, 26 Jun 2023 05:24:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jun 2023 05:24:15 GMT
CMD ["eswrapper"]
# Mon, 26 Jun 2023 05:24:15 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bad5883434bc896c3bdb2d7ace1dccac70ecce0ebc9495507d401c1d545dfb`  
		Last Modified: Sun, 02 Jul 2023 15:16:27 GMT  
		Size: 10.4 MB (10443212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c285faa9f620d7b23c52641dd0653548bda3cdbb164d14a9596af0eaedf4fddb`  
		Last Modified: Sun, 02 Jul 2023 15:16:22 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3d9862ed448144b9092684b4b611da9794ce7ae92cddf7ff2130f011b91925`  
		Last Modified: Sun, 02 Jul 2023 15:18:19 GMT  
		Size: 604.3 MB (604308456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1418c59bacdfc75b9c4bf1aa683ffd7cbe42ca6c2e3ea7bb57eddcc261b99889`  
		Last Modified: Sun, 02 Jul 2023 15:16:21 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b0a61ada76ccc25d5af4e12be82ff8cc951efadfe48c2441cc05940cd5008`  
		Last Modified: Sun, 02 Jul 2023 15:16:19 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6736a97fc18ef1a11341c81ea220d884ecc61c55c529c1ee76b2bb2a2b36bf`  
		Last Modified: Sun, 02 Jul 2023 15:16:19 GMT  
		Size: 191.9 KB (191868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50880bcf0295a16c6b42eacfb3ae62e85d9e3d7dbea061d3b2746fbf8fb14416`  
		Last Modified: Sun, 02 Jul 2023 15:16:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef243ce31f27bef9fdb779d5f40ebe4d96f6b1849d03a6bcac5f0849a774fc22`  
		Last Modified: Sun, 02 Jul 2023 15:16:20 GMT  
		Size: 109.2 KB (109243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.8.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:00f2b1375969c787297a18dd309cbd1d85b0ea183253af516bd7799de6f02f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436886793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035ac81895b7cf30c22560fc72ca0362853a506cb8f67cfaf9db8221100cf7dd`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Mon, 26 Jun 2023 05:24:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 26 Jun 2023 05:24:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jun 2023 05:24:16 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jun 2023 05:24:16 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jun 2023 05:24:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 26 Jun 2023 05:24:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jun 2023 05:24:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jun 2023 05:24:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 05:24:36 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jun 2023 05:24:38 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 26 Jun 2023 05:24:39 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 26 Jun 2023 05:24:39 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jun 2023 05:24:39 GMT
LABEL org.label-schema.build-date=2023-06-26T05:16:16.196344851Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=98e1271edf932a480e4262a471281f1ee295ce6b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.8.2 org.opencontainers.image.created=2023-06-26T05:16:16.196344851Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=98e1271edf932a480e4262a471281f1ee295ce6b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.8.2
# Mon, 26 Jun 2023 05:24:39 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jun 2023 05:24:39 GMT
CMD ["eswrapper"]
# Mon, 26 Jun 2023 05:24:39 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a8f3d196d11001927e8483bc8265aaade9bcd5c15765aca97a5a235d4cf35`  
		Last Modified: Mon, 03 Jul 2023 22:40:20 GMT  
		Size: 10.2 MB (10211435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ffa39d366754fc32a945752d33c86d81f64e076e28cc4d6cb078895b89387c`  
		Last Modified: Mon, 03 Jul 2023 22:39:29 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb02a5e19991f048fe1dc68108d754294d01a0e93bd2b59c7213573449920e`  
		Last Modified: Mon, 03 Jul 2023 22:46:39 GMT  
		Size: 399.2 MB (399164152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f78c8be7b95293ff0cad1892211670339ad67116bd6e52a778c584f534c0b9`  
		Last Modified: Mon, 03 Jul 2023 22:39:23 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8c37e28e9d4949a778c1b36b57fe5d28297360fab4218e3088e6a293219dbe`  
		Last Modified: Mon, 03 Jul 2023 22:39:23 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619581e69404dcd31088f8e95973f9eb9956c5ad724ec85bd5c1bc4a54fbd8dc`  
		Last Modified: Mon, 03 Jul 2023 22:39:24 GMT  
		Size: 185.9 KB (185899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd3002dbfefdb186b4ef5c3ca3ac235a660d507e2de904e2813976f8b080116`  
		Last Modified: Mon, 03 Jul 2023 22:39:23 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89999b80bc774a9c847316a0ea2f3ef002b0dc9c40552fcdd8f592aa1f701efe`  
		Last Modified: Mon, 03 Jul 2023 22:39:24 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.9.0`

```console
$ docker pull elasticsearch@sha256:ac562ea8af1606ea65df64fc775f384a5cae82ae20e78f07ce31dc91c6943437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.9.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d84dcd18c9a35d63d6d92c3ee40b5a7e4caf2c3c7a931a587eba18ff8ecf5bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.4 MB (649355165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281908e9f34edac2296408200fc803272bfa0f9b4bffb490132ce68bc069db3c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 14:49:59 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 19 Jul 2023 14:50:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 19 Jul 2023 14:50:00 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 19 Jul 2023 14:50:00 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 19 Jul 2023 14:50:18 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 19 Jul 2023 14:50:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 19 Jul 2023 14:50:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jul 2023 14:50:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 19 Jul 2023 14:50:21 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 19 Jul 2023 14:50:21 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 19 Jul 2023 14:50:23 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 19 Jul 2023 14:50:23 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 19 Jul 2023 14:50:23 GMT
LABEL org.label-schema.build-date=2023-07-19T14:43:58.555259655Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8aa461beb06aa0417a231c345a1b8c38fb498a0d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.9.0 org.opencontainers.image.created=2023-07-19T14:43:58.555259655Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8aa461beb06aa0417a231c345a1b8c38fb498a0d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.0
# Wed, 19 Jul 2023 14:50:23 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 14:50:23 GMT
CMD ["eswrapper"]
# Wed, 19 Jul 2023 14:50:23 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47490874885d7021816a64ef31898e6e7767ea9e08fb508a1701f25705a485b`  
		Last Modified: Wed, 26 Jul 2023 03:35:19 GMT  
		Size: 7.5 MB (7509989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4291a01077de1b3bab4ae295dbb1ee4a0ccead9c7c27220820be5e1810cfaa2c`  
		Last Modified: Wed, 26 Jul 2023 03:35:18 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644b25dbb32884a0cf267e6f31dfcae18a73147eeb20ef19c6a06cafde50fece`  
		Last Modified: Wed, 26 Jul 2023 03:36:11 GMT  
		Size: 612.9 MB (612948019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfc7ad281e864e1a87f2597d1089b8617f4dabd29af05d8142320ffe11f35fb`  
		Last Modified: Wed, 26 Jul 2023 03:35:16 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf3c7ca8573aa7de16af68d4d1c004965c29d2f8512c93759f57723ce2f246`  
		Last Modified: Wed, 26 Jul 2023 03:35:16 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c607d6865200b5849626aebc59d529ab41b723d98193c1967e539d354666ad10`  
		Last Modified: Wed, 26 Jul 2023 03:35:16 GMT  
		Size: 191.9 KB (191866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334f7067d9b79bf58e6ed596a3f54b11abf44ea4afb25725d90a6ed4b36fd55`  
		Last Modified: Wed, 26 Jul 2023 03:35:15 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91ac6140bf90987077ce77a6d945a7e9690f6807c3131e8f40c05a4477004d9`  
		Last Modified: Wed, 26 Jul 2023 03:35:15 GMT  
		Size: 109.2 KB (109244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.9.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d20e9e782e86d7c791b0341c17f90f5ab5205401987825471cc46f9908b24c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.6 MB (442615989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c68c103c8852cee788833860064eb34899fe9fb213f80085f9b35e87e35b21c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 14:51:03 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 19 Jul 2023 14:51:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 19 Jul 2023 14:51:06 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 19 Jul 2023 14:51:06 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 19 Jul 2023 14:51:09 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 19 Jul 2023 14:51:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 19 Jul 2023 14:51:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jul 2023 14:51:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 19 Jul 2023 14:51:10 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 19 Jul 2023 14:51:10 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 19 Jul 2023 14:51:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 19 Jul 2023 14:51:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 19 Jul 2023 14:51:12 GMT
LABEL org.label-schema.build-date=2023-07-19T14:43:58.555259655Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8aa461beb06aa0417a231c345a1b8c38fb498a0d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.9.0 org.opencontainers.image.created=2023-07-19T14:43:58.555259655Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8aa461beb06aa0417a231c345a1b8c38fb498a0d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.0
# Wed, 19 Jul 2023 14:51:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 14:51:12 GMT
CMD ["eswrapper"]
# Wed, 19 Jul 2023 14:51:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87ed88089fcdec10a5b2607bf3ee4c1561a7498c963505fc68330085d4f05d4`  
		Last Modified: Tue, 08 Aug 2023 14:32:29 GMT  
		Size: 7.3 MB (7330982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395974a8ae1feee5970122cd80d9f2cac847d52ff2b0c9a9fc3f2e7cca4fa2c5`  
		Last Modified: Tue, 08 Aug 2023 14:32:23 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65704619447f5d44c3f5259c6dd3da476059c0486a4aa4c7cf03843ec366006c`  
		Last Modified: Tue, 08 Aug 2023 14:33:10 GMT  
		Size: 407.8 MB (407775915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaa0cbb0840ec7759be1f319f30044f8b0e6b9ef9c4dcaabfa1b44454f374bf`  
		Last Modified: Tue, 08 Aug 2023 14:32:21 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01410cd0efc9a31d431eb4b2373dbcffa464f47eddf28f1946e8af45d0b4e3`  
		Last Modified: Tue, 08 Aug 2023 14:32:21 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c16c3cf82e5cd80a82cccc186b273643b701a5f23a12e23a727aaaf2b64a6d7`  
		Last Modified: Tue, 08 Aug 2023 14:32:21 GMT  
		Size: 185.9 KB (185898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e47af996750ff2a127b115b78a14f10c9080dd4d8abfd2f4d238aa75a74c6b8`  
		Last Modified: Tue, 08 Aug 2023 14:32:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e186cbc76351e2824d13fea97c48cbcb721004c01d333521b4f67383c00629`  
		Last Modified: Tue, 08 Aug 2023 14:32:21 GMT  
		Size: 109.2 KB (109243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.9.1`

```console
$ docker pull elasticsearch@sha256:767f3d4fbc45c757bf167ac4dbafd05a6502bc2521a604d3a25c26b246fb36b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.9.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f553b6c7f05abc35e8997f375644857b868dcc4370fe42fdd3f2a074bc9c075c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.4 MB (649381965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a61551b302003765c449a9530f5d07713b04182c8f8f3dccd35870303935add`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 10 Aug 2023 05:08:42 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 10 Aug 2023 05:08:43 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 10 Aug 2023 05:08:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Aug 2023 05:08:43 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 10 Aug 2023 05:09:05 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 10 Aug 2023 05:09:05 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 10 Aug 2023 05:09:05 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Aug 2023 05:09:05 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 10 Aug 2023 05:09:06 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 10 Aug 2023 05:09:06 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 10 Aug 2023 05:09:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 10 Aug 2023 05:09:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 10 Aug 2023 05:09:09 GMT
LABEL org.label-schema.build-date=2023-08-10T05:02:32.517455352Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=a813d015ef1826148d9d389bd1c0d781c6e349f0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.9.1 org.opencontainers.image.created=2023-08-10T05:02:32.517455352Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=a813d015ef1826148d9d389bd1c0d781c6e349f0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.1
# Thu, 10 Aug 2023 05:09:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 10 Aug 2023 05:09:09 GMT
CMD ["eswrapper"]
# Thu, 10 Aug 2023 05:09:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0e136a4bb2ac2045dacc9775e92adb15a9189da6e413de8f09f9f04096e6a2`  
		Last Modified: Tue, 22 Aug 2023 03:00:31 GMT  
		Size: 7.5 MB (7509952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7152b76747e43beb8edde587195c26f6e8d67ebd919f59ab1cbf98139147835b`  
		Last Modified: Tue, 22 Aug 2023 03:00:22 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8013ece6ebe8a883c60f71fcef310e4fd6d866219fec353e345923a2ce90751`  
		Last Modified: Tue, 22 Aug 2023 03:01:12 GMT  
		Size: 613.0 MB (612974218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849477e03c16efeae31da371596d63c919e0ef03689bcc3e0a88a061af37365c`  
		Last Modified: Tue, 22 Aug 2023 03:00:21 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d088e0be5d68b28f2a15a56188eb5ba4cffe0b81a9f92ead66b9047d2214d6dd`  
		Last Modified: Tue, 22 Aug 2023 03:00:16 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fade93157f3c6af355865d8842d7ed9f75595cc0c487f1933efd2b79b8738f`  
		Last Modified: Tue, 22 Aug 2023 03:00:17 GMT  
		Size: 191.9 KB (191860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7486b389bb9cfb1071683b48eef58fe462fd7a8dd5158788c0a61ac568d78e29`  
		Last Modified: Tue, 22 Aug 2023 03:00:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c48a6f0a873607ebf277a4cbcc2b91657d63ce74759d12ef2769f92a666e935`  
		Last Modified: Tue, 22 Aug 2023 03:00:17 GMT  
		Size: 109.2 KB (109240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.9.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:88073c594d4991fb73bf663c40d8b6b5e1604655a6d5775408d97a500d6b66de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.7 MB (442650837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180d266daa33362dde05444f275d8803a7b9dc43d27ae57dd55dc3f574ace1a4`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 10 Aug 2023 05:09:49 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 10 Aug 2023 05:09:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 10 Aug 2023 05:09:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Aug 2023 05:09:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 10 Aug 2023 05:09:55 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 10 Aug 2023 05:09:56 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 10 Aug 2023 05:09:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Aug 2023 05:09:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 10 Aug 2023 05:09:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 10 Aug 2023 05:09:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 10 Aug 2023 05:09:58 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 10 Aug 2023 05:09:58 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 10 Aug 2023 05:09:58 GMT
LABEL org.label-schema.build-date=2023-08-10T05:02:32.517455352Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=a813d015ef1826148d9d389bd1c0d781c6e349f0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.9.1 org.opencontainers.image.created=2023-08-10T05:02:32.517455352Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=a813d015ef1826148d9d389bd1c0d781c6e349f0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.1
# Thu, 10 Aug 2023 05:09:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 10 Aug 2023 05:09:58 GMT
CMD ["eswrapper"]
# Thu, 10 Aug 2023 05:09:58 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a7aa74f5917a2e171f248ab4ba4a9b17415615d12c4beaa4df0b761ad7a305`  
		Last Modified: Wed, 23 Aug 2023 23:47:12 GMT  
		Size: 7.3 MB (7331589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e25ec58a64fb7ac615c80677c9dd5c13adb868ed210607266248d2f4bdf434`  
		Last Modified: Wed, 23 Aug 2023 23:47:11 GMT  
		Size: 4.3 KB (4350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70c394c55d6956f8da7990a54d48ed778c942bdc6c52bfe631a02abbe79766`  
		Last Modified: Wed, 23 Aug 2023 23:47:33 GMT  
		Size: 407.8 MB (407807926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c88cf13a97892a263710d369d78bf795d90ae66f738406ea26b5d7c40eeda`  
		Last Modified: Wed, 23 Aug 2023 23:47:08 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d18493ceb72af7b5f735023b09cb0e55d05ec1e9f7cf40be8c29844a0eb779`  
		Last Modified: Wed, 23 Aug 2023 23:47:09 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e25530749bd39b9b0937b4243abc778961bce94456f7dcb0bfa9ec3bb35f172`  
		Last Modified: Wed, 23 Aug 2023 23:47:09 GMT  
		Size: 185.9 KB (185892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e749de4d29cc57bda3ded4bf4d4b55dde96063f42273f81059d85740d68988a5`  
		Last Modified: Wed, 23 Aug 2023 23:47:08 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ebbc569dcfd1b7fdeea7c7f0e30dd801227e8e932ed9a9368aff3565faefef`  
		Last Modified: Wed, 23 Aug 2023 23:47:10 GMT  
		Size: 109.2 KB (109236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
