<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.18`](#elasticsearch6818)
-	[`elasticsearch:7.14.1`](#elasticsearch7141)

## `elasticsearch:6.8.18`

```console
$ docker pull elasticsearch@sha256:a676c5eadeaff21fb0ed9b7f6be7dcb559dc25dcc017940197dd5ced0f90dbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:6.8.18` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0f16a358b58c4d233258c87fe2dd9762d02eb0561ff9e72aa9814e03f2e2dd15
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482221730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b226f5ba29f397cac809b642d7f9f9bc7e865c4e248ccb65e6b9cee09bea2d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Wed, 28 Jul 2021 16:10:35 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 28 Jul 2021 16:10:36 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Wed, 28 Jul 2021 16:10:41 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Wed, 28 Jul 2021 16:11:23 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Wed, 28 Jul 2021 16:11:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Wed, 28 Jul 2021 16:11:25 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 28 Jul 2021 16:11:28 GMT
COPY --chown=1000:0dir:2b0d1a24665560d0012df6c5f68f16ea5e598782bfc6749adbf0f56f745fdcf3 in /usr/share/elasticsearch 
# Wed, 28 Jul 2021 16:11:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 16:11:29 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 28 Jul 2021 16:11:30 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Wed, 28 Jul 2021 16:11:30 GMT
EXPOSE 9200 9300
# Wed, 28 Jul 2021 16:11:31 GMT
LABEL org.label-schema.build-date=2021-07-28T16:06:05.232873Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aca23296a2422a5abea96a1b6b590f6566e9c02f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.18 org.opencontainers.image.created=2021-07-28T16:06:05.232873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=aca23296a2422a5abea96a1b6b590f6566e9c02f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.18
# Wed, 28 Jul 2021 16:11:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 28 Jul 2021 16:11:31 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0128b25cc806662d7fe5ee6828f183c810828baa43cf452ddb469980ae5c4ff3`  
		Last Modified: Tue, 03 Aug 2021 12:57:47 GMT  
		Size: 207.7 MB (207657662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e926b4f11fd8c1a1adffe67a9c0803a29698dba31660155078e0b337de05753`  
		Last Modified: Tue, 03 Aug 2021 12:57:27 GMT  
		Size: 48.3 MB (48319743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01aa6e6c3b0500fe4d3d1bc5e21b20db804d517a6f48bc911b001e0577b3544`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f53e5ee82cadd34edd16d8d5f9354aa1615988ba5c57670bb2b7dce330df0f3`  
		Last Modified: Tue, 03 Aug 2021 12:57:34 GMT  
		Size: 150.1 MB (150140389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6045fa98c98d76b32e4a3f9ea1ab9f8e56b0efb02a13451db236b413feec67e7`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec43e9f984f6fc2ffe54f846e2ca96c37af763371f2333fb82c3e54bb3468b1`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.4 KB (2402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.14.1`

**does not exist** (yet?)
