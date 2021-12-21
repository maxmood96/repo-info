<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.22`](#logstash6822)
-	[`logstash:7.16.2`](#logstash7162)

## `logstash:6.8.22`

```console
$ docker pull logstash@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `logstash:7.16.2`

```console
$ docker pull logstash@sha256:27a0fb18a0de09de59690b8fcf6e3a3f4453cacb5f8aae1a4d32ed62ae6a1b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:7.16.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c2350fb6b74b694615e628764b338a2885ea55d7cfdd4344feb1e5ed41b7f12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.3 MB (805303628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8401c9eb71c92ee9955ec8fd7b69062d2704b3f148fcbe0ad9f15909a9acba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Sat, 18 Dec 2021 20:05:57 GMT
RUN for iter in {1..10}; do yum install -y http://mirror.centos.org/centos/7/updates/x86_64/Packages/bind-license-9.11.4-26.P2.el7_9.5.noarch.rpm &&     yum clean all &&     yum clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all &&     yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 18 Dec 2021 20:07:29 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 18 Dec 2021 20:07:32 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 18 Dec 2021 20:07:52 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.16.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.16.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 18 Dec 2021 20:07:54 GMT
WORKDIR /usr/share/logstash
# Sat, 18 Dec 2021 20:07:54 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 18 Dec 2021 20:07:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 18 Dec 2021 20:07:55 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 18 Dec 2021 20:07:55 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 18 Dec 2021 20:07:55 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 18 Dec 2021 20:07:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 18 Dec 2021 20:07:56 GMT
USER 1000
# Sat, 18 Dec 2021 20:07:56 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Sat, 18 Dec 2021 20:07:56 GMT
EXPOSE 5044 9600
# Sat, 18 Dec 2021 20:07:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.16.2 org.opencontainers.image.version=7.16.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-12-18T19:44:11+00:00 org.opencontainers.image.created=2021-12-18T19:44:11+00:00
# Sat, 18 Dec 2021 20:07:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e22c994e04d185cbe3bde1cd97f5c58be03fa5ff598703efe48c22af35a969`  
		Last Modified: Mon, 20 Dec 2021 13:28:27 GMT  
		Size: 6.3 MB (6297485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63127af4085917c51829ff5302f0e32394478d8a2705e46f576136605a115faf`  
		Last Modified: Mon, 20 Dec 2021 13:42:54 GMT  
		Size: 324.1 MB (324128749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869f71e582fbf67895471266f86193ffd212d2bd37e52e010d1d0a5b3473bd3`  
		Last Modified: Mon, 20 Dec 2021 13:28:04 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2f0934cfacddcd9b6f026c05b99da617f70630cb1c245203333b9260ccbcfc`  
		Last Modified: Tue, 21 Dec 2021 00:43:36 GMT  
		Size: 365.0 MB (364965262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954001ff78ecbc1ce0c8171c671775923bd0d1e8eeb43f6f2fc58379e38ac5d4`  
		Last Modified: Tue, 21 Dec 2021 00:43:01 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c5a03b4e9a22c18cdd96db77cea38691b078284c6403cd6850bb0bb82d2118`  
		Last Modified: Tue, 21 Dec 2021 00:43:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f22b6368abfa49396004477c66df935ef4462022a5c00f299081fbd688aea`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aad3adf94a954c6ce1bddf7c75a3d161cd74b74281b10de46738067c0821494`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f18c19168272ff7e91a136bdf26bff872807cbb6cc57f7a8b0f32f9b0216d`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 2.8 KB (2809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f73b191a52af8bdbd4839f691121a36922895be0b2eedb4f3c0af763819be04`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f73b191a52af8bdbd4839f691121a36922895be0b2eedb4f3c0af763819be04`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d995ae082094dda286de735eb5243a7cf719b8586143eb269bbde629a77a2d71`  
		Last Modified: Tue, 21 Dec 2021 00:42:59 GMT  
		Size: 1.5 MB (1530120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
