<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.5`](#logstash7175)
-	[`logstash:8.3.2`](#logstash832)

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

## `logstash:8.3.2`

```console
$ docker pull logstash@sha256:9d3c86deee39108a26f8b7e6627938aefeb6d33b9831a62d0a92aaa5e32d2cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.3.2` - linux; amd64

```console
$ docker pull logstash@sha256:0004a7587f982c8c412ad096018e525328225ea5733fff4b519d3472b7cd2744
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415537076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c50ffe78629f40cfa10f9a6bbdba80587b16a55fd9d35a236b97a86842cfc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Wed, 06 Jul 2022 16:04:18 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 06 Jul 2022 16:04:18 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Wed, 06 Jul 2022 16:04:42 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.3.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.3.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 06 Jul 2022 16:04:45 GMT
WORKDIR /usr/share/logstash
# Wed, 06 Jul 2022 16:04:45 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 06 Jul 2022 16:04:45 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jul 2022 16:04:45 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 06 Jul 2022 16:04:45 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 06 Jul 2022 16:04:46 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 06 Jul 2022 16:04:46 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 06 Jul 2022 16:04:46 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 06 Jul 2022 16:04:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 06 Jul 2022 16:04:46 GMT
ADD file:61f93c20f0bfb768d33204e33d049f8843d1af53b9a94b0976af4dc6c856b472 in /usr/local/bin/ 
# Wed, 06 Jul 2022 16:04:46 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 06 Jul 2022 16:04:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 06 Jul 2022 16:04:47 GMT
USER 1000
# Wed, 06 Jul 2022 16:04:47 GMT
EXPOSE 5044 9600
# Wed, 06 Jul 2022 16:04:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.3.2 org.opencontainers.image.version=8.3.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-07-06T15:17:46Z org.opencontainers.image.created=2022-07-06T15:17:46Z
# Wed, 06 Jul 2022 16:04:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2e100fdc5dae24e0f41f85c2c6f7d221ab010973c0a079d9e4cf4b0134e098`  
		Last Modified: Thu, 07 Jul 2022 21:22:01 GMT  
		Size: 41.4 MB (41448497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105a0f70d402c8d2a9519f941373d6fb5b66484cfe05c90fbfcc2a5cd2d79d27`  
		Last Modified: Thu, 07 Jul 2022 21:21:56 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1999179de006ad58988bd8d3a4d72173a33d5389172883346f8793dc5eb32ae6`  
		Last Modified: Thu, 07 Jul 2022 21:22:24 GMT  
		Size: 343.8 MB (343797956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367a87a034088480481a65d2d80c68b6c77d04753b3efa916327655297b77cb`  
		Last Modified: Thu, 07 Jul 2022 21:21:56 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc3f979db7ad9cb2d7e6ceb6447b3f0de282c395340d4f0408cee4b81f540`  
		Last Modified: Thu, 07 Jul 2022 21:21:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3e13956a252b2f132c9ef0f28199d9f6bd547916c82fd65a8941b837287c9c`  
		Last Modified: Thu, 07 Jul 2022 21:21:54 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2baf74873ad161efba743dab12744c0074f9c58d18f9359f8abdc5cb388fb560`  
		Last Modified: Thu, 07 Jul 2022 21:21:53 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472ed0e021a24d03648d31ff061fac10b416e68ed3e77c00fba202e6994b3dd0`  
		Last Modified: Thu, 07 Jul 2022 21:21:53 GMT  
		Size: 2.7 KB (2724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa8c6970a4430a9ad0e522db9454a9726488c378483325d860a7ab37e745871`  
		Last Modified: Thu, 07 Jul 2022 21:21:54 GMT  
		Size: 1.7 MB (1710996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89340b81a27aab9889240b42ee6cec22c2873fae62509a9bf2d5a48f5e13b30`  
		Last Modified: Thu, 07 Jul 2022 21:21:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89340b81a27aab9889240b42ee6cec22c2873fae62509a9bf2d5a48f5e13b30`  
		Last Modified: Thu, 07 Jul 2022 21:21:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.3.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c351384d09a3aa312efb99eb90f8cfd1714f10b09d3a3ad22ccb294914598c4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405444208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25074c49d17d9043393cafd79482f8647388464f231475a2101f2ea0cb7a7e2d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Wed, 06 Jul 2022 15:32:08 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 06 Jul 2022 15:32:09 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash
# Wed, 06 Jul 2022 15:32:28 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.3.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.3.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 06 Jul 2022 15:32:29 GMT
WORKDIR /usr/share/logstash
# Wed, 06 Jul 2022 15:32:29 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 06 Jul 2022 15:32:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jul 2022 15:32:30 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 06 Jul 2022 15:32:30 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 06 Jul 2022 15:32:30 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 06 Jul 2022 15:32:30 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 06 Jul 2022 15:32:30 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 06 Jul 2022 15:32:30 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 06 Jul 2022 15:32:30 GMT
ADD file:576cee71ee8a223376d8060da8cb64ef8f658a883d27e49ae298e87344e9ceb3 in /usr/local/bin/ 
# Wed, 06 Jul 2022 15:32:31 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 06 Jul 2022 15:32:31 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 06 Jul 2022 15:32:31 GMT
USER 1000
# Wed, 06 Jul 2022 15:32:31 GMT
EXPOSE 5044 9600
# Wed, 06 Jul 2022 15:32:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.3.2 org.opencontainers.image.version=8.3.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-07-06T15:18:54+00:00 org.opencontainers.image.created=2022-07-06T15:18:54+00:00
# Wed, 06 Jul 2022 15:32:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc538bbaea50b1eb46349921c75fc630c0c286335a171cb28be542e1899e755`  
		Last Modified: Fri, 08 Jul 2022 00:21:16 GMT  
		Size: 36.1 MB (36106136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0edbf2cf7f5e8dff3ec6d88002f7b588b8c00ca323c127e4aa94a70bb8a044`  
		Last Modified: Fri, 08 Jul 2022 00:21:11 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfda48e621bfdd572ecbea205bfc0def0fbb13abcacfcf40fb274a333e98af8`  
		Last Modified: Fri, 08 Jul 2022 00:21:41 GMT  
		Size: 340.5 MB (340539084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ab1b207711cb3c1305f71ff61c653dc8dd0df570d58d449ae0b60498635f6`  
		Last Modified: Fri, 08 Jul 2022 00:21:11 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9be799c2422d2fd5e64b223c9ecfcd639e809c1db8fb69097000767217fed35`  
		Last Modified: Fri, 08 Jul 2022 00:21:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20523cd90ee7b27ba7a17fb83cda4055ab639c0316b10e0a408761cfa853e0b1`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59755d6204264a5f1dcbcecb1bd64bf16eef53bd26e6a0e47a6d0e22020bee76`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d8a5c2039e14d60ed639b8ab67bb1e9142386739fae9d77bebe88978f7759`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbbd01821946e4238c595bd9d2cb661af7001ce43ac15462ec224e57b21a400`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 1.6 MB (1600794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d62911815a917ecaa675d9ca936f51ab08aa34afece2050e6529b668836f6`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d62911815a917ecaa675d9ca936f51ab08aa34afece2050e6529b668836f6`  
		Last Modified: Fri, 08 Jul 2022 00:21:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
