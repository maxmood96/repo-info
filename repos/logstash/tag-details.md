<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.21`](#logstash6821)
-	[`logstash:7.16.1`](#logstash7161)

## `logstash:6.8.21`

```console
$ docker pull logstash@sha256:d04190da332c1f1789c710d76af81dc8f81523dff48d875ec09b6ec5d4c8d3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `logstash:6.8.21` - linux; amd64

```console
$ docker pull logstash@sha256:6880c91a24330698d8ec70ffed5d4a26a385bdcc00c9a74197b3fb155c967142
```

-	Docker Version: 20.10.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396993639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0490e5ada1aaf96dde7c19027bbe91944a185cdfea90f53ed14bfdef35a2557c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Sat, 11 Dec 2021 01:50:53 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel-1.8.0.282.b08 java-1.8.0-openjdk-headless-1.8.0.282.b08 which &&     yum clean all
# Sat, 11 Dec 2021 01:50:55 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 11 Dec 2021 01:51:13 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.21.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.21 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 11 Dec 2021 01:51:15 GMT
WORKDIR /usr/share/logstash
# Sat, 11 Dec 2021 01:51:15 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 11 Dec 2021 01:51:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Dec 2021 01:51:15 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 11 Dec 2021 01:51:15 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 11 Dec 2021 01:51:16 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Sat, 11 Dec 2021 01:51:16 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 11 Dec 2021 01:51:16 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 11 Dec 2021 01:51:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 11 Dec 2021 01:51:16 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 11 Dec 2021 01:51:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 11 Dec 2021 01:51:17 GMT
USER 1000
# Sat, 11 Dec 2021 01:51:17 GMT
ADD file:c571f1340b3840928052ac69357eca598068bd1a752b377b661e4a526205c25b in /usr/local/bin/ 
# Sat, 11 Dec 2021 01:51:17 GMT
EXPOSE 5044 9600
# Sat, 11 Dec 2021 01:51:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Sat, 11 Dec 2021 01:51:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02342dd4d97866b66dac2e07aaa44a7558f916f562bdf410c4d6155274da8f61`  
		Last Modified: Mon, 13 Dec 2021 11:45:16 GMT  
		Size: 139.1 MB (139126706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff724e4d4ce05924abfbf401002871bbb98dc467a730faa2dfe829e92f5ba3e`  
		Last Modified: Mon, 13 Dec 2021 11:43:25 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c65fed98e53128ae8b41da0e398e4f1d76e9ef7b8586833cb7953508ce8ca29`  
		Last Modified: Mon, 13 Dec 2021 11:45:14 GMT  
		Size: 180.1 MB (180099297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48dfb543723369a2374656bb84811085d752f0b70831417a99a826e91b2a8c0`  
		Last Modified: Mon, 13 Dec 2021 11:43:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f13464c866ccf7e4b09deb1801f1024b0c57d2637d1253c9beabbc8059a2848`  
		Last Modified: Mon, 13 Dec 2021 11:43:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decbf70b32e9d325a58ffe1bf78f26dba227cfa8dc5865bd0f9cfe4592b1d656`  
		Last Modified: Mon, 13 Dec 2021 11:43:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faf6d015ef0af8694a8697f2ad5fb62daa5fab0e0588453b7746a370982e007`  
		Last Modified: Mon, 13 Dec 2021 11:43:18 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf48afc517cc517fd341350e75f0194401dc52d180fb014fa49c3fd55f166c`  
		Last Modified: Mon, 13 Dec 2021 11:43:18 GMT  
		Size: 2.7 KB (2683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7984c9c81abd11cb7386cfe22a40bcc1ef2bf63b363de1b445eb71560c5cc942`  
		Last Modified: Mon, 13 Dec 2021 11:43:18 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7984c9c81abd11cb7386cfe22a40bcc1ef2bf63b363de1b445eb71560c5cc942`  
		Last Modified: Mon, 13 Dec 2021 11:43:18 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df476485284c41bfa32f3368ce4578ea83c9b31d9c0e70e783f8f5dff0e9b5af`  
		Last Modified: Mon, 13 Dec 2021 11:43:17 GMT  
		Size: 1.7 MB (1663549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.16.1`

```console
$ docker pull logstash@sha256:a0d660702a68f36dee1174b68fb9711f989385009d52309b0f7618569cf0f808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.16.1` - linux; amd64

```console
$ docker pull logstash@sha256:8b55dd0bcf34783e5653a26da577cec14980a8ecf838cf3ab309329ebe0c124c
```

-	Docker Version: 20.10.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 MB (505163027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed133b351f2ce52be82994a855421c55f8d3798c4053f1948d36b73d19f1be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Sat, 11 Dec 2021 01:50:48 GMT
RUN for iter in {1..10}; do yum update -y &&     yum install -y procps findutils tar gzip which shadow-utils &&     yum clean all && yum clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     yum clean all && yum clean metadata && sleep 10; done;     (exit $exit_code)
# Sat, 11 Dec 2021 01:50:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Sat, 11 Dec 2021 01:51:14 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.16.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.16.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Sat, 11 Dec 2021 01:51:17 GMT
WORKDIR /usr/share/logstash
# Sat, 11 Dec 2021 01:51:18 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 11 Dec 2021 01:51:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Dec 2021 01:51:18 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Sat, 11 Dec 2021 01:51:18 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Sat, 11 Dec 2021 01:51:18 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Sat, 11 Dec 2021 01:51:18 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Sat, 11 Dec 2021 01:51:19 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Sat, 11 Dec 2021 01:51:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Sat, 11 Dec 2021 01:51:19 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Sat, 11 Dec 2021 01:51:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Sat, 11 Dec 2021 01:51:20 GMT
USER 1000
# Sat, 11 Dec 2021 01:51:20 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Sat, 11 Dec 2021 01:51:20 GMT
EXPOSE 5044 9600
# Sat, 11 Dec 2021 01:51:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.16.1 org.opencontainers.image.version=7.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2021-12-11T00:29:08Z org.opencontainers.image.created=2021-12-11T00:29:08Z
# Sat, 11 Dec 2021 01:51:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ed06e98788d7cebe1df9bd2ad2a0a79a6e34569b26c8af847d3c982e1982de`  
		Last Modified: Mon, 13 Dec 2021 10:26:52 GMT  
		Size: 57.6 MB (57551969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c05214fa415d4f03bb3d939d9cb64664de3d736f93d9e51e4451bec13e78506`  
		Last Modified: Mon, 13 Dec 2021 10:26:35 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c57880f1efe0135c1ee34dae41aa26b30882b69b985b26c9d52f909955f129`  
		Last Modified: Mon, 13 Dec 2021 10:27:29 GMT  
		Size: 369.8 MB (369843044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bbd2eee8582c8e639eda0ef8820bdb3edd27573d082ee1aa164667a55be193`  
		Last Modified: Mon, 13 Dec 2021 10:26:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af0f1c3ece0586aeed1960600af122f188ca799b33261e9090b820b9fd273a6`  
		Last Modified: Mon, 13 Dec 2021 10:26:32 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a362e7870e627bc07ee8b7a5ad5ae9647712ff4fd54c150e91daabdc79ecc`  
		Last Modified: Mon, 13 Dec 2021 10:26:32 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c64bf56e29dcad49b95f4c567473e6e4c6b420aadd808d9e12c1ed6288e73`  
		Last Modified: Mon, 13 Dec 2021 10:26:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0122c4679d971f5789e73d1b371d27f8cc4e3538ff3b3408cce45508a28546e3`  
		Last Modified: Mon, 13 Dec 2021 10:26:28 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7f23ed1d1d12148213c79ff02a7e388602420455ecf9ad3aa9b6d18ed4c56`  
		Last Modified: Mon, 13 Dec 2021 10:26:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7f23ed1d1d12148213c79ff02a7e388602420455ecf9ad3aa9b6d18ed4c56`  
		Last Modified: Mon, 13 Dec 2021 10:26:28 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a602964f85d0b5015611501136f43b2d49863d7b41d5f7752194b27cadf347`  
		Last Modified: Mon, 13 Dec 2021 10:26:29 GMT  
		Size: 1.7 MB (1663766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
