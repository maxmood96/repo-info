<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.10`](#elasticsearch6810)
-	[`elasticsearch:7.7.1`](#elasticsearch771)

## `elasticsearch:6.8.10`

```console
$ docker pull elasticsearch@sha256:95d624106abc6d41340a736e2086d1d7b13d8334bee9a1c987f36fb0f9e6c16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6c36fa585104d28d3a9e53c799a4e20058445476cadb3b3d3e789d3793eed10a
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.7 MB (462714490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa00077159cd4b5ac8cca1e84ec2c5d187d4395d459a661e2a901f0426c013f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2020 14:57:45 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2020 14:57:45 GMT
ENV JAVA_HOME=/opt/jdk-14.0.1+7
# Thu, 28 May 2020 14:57:51 GMT
COPY dir:170319d0c30c0291abfea65bce51d4fa7bfdeba3e2278bcdd7c345f06cc9303d in /opt/jdk-14.0.1+7 
# Thu, 28 May 2020 14:58:06 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 28 May 2020 14:58:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 28 May 2020 14:58:10 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2020 14:58:15 GMT
COPY --chown=1000:0dir:e0d48488cb486bbdd0f929f36bd9589d20684922bb1d507041500d6bb0d91a72 in /usr/share/elasticsearch 
# Thu, 28 May 2020 14:58:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2020 14:58:16 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 28 May 2020 14:58:18 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 28 May 2020 14:58:18 GMT
EXPOSE 9200 9300
# Thu, 28 May 2020 14:58:18 GMT
LABEL org.label-schema.build-date=2020-05-28T14:47:19.882936Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=537cb22e7ffb62ee541e1af1881d18e3a78e6133 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.10 org.opencontainers.image.created=2020-05-28T14:47:19.882936Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=537cb22e7ffb62ee541e1af1881d18e3a78e6133 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.10
# Thu, 28 May 2020 14:58:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2020 14:58:19 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf34341d86d3d59e99d027d4fc69731cf8cb9b71d90381af2fc707e97e1fb1b`  
		Last Modified: Wed, 03 Jun 2020 14:50:57 GMT  
		Size: 211.9 MB (211934763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551de3bae6fbdc0ce3dd44e4b669368ea613081815c1cb977dd924d5a960123a`  
		Last Modified: Wed, 03 Jun 2020 14:50:36 GMT  
		Size: 23.9 MB (23934482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cc3405237863a7d97735ee56d391c4260ed50caacde466cd099943f32fdbd6`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bab9bbf7644c2c0fb4ee67a14e690f56316325c9196683a20338ca0f9451032`  
		Last Modified: Wed, 03 Jun 2020 14:50:51 GMT  
		Size: 151.0 MB (150958368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52184024c46082b666e5c1e775619ca7a297d8a50afe259ce32d329e19541b84`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80935e4ae0b9ed4a2ca533a27c8363587b2e4c0421001dc9f2459829108ae265`  
		Last Modified: Wed, 03 Jun 2020 14:50:32 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.7.1`

```console
$ docker pull elasticsearch@sha256:dff614393a31b93e8bbe9f8d1a77be041da37eac2a7a9567166dd5a2abab7c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:7.7.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:85afaf2752085119a3835127a06001aecb2780ef070ce8dc74a1610e64aa5769
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.3 MB (416269473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a894845e39d20e413d8a824ba1f7562d76a02cf9a85a8b6d1d9d47a4d5dd3`
-	Entrypoint: `["\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2020 16:34:36 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2020 16:34:37 GMT
COPY file:df9158ae8b9b283e8ea5bd72d1e344c08dea733e283f9f0941833f467466323c in /tini 
# Thu, 28 May 2020 16:35:07 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 28 May 2020 16:35:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 28 May 2020 16:35:08 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2020 16:35:19 GMT
COPY --chown=1000:0dir:9c49dbccde77e200cb496a42bb738b343834cce925f6c128737575f84c32cbd2 in /usr/share/elasticsearch 
# Thu, 28 May 2020 16:35:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Thu, 28 May 2020 16:35:21 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2020 16:35:21 GMT
COPY file:d964df1452418918baf1d29ee20df18c9648ca6c9d51764640fca470bd9a9366 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 28 May 2020 16:35:22 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 28 May 2020 16:35:23 GMT
RUN find / -xdev -perm -4000 -exec chmod ug-s {} +
# Thu, 28 May 2020 16:35:23 GMT
EXPOSE 9200 9300
# Thu, 28 May 2020 16:35:23 GMT
LABEL org.label-schema.build-date=2020-05-28T16:30:01.040088Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ad56dce891c901a492bb1ee393f12dfff473a423 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.7.1 org.opencontainers.image.created=2020-05-28T16:30:01.040088Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=ad56dce891c901a492bb1ee393f12dfff473a423 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.7.1
# Thu, 28 May 2020 16:35:24 GMT
ENTRYPOINT ["/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2020 16:35:24 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79045bc94aaaa1467cc2932e15d52087c3764c7f2c96e3576db0bf8cf1a339`  
		Last Modified: Wed, 06 May 2020 14:38:52 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4602c5830f92b55fbfdeebaf1588e09c64f4eed5e4a2293b396b81f45b489dff`  
		Last Modified: Wed, 03 Jun 2020 14:49:32 GMT  
		Size: 24.0 MB (23980019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ef2eb1c9b12741ff275f1e64b90b711fdcad816a74ca1df96e24bf187088a4`  
		Last Modified: Wed, 03 Jun 2020 14:49:25 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fca9194a1bdf209be1463cff0593992ee663c318f4d0b3b117ecd63ba4602a`  
		Last Modified: Wed, 03 Jun 2020 14:50:06 GMT  
		Size: 316.2 MB (316192898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c282e1371ecc02fc70d2e3b352a9e46fc6583c9ecc500e1829d62e7137f90fa1`  
		Last Modified: Wed, 03 Jun 2020 14:49:24 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e1effd34b22625ef8fe506debb77a7680584ad906b24fe2afc7960b45cec3`  
		Last Modified: Wed, 03 Jun 2020 14:49:24 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50acbec75309b64150d39ff3d51ef4b583c08ec17928fd59cd42adc8d7639391`  
		Last Modified: Wed, 03 Jun 2020 14:49:24 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89bc5c60b5f633533bbd5eba6e2a8cdae324504b01ecf3f0fc752780d404320`  
		Last Modified: Wed, 03 Jun 2020 14:49:24 GMT  
		Size: 200.6 KB (200611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
