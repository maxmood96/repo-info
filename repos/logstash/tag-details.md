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
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 49.8 MB (49811886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a75ed7773cbf70823ab6f16214f069c73a448c56e85b629af42ccca888f332e`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116f452c2b93845c457613af44b5bec51a6716e842c2c8344d60a6cea88da1d`  
		Last Modified: Thu, 15 Jan 2026 22:33:12 GMT  
		Size: 441.6 MB (441640221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e55bbed2aef1fa6dc69dee5568808f3cc413ab6bd97be2783c0142469d0b0`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0740e857072ed647e436c435e397b2b1325d2ece9b013b3c33d804d78cb4e`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaee70b78cf97de53ab844f5847ecf41806aea1795fa4c32caedd0205c6c233`  
		Last Modified: Thu, 15 Jan 2026 22:32:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20401eda2953ef0b0ead602de4b6255b5cb4d43dd0242c34099ea4dca2d4d9ee`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a1de0bed25db992ea94b99e45fb796bf4d4a0ea21c7a71446f2ead25d42dd`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be2883b856b67a053014231e409532dc327b15369bead35116ac7dad522e23b`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cac1d1d0771b591c0e22f728b3c3b6372e540e23a818bbb3ab6a184a2be844`  
		Last Modified: Thu, 15 Jan 2026 22:32:56 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417ef8ab86e54a79dec82445546991485365e8ea978094c1728767e4e7ffc2b2`  
		Last Modified: Thu, 15 Jan 2026 22:32:43 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:25:39 GMT  
		Size: 52.1 MB (52065432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7bcac2f41a34a4e6da98b8f3af1305316671dd8dfa5528cc81a608686d65a`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:51 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d74cb030ea7e313e8cd7a0ed66c22c26370442c070dde06d5b7a9a526fc008`  
		Last Modified: Thu, 15 Jan 2026 22:34:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d699a4f40f9e4169b2941e11a512305fe497924f849469ec9f6f074e853eba`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59793887602ab2816f376a5174af463b8192bad06c347f60f7b53718896bf2`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:54 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 3.7 MB (3652171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9636c18161852dc6094863744875e4fa85977c8d6767aea42d4b81755c8b4b9`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.10`

```console
$ docker pull logstash@sha256:9551615acd98b4dc6416a5a016b601b55f3c89bd672c6f7197b895cc69468a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.10` - linux; amd64

```console
$ docker pull logstash@sha256:f2322f90499b06c9c2087a3228de62a000b797e3f7d3212fea2b6eaf4a73a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (476029158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea9f2c421c88667ec28e6092dd2a27dcba9d0d069e6f21d3d4c476ff34b1911`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:15:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:53 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 20 Jan 2026 19:15:53 GMT
WORKDIR /usr/share
# Tue, 20 Jan 2026 19:15:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:46 GMT
WORKDIR /usr/share/logstash
# Tue, 20 Jan 2026 19:16:46 GMT
USER 1000
# Tue, 20 Jan 2026 19:16:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 20 Jan 2026 19:16:46 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 20 Jan 2026 19:16:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e59b4e92811ed49652ac2323ac19a28420e64967005aabbabce69dd1c0ed0`  
		Last Modified: Tue, 20 Jan 2026 19:17:33 GMT  
		Size: 5.2 MB (5159474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c0a39e8159b83a21dd9622e13a49d1ba106747af982700dcc7d5aa000cf526`  
		Last Modified: Tue, 20 Jan 2026 19:17:28 GMT  
		Size: 430.6 MB (430571727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b57fba51c5f1511f489dd938b89734bb15966f28afff799aba17f57f7d2f80`  
		Last Modified: Tue, 20 Jan 2026 19:17:33 GMT  
		Size: 6.3 KB (6299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af098f0cc27b0578cda6b9ced8da6d82d3543921f6f20eed5397c67958fefa6`  
		Last Modified: Tue, 20 Jan 2026 19:17:32 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa4e1d2ff7e62dc401c2401e5a6703361ced916a9f86dcd05d14133d2f05e5`  
		Last Modified: Tue, 20 Jan 2026 19:17:21 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02511c0768c8f7bf3a47dd2f524dfbb235ab3277971c6acbff651a8fdaa662f`  
		Last Modified: Tue, 20 Jan 2026 19:17:21 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4bd61f0b48bfe565cd8f2f7aa2de682e3a1babaf1cf89fd6b789135555ecf9`  
		Last Modified: Tue, 20 Jan 2026 19:17:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bee7b1f0930d1c7e0d3f22dd9dd4b3640d4f7a9bd7651d627e9746a0dd73d8`  
		Last Modified: Tue, 20 Jan 2026 19:17:23 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd16d78444a6ccfade867a8970fa92488efeef52ca54ab75e523ba7178e4870`  
		Last Modified: Tue, 20 Jan 2026 19:17:33 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:9fb4f2dd3c21ad004a290a9d8ae680e499a49b8875c92a85eea438d698b93479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc28bd77e00a1a442a02f0aea188cbff4bf370707472110f5b993111d3c374b`

```dockerfile
```

-	Layers:
	-	`sha256:80a15f745f46ce9e2ac968eafd810a90fbdb7cf6f3ed6592d45655d66febc667`  
		Last Modified: Tue, 20 Jan 2026 19:17:20 GMT  
		Size: 2.1 MB (2088541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f2be7e86a004df8453d2da21f9f3741f6eb0f734a87c0c27d28473273d9acb`  
		Last Modified: Tue, 20 Jan 2026 19:17:20 GMT  
		Size: 30.2 KB (30164 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d6ffcf42362cd3177e21ff24fe2264bf3cbc2c230bdf1d2de9a6dee26f6cefe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.5 MB (472481185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248cbdc02d3132cd16b3ea3b225b38a779e784e194e530baa690b0a53c28739`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:15:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:39 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:39 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 20 Jan 2026 19:15:39 GMT
WORKDIR /usr/share
# Tue, 20 Jan 2026 19:15:41 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:16:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 20 Jan 2026 19:16:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 20 Jan 2026 19:16:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 20 Jan 2026 19:16:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 20 Jan 2026 19:16:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 20 Jan 2026 19:16:10 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 20 Jan 2026 19:16:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 20 Jan 2026 19:16:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:10 GMT
WORKDIR /usr/share/logstash
# Tue, 20 Jan 2026 19:16:10 GMT
USER 1000
# Tue, 20 Jan 2026 19:16:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 20 Jan 2026 19:16:10 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 20 Jan 2026 19:16:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2876391fe4aa556d3ab2341e1c7ea8f85d06cb97ccddee7141ff3b211416fb`  
		Last Modified: Tue, 20 Jan 2026 19:17:00 GMT  
		Size: 5.2 MB (5157883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0165b9a87bfd8d1205a55493b5578491bd2c522171998a1a66e9a68b4e88c224`  
		Last Modified: Tue, 20 Jan 2026 19:16:53 GMT  
		Size: 428.8 MB (428849906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee03f2a7277e5f7eef93a1fad8f0ccc27b9915a9bce545968d459918b5a8966`  
		Last Modified: Tue, 20 Jan 2026 19:16:45 GMT  
		Size: 6.3 KB (6291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f3b3279bb943a0e051b78ce14bee08a4831eb7ff10daef2c6c2af674b8f1d9`  
		Last Modified: Tue, 20 Jan 2026 19:16:45 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ea2f324b54a44763c0e8606101c8b8117b32ac4e8901328eb233fa6876618`  
		Last Modified: Tue, 20 Jan 2026 19:16:47 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc3b8da97148538855051c7f3eaf5d04ddb9f7fa144136578c59a0a80b738d`  
		Last Modified: Tue, 20 Jan 2026 21:11:54 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd2b038211f64ad9040b6ee0a26c72f9eb0eb5f222812752e9372136a2ba854`  
		Last Modified: Tue, 20 Jan 2026 19:16:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4195168d6ffbd66571c3d07628caff81b9999bdf27cd811eeaf9f568007f7436`  
		Last Modified: Tue, 20 Jan 2026 21:11:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb6b2064bf3ede2221c42e0c3948131d97d1e7f31fa00739f0c6eb09b3251b`  
		Last Modified: Tue, 20 Jan 2026 23:06:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:1645bbde7979a2b931f0c9640f7428b2f1fa6df1a5f3ae0befd0689e7a47e587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ae4ffd9a0f51e266a6c22c1d8750d2c3017d360b4a79c5244e489adb26b730`

```dockerfile
```

-	Layers:
	-	`sha256:993ef0199563b582e29b5e4744361e39f8db5c64c6425807c040c861bc1154b1`  
		Last Modified: Tue, 20 Jan 2026 19:16:45 GMT  
		Size: 2.1 MB (2089111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e00c72064845798cb0ded4aa00bbe5f450e1a6bc74c2b17f05129f2c8e98f5`  
		Last Modified: Tue, 20 Jan 2026 22:53:27 GMT  
		Size: 30.2 KB (30240 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.4`

```console
$ docker pull logstash@sha256:0d74532106c55d513db3a426ff964bc41b2b244373b305ee38e063052a87af1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.4` - linux; amd64

```console
$ docker pull logstash@sha256:af6cbc52ecf7e89565a8be44f15651bddf6d726f46d60608896c04d2e378ae02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486335834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9aa71c4c279015536e9c4e56e889b07698b19326c38dfb18fe2aff6c0268e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:16:02 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:16:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:16:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 20 Jan 2026 19:16:02 GMT
WORKDIR /usr/share
# Tue, 20 Jan 2026 19:16:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:16:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 20 Jan 2026 19:16:51 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
WORKDIR /usr/share/logstash
# Tue, 20 Jan 2026 19:16:52 GMT
USER 1000
# Tue, 20 Jan 2026 19:16:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 20 Jan 2026 19:16:52 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 20 Jan 2026 19:16:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfb71b224e826f3260b901618edada4c6b9ef8b8ae84c84e4ea876867300218`  
		Last Modified: Tue, 20 Jan 2026 23:39:24 GMT  
		Size: 5.2 MB (5159490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f6a146356fa9465ec70b26195e4c7b9815371c8c6aa3799881acc92c3401f1`  
		Last Modified: Tue, 20 Jan 2026 19:17:38 GMT  
		Size: 440.9 MB (440878386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2c82e8b15e22774983fb80b2d930743680d4f61b76c05c713402721774b9e7`  
		Last Modified: Tue, 20 Jan 2026 19:17:44 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8388b2b00710f280867c930d19bdfa4d52eb8a186a09ba97c4ae55114e06f435`  
		Last Modified: Tue, 20 Jan 2026 21:14:12 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14179eaf3ec77f9845dc64cc3e494a6232416daeaf807c5da9496fecf5e39a2`  
		Last Modified: Tue, 20 Jan 2026 21:14:10 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e7f3b102a9204248319a7dacd1a5968e1ea16cad228eb7e10d278dcbe5880`  
		Last Modified: Tue, 20 Jan 2026 19:17:44 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1081bf69db01a3be7f06c09a5f8f120ea7918d44fe6c8351274f9a4df662f7`  
		Last Modified: Tue, 20 Jan 2026 19:17:44 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ae6351a91b746b589f45160e200bb95d124e577a428018d87d3d1cc86e6cf`  
		Last Modified: Tue, 20 Jan 2026 19:17:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8250f4aeec8a0b2a29b073d70753b43769a3b3eb3f7746cbf028beea5d7c3caf`  
		Last Modified: Tue, 20 Jan 2026 21:14:12 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:55370cd73a50db85b4e18cb7e64078d8f6e3bdd98ec44b64bbd2869b7d03af1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2128556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a67851cbf6ce1af079d8bcf86d76c0fd519600d1ff8071a7b065d320df1eb4`

```dockerfile
```

-	Layers:
	-	`sha256:56fea6c23dfaf3d61d221b0b8750894149f626c6e57334d73986d7fc400a2e61`  
		Last Modified: Tue, 20 Jan 2026 22:53:33 GMT  
		Size: 2.1 MB (2098356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbea646e3cd9175612e33d5c94484f78a9ef110d33a1edabf24ea191ec067b07`  
		Last Modified: Tue, 20 Jan 2026 22:53:33 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e0d2cf12282c7cd622e2dac8824740c40ead832113901d4484b6f94506ae7295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482787575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33539ddf426d481efe85f34084f06b874fce0cf2fb8cb6977e5387ec42b2043f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:15:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:40 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 20 Jan 2026 19:15:40 GMT
WORKDIR /usr/share
# Tue, 20 Jan 2026 19:15:42 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 20 Jan 2026 19:16:31 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:16:32 GMT
WORKDIR /usr/share/logstash
# Tue, 20 Jan 2026 19:16:32 GMT
USER 1000
# Tue, 20 Jan 2026 19:16:32 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 20 Jan 2026 19:16:32 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 20 Jan 2026 19:16:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd70aa0f5547b1c04fceab954c421de0fc774052934658e764c80db2760eb7c`  
		Last Modified: Tue, 20 Jan 2026 19:17:26 GMT  
		Size: 5.2 MB (5157856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9798972d899ac6c528c6e2ec2a3f9c7cd371187d1e7e9bc5fd1947aa4f1eb7c`  
		Last Modified: Tue, 20 Jan 2026 19:17:16 GMT  
		Size: 439.2 MB (439156308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61d780bb2318164739f5d6562f4dad74dbc994d0626730277fda7d947545d9`  
		Last Modified: Tue, 20 Jan 2026 19:17:26 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c53f7ac129117f58a7145a39ec9225472f430ea8d080abe0cd7f43229d37121`  
		Last Modified: Tue, 20 Jan 2026 19:17:27 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb82d4b6591e670c326feb6462249fa1e2f1a5be31c5599fdcef254586729ac`  
		Last Modified: Tue, 20 Jan 2026 21:11:53 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7294c5031db15831089f5ef18dd5de9d07ff28bd1014bea42f76de6e9ca76f01`  
		Last Modified: Tue, 20 Jan 2026 19:17:27 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4b691d77b0cddbae624db6527453b634aac1db4a93d0f5dc1c8ca6112bb70`  
		Last Modified: Tue, 20 Jan 2026 21:11:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9514e93d041c27a673d16579b249fe5ff1303c4aeb876c4eea36ef9f6356ff74`  
		Last Modified: Tue, 20 Jan 2026 19:17:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d55bc8ddf479aa291d3abba0de09a57cdc15933408460ef0e81f3d57fba0a5`  
		Last Modified: Tue, 20 Jan 2026 19:17:29 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:81bd3c424d759f01b076ec3352deff79b6e6cd8a8f8378e0b0f34a2e46a789db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5570f2934db094c8218f5e8a5f8d95909cd1c3654f84f2bf0d58f6e870b774a8`

```dockerfile
```

-	Layers:
	-	`sha256:909adfa21e85f5f9a96802fc6d127972b010e738f21f8183f8c4f29c04e36a6a`  
		Last Modified: Tue, 20 Jan 2026 22:53:39 GMT  
		Size: 2.1 MB (2098926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8186a680ba4d9cbfe8f44ea2308c732cb6b4f0b400245389d36f37f4a1fb81c4`  
		Last Modified: Tue, 20 Jan 2026 22:53:53 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
