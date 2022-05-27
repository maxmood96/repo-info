<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.23`](#logstash6823)
-	[`logstash:7.17.4`](#logstash7174)
-	[`logstash:8.2.2`](#logstash822)

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

## `logstash:7.17.4`

```console
$ docker pull logstash@sha256:0f97e1c1cd0d990e1126744418a8ae1a45d73cf0067102985322b21ebfc22ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:7.17.4` - linux; amd64

```console
$ docker pull logstash@sha256:c21bfa31e698d15722315ebcc63f4e9f164840b26f3588d91ad00448ca003dc5
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444300097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93aa11296788cfc973ae0473bfbe469137dff8aa197fb8e2f22be975aaffd70b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Wed, 18 May 2022 16:21:27 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 18 May 2022 16:21:28 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 18 May 2022 16:21:52 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.4-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.4 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 18 May 2022 16:21:55 GMT
WORKDIR /usr/share/logstash
# Wed, 18 May 2022 16:21:56 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 16:21:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 16:21:56 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 18 May 2022 16:21:56 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 18 May 2022 16:21:56 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 18 May 2022 16:21:56 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 18 May 2022 16:21:57 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 18 May 2022 16:21:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 18 May 2022 16:21:57 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 18 May 2022 16:21:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 18 May 2022 16:21:58 GMT
USER 1000
# Wed, 18 May 2022 16:21:58 GMT
ADD file:bc2ff40ec3323fe4b7e3cc88ed3e05a6716f206361909a69b57058b5e140a579 in /usr/local/bin/ 
# Wed, 18 May 2022 16:21:58 GMT
EXPOSE 5044 9600
# Wed, 18 May 2022 16:21:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.4 org.opencontainers.image.version=7.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-05-18T15:32:43Z org.opencontainers.image.created=2022-05-18T15:32:43Z
# Wed, 18 May 2022 16:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9448cb0fbc8d5ccc839e68669fb28cdee9d5dc6b6345f7f4fb1e06017ab642d2`  
		Last Modified: Wed, 25 May 2022 17:26:38 GMT  
		Size: 48.0 MB (47975874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765a92c6bc8c3e8acf7f598eadf2061735556ec70900374ac632bbb91ed8e4fd`  
		Last Modified: Wed, 25 May 2022 17:26:31 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc3b6c90fdc53ae93a59acfd39edd813bda8776d67dd369885de960bc9c4dd4`  
		Last Modified: Wed, 25 May 2022 17:26:59 GMT  
		Size: 366.1 MB (366087126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51db48b305904e93d8223ecf2266985bd6389b446c4a84f85107260993e00516`  
		Last Modified: Wed, 25 May 2022 17:26:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd65ee8cca0f3ec1bffde29783f721e42becd7b0a9ed6deca264fe72927db36`  
		Last Modified: Wed, 25 May 2022 17:26:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2013c198b56472ba571d60de76a1f6d2d18da48d088cafe2a1a6a3baa0d0e7`  
		Last Modified: Wed, 25 May 2022 17:26:29 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ceb69332825292ce15bd67e315f85b4240c546f40774f646dfad13e7ab22af`  
		Last Modified: Wed, 25 May 2022 17:26:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c143ee9d0a50efd9da40a85d9d9f6193d87c1f79b1ad75284f6ee1708dbf656`  
		Last Modified: Wed, 25 May 2022 17:26:29 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961e2d968e85e39bd232427881b15997df23fe99f4e17fe4585a4bed8cb034a2`  
		Last Modified: Wed, 25 May 2022 17:26:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961e2d968e85e39bd232427881b15997df23fe99f4e17fe4585a4bed8cb034a2`  
		Last Modified: Wed, 25 May 2022 17:26:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724d09cc29ebacb6c87a0bdc5450ca1c2628657802d1b8a0d77a6aaf5bc74827`  
		Last Modified: Wed, 25 May 2022 17:26:29 GMT  
		Size: 1.7 MB (1663761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:7.17.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:51ec6cfe9b4927f5b5bdaef853d3d0a271db2a4e3d224d4ac6c6325b4ee59b93
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433574795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d923c04ffb69b63ac06424e4caf8c99824eb87e6dd1ce3a2525838be775a1e25`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Wed, 18 May 2022 15:48:29 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 18 May 2022 15:48:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 18 May 2022 15:48:48 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.17.4-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.4 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 18 May 2022 15:48:51 GMT
WORKDIR /usr/share/logstash
# Wed, 18 May 2022 15:48:51 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 15:48:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 15:48:51 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 18 May 2022 15:48:51 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 18 May 2022 15:48:51 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 18 May 2022 15:48:51 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 18 May 2022 15:48:52 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 18 May 2022 15:48:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 18 May 2022 15:48:52 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 18 May 2022 15:48:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 18 May 2022 15:48:52 GMT
USER 1000
# Wed, 18 May 2022 15:48:52 GMT
ADD file:86be8b3554008b0941aee895258eda0ddb8a6aa71aaa83d0b5f7ef3c5ef5697e in /usr/local/bin/ 
# Wed, 18 May 2022 15:48:52 GMT
EXPOSE 5044 9600
# Wed, 18 May 2022 15:48:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.4 org.opencontainers.image.version=7.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-05-18T15:34:20+00:00 org.opencontainers.image.created=2022-05-18T15:34:20+00:00
# Wed, 18 May 2022 15:48:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f41f768c1585b7eb2a46630e50e0ae302ffeb88ba20c36881395776161ea2e`  
		Last Modified: Wed, 25 May 2022 18:12:20 GMT  
		Size: 42.0 MB (42034369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd58fd3373dedbef00a95a3a4375ebff9744f122af9de93dc9721aaca663e62e`  
		Last Modified: Wed, 25 May 2022 18:12:14 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18e93561715c96a7e4d92bce66e810a475e0ac7af9aa07651d39053f25d19b0`  
		Last Modified: Wed, 25 May 2022 18:12:47 GMT  
		Size: 362.8 MB (362833809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1c67326069f99123953793cc863f5c6a16e90d4220b7cbad4e37ee5d0e459d`  
		Last Modified: Wed, 25 May 2022 18:12:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0320908611e5e29a621d3fc9576cee19d0fb20230dac16757df8326b076292`  
		Last Modified: Wed, 25 May 2022 18:12:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ad7060be3a7527ebbd0f961a9203f727f56a3ae7f08bb6a1978b8c12f31fe`  
		Last Modified: Wed, 25 May 2022 18:12:12 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a91a1a947f2169c177350a746c76ef459d7dc334ffcea9207d1b90e641b5428`  
		Last Modified: Wed, 25 May 2022 18:12:11 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686eca6cab98501324ae0a07d5b65013b7672dac11b317285ac19144f05e530`  
		Last Modified: Wed, 25 May 2022 18:12:11 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b9ff0f8cff83b5e2c5f3f083fc5f519a216285db74d8bd34ab68d1a5d7769`  
		Last Modified: Wed, 25 May 2022 18:12:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b9ff0f8cff83b5e2c5f3f083fc5f519a216285db74d8bd34ab68d1a5d7769`  
		Last Modified: Wed, 25 May 2022 18:12:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b1398c1b22d0de351476474152706e71f6a062c55f8a61e5764cb68d92ca47`  
		Last Modified: Wed, 25 May 2022 18:12:12 GMT  
		Size: 1.5 MB (1530117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:8.2.2`

```console
$ docker pull logstash@sha256:033f5bf0d7953ea2319a9e433031a7abe1f5c2b3c4b8229dcb137ae75598a543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `logstash:8.2.2` - linux; amd64

```console
$ docker pull logstash@sha256:5e29e189c8282aeb568eb9dc3308b84184f5d300c2bcf8baaed145388cf91c87
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.8 MB (417817449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0731ee0df3d1881e46cd91da2e3c83535fd48892f13ed852140b8b776fc79e49`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Wed, 25 May 2022 16:37:57 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 25 May 2022 16:37:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 25 May 2022 16:38:22 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.2.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.2.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 25 May 2022 16:38:25 GMT
WORKDIR /usr/share/logstash
# Wed, 25 May 2022 16:38:25 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 25 May 2022 16:38:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 May 2022 16:38:25 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 25 May 2022 16:38:26 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 25 May 2022 16:38:26 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 25 May 2022 16:38:26 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 25 May 2022 16:38:26 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 25 May 2022 16:38:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 25 May 2022 16:38:27 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 25 May 2022 16:38:27 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 25 May 2022 16:38:27 GMT
USER 1000
# Wed, 25 May 2022 16:38:27 GMT
ADD file:74f1240397564c8006436b57526b98f8b3e9fcbad9cb9f7c905c223de143c5f3 in /usr/local/bin/ 
# Wed, 25 May 2022 16:38:27 GMT
EXPOSE 5044 9600
# Wed, 25 May 2022 16:38:27 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.2.2 org.opencontainers.image.version=8.2.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-05-25T15:50:17Z org.opencontainers.image.created=2022-05-25T15:50:17Z
# Wed, 25 May 2022 16:38:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e6c13c88f4a824c0ef4f23677fd5fb851ca8da6c8bf73b37fd05834478e680`  
		Last Modified: Fri, 27 May 2022 00:37:18 GMT  
		Size: 48.1 MB (48076799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd540c2396de2b46aa32d269184d74ede19444ac84d9a589ecaa6360d9653e73`  
		Last Modified: Fri, 27 May 2022 00:37:11 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55de6c1bf74ddd35ca7b07dc226209288a71972272254946174914708a695c1`  
		Last Modified: Fri, 27 May 2022 00:37:38 GMT  
		Size: 339.5 MB (339503603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfee97fde58c54a0a6c7c1fd507d8ccd3be42bb65177076314c3563e1a3c4dc`  
		Last Modified: Fri, 27 May 2022 00:37:11 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718ea4131a22017d86e36528d22141083cd4f50465690508ab2d7bf069e4b8be`  
		Last Modified: Fri, 27 May 2022 00:37:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d71c4a2b10eb6a5cd7dab3ed53ef7a874dbc6ea99787b68245171e22dc7169`  
		Last Modified: Fri, 27 May 2022 00:37:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c5302b2d5c3197febb143d1fb6df5e22486bcf4a7378459ada805274320394`  
		Last Modified: Fri, 27 May 2022 00:37:08 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc5ada19ae963382d174dd9984aebaf725f33dd3eca97c14d854a6e4b76ce16`  
		Last Modified: Fri, 27 May 2022 00:37:08 GMT  
		Size: 2.7 KB (2717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dc41a1db78550656cdef15b805bc75aefef1d2fc03decb52139ab494f4505e`  
		Last Modified: Fri, 27 May 2022 00:37:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dc41a1db78550656cdef15b805bc75aefef1d2fc03decb52139ab494f4505e`  
		Last Modified: Fri, 27 May 2022 00:37:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0812e67c76404b6d9e82e1e42cd1fa2b3f4ad0561427c9da167cec729052b1e3`  
		Last Modified: Fri, 27 May 2022 00:37:09 GMT  
		Size: 1.7 MB (1663835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `logstash:8.2.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3f5094fac4bf09ed19db7af0f2a7b459265fc6f0cfb03ae63b59ef0e4f274f90
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 MB (407030715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d28bed1e1c11fe2bb3c07a993feb0d190ef65d8a1e8c241dde8943162815036`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Wed, 25 May 2022 16:04:31 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code)
# Wed, 25 May 2022 16:04:32 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home /usr/share/logstash --no-create-home       logstash
# Wed, 25 May 2022 16:04:49 GMT
RUN curl -Lo - http://localhost:8000/logstash-8.2.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.2.2 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Wed, 25 May 2022 16:04:52 GMT
WORKDIR /usr/share/logstash
# Wed, 25 May 2022 16:04:52 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 25 May 2022 16:04:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 May 2022 16:04:52 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Wed, 25 May 2022 16:04:52 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Wed, 25 May 2022 16:04:52 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Wed, 25 May 2022 16:04:52 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Wed, 25 May 2022 16:04:53 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Wed, 25 May 2022 16:04:53 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 25 May 2022 16:04:53 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Wed, 25 May 2022 16:04:53 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Wed, 25 May 2022 16:04:53 GMT
USER 1000
# Wed, 25 May 2022 16:04:53 GMT
ADD file:945c6fce9a9e80bbe91b66f2c2535aba760ab72a0b46cff684339f8e5b553444 in /usr/local/bin/ 
# Wed, 25 May 2022 16:04:53 GMT
EXPOSE 5044 9600
# Wed, 25 May 2022 16:04:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.2.2 org.opencontainers.image.version=8.2.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2022-05-25T15:51:26+00:00 org.opencontainers.image.created=2022-05-25T15:51:26+00:00
# Wed, 25 May 2022 16:04:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1daf7db55c56bc1fb87176f71e04c48732636f636ab177d3aac3db68842c40c`  
		Last Modified: Fri, 27 May 2022 00:58:44 GMT  
		Size: 42.1 MB (42072909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbcd52a6bd59b5fa551e0b1b2660ce37b8fb168f3764972d0e911770b5198da`  
		Last Modified: Fri, 27 May 2022 00:58:39 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3974d674b4b16330266ae697eb0b35ffdd5bc1c5840aa7385aa331452b7730`  
		Last Modified: Fri, 27 May 2022 00:59:11 GMT  
		Size: 336.3 MB (336251350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87bf1177c052cfd5561856f1f9f2bb386ee8f96953d76d6484cfcd2a4aeaa4c`  
		Last Modified: Fri, 27 May 2022 00:58:38 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccbfdd1b0e08068f99bd6ce02657e3d74212dbb7663dfe2a06168556c4bca7`  
		Last Modified: Fri, 27 May 2022 00:58:39 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f162b5bf527da37dc3cea2862c1bf6113e9336631af36e8deb458cf6cee24887`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf2906c9e04234c07ca038e455176f4e53a563f4382cfd9c172a02f21956f17`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b63f4e95f2c01750e6da9a91e547ba7cfad54f17e043d0e1e148d847993a355`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 2.7 KB (2718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ddd4a1d1d21c47a8bbc6554793ef165cf0d414cadc311561b8535d0e15a6fc`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ddd4a1d1d21c47a8bbc6554793ef165cf0d414cadc311561b8535d0e15a6fc`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa88b997190ccd6d7bd7c0239bcbf32752f4048a7e1283dea1e8a2c55d761e60`  
		Last Modified: Fri, 27 May 2022 00:58:36 GMT  
		Size: 1.5 MB (1530083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
