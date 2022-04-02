<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.2`](#logstash7172)
-	[`logstash:8.1.2`](#logstash812)

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

## `logstash:7.17.2`

```console
$ docker pull logstash@sha256:767f865fbfbe30f64a94f608cf4af1f97c4ea5239c727784ebb76967d00ec9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.2` - linux; amd64

```console
$ docker pull logstash@sha256:d4dbfb80d4dcc605523105f1348ac6c7b6572100d39fe670ba3ca29e785485f9
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.9 MB (433876541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2f260d55338b1efd85eda32304edcb7737918e401f7cb7f2e3127b8bb3b2bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Mon, 28 Mar 2022 09:20:40 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Mon, 28 Mar 2022 09:20:41 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Mon, 28 Mar 2022 09:21:05 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Mon, 28 Mar 2022 09:21:08 GMT
WORKDIR /usr/share/logstash
# Mon, 28 Mar 2022 09:21:08 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 28 Mar 2022 09:21:08 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Mar 2022 09:21:08 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Mon, 28 Mar 2022 09:21:09 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Mon, 28 Mar 2022 09:21:09 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Mon, 28 Mar 2022 09:21:09 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Mon, 28 Mar 2022 09:21:09 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Mon, 28 Mar 2022 09:21:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 28 Mar 2022 09:21:10 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Mon, 28 Mar 2022 09:21:10 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Mon, 28 Mar 2022 09:21:10 GMT
USER 1000
# Mon, 28 Mar 2022 09:21:10 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Mon, 28 Mar 2022 09:21:10 GMT
EXPOSE 5044 9600
# Mon, 28 Mar 2022 09:21:11 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.2 org.opencontainers.image.version=7.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-28T08:33:20Z org.opencontainers.image.created=2022-03-28T08:33:20Z
# Mon, 28 Mar 2022 09:21:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf76a4fdd8a683c982ef991f4c244cf1273d39a9f8b491960f1129fb57961837`  
		Last Modified: Fri, 01 Apr 2022 20:59:34 GMT  
		Size: 37.6 MB (37558666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d622d34a9638223927cd64750cfe8ec1368dcba82ceb2d65a4b3b64ed2eab92f`  
		Last Modified: Fri, 01 Apr 2022 20:59:30 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61be5edb2d9d919e6e6f31c3002d30cdb2f328b1e6df3e54b7392dc569f11169`  
		Last Modified: Fri, 01 Apr 2022 20:59:57 GMT  
		Size: 366.1 MB (366081129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65415cad4f91d90154f0cceb1be31db64d5392b0e45e2473f191def8115a14ae`  
		Last Modified: Fri, 01 Apr 2022 20:59:29 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547b50e008de7b5270ca06b6c88bc2dd09a7723a12fde0aca83f9d48cbde4923`  
		Last Modified: Fri, 01 Apr 2022 20:59:29 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f56a5afcbeba80af189147e53e8ad22d79b112a8c0cffbb52b73db5fcbb6ef4`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6075c1cfffb768fe85458b74e1fb87e29ac77e75c05c52796fd33e940e120f`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4790ff3977d0d8ab610fd0c2233f1e403fb39a4fd617cf6ff352bb65ba1836e3`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 2.8 KB (2809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7f00a2462d8be29b0655aeea33fe92b4b790b816667bc57eee08e3953fc28`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7f00a2462d8be29b0655aeea33fe92b4b790b816667bc57eee08e3953fc28`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c45cb66b40eb3b2d752d452dff840321bde0960d8ddd789c98e458183848d1`  
		Last Modified: Fri, 01 Apr 2022 20:59:27 GMT  
		Size: 1.7 MB (1663762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:efee28519aa0d6e0c4b4cbd3a470129aa2460fc1eb0328d330ee2f8a1f2288a0
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424653439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3d7ae9cb2f9b42f6e4c203ccf2f946fd76b8b52c8b1898b9fb6c1cb364d3ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Mon, 28 Mar 2022 08:47:17 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Mon, 28 Mar 2022 08:47:18 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Mon, 28 Mar 2022 08:47:38 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Mon, 28 Mar 2022 08:47:40 GMT
WORKDIR /usr/share/logstash
# Mon, 28 Mar 2022 08:47:40 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 28 Mar 2022 08:47:40 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Mar 2022 08:47:40 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Mon, 28 Mar 2022 08:47:40 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Mon, 28 Mar 2022 08:47:41 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Mon, 28 Mar 2022 08:47:41 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Mon, 28 Mar 2022 08:47:41 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Mon, 28 Mar 2022 08:47:41 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 28 Mar 2022 08:47:41 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Mon, 28 Mar 2022 08:47:42 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Mon, 28 Mar 2022 08:47:42 GMT
USER 1000
# Mon, 28 Mar 2022 08:47:42 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Mon, 28 Mar 2022 08:47:42 GMT
EXPOSE 5044 9600
# Mon, 28 Mar 2022 08:47:42 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.2 org.opencontainers.image.version=7.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-28T08:33:45+00:00 org.opencontainers.image.created=2022-03-28T08:33:45+00:00
# Mon, 28 Mar 2022 08:47:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8a85ce61274b7dbf529928a31a0fcece0f6457d49bbd6a448f9b56876ce3a8`  
		Last Modified: Fri, 01 Apr 2022 19:21:58 GMT  
		Size: 33.1 MB (33124980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ca2853a89b321f607dc108a00f9afb29534695798b0d3994664e0d9fd352e2`  
		Last Modified: Fri, 01 Apr 2022 19:21:54 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e169cefc271fd6b8aa2b780cb76ff7ea5d7c110af3bb0855cf0a4d804413e8ca`  
		Last Modified: Fri, 01 Apr 2022 19:22:25 GMT  
		Size: 362.8 MB (362821635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c712954b280cbd1d1d2e74a4a069aa38c272c98f2bf2173be94c54cd552530de`  
		Last Modified: Fri, 01 Apr 2022 19:21:53 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b6a5d1c25494d94fbbe87181730794d59e1806bd235e1522244eb16b461ea7`  
		Last Modified: Fri, 01 Apr 2022 19:21:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb37f2554bb64aada60cea06a217dc71aa770a1784ba060f8a70cf100861c29e`  
		Last Modified: Fri, 01 Apr 2022 19:21:50 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2137209864e8a22fc70b113f93e025fa32679baeeb1a5fb0e1bde9d74d00839`  
		Last Modified: Fri, 01 Apr 2022 19:21:50 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2393b95437a78ff42eabdc4c57c0fda6477823ff3dc67f7cb7215a3ea989e6`  
		Last Modified: Fri, 01 Apr 2022 19:21:50 GMT  
		Size: 2.8 KB (2810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01cca9ac12c6047bf7f87d06d04ea6f4f0d833bb440f8262c7bfbce7182b3c`  
		Last Modified: Fri, 01 Apr 2022 19:21:51 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01cca9ac12c6047bf7f87d06d04ea6f4f0d833bb440f8262c7bfbce7182b3c`  
		Last Modified: Fri, 01 Apr 2022 19:21:51 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96f5f3fdb148da9f23f1f0ea0807edd629471092b61e5d28c573e5679e01bff`  
		Last Modified: Fri, 01 Apr 2022 19:21:51 GMT  
		Size: 1.5 MB (1530122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.1.2`

```console
$ docker pull logstash@sha256:063bd539c5c70897a20aaa14978efbf85957d4dce9ed525f18ec1cad78841dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.1.2` - linux; amd64

```console
$ docker pull logstash@sha256:8bab25fa7b16fe0b2b71ee4f9ec477e7b882d357d8e2e7b11d673560264345b0
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415337924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ac898ceb0666512b6d1837a34390c5b02e921b3740cf3f057f6bce7d9cd34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:12:18 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Tue, 29 Mar 2022 22:12:19 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Tue, 29 Mar 2022 22:12:42 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 29 Mar 2022 22:12:45 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Mar 2022 22:12:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Mar 2022 22:12:45 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 22:12:45 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 29 Mar 2022 22:12:46 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 29 Mar 2022 22:12:46 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 29 Mar 2022 22:12:46 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 29 Mar 2022 22:12:46 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 29 Mar 2022 22:12:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 29 Mar 2022 22:12:47 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 29 Mar 2022 22:12:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 29 Mar 2022 22:12:47 GMT
USER 1000
# Tue, 29 Mar 2022 22:12:47 GMT
ADD file:74f1240397564c8006436b57526b98f8b3e9fcbad9cb9f7c905c223de143c5f3 in /usr/local/bin/ 
# Tue, 29 Mar 2022 22:12:47 GMT
EXPOSE 5044 9600
# Tue, 29 Mar 2022 22:12:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.2 org.opencontainers.image.version=8.1.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-29T21:20:06Z org.opencontainers.image.created=2022-03-29T21:20:06Z
# Tue, 29 Mar 2022 22:12:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40f58b85057d6ea9dc0b856d91fb79f8ad61d448ec287949802295e6f85d67c`  
		Last Modified: Fri, 01 Apr 2022 01:17:00 GMT  
		Size: 37.6 MB (37577473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9ad60700d23aaaaebc7cea41a31c27d4c8d682fd6410d39d55177551e21d74`  
		Last Modified: Fri, 01 Apr 2022 01:16:36 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e942c819880ed6d0f675765bd2eee5794f8572eca24f7fe54ae056ce0b97a3f`  
		Last Modified: Fri, 01 Apr 2022 01:19:07 GMT  
		Size: 347.5 MB (347523622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968d90f7ad45e8a86652dd4defea54f9facade5327dfb2080bb93e275f1b507`  
		Last Modified: Fri, 01 Apr 2022 01:16:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0eb331b113d1bc446acfd7c228b51eff070019d61829d1ad99c3052343cb1b`  
		Last Modified: Fri, 01 Apr 2022 01:16:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc6255c6af435e63ee97f5aade05b9dd808fd5e5b1a20d51cf03fa7fdcf2275`  
		Last Modified: Fri, 01 Apr 2022 01:16:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9527d2255a29aa479cc2c734ac557f7a218e2dd15e5312a57575faf1b800dd3`  
		Last Modified: Fri, 01 Apr 2022 01:16:24 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c87cc95c456ab67e85a9bf7b04e1fba0f7f4267be6a9685fc8f87def30db1`  
		Last Modified: Fri, 01 Apr 2022 01:16:24 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d035fc3248413898a1228107df24b588704cf197d0d3ce188afe7dacd3e9b9`  
		Last Modified: Fri, 01 Apr 2022 01:16:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d035fc3248413898a1228107df24b588704cf197d0d3ce188afe7dacd3e9b9`  
		Last Modified: Fri, 01 Apr 2022 01:16:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2c9fb881680a0c02ccbc704be0bb9b12712b38cb417bb2ee3dcbe567dd9c89`  
		Last Modified: Fri, 01 Apr 2022 01:16:25 GMT  
		Size: 1.7 MB (1663830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.1.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ff85ea7b4f9cffe5417b9ca08b52cc4a3b43d29359ef49706a97345671ef8ea9
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406091835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e11e8d9a0e4c8f004dd24a62d58f1a1fdfa10f9bae5857efa115696109bc62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 21:34:57 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Tue, 29 Mar 2022 21:34:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Tue, 29 Mar 2022 21:35:17 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 29 Mar 2022 21:35:19 GMT
WORKDIR /usr/share/logstash
# Tue, 29 Mar 2022 21:35:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 29 Mar 2022 21:35:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 21:35:20 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 29 Mar 2022 21:35:20 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 29 Mar 2022 21:35:20 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 29 Mar 2022 21:35:20 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 29 Mar 2022 21:35:20 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 29 Mar 2022 21:35:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 29 Mar 2022 21:35:20 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 29 Mar 2022 21:35:21 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 29 Mar 2022 21:35:21 GMT
USER 1000
# Tue, 29 Mar 2022 21:35:21 GMT
ADD file:945c6fce9a9e80bbe91b66f2c2535aba760ab72a0b46cff684339f8e5b553444 in /usr/local/bin/ 
# Tue, 29 Mar 2022 21:35:21 GMT
EXPOSE 5044 9600
# Tue, 29 Mar 2022 21:35:21 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.2 org.opencontainers.image.version=8.1.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-29T21:21:51+00:00 org.opencontainers.image.created=2022-03-29T21:21:51+00:00
# Tue, 29 Mar 2022 21:35:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6ca8705952ce85cafe70258ec45d09e66918652b8985210f22a2ff33745c04`  
		Last Modified: Fri, 01 Apr 2022 19:21:16 GMT  
		Size: 33.1 MB (33128636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ec33fa02b1248c43b7e8564e6799e3ffd76c3559cca898f52e08c41453367`  
		Last Modified: Fri, 01 Apr 2022 19:21:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dcdbebcfcf6f6f8bc68845adcf34ca3b2378548f03de50e5f07a82d9e2a58a`  
		Last Modified: Fri, 01 Apr 2022 19:21:42 GMT  
		Size: 344.3 MB (344256400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04de326c03c6c8267eb956e96bd0317f7c58ce4ab907eedaad9ee5754d4d2f3`  
		Last Modified: Fri, 01 Apr 2022 19:21:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e424832ddd52d069b219beeea5ddda0277b8dffd31df64f5815b1c0a2b91e2`  
		Last Modified: Fri, 01 Apr 2022 19:21:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041c077754e014dad5e647997132f410d7135e3a14ba4f459ae58fc04949385`  
		Last Modified: Fri, 01 Apr 2022 19:21:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f6ff24bda3f4870eab7d7c5f588e29fc97cdfe77a67b2e364171840b11a07e`  
		Last Modified: Fri, 01 Apr 2022 19:21:09 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd83a5edc537a4ad9c3ce7e66c3fe12714c191f964f999f81acccb5dbe8396`  
		Last Modified: Fri, 01 Apr 2022 19:21:09 GMT  
		Size: 2.8 KB (2831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13921d00f481cfbe4b47b880e4f0ea552e33326848a745ccc6678edefa928735`  
		Last Modified: Fri, 01 Apr 2022 19:21:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13921d00f481cfbe4b47b880e4f0ea552e33326848a745ccc6678edefa928735`  
		Last Modified: Fri, 01 Apr 2022 19:21:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629c58cb4917cfcb3740f592c2595c5329e243dd5efad94c4f1dbfe03151c2fc`  
		Last Modified: Fri, 01 Apr 2022 19:21:10 GMT  
		Size: 1.5 MB (1530083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
