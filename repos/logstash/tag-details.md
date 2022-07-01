<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.5`](#logstash7175)
-	[`logstash:8.3.1`](#logstash831)

## `logstash:6.8.23`

```console
$ docker pull logstash@sha256:53d822de31e74c91dcb623abf0d0bfd95192ee571e695e39ea4fe2af626c9232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `logstash:6.8.23` - linux; amd64

```console
$ docker pull logstash@sha256:347be947d25fad34bcb808af6884c9f7c06a3d9a1f9599d036bb4d05bd2a46a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395596751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e03e2750214e21b7f3a5a7b5cf55db2adb0aad5eb897eb03e77e05b2e6a1ebb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 20:50:28 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel-1.8.0.282.b08 java-1.8.0-openjdk-headless-1.8.0.282.b08 which &&     yum clean all
# Thu, 06 Jan 2022 20:50:30 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Thu, 06 Jan 2022 20:50:46 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.23.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 06 Jan 2022 20:50:48 GMT
WORKDIR /usr/share/logstash
# Thu, 06 Jan 2022 20:50:48 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 20:50:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Thu, 06 Jan 2022 20:50:49 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 06 Jan 2022 20:50:49 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 06 Jan 2022 20:50:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 06 Jan 2022 20:50:50 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 06 Jan 2022 20:50:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 06 Jan 2022 20:50:50 GMT
USER 1000
# Thu, 06 Jan 2022 20:50:50 GMT
ADD file:c571f1340b3840928052ac69357eca598068bd1a752b377b661e4a526205c25b in /usr/local/bin/ 
# Thu, 06 Jan 2022 20:50:51 GMT
EXPOSE 5044 9600
# Thu, 06 Jan 2022 20:50:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Thu, 06 Jan 2022 20:50:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1fb6f60b9250e42308ecf6503a441f9fc10b2e603a46e8767f9646555f43d`  
		Last Modified: Thu, 13 Jan 2022 16:12:17 GMT  
		Size: 139.1 MB (139127934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab13d3e354e35c347031eddca0d4bb20209d98ace9d3223a8358de9120fc72b`  
		Last Modified: Thu, 13 Jan 2022 16:11:56 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5ffc479f94b8a50d1647f4dfce26f0045e4fcb2055db4859ddcc840208bb96`  
		Last Modified: Thu, 13 Jan 2022 16:12:10 GMT  
		Size: 178.7 MB (178701203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88d374d1955f1098a61ca9fee227fce373072d7b9379399153efe94b7a0774f`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07700abd6d6ac998267b237b6308c2722005f4b43601aadf6fe67b2ff92a4d3`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a109f862359a4f53f5f8b0c2c48138454070d95f9b003bd4332b725f466223`  
		Last Modified: Thu, 13 Jan 2022 16:11:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8800e09be38effb116e9b61cbfe8810b2c48c0a08af461cbfd3e58d52bf84f`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2282ae509684254b6426aa0880f79c8147ebf07313803f64519567c602654a`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 2.7 KB (2676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b4125dcde9ccc2725f69e8f367f96efe05fc158888dad1fb7d3502c268f7e0`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b4125dcde9ccc2725f69e8f367f96efe05fc158888dad1fb7d3502c268f7e0`  
		Last Modified: Thu, 13 Jan 2022 16:11:50 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fece8ba60aee91b52cdf69bf5b3548119d5efb180f0c3ccb045831ac1cd18`  
		Last Modified: Thu, 13 Jan 2022 16:11:49 GMT  
		Size: 1.7 MB (1663550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.17.5`

```console
$ docker pull logstash@sha256:97e76ad87121eb77621c15f7dfa9d93516d56c096d100306729c08d6802cd726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.5` - linux; amd64

```console
$ docker pull logstash@sha256:75be39166b444847ec6e1a45a4fdb5faed1858972ce261891d181df85bbaa1fe
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.6 MB (437579220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6a0dd89b723ecc98726f17e26617465686eaba1cce120dfd98730e884723ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 22:46:06 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 23 Jun 2022 22:46:07 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 23 Jun 2022 22:46:30 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.5-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.5 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 23 Jun 2022 22:46:34 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Jun 2022 22:46:34 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Jun 2022 22:46:34 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:46:34 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 23 Jun 2022 22:46:34 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 23 Jun 2022 22:46:35 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 23 Jun 2022 22:46:35 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 23 Jun 2022 22:46:35 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 23 Jun 2022 22:46:35 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 23 Jun 2022 22:46:35 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 23 Jun 2022 22:46:36 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 23 Jun 2022 22:46:36 GMT
USER 1000
# Thu, 23 Jun 2022 22:46:36 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Thu, 23 Jun 2022 22:46:36 GMT
EXPOSE 5044 9600
# Thu, 23 Jun 2022 22:46:36 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.5 org.opencontainers.image.version=7.17.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-06-23T21:58:05Z org.opencontainers.image.created=2022-06-23T21:58:05Z
# Thu, 23 Jun 2022 22:46:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c780476be46b37044ab8aa6b3efcb37763e304ddbc4aebe50ad91ad3b05af4b`  
		Last Modified: Tue, 28 Jun 2022 18:44:22 GMT  
		Size: 41.1 MB (41112113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409fc44aee5a7d69e5c52157483131f0dd5c68ccb02e660d237c1322fa61da7c`  
		Last Modified: Tue, 28 Jun 2022 18:44:14 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad0145d00ecc430973aafc063959e3319f137b8ef7e7ba6faaf3a3009c072e7`  
		Last Modified: Fri, 01 Jul 2022 01:27:21 GMT  
		Size: 366.2 MB (366223586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa61337d8ea50192d567a60ab4884601b19ef58547988035a042a478998e7d6`  
		Last Modified: Fri, 01 Jul 2022 01:26:54 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f56037d471b611b06298e7fab9cb303569fb22ae8cd8e52786615dc691dbd0`  
		Last Modified: Fri, 01 Jul 2022 01:26:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e484e21c01cad487105bf5091dcd954dc13733acb41814dda174ae54aac554`  
		Last Modified: Fri, 01 Jul 2022 01:26:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f286d565c7c0778623530dc1bd6b493cbba066322d36d3cb386721e57bcd9161`  
		Last Modified: Fri, 01 Jul 2022 01:26:52 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98782028098f2317810bc378294a830546d97bb987b85de0fcf379d65db7185`  
		Last Modified: Fri, 01 Jul 2022 01:26:51 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37495cfec2ebf98b263975a89e6d70c5b172e86be2cad2ba33923e9a453f8206`  
		Last Modified: Fri, 01 Jul 2022 01:26:51 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37495cfec2ebf98b263975a89e6d70c5b172e86be2cad2ba33923e9a453f8206`  
		Last Modified: Fri, 01 Jul 2022 01:26:51 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e72a437b4a81081e90db6391e56d07060ba71dbd7d40565091f96097bef8c5`  
		Last Modified: Fri, 01 Jul 2022 01:26:52 GMT  
		Size: 1.7 MB (1663763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1662d1dc8c484cee5416cf6019a4a9258fd0fe0ad23f18d22645010c579c82c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427558257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb62fffeabe38c77782c6e3e4f634f25d2047880934ec5dab63f928ca3e4965`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 22:13:07 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 23 Jun 2022 22:13:08 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 23 Jun 2022 22:13:27 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.5-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.5 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 23 Jun 2022 22:13:29 GMT
WORKDIR /usr/share/logstash
# Thu, 23 Jun 2022 22:13:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Jun 2022 22:13:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:13:29 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 23 Jun 2022 22:13:29 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 23 Jun 2022 22:13:29 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 23 Jun 2022 22:13:30 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 23 Jun 2022 22:13:30 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 23 Jun 2022 22:13:30 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 23 Jun 2022 22:13:30 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 23 Jun 2022 22:13:30 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 23 Jun 2022 22:13:31 GMT
USER 1000
# Thu, 23 Jun 2022 22:13:31 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Thu, 23 Jun 2022 22:13:31 GMT
EXPOSE 5044 9600
# Thu, 23 Jun 2022 22:13:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.5 org.opencontainers.image.version=7.17.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-06-23T21:59:27+00:00 org.opencontainers.image.created=2022-06-23T21:59:27+00:00
# Thu, 23 Jun 2022 22:13:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8114a33fb81169ee1d477d826b514aae3bc639fbde01d89c26cc50649723e11`  
		Last Modified: Fri, 01 Jul 2022 00:43:34 GMT  
		Size: 35.9 MB (35851547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788791c40cf32cda26988980e476ae6d0f327fa4aa9fe73cf0b5f4f15b43b893`  
		Last Modified: Fri, 01 Jul 2022 00:43:29 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7153582fbab4b103db8ad7a2f104bec3b1265d2e9af5cb161430b22baa38e522`  
		Last Modified: Fri, 01 Jul 2022 00:44:02 GMT  
		Size: 363.0 MB (362978254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f04199602f20583b739e62c5ff66c0588d538101be38c1e720f0b5d8735fb5c`  
		Last Modified: Fri, 01 Jul 2022 00:43:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56957dadad5be0b938a09367836ed1e19d7f3e7290cab63a8de7e5f45a757a1`  
		Last Modified: Fri, 01 Jul 2022 00:43:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5d6e24647804af7e5b655a480f7c85a20346caf6add5e0e5f222f84ae72e6`  
		Last Modified: Fri, 01 Jul 2022 00:43:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26265f53c56705dbb89c238d00ee79cd4e5b26247ffb0be6a242980901d4f867`  
		Last Modified: Fri, 01 Jul 2022 00:43:26 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0046d7c51dfbe12c4bd1e021199a2b8a493dae7f06dda7b71cec70408e4aabbe`  
		Last Modified: Fri, 01 Jul 2022 00:43:27 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff32fadf026fafcf519425672b7338b6563f2d487792715f7d98703531ad69c`  
		Last Modified: Fri, 01 Jul 2022 00:43:26 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff32fadf026fafcf519425672b7338b6563f2d487792715f7d98703531ad69c`  
		Last Modified: Fri, 01 Jul 2022 00:43:26 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad692151579a32266675ae3444e1206972b4f897ec497ab717fa5fea8bf5c272`  
		Last Modified: Fri, 01 Jul 2022 00:43:27 GMT  
		Size: 1.5 MB (1530113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.3.1`

```console
$ docker pull logstash@sha256:d99fea300bb4aa7e333526baffdb8102db7b5bbf8614c7d4adca45063023d1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.3.1` - linux; amd64

```console
$ docker pull logstash@sha256:39281f1cfcb1656a3bbdf974ad32c8ab5020101027e97ea25f9ee4cafa00ec7d
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.2 MB (415242872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81c04c26d07cb9abe3a75c32f5b0850375e992f3b16e28672d43ec9c60959ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Wed, 29 Jun 2022 19:27:14 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 29 Jun 2022 19:27:15 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Wed, 29 Jun 2022 19:27:38 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.3.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.3.1 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 29 Jun 2022 19:27:41 GMT
WORKDIR /usr/share/logstash
# Wed, 29 Jun 2022 19:27:42 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 29 Jun 2022 19:27:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jun 2022 19:27:42 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 29 Jun 2022 19:27:42 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 29 Jun 2022 19:27:42 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 29 Jun 2022 19:27:42 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 29 Jun 2022 19:27:43 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 29 Jun 2022 19:27:43 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 29 Jun 2022 19:27:43 GMT
ADD file:61f93c20f0bfb768d33204e33d049f8843d1af53b9a94b0976af4dc6c856b472 in /usr/local/bin/ 
# Wed, 29 Jun 2022 19:27:43 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 29 Jun 2022 19:27:43 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 29 Jun 2022 19:27:44 GMT
USER 1000
# Wed, 29 Jun 2022 19:27:44 GMT
EXPOSE 5044 9600
# Wed, 29 Jun 2022 19:27:44 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.3.1 org.opencontainers.image.version=8.3.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-06-29T18:41:31Z org.opencontainers.image.created=2022-06-29T18:41:31Z
# Wed, 29 Jun 2022 19:27:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d834c79ce875ee0af3b7b8ca7f64e2f8229acd491835965835434e20e0b095`  
		Last Modified: Fri, 01 Jul 2022 01:26:22 GMT  
		Size: 41.2 MB (41155125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4af0f8031440287d8b2dc64643e30678b9833a28f9f94d1ea080cf8b0335230`  
		Last Modified: Fri, 01 Jul 2022 01:26:17 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639730833689ced516620cb7f0420f81a0b966503299726600807dae2019e24b`  
		Last Modified: Fri, 01 Jul 2022 01:26:44 GMT  
		Size: 343.8 MB (343797133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d1edc56a22da1ee803a691c4763190aa3b01700f6c1ded3ba511e89a4739ad`  
		Last Modified: Fri, 01 Jul 2022 01:26:17 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6012f75123d633c2d476f1fc4d51495a1fddf8aa17c94091bc6b336634c4a76`  
		Last Modified: Fri, 01 Jul 2022 01:26:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42902a00ca223b582739430e07b5e24bf4df9dfa964abaa20c5d8848f0a6fd5`  
		Last Modified: Fri, 01 Jul 2022 01:26:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95974ad451cfd58b2ed89492aba936e0f0d3cad94f8d9ed9e45cd169c4dfdc57`  
		Last Modified: Fri, 01 Jul 2022 01:26:14 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdad4343aa3a1c316f965b7caa7ebe925b10c7d406850abc9ca9526f9f6b4b3`  
		Last Modified: Fri, 01 Jul 2022 01:26:14 GMT  
		Size: 2.7 KB (2719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9656a97c49ff0a915ae32c07862898bde4230a310461b45bd47f4d7daa3d615a`  
		Last Modified: Fri, 01 Jul 2022 01:26:15 GMT  
		Size: 1.7 MB (1710998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b53073a7a189948531a604a9cec8130df072bc72461dfece53116799248be`  
		Last Modified: Fri, 01 Jul 2022 01:26:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b53073a7a189948531a604a9cec8130df072bc72461dfece53116799248be`  
		Last Modified: Fri, 01 Jul 2022 01:26:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.3.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:4e4da1d252b4050a7ad0f84a151edf43dabe16788c13223c783c6af4e0979f82
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.2 MB (405190376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aae79179c705f0cfcda907509ed32a30e94a555b89563c86b0295569958637`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Wed, 29 Jun 2022 18:57:52 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 29 Jun 2022 18:57:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Wed, 29 Jun 2022 18:58:12 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.3.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.3.1 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 29 Jun 2022 18:58:13 GMT
WORKDIR /usr/share/logstash
# Wed, 29 Jun 2022 18:58:13 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 29 Jun 2022 18:58:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jun 2022 18:58:13 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 29 Jun 2022 18:58:13 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 29 Jun 2022 18:58:14 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 29 Jun 2022 18:58:14 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 29 Jun 2022 18:58:14 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 29 Jun 2022 18:58:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 29 Jun 2022 18:58:14 GMT
ADD file:576cee71ee8a223376d8060da8cb64ef8f658a883d27e49ae298e87344e9ceb3 in /usr/local/bin/ 
# Wed, 29 Jun 2022 18:58:14 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 29 Jun 2022 18:58:15 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 29 Jun 2022 18:58:15 GMT
USER 1000
# Wed, 29 Jun 2022 18:58:15 GMT
EXPOSE 5044 9600
# Wed, 29 Jun 2022 18:58:15 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.3.1 org.opencontainers.image.version=8.3.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-06-29T18:44:08+00:00 org.opencontainers.image.created=2022-06-29T18:44:08+00:00
# Wed, 29 Jun 2022 18:58:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eb1ff0fd30083a64edb1ef7c0fec909d648bb3e711d4234ef13cdf7ccd23a1`  
		Last Modified: Fri, 01 Jul 2022 00:42:53 GMT  
		Size: 35.9 MB (35852429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed821f23918801855118f739d8b90288d6a4072908f576c6dae46c79a45ddef4`  
		Last Modified: Fri, 01 Jul 2022 00:42:49 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a321457909e6ad918b2a8e5e4b043b0ece97326834d535e1e14ad29743039`  
		Last Modified: Fri, 01 Jul 2022 00:43:19 GMT  
		Size: 340.5 MB (340538959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df22d36c6aa1b1f81d5a014e989747e49c2fda2d9a86fc94343f6c019d310bdf`  
		Last Modified: Fri, 01 Jul 2022 00:42:48 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1e822a884d5895c9b68fd8fbad553bba5ab6e8676995204542311f56d7565f`  
		Last Modified: Fri, 01 Jul 2022 00:42:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f53790db942d21498e8a94521e403de13a174a350b7eecfdf8c6ba3bba484ff`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f1fc6334742d1cabd006783a21c997568e76dee268c6f3c96e33e68b11fc2b`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c480b8d3e8b4c7b986a933db26a1a87280c0f2223aa2817e40d97437654103`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 2.7 KB (2720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fb1284dbf0b45feab4a6442ce5ae585421a8a2c71365ffcde980130f598b5`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 1.6 MB (1600794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b04b2f9eb803a49d1c1f0418fa2195ae187840e369a1d955aadb5c897acd201`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b04b2f9eb803a49d1c1f0418fa2195ae187840e369a1d955aadb5c897acd201`  
		Last Modified: Fri, 01 Jul 2022 00:42:46 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
