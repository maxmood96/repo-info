<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.21`](#logstash6821)
-	[`logstash:7.16.1`](#logstash7161)

## `logstash:6.8.21`

```console
$ docker pull logstash@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `logstash:7.16.1`

```console
$ docker pull logstash@sha256:c363998a215cf939fa0137d667b3ecfae27ae62bb2b5a88e2f79ec22093f6cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `logstash:7.16.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:803225b4b23ec04279a8582fbb7dea6c0449150b8931bfe174848796c746250a
```

-	Docker Version: 20.10.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.9 MB (806890644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad59301e2cf54c48f9107f238bfc3e8d642a2c2f58150587c262f6af747ee42c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Sat, 11 Dec 2021 00:51:24 GMT
RUN for iter in {1..10}; do yum install -y http://mirror.centos.org/centos/7/updates/x86_64/Packages/bind-license-9.11.4-26.P2.el7_9.5.noarch.rpm &&     yum clean all &&     yum clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all &&     yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 11 Dec 2021 00:52:57 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 11 Dec 2021 00:53:01 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 11 Dec 2021 00:53:20 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.16.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.16.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 11 Dec 2021 00:53:22 GMT
WORKDIR /usr/share/logstash
# Sat, 11 Dec 2021 00:53:22 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 11 Dec 2021 00:53:23 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Dec 2021 00:53:23 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 11 Dec 2021 00:53:23 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 11 Dec 2021 00:53:23 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 11 Dec 2021 00:53:23 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 11 Dec 2021 00:53:23 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 11 Dec 2021 00:53:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 11 Dec 2021 00:53:24 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 11 Dec 2021 00:53:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 11 Dec 2021 00:53:24 GMT
USER 1000
# Sat, 11 Dec 2021 00:53:24 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Sat, 11 Dec 2021 00:53:24 GMT
EXPOSE 5044 9600
# Sat, 11 Dec 2021 00:53:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.16.1 org.opencontainers.image.version=7.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-12-11T00:29:46+00:00 org.opencontainers.image.created=2021-12-11T00:29:46+00:00
# Sat, 11 Dec 2021 00:53:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fcaed214e44ee68a6b8d327767d04c1623552e21460da4157be40135e033de`  
		Last Modified: Tue, 14 Dec 2021 00:47:05 GMT  
		Size: 6.3 MB (6297469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff1cdaf5b6c1fc13e8372d28935a1c361a8c6ee0dffb154bcbeaf92030db751`  
		Last Modified: Tue, 14 Dec 2021 00:47:38 GMT  
		Size: 324.1 MB (324127604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e978b560492b66c2225e4c006798bd14ecdc854178f003e6f271c8b644908a`  
		Last Modified: Tue, 14 Dec 2021 00:47:02 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877fbc7c6cd40ef00dbc1a8bfa808f19da2cadb1bc5275fdeb053e8efc509421`  
		Last Modified: Tue, 14 Dec 2021 00:47:37 GMT  
		Size: 366.6 MB (366553449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f77d70ada0cd73209d759988c33bfba635a613d67ee76628dffac531e530fea`  
		Last Modified: Tue, 14 Dec 2021 00:47:01 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bbc9e9dda9000f051ed25cd37e6ee5932a6cf385637436469a92a3128eb2a6`  
		Last Modified: Tue, 14 Dec 2021 00:47:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397caea833f07bb75efcecfbe3d5a167e7df457dc24ba9922e9ba2f57dc7a711`  
		Last Modified: Tue, 14 Dec 2021 00:46:59 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f42b45bf15a5e7b029f2b585305abdc32bd71c95f42f6133a4c2929614bed5`  
		Last Modified: Tue, 14 Dec 2021 00:46:58 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c7885bd44a19ce73afb8e7623abf33397756dc010253bb94d4bf6b257a963`  
		Last Modified: Tue, 14 Dec 2021 00:46:59 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdab216af562560ab61616e715856459f88049d3a3e235cc8aed5774f7044932`  
		Last Modified: Tue, 14 Dec 2021 00:46:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdab216af562560ab61616e715856459f88049d3a3e235cc8aed5774f7044932`  
		Last Modified: Tue, 14 Dec 2021 00:46:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864ca89ca804bd6542418c56da6db705a4ace61562aa86cb60187f3cc21e1f09`  
		Last Modified: Tue, 14 Dec 2021 00:46:59 GMT  
		Size: 1.5 MB (1530124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
