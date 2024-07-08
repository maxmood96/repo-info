<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.22`](#logstash71722)
-	[`logstash:8.14.2`](#logstash8142)

## `logstash:7.17.22`

```console
$ docker pull logstash@sha256:e2a62b2b7d5cd74482d7124e7caf5d31f80ecee773c34a0a09ad0f11916ef6b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.22` - linux; amd64

```console
$ docker pull logstash@sha256:acd7982d8a7ee5532ac875d5e5f7a1db3817c49cb3f054cf76e76a067e8660b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.1 MB (445138755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e0e917edf67f87137c9d46e99999bf610dba804600a0120458751c926b6a08`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 13:25:43 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.22-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.22 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Jun 2024 13:25:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Jun 2024 13:25:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Jun 2024 13:25:43 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
USER 1000
# Thu, 13 Jun 2024 13:25:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Jun 2024 13:25:43 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.22 org.opencontainers.image.version=7.17.22 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-02T09:01:17+00:00 org.opencontainers.image.created=2024-05-02T09:01:17+00:00
# Thu, 13 Jun 2024 13:25:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02ca5a788155d175547e47b51c81c0ddd48772e71a60669f6eb2f81a45b510`  
		Last Modified: Thu, 13 Jun 2024 18:29:52 GMT  
		Size: 48.4 MB (48385218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c305ffdb063b270b41b6732557603a4ea278c4e19dc760ff8cac035f97b648`  
		Last Modified: Thu, 13 Jun 2024 18:29:52 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ea97f47c1c959b312140fbe8563f86dc2d15fc5e3cf9c014950cc868869c77`  
		Last Modified: Thu, 13 Jun 2024 18:29:57 GMT  
		Size: 367.3 MB (367333970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b3c0e3b251f71e28214ce5f93cb041c040971f31555e920a864093ff6f7f0`  
		Last Modified: Thu, 13 Jun 2024 18:29:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73edba60e9c1be93de7b578cf145b8f2ce55d642acdafa568a428c72b8ca68ba`  
		Last Modified: Thu, 13 Jun 2024 18:29:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fab39005dcd260a99b021b6bd7b437e646198cef87d572774210066a1eb1d4`  
		Last Modified: Thu, 13 Jun 2024 18:29:53 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7ffbc8dbb9724a2df62bdb375a0c6ba0f0c4307d5186992e911fc1bb402bce`  
		Last Modified: Thu, 13 Jun 2024 18:29:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd02bacd0050203c0ae060cbe85ef0755832e37bbfe0d109e2a1b1353f033b8`  
		Last Modified: Thu, 13 Jun 2024 18:29:54 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1dbd9cd5a71905ef2f5187ce2f421c55b2eb0704f9074105447f49894aadaf`  
		Last Modified: Thu, 13 Jun 2024 18:29:54 GMT  
		Size: 1.9 MB (1902748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51df365fb00bd990c2a9c18e5fedd4b91b24ddf2d84f10a8a2bb9a213932761`  
		Last Modified: Thu, 13 Jun 2024 18:29:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b3c7fa5ba571c3a06ce46da48809bf9fb2b3ed608d7848e3661f63359c1a25`  
		Last Modified: Thu, 13 Jun 2024 18:29:54 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.22` - unknown; unknown

```console
$ docker pull logstash@sha256:72d4ad1d4e32775a94c686fd31a2219833c6855875549d5f105af0dd62dab8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5968363a39dafea05bfeeb98bb53de5cf33c784a41889820a018dfbff85d6`

```dockerfile
```

-	Layers:
	-	`sha256:987270fa48557ba8f2c37c4ef0af669572e32f586045b023f123b9d1559b65f0`  
		Last Modified: Thu, 13 Jun 2024 18:29:52 GMT  
		Size: 3.0 MB (2979398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8f28feb17068d1d0e7e754ae65d8969d09d74ccc029afc24bd6a855819cf85`  
		Last Modified: Thu, 13 Jun 2024 18:29:51 GMT  
		Size: 32.1 KB (32062 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.22` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:9ddb5c257a051afb0c607e3689b19e9ab2d09e74bbbbb82a19817990a920eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.5 MB (429495765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebdfc70b0b58dc11fcde6db1ab41aa6356912d7871be8cea3a25356da25a340`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 13:25:43 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.22-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.22 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Jun 2024 13:25:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Jun 2024 13:25:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Jun 2024 13:25:43 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
USER 1000
# Thu, 13 Jun 2024 13:25:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Jun 2024 13:25:43 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.22 org.opencontainers.image.version=7.17.22 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-02T09:01:17+00:00 org.opencontainers.image.created=2024-05-02T09:01:17+00:00
# Thu, 13 Jun 2024 13:25:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18534421e48eab0a6b1e9a2827be11f329c0c6b5d8aef5c2c5f5e4a241b68064`  
		Last Modified: Wed, 05 Jun 2024 16:09:33 GMT  
		Size: 37.6 MB (37566200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ca6db970e1e2f7ecb9606034525b99847e65fbb4e26e77c9e92071c598f59`  
		Last Modified: Wed, 05 Jun 2024 16:09:32 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b198873d1bd34de60d1e57cb52a22e67127ef5b7f2f4f678ff73a55b4c23387`  
		Last Modified: Fri, 14 Jun 2024 03:54:26 GMT  
		Size: 364.0 MB (364047524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec50aaaca7e720647ba1e11e593e1c8c1bf3ad69f54ccb55b3d67488e9247b`  
		Last Modified: Fri, 14 Jun 2024 03:54:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b659d2c0f21e26156bd54d39c96a6c8529ab6f352211fa8b586572e7d9640`  
		Last Modified: Fri, 14 Jun 2024 03:54:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239da3b48ad0e4dc0eab1eb54b856c7d0c8c1dc65658724e7ad9d5fb92ba0d5c`  
		Last Modified: Fri, 14 Jun 2024 03:54:19 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9afbea222cf0952a3ba9d19ff1f0d1c2944615da4b6886d050570d8d1cda8da`  
		Last Modified: Fri, 14 Jun 2024 03:54:20 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e8159a60d87cf809111a987f217da5cada835cf08d13679952c4b58667961`  
		Last Modified: Fri, 14 Jun 2024 03:54:20 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee956de228d14c1ea0e5bb27fd07ebc1ecd49768117cb879111e40adb44713c9`  
		Last Modified: Fri, 14 Jun 2024 03:54:20 GMT  
		Size: 1.9 MB (1902755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60153a1d349f65c2accb0847360f580f61edc789df0aee5acd4b0ee833fe42`  
		Last Modified: Fri, 14 Jun 2024 03:54:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b79263c7605f08ca8d1cd9db7db5001a005b50c0abc7a0b25cc47ba092ae37c`  
		Last Modified: Fri, 14 Jun 2024 03:54:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.22` - unknown; unknown

```console
$ docker pull logstash@sha256:a04acf66ab71f28b29aa97a399ba6e3d7c63c459ddf0f156e33c30d867d4fec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62281bd5b146c9ffbf68e0bc1954b9cca4e10fed00ee8937a9cc80afb6a5f9eb`

```dockerfile
```

-	Layers:
	-	`sha256:c7b5c49f55d0fe22108948321cacfed25f187c2d0de646b90e7f64aba1c5d14a`  
		Last Modified: Fri, 14 Jun 2024 03:54:19 GMT  
		Size: 3.0 MB (2979633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7927bf5b0da63b996ada1106a848c3c9823b77e3ab1168f18e7e855e3f899798`  
		Last Modified: Fri, 14 Jun 2024 03:54:19 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.14.2`

```console
$ docker pull logstash@sha256:ef9981c4182a63a9205b3bbd46de08c8437857ff762c0340a86c9a6af24e23af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.14.2` - linux; amd64

```console
$ docker pull logstash@sha256:cc57f9eb2e785f5b3dc95b2ed77d7ee0a7ecc35b9c58edf54101ad413be64bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487860888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3c44fc32a7882777a9cce09d0b5b1195008155dee2b51534742548d31a91db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 07:59:16 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
WORKDIR /usr/share/logstash
# Thu, 04 Jul 2024 07:59:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 04 Jul 2024 07:59:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 07:59:16 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 04 Jul 2024 07:59:16 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
USER 1000
# Thu, 04 Jul 2024 07:59:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 04 Jul 2024 07:59:16 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.2 org.opencontainers.image.version=8.14.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-06-27T16:49:00+00:00 org.opencontainers.image.created=2024-06-27T16:49:00+00:00
# Thu, 04 Jul 2024 07:59:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d865ad495063c3155ac3c340490e8dd8ee3722263ec2e6c6fbcde8047c2efff3`  
		Last Modified: Mon, 08 Jul 2024 17:59:41 GMT  
		Size: 48.7 MB (48730282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f3b3bdc37eb2ead66fdb672435f1e5f864f7bc7603b7e056d3d9b390bde731`  
		Last Modified: Mon, 08 Jul 2024 17:59:40 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e145865c6dc6fa61ccd056a4dbc34f5bf840024028c29bbec539fd3b4120d72`  
		Last Modified: Mon, 08 Jul 2024 17:59:45 GMT  
		Size: 406.0 MB (406019328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff340c38d452e29150936733c5dfc5ec810227ddb9c3098d3101ef570b6506`  
		Last Modified: Mon, 08 Jul 2024 17:59:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ca6e497cfeaa3cac600b173028d7e1e2efe01d3e11e247d3c579a2db234b8a`  
		Last Modified: Mon, 08 Jul 2024 17:59:41 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbd15830f99069bb05cd720846b2eb3c98e0ea030dfe650a0e8a5a5b15cae40`  
		Last Modified: Mon, 08 Jul 2024 17:59:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ca150e410495287ecc736979f409379f5a2c4edeba88329d61e3f66d4bc3f`  
		Last Modified: Mon, 08 Jul 2024 17:59:42 GMT  
		Size: 3.7 MB (3690799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20006cf748cdf88d8d987dc62a7eb08f08218f43ed0fd5a88ffd95fce98d3fc1`  
		Last Modified: Mon, 08 Jul 2024 17:59:42 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81131a2ee5356cd83f85039b129af54156297895c3f4273fca1fdc554a1350be`  
		Last Modified: Mon, 08 Jul 2024 17:59:43 GMT  
		Size: 1.9 MB (1902234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc92ad4840fb1368bc232e2476f9594468eb15c51811a574175bb52281fc39b5`  
		Last Modified: Mon, 08 Jul 2024 17:59:43 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.2` - unknown; unknown

```console
$ docker pull logstash@sha256:151a6dbe6d081dd2709fa333aab8be4f0131de9c31c4ddb894536d5b3e6ecbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e368f9ef1b47a9cd5e3659ee18c060360cc784d13f049cd3beaffc4a22120af`

```dockerfile
```

-	Layers:
	-	`sha256:d45f96e431f1fb94eff31575c1684a191fad51e0a9a7679b2010c5c46a22efb6`  
		Last Modified: Mon, 08 Jul 2024 17:59:40 GMT  
		Size: 3.1 MB (3137264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad024e820c4461b5cdd0280794116e8512827defd40ae61dd25152a76b8b07a`  
		Last Modified: Mon, 08 Jul 2024 17:59:41 GMT  
		Size: 34.1 KB (34127 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.14.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f20730af7d5c1a5eee97fd173e0c4aefbd54d2af6cb480036013e3753cb83f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.1 MB (474068275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec01ab0085f3667f61199bb596dd906eda144200ab094ada5f6a0f06638df1e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 07:59:16 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
WORKDIR /usr/share/logstash
# Thu, 04 Jul 2024 07:59:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 04 Jul 2024 07:59:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 07:59:16 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 04 Jul 2024 07:59:16 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
USER 1000
# Thu, 04 Jul 2024 07:59:16 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 04 Jul 2024 07:59:16 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.2 org.opencontainers.image.version=8.14.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-06-27T16:49:00+00:00 org.opencontainers.image.created=2024-06-27T16:49:00+00:00
# Thu, 04 Jul 2024 07:59:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22016c99f4b1eaa60a0dbf418d06655ada9612082dcdd79893edc4df3ef6932a`  
		Last Modified: Mon, 08 Jul 2024 18:48:00 GMT  
		Size: 37.8 MB (37806478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81526eaa62eda1ab282198e2d9de62fb2795dd9974d9d2715d59cf7c8ddf01f`  
		Last Modified: Mon, 08 Jul 2024 18:47:59 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd509a5f7cf708406811d7529dc3293d8b842ac889d30d406ce9e747f6721cc`  
		Last Modified: Mon, 08 Jul 2024 18:48:08 GMT  
		Size: 404.8 MB (404802745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f65703be55fae711739bc16ff50559c50b41a2d5d3cb7b3b1a2b5a940829ca3`  
		Last Modified: Mon, 08 Jul 2024 18:47:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b612b855ecef5cf0d7a2b8e809cc46863e7805f7f248b9adf02c44f1dfb4fe`  
		Last Modified: Mon, 08 Jul 2024 18:48:00 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0c793c4fb93441b5858163609ed68bd6d299f62564de65995f1ec9235d9de`  
		Last Modified: Mon, 08 Jul 2024 18:48:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cc142bb1f3a99756e0034282ad059223206859a83e2263318de6d63a0ffa3e`  
		Last Modified: Mon, 08 Jul 2024 18:48:02 GMT  
		Size: 3.7 MB (3690794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f262a568e5d4df1fb6cfcbf22c0d5addd221cd6a2a2133c38392b1619414ba5`  
		Last Modified: Mon, 08 Jul 2024 18:48:01 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccb9a940807dc8fa5a4ce92bcd2e839ab927fbb6c22c9a98413f22094793cbf`  
		Last Modified: Mon, 08 Jul 2024 18:48:02 GMT  
		Size: 1.8 MB (1787557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f122170b2242dcb9694b0ab261a1f1193ec542a9c6cc67e86d7b082933432b`  
		Last Modified: Mon, 08 Jul 2024 18:48:02 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.2` - unknown; unknown

```console
$ docker pull logstash@sha256:879a9365d3169221c634d7657b6dc0cd024de10d9199b3b653860cf83b5d6f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbf10ac54d5570febd97b21dc7cb25ca4a30a294078ee03ba730df2d7b9a453`

```dockerfile
```

-	Layers:
	-	`sha256:f85ef4dba9c68633979dc065e9555bdee9fedb7435bd5b07fb9921f0a880e3bf`  
		Last Modified: Mon, 08 Jul 2024 18:47:59 GMT  
		Size: 3.1 MB (3137499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55c25295f8219ee3e7cccfb55573994c192f97dc6fe47253c40f5472fe760202`  
		Last Modified: Mon, 08 Jul 2024 18:47:59 GMT  
		Size: 34.4 KB (34391 bytes)  
		MIME: application/vnd.in-toto+json
