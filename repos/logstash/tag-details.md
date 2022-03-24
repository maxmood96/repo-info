<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.1`](#logstash7171)
-	[`logstash:8.1.1`](#logstash811)

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

## `logstash:7.17.1`

```console
$ docker pull logstash@sha256:78f68b476a2f727cd8cef12610f4e7b7dd8434ba8cf45758326cfc1f299beb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.1` - linux; amd64

```console
$ docker pull logstash@sha256:4b00f23786ab028a8a6803b06ccfa9c6e233c8952c1c2022f7a3d6074c5898d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436913412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6867cdc686066dd4a5fe0df50513348df1a40067604770a465ef76d92b1ff8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 23 Feb 2022 23:40:34 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 23 Feb 2022 23:40:35 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 23 Feb 2022 23:41:01 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 23 Feb 2022 23:41:04 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Feb 2022 23:41:04 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Feb 2022 23:41:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 23 Feb 2022 23:41:05 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 23 Feb 2022 23:41:06 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 23 Feb 2022 23:41:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Feb 2022 23:41:06 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 23 Feb 2022 23:41:06 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 23 Feb 2022 23:41:06 GMT
USER 1000
# Wed, 23 Feb 2022 23:41:07 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Wed, 23 Feb 2022 23:41:07 GMT
EXPOSE 5044 9600
# Wed, 23 Feb 2022 23:41:07 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.1 org.opencontainers.image.version=7.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-02-23T22:23:10Z org.opencontainers.image.created=2022-02-23T22:23:10Z
# Wed, 23 Feb 2022 23:41:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869740cab373cb4e24b08037aa862b56a8c5798f98d2f1e1bbe8aaaa0c9f20cd`  
		Last Modified: Tue, 01 Mar 2022 04:00:42 GMT  
		Size: 39.7 MB (39711775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501681a4236f95934d8988ebf8de67eb9608d0e164a73dc3e45eb469cca26b2`  
		Last Modified: Tue, 01 Mar 2022 04:00:34 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2a6f0d667162bc2833de08b283b82c48d86f0fda65cd4c4bed56fe7d2d2e1c`  
		Last Modified: Tue, 01 Mar 2022 04:01:19 GMT  
		Size: 367.0 MB (366966688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8500ce3174d2858f8109d9b2509929f6117fe71d74ac19e1e2ca5ceb218111b9`  
		Last Modified: Tue, 01 Mar 2022 04:00:32 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9f510e031005b78892fb89ec4eb5970b61c25afdfc2a059db391207798ffc8`  
		Last Modified: Tue, 01 Mar 2022 04:00:30 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad19b15dcc5292d2c554994c454ac46d5316928135b1145f21a4aefa72921a80`  
		Last Modified: Tue, 01 Mar 2022 04:00:29 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066f96dfc588192827ff8b2ef25b67258fecd5bf56582d9b6586f986d1815ae0`  
		Last Modified: Tue, 01 Mar 2022 04:00:28 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0d1c896fadd28d3fcb48a46a02f27ad0ef1c65d37e7765fb9d43579959d63`  
		Last Modified: Tue, 01 Mar 2022 04:00:27 GMT  
		Size: 2.8 KB (2810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029db52cc072a1a4651e3f524b28194b9c9f0675873e871c817f4b27b55fd2c`  
		Last Modified: Tue, 01 Mar 2022 04:00:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029db52cc072a1a4651e3f524b28194b9c9f0675873e871c817f4b27b55fd2c`  
		Last Modified: Tue, 01 Mar 2022 04:00:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcf0a9df4e11f0a7c5ac5e7a9f1ea07db6ac6aca35b917acaa00de9db39696f`  
		Last Modified: Tue, 01 Mar 2022 04:00:24 GMT  
		Size: 1.7 MB (1663767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7e837d6b07f0432af31084919fe240135a38ef118e026c3a15b9c50924880bf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427874582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f6b4baaeb29fa98b1feed6dc42760cb72b012ac62055f6a4ff1edb52ff932`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 23 Feb 2022 22:45:54 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 23 Feb 2022 22:45:55 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 23 Feb 2022 22:46:13 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 23 Feb 2022 22:46:15 GMT
WORKDIR /usr/share/logstash
# Wed, 23 Feb 2022 22:46:15 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 23 Feb 2022 22:46:15 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Feb 2022 22:46:15 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 23 Feb 2022 22:46:16 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 23 Feb 2022 22:46:16 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 23 Feb 2022 22:46:16 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:46:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 23 Feb 2022 22:46:17 GMT
USER 1000
# Wed, 23 Feb 2022 22:46:17 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Wed, 23 Feb 2022 22:46:17 GMT
EXPOSE 5044 9600
# Wed, 23 Feb 2022 22:46:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.1 org.opencontainers.image.version=7.17.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-02-23T22:24:19+00:00 org.opencontainers.image.created=2022-02-23T22:24:19+00:00
# Wed, 23 Feb 2022 22:46:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd90f70abb904972921dab34007ebc18d299a6ba7f61614bbc4a8262914c55c0`  
		Last Modified: Wed, 02 Mar 2022 16:05:39 GMT  
		Size: 35.5 MB (35489080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54f644c418c77e329fe7402ea9ce1e343c5ace85588c22a11ab786b7bbb82f5`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255a48aeca3553f1ba342bf05e450e1b3d58724993310ef366cfed2aadc61b3a`  
		Last Modified: Wed, 02 Mar 2022 16:06:12 GMT  
		Size: 363.7 MB (363678673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc176bb1a33dcaedebb24862544ba21c7be693ccdb8e203079cd1d89af3fbe8`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ee2535495bf3ee0e0ca58c3d22e50cfcd8705ae562fb5c33d3bd7cbad18893`  
		Last Modified: Wed, 02 Mar 2022 16:05:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d209b999c4ad404147321b650460e9365c604912130ff42144a89ce71a7ee7f`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18719dde5e053f719721a6d33325ac202289b2f71f8618eb9cd774f5fbbfb82`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f29dd1f46359873e13c72fba512072393470bb5cebc33b7b5d23b8df4042b7`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 2.8 KB (2806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e55890d1d23225e60c44d0f84d2336f484a479cdb03764e3bf5626029fac0d`  
		Last Modified: Wed, 02 Mar 2022 16:05:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e55890d1d23225e60c44d0f84d2336f484a479cdb03764e3bf5626029fac0d`  
		Last Modified: Wed, 02 Mar 2022 16:05:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042766f2e06ae9b45012bafa9b78212c08ac630767a1e97efd9e0bc94d487b9`  
		Last Modified: Wed, 02 Mar 2022 16:05:32 GMT  
		Size: 1.5 MB (1530117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.1.1`

```console
$ docker pull logstash@sha256:4b098877605011c7af2209103920ee7daa425a64f3d0c6f118175f5445a1926b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.1.1` - linux; amd64

```console
$ docker pull logstash@sha256:bd1dd6fc249af3b941c6e2cc2c6b0d5a38a811547abeb45678c9fc3863c0ee5f
```

-	Docker Version: 20.10.13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523482831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9669367812d122e98045bb434fd793134908e80e89cca382128b7ef76b53683a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:51:21 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 17 Mar 2022 22:51:22 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 17 Mar 2022 22:51:49 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 17 Mar 2022 22:51:53 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Mar 2022 22:51:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Mar 2022 22:51:53 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 22:51:53 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 17 Mar 2022 22:51:53 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 17 Mar 2022 22:51:54 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 17 Mar 2022 22:51:54 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 17 Mar 2022 22:51:54 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 17 Mar 2022 22:51:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 22:51:55 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 17 Mar 2022 22:51:55 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 17 Mar 2022 22:51:55 GMT
USER 1000
# Thu, 17 Mar 2022 22:51:55 GMT
ADD file:74f1240397564c8006436b57526b98f8b3e9fcbad9cb9f7c905c223de143c5f3 in /usr/local/bin/ 
# Thu, 17 Mar 2022 22:51:55 GMT
EXPOSE 5044 9600
# Thu, 17 Mar 2022 22:51:55 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.1 org.opencontainers.image.version=8.1.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-17T22:01:47Z org.opencontainers.image.created=2022-03-17T22:01:47Z
# Thu, 17 Mar 2022 22:51:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd16e3b4055e599cb2910ae4ac9905a230812f483e0444ac70ffbf5d9d12ba`  
		Last Modified: Tue, 22 Mar 2022 20:37:52 GMT  
		Size: 37.6 MB (37625366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dafa14204cab79ed2661df92f6c71dd86459c3eb9c3d2e71b7e95e928b4590`  
		Last Modified: Tue, 22 Mar 2022 20:37:37 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a389e98806b816cc8ec82b7b71e6f8c9714689b7c44351123a580b38c77fbdfe`  
		Last Modified: Tue, 22 Mar 2022 20:41:39 GMT  
		Size: 455.6 MB (455620780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb63f8fb21788c42766f7ce711b579778b6527e1d0a47f75a206814c6c9f36d6`  
		Last Modified: Tue, 22 Mar 2022 20:37:32 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4fb1f41c20d0785daafeef8ed11785c53652c83752e6dea788883890a3ef6c`  
		Last Modified: Tue, 22 Mar 2022 20:37:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87156adb4bc0976fecac9ee74298e165c246fd61e9491e8518de40e401a887c5`  
		Last Modified: Tue, 22 Mar 2022 20:37:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61498d4f37943ac39afcb684f17fee3658fd01c0daa47f75ba42b3c2a7e52b9e`  
		Last Modified: Tue, 22 Mar 2022 20:37:26 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba67669a1d52995aeacce026bba3f30737c2e36cedbaf88fd9c07bbf59ac9fa`  
		Last Modified: Tue, 22 Mar 2022 20:37:24 GMT  
		Size: 2.8 KB (2829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f515722dd87f692bf58a3c09e7f7aef8ec1db64b8d2245fe17f2c8a722e30`  
		Last Modified: Tue, 22 Mar 2022 20:37:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f515722dd87f692bf58a3c09e7f7aef8ec1db64b8d2245fe17f2c8a722e30`  
		Last Modified: Tue, 22 Mar 2022 20:37:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df416ba2ad0aa47de104238b1059ba2fa10f3190930e1aa22fad001f1a887b93`  
		Last Modified: Tue, 22 Mar 2022 20:37:26 GMT  
		Size: 1.7 MB (1663836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.1.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5f68c6e70ad018b4da99e2794a3ad54bdc2abf0a71662d12d585a18d115d788c
```

-	Docker Version: 20.10.13
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.4 MB (514391501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d24ab20ec73552e56d5ba0f9bdf95062bbae008f8c78f155b8719d37a221510`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:17:28 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Thu, 17 Mar 2022 22:17:28 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Thu, 17 Mar 2022 22:17:49 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.1.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.1.1 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Thu, 17 Mar 2022 22:17:51 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Mar 2022 22:17:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Mar 2022 22:17:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 22:17:51 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Thu, 17 Mar 2022 22:17:52 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Thu, 17 Mar 2022 22:17:52 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Thu, 17 Mar 2022 22:17:52 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Thu, 17 Mar 2022 22:17:52 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Thu, 17 Mar 2022 22:17:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 22:17:52 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Thu, 17 Mar 2022 22:17:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Thu, 17 Mar 2022 22:17:53 GMT
USER 1000
# Thu, 17 Mar 2022 22:17:53 GMT
ADD file:945c6fce9a9e80bbe91b66f2c2535aba760ab72a0b46cff684339f8e5b553444 in /usr/local/bin/ 
# Thu, 17 Mar 2022 22:17:53 GMT
EXPOSE 5044 9600
# Thu, 17 Mar 2022 22:17:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.1.1 org.opencontainers.image.version=8.1.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-03-17T22:03:05+00:00 org.opencontainers.image.created=2022-03-17T22:03:05+00:00
# Thu, 17 Mar 2022 22:17:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a09a0d716322735eacfdf0e9bce1007f044b7069f45415b72facb635044de8`  
		Last Modified: Thu, 24 Mar 2022 02:09:06 GMT  
		Size: 33.3 MB (33328818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be619964314cdd316a6cb8a5886407c0a83d371b7fe2e75e38b6c71f95283df5`  
		Last Modified: Thu, 24 Mar 2022 02:09:00 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9a1f692eaaea88cf56c2ee5c05358fb7707c3bd4befaeae12fc5c2a00333c7`  
		Last Modified: Thu, 24 Mar 2022 02:09:38 GMT  
		Size: 452.4 MB (452355861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c82e4c1b2df8134abcc1db4dd6b1e1c9333069b6cb61277b22b2a8e6953b96a`  
		Last Modified: Thu, 24 Mar 2022 02:08:59 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34141e7304ad24a1a8483d741462eabf26c5492edb464a13e4e31906a233f62e`  
		Last Modified: Thu, 24 Mar 2022 02:08:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6604b502cb5cadd793867a084294deae886bbaf8bd9b62c3c6dc811d4fa94abd`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b0b68fb211fe43968d4f398995a7a238ad7a7714bc75dcbdc188f0e2492507`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5199c3f1b12d8d9d58693b4f3ffddb2efba45ee44652f364faf083b2c9098`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 2.8 KB (2833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d75e78373e121672dd0d79b582acdbe953b5c572ceb721afcb0ce9a788f0`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa4d75e78373e121672dd0d79b582acdbe953b5c572ceb721afcb0ce9a788f0`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b93dc0b5682ea0a25e22752ad175393008d4d6e35288c0702f3c13fba9bcb6`  
		Last Modified: Thu, 24 Mar 2022 02:08:57 GMT  
		Size: 1.5 MB (1530085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
