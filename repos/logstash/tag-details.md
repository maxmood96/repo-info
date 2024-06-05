<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.21`](#logstash71721)
-	[`logstash:8.14.0`](#logstash8140)

## `logstash:7.17.21`

```console
$ docker pull logstash@sha256:9ec61145e5ab06af9ac9fcf3d9eb438912c72d22bf06f03f52e5ce6b9c9346df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.21` - linux; amd64

```console
$ docker pull logstash@sha256:4b9f4948bcc76efb632c0dcc057a00823d72f88d7f0f99b49f2a203d4b6faac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.0 MB (444979767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ef8065975401a5f32e2e561f2c327bd0094b92bcf7db001c86dd39bd44d4fa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cba70f324522678988bcb1f0d546469f7c4a7173b759f657071aa32670a8957`  
		Last Modified: Wed, 05 Jun 2024 02:20:51 GMT  
		Size: 48.2 MB (48226494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec42bb6466ee8c7e6aed53169737ab94a39a0bed4cb76b22d1d61fd876c6771`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80afdc55cdcd137a2efa41de9e2f4aa4f2686d7a60dafe91f705e6a37623cc2`  
		Last Modified: Wed, 05 Jun 2024 02:20:55 GMT  
		Size: 367.3 MB (367333713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c1060cc1577a519741f50cbf339da73742e0a90ecdeaeea5d067758296edbb`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911313e6a40712ca5a2508a698d1d30cd4ffc5dd3c41931985f6f171d8f51071`  
		Last Modified: Wed, 05 Jun 2024 02:20:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf863567fb05da126fb42f0353b2742229b053d4a729af3fecf3587255ee98b`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf0392f4ba0d47d2bbff044ea2ae0ee404deca48f1d31360de6e93d9a46733`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd44c39d3df2e6b2d4c87ffd19725892e5b677fd2e8dad5aa7e50a5583ea7a7`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e234b0088f10c914e7675c6b79f8b5946ed9eb4f9c807da765283104b164d15`  
		Last Modified: Wed, 05 Jun 2024 02:20:52 GMT  
		Size: 1.9 MB (1902745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba34c737e8b3bfea312e2f1433d01fa6ed2c1eae51a7106a88cf7561227f2a`  
		Last Modified: Wed, 05 Jun 2024 02:20:53 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f69d82d74007b90acc9d3e3cafa6f97387341be0f7f57e7eb8263a18b20f040`  
		Last Modified: Wed, 05 Jun 2024 02:20:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:a819e5be1382a3ea273146366f9e1227677e8af902e140a8af8b22555cb5aa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d01b66270560989a4acba7d7de47eb8b525fc6916aa1871040b0d9083d71187`

```dockerfile
```

-	Layers:
	-	`sha256:1dab30abb4ac639a5dbf858c6f58abf7be4e6d97b43ea51de202a3ff59d27002`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 3.0 MB (2979398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4769e0138cd16306efacaedd4dafd0658efc6f30aa5acc84d290748ecf6fd061`  
		Last Modified: Wed, 05 Jun 2024 02:20:50 GMT  
		Size: 32.0 KB (32013 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.21` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c7b7c326d81d198d95519a974968a9c74537c7338fe27b1554b611bffd69a75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.5 MB (429495637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2946b95337bf5a84d953fc81db3abb3b1f6c75a2f575e426f6e24c4d6d16da1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
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
	-	`sha256:2989e0ee719629b5d57ef645b05743ed1e7c7a75b8c87dcc243b432e297b135f`  
		Last Modified: Wed, 05 Jun 2024 16:09:40 GMT  
		Size: 364.0 MB (364047393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c41eeffc83df576f57e5b0e3944ce95ee8f1b510a1b4720f9543e5655acd77`  
		Last Modified: Wed, 05 Jun 2024 16:09:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccb16b17376f2f11f6738ecb50e96174d089216bb973469e174a3133933ce3f`  
		Last Modified: Wed, 05 Jun 2024 16:09:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec1349bce30064c23384ce28775d814c4178cb8c8a86cc5c377eae00a583890`  
		Last Modified: Wed, 05 Jun 2024 16:09:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7450968c656dc008154923adefa9c1eceacb2acf168809d52f8a2fd1a87415`  
		Last Modified: Wed, 05 Jun 2024 16:09:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32554d711267946ea3ef7c5314229633c26b1c0b3c94680c0f34a021cdd1edd1`  
		Last Modified: Wed, 05 Jun 2024 16:09:34 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b091057b8cb73cfc847f0e402efcb959e64fd988e798641728a73e14818e6fb7`  
		Last Modified: Wed, 05 Jun 2024 16:09:36 GMT  
		Size: 1.9 MB (1902756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c670432c6500cea10dfaf132b7bec232d7112b99ee7696f9f2df61263b11d75`  
		Last Modified: Wed, 05 Jun 2024 16:09:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fcbb6baf86df767276146167802f7422d238165cac5302648a278d7c63ce51`  
		Last Modified: Wed, 05 Jun 2024 16:09:35 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:11d23b7c1a1acafcf1d56f6422421958b379693a48ae308d377803bf0f11bee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef30d7d0089b66c513d253cf84ea81b3bd503b196584d1daefda1fccc0e863e4`

```dockerfile
```

-	Layers:
	-	`sha256:613c1e8e82637139e6b29157561c47221d3856c6198fbcb15d85081802d8c264`  
		Last Modified: Wed, 05 Jun 2024 16:09:32 GMT  
		Size: 3.0 MB (2979633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c363d02779bb1c96ee59d6ef001837531a779b70cffeaa1a3da23c6837a36189`  
		Last Modified: Wed, 05 Jun 2024 16:09:32 GMT  
		Size: 32.3 KB (32278 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.14.0`

```console
$ docker pull logstash@sha256:3d014570de8323bad2f871a5c14c0925ba7ed9458ee4d0d5de7e64e886a16f46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.14.0` - linux; amd64

```console
$ docker pull logstash@sha256:8329818fa41dde1eb076d92d62e7f82875fd8d8abd53d495750dd14dfa1f3bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (487022417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3707553fe4e02c09a936853c28bcac4c253cbe93fdee2978a285ab9a6e07d3fb`
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
# Wed, 05 Jun 2024 11:38:24 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Jun 2024 11:38:24 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Jun 2024 11:38:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 11:38:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 11:38:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
USER 1000
# Wed, 05 Jun 2024 11:38:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Jun 2024 11:38:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.0 org.opencontainers.image.version=8.14.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-31T10:59:17+00:00 org.opencontainers.image.created=2024-05-31T10:59:17+00:00
# Wed, 05 Jun 2024 11:38:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2269310f745110c24c982580fcf02cb98255935f9295394ab38ff9e3601a4411`  
		Last Modified: Wed, 05 Jun 2024 18:55:56 GMT  
		Size: 48.2 MB (48239805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e79a2709800a160efa7ee57036a9873bba968f2c5792c79685c561b11e3d45b`  
		Last Modified: Wed, 05 Jun 2024 18:55:55 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825afab5e3643bd5f2aba2fd72082371e1ccef7a1995391f3fa901a17f1ed2e4`  
		Last Modified: Wed, 05 Jun 2024 18:56:00 GMT  
		Size: 405.7 MB (405671372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac7492fa0a14410b5ef8d7933f96a347016e4734aa1782432fc8fc59b17e9a`  
		Last Modified: Wed, 05 Jun 2024 18:55:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f5591315265a043dc02c9c6d107b51a454f206f2e821b472c86b3005de4213`  
		Last Modified: Wed, 05 Jun 2024 18:55:56 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5062f45a9e57839875f7967395d3b2802d35949c6e19ef6ac4eb6a3aa4d00f9a`  
		Last Modified: Wed, 05 Jun 2024 18:55:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85529ce4e01c63a9f0b05b5f9ff70642d4138ff9f00bae56600366e2c4ab5c58`  
		Last Modified: Wed, 05 Jun 2024 18:55:57 GMT  
		Size: 3.7 MB (3690007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7168da48b7b223d16786fd0d2d25fa57f4da561776fbf765b6c3843805979c6`  
		Last Modified: Wed, 05 Jun 2024 18:55:57 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2f166950216e032dbea060f40700a048768f4d7a66bc3dc5972564eb835928`  
		Last Modified: Wed, 05 Jun 2024 18:55:57 GMT  
		Size: 1.9 MB (1902295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ea74013009ad26adf98624533f7e4b6c665d03ff43668df519aa6c73b63e84`  
		Last Modified: Wed, 05 Jun 2024 18:55:58 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebd18f3c652ec818e53bc26076abffa09859896d648afb3ef92d5098b38d96`  
		Last Modified: Wed, 05 Jun 2024 18:55:58 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.0` - unknown; unknown

```console
$ docker pull logstash@sha256:f8c12bede71e69e9a533f95df144e936db2c893209b0e793336fbc906b9e46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bd56c42681de948daf039fe44c2a1da1740e8483128558c69f518d8705af06`

```dockerfile
```

-	Layers:
	-	`sha256:fc2ca83fffd6441eb186a84f8a07443e980cb092fc9c314cddfce50413d1c600`  
		Last Modified: Wed, 05 Jun 2024 18:55:55 GMT  
		Size: 3.1 MB (3135214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7e90ab1e3831f98b5954f2959fe93e4f1c95d6607bb4d9f25994c914e79afa`  
		Last Modified: Wed, 05 Jun 2024 18:55:55 GMT  
		Size: 34.1 KB (34079 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.14.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:96f9f42cd5f0ae444b81ff610858594d61c8e96df9b9eb4b1ae7d6688a48009e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.5 MB (473490205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1f948f3d1f573e85a4ea7ccfff057af0c00f06845c829b323091b443d858b5`
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
# Wed, 05 Jun 2024 11:38:24 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.14.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.14.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
WORKDIR /usr/share/logstash
# Wed, 05 Jun 2024 11:38:24 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Jun 2024 11:38:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 11:38:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 11:38:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
USER 1000
# Wed, 05 Jun 2024 11:38:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 05 Jun 2024 11:38:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.14.0 org.opencontainers.image.version=8.14.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-05-31T10:59:17+00:00 org.opencontainers.image.created=2024-05-31T10:59:17+00:00
# Wed, 05 Jun 2024 11:38:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fadc34356d1dfeecbbe5fe1d94d4a07c65b12b1e1a7fc869682607d47c18ff`  
		Last Modified: Wed, 05 Jun 2024 16:07:57 GMT  
		Size: 37.6 MB (37573454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaad5940dd746a89be1e653af42ed08ac0e430cbf635510e652644a0730183d`  
		Last Modified: Wed, 05 Jun 2024 16:07:55 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143071b6ce88808074d364c9c000d4d383cb4aec20dc63acd9c688a07a75190`  
		Last Modified: Wed, 05 Jun 2024 19:17:16 GMT  
		Size: 404.5 MB (404458505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7e64fa29e0ef8f4a9f7f997eded854c7e395dd51d9d17ebd6682a48c270a2`  
		Last Modified: Wed, 05 Jun 2024 19:17:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f8113bcb4f05272d5d7c5b735e03ddb15d2ab02198ddb703ade9043ee3dc83`  
		Last Modified: Wed, 05 Jun 2024 19:17:06 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04592aeb5e77de0c73f614aed81913ad786801b9e2bf69cdaee7c0f0f7779c60`  
		Last Modified: Wed, 05 Jun 2024 19:17:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd193dc83a7be0c20e87cdba4c3e5274a862c7af917b24edcc0c097ccc603cc`  
		Last Modified: Wed, 05 Jun 2024 19:17:08 GMT  
		Size: 3.7 MB (3690015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94221aa180822f74c999d5047d3468e7323f8955fc0af4ae5091cde9721dc00`  
		Last Modified: Wed, 05 Jun 2024 19:17:08 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ceab1bd2600fdb7f333237c8b78e6313fea0a8173cbbaca5ba2f109b915853`  
		Last Modified: Wed, 05 Jun 2024 19:17:08 GMT  
		Size: 1.8 MB (1786833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f10597065213c32452b23f322c3251c21c9620803432da7db652c93783852f`  
		Last Modified: Wed, 05 Jun 2024 19:17:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4323c66b07cd51976a378b14b1f07bd0fce42ab6c1d11560801be8c3030693c2`  
		Last Modified: Wed, 05 Jun 2024 19:17:09 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.14.0` - unknown; unknown

```console
$ docker pull logstash@sha256:846ea69512797254a75b1941d35adcb26e1e73a51bf49f9971b6cd535d5b5556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c377008faa6534e8352993768d7eba5debea543ed6dbd3346f7e26dfda0c8`

```dockerfile
```

-	Layers:
	-	`sha256:15ec2cec11772d2913b8409455ce71feb077b65eda9524e4ba78b7cb9848e3eb`  
		Last Modified: Wed, 05 Jun 2024 19:17:06 GMT  
		Size: 3.1 MB (3135449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec575e33717e0451ea1411164da31972a1838b8c1e1484189a9572e1ecb38584`  
		Last Modified: Wed, 05 Jun 2024 19:17:06 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
