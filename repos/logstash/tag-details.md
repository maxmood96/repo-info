<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.10`](#logstash81910)
-	[`logstash:9.1.10`](#logstash9110)
-	[`logstash:9.2.4`](#logstash924)

## `logstash:8.19.10`

```console
$ docker pull logstash@sha256:555e8dadf9ad013dfd2fdd7e71d7b478074a80edd86822c2fa079b84883847e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.10` - linux; amd64

```console
$ docker pull logstash@sha256:7b953ad28867b5ba54523ac4abc25b07970b3d6beb9c2fdd737452335c542af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521445846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41608b84701fc16a2041abb8c6c4693f8ae45db2c1fd20c717174e369805bbc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:23 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 15 Jan 2026 22:31:23 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
WORKDIR /usr/share/logstash
# Thu, 15 Jan 2026 22:32:04 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:32:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:32:04 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:32:04 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
USER 1000
# Thu, 15 Jan 2026 22:32:05 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 15 Jan 2026 22:32:05 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Thu, 15 Jan 2026 22:32:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ff9c60e3b0c5caf9876f75b0e7310b18887ab073d5b6c254b6e51484e3765`  
		Last Modified: Thu, 15 Jan 2026 22:33:02 GMT  
		Size: 49.8 MB (49811886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a75ed7773cbf70823ab6f16214f069c73a448c56e85b629af42ccca888f332e`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116f452c2b93845c457613af44b5bec51a6716e842c2c8344d60a6cea88da1d`  
		Last Modified: Thu, 15 Jan 2026 22:32:49 GMT  
		Size: 441.6 MB (441640221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e55bbed2aef1fa6dc69dee5568808f3cc413ab6bd97be2783c0142469d0b0`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0740e857072ed647e436c435e397b2b1325d2ece9b013b3c33d804d78cb4e`  
		Last Modified: Thu, 15 Jan 2026 22:32:57 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaee70b78cf97de53ab844f5847ecf41806aea1795fa4c32caedd0205c6c233`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20401eda2953ef0b0ead602de4b6255b5cb4d43dd0242c34099ea4dca2d4d9ee`  
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a1de0bed25db992ea94b99e45fb796bf4d4a0ea21c7a71446f2ead25d42dd`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be2883b856b67a053014231e409532dc327b15369bead35116ac7dad522e23b`  
		Last Modified: Thu, 15 Jan 2026 22:32:43 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cac1d1d0771b591c0e22f728b3c3b6372e540e23a818bbb3ab6a184a2be844`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417ef8ab86e54a79dec82445546991485365e8ea978094c1728767e4e7ffc2b2`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:23be666d31cd06d5b49345ed65138200dc2d1149ac89ae387ce9a543cf356b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20e2c5bffc3cf590f6a8b7f8c0ef303bd67864904b8d34e4bb6759db54385c8`

```dockerfile
```

-	Layers:
	-	`sha256:f054f1846362af1924cf04b0fc62923d8c6c168aa71248b4f28a15a6b38d532d`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 3.7 MB (3651746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf40b739af4bd5f782971edd51cd904f0028d40ea7acffb0dea322561fc3f9ec`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:dc292a7be44ad6b4403195e37d5b0beaecb19ea81ede8f9ff73b8d84e8d34db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 MB (521121894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c13ffd3c2cdcee2ea46e59d39e95457336163d0cfb996bbd2c0c1c9fe5941c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:33:28 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 15 Jan 2026 22:33:28 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
WORKDIR /usr/share/logstash
# Thu, 15 Jan 2026 22:34:11 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:34:11 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:34:11 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
USER 1000
# Thu, 15 Jan 2026 22:34:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 15 Jan 2026 22:34:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Thu, 15 Jan 2026 22:34:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78c15fc0b37d907e3bb93005da18e1c66d8c7f5ce81ec7adc4cbf1f453923e`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
		Size: 52.1 MB (52065432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7bcac2f41a34a4e6da98b8f3af1305316671dd8dfa5528cc81a608686d65a`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9846089205883a9e4c376f9b125e71f7eeee2ef25910211f37152150b0a652`  
		Last Modified: Thu, 15 Jan 2026 22:35:00 GMT  
		Size: 439.9 MB (439924907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0b366a472f185bd2a11956165160bb3f460a2c3e440087b1c6837170cd4260`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14936df0f6a23e4429128c2a1b1432d1ad70b48b53fb617d2c4e92374f3523b`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d74cb030ea7e313e8cd7a0ed66c22c26370442c070dde06d5b7a9a526fc008`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d699a4f40f9e4169b2941e11a512305fe497924f849469ec9f6f074e853eba`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59793887602ab2816f376a5174af463b8192bad06c347f60f7b53718896bf2`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec084120a0a5d3867ad36240eed627b971ebab6cbe9ec89caf2ba49cf02e844e`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51d0d79ab269e9945110621d4da0c32fea5cb60a68d0940ff2991224f1db33`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b22e41bf5db741511ee69eeea3bf419b6a1c8a7467ed8a1e47ec6e4db89f5d`  
		Last Modified: Thu, 15 Jan 2026 22:35:04 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:8872adf5a502a162012c618e93c48a159f4d74fe380a5dd6dcdfc69ac3e18c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3245f4bbea9e8bb1c09b8675d6ba84d3433d6e39b2a17f4bf78340b6ef44d91c`

```dockerfile
```

-	Layers:
	-	`sha256:e492d2475306c543c8d15ad77c572cf19b4ba7c65b98649256f09398500f74e7`  
		Last Modified: Fri, 16 Jan 2026 01:54:28 GMT  
		Size: 3.7 MB (3652171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9636c18161852dc6094863744875e4fa85977c8d6767aea42d4b81755c8b4b9`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 19:08:02 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 19:07:53 GMT  
		Size: 6.3 KB (6292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1f5712e2b8c936e67c9497449898632e676a58518c9fc01b01451e659b7a0`  
		Last Modified: Tue, 13 Jan 2026 19:08:15 GMT  
		Size: 255.2 KB (255188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078bc50ad7a9fc7ce83899e7f18af1e11b4762c643676a17f4dd40d140fafe0`  
		Last Modified: Tue, 13 Jan 2026 19:07:54 GMT  
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
		Last Modified: Tue, 13 Jan 2026 19:07:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c064a0c07b985773948ae6059fdd04442b0057ede5028e9e0ba8ad086750367`  
		Last Modified: Tue, 13 Jan 2026 19:07:56 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 19:08:05 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529696c893b2288c405623fa3d6e126d1fd1a9b7fd82f65096b5b2bc32c269`  
		Last Modified: Tue, 13 Jan 2026 19:08:05 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b302f796d1537d31d18e036b97c7f2285995906d4cc3a9e6a6d62dbc3b02060`  
		Last Modified: Tue, 13 Jan 2026 19:08:06 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f73397c45ce113628f36be16560d914fc7abe0edcbea53d9b1a6e13c2be27c8`  
		Last Modified: Tue, 13 Jan 2026 19:08:06 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193a5c32cfa83cabcff5d74d666f7b99ad8952c07ea094406bf9aa8a185807d0`  
		Last Modified: Tue, 13 Jan 2026 19:06:07 GMT  
		Size: 7.9 MB (7900511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993ef861233b752e2e7a15fbab4ec248ea0a1207a4a9ef1cea8ca68f14fe6972`  
		Last Modified: Tue, 13 Jan 2026 19:06:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 19:06:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7890cb1809d6af4da94ae52aa97b139dd6c050de0fa4acf1f994e0849fd15102`  
		Last Modified: Tue, 13 Jan 2026 19:06:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e43e3097005ee26fc824c7eaa8a6ef4ac919dcfdb158c8ae7f47f24e3d9622c`  
		Last Modified: Tue, 13 Jan 2026 19:06:31 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
